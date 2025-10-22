## To‑Be Late Payment Reminder Workflow (HK Property Management)

This proposal defines a configurable late payment reminder (dunning) workflow aligned to Hong Kong property management practices, with clear swimlanes and escalation thresholds.

### Scope and assumptions
- Residential/commercial tenancies with monthly recurring charges and ad‑hoc charges
- Supported payments: FPS, bank transfer/Autopay, cheque, card (optional)
- Dunning is per‑account with invoice‑level detail; disputes and payment plans pause dunning
- Bilingual communications (EN/ZH) with PDPO‑compliant consent and audit trail

### Roles (swimlanes)
- Tenant / Occupant
- PMS – Billing & Dunning Engine
- Comms Service – Email/SMS/Letter generation and delivery
- AR / Collections
- Property Manager
- Finance / Legal Escalation

### Swimlane diagram

```mermaid
flowchart TB
classDef event fill:#fff,stroke:#333,stroke-width:1px;
classDef task fill:#dfefff,stroke:#4a76b8,stroke-width:1px;
classDef decision fill:#fff9c4,stroke:#b59a00,stroke-width:1px;
classDef offsys fill:#f6f6f6,stroke:#888,stroke-dasharray: 3 3;

subgraph TENANT["Tenant / Occupant"]
  T_notice((Receives notice)):::event
  T_pay[Pay: FPS/Autopay/Bank/Cheque]:::task
  T_dispute[Raise dispute / query]:::task
end

subgraph PMS["PMS - Billing & Dunning Engine"]
  P_sched[Daily scheduler: identify overdue invoices]:::task
  P_excl{Excluded? dispute, payment plan, hold}:::decision
  P_level[Compute dunning level and days past due]:::task
  P_fee[Apply late fee/interest if crossing threshold]:::task
  P_action[Create dunning action + case]:::task
  P_log[Log comms & audit trail]:::task
end

subgraph NOTIFY["Comms Service (Email/SMS/Letter)"]
  N_send[Send notice per template & language]:::task
  N_bounce{Bounce or delivery failure?}:::decision
  N_call[Queue outbound call task]:::task
end

subgraph AR["AR / Collections"]
  A_queue[Review dunning queue]:::task
  A_pay{Payment received?}:::decision
  A_alloc[Allocate receipt and clear case]:::task
  A_partial{Partial or short-payment?}:::decision
  A_plan[Offer payment plan; capture terms]:::task
  A_dispute[Mark as dispute; suspend dunning]:::task
end

subgraph PMGR["Property Manager"]
  M_invest[Investigate dispute]:::task
  M_valid{Dispute valid?}:::decision
  M_adjust[Adjust charge / issue credit note]:::task
  M_reject[Reject dispute; resume dunning]:::task
end

subgraph FINLEGAL["Finance / Legal Escalation"]
  F_escalate{Age > 45d or Amt > threshold?}:::decision
  F_final[Final notice; service hold request]:::task
  F_legal{Age > 60d or >HKD X?}:::decision
  F_referral[Refer to legal / DCA]:::task
end

%% Main flow
P_sched-->P_excl
P_excl--"Yes"-->P_log-->P_sched
P_excl--"No"-->P_level-->P_fee-->P_action-->N_send
N_send-->N_bounce
N_bounce--"Yes"-->N_call-->A_queue
N_bounce--"No"-->A_queue

%% Customer reactions
T_notice-->T_pay-->A_queue
T_notice-->T_dispute-->A_dispute-->M_invest

%% AR handling
A_queue-->A_pay
A_pay--"Yes (Full)"-->A_alloc-->P_log
A_pay--"Yes (Partial)"-->A_partial
A_partial--"Offer accepted"-->A_plan-->P_log
A_partial--"Declined"-->F_escalate
A_pay--"No"-->F_escalate

%% Dispute handling
M_invest-->M_valid
M_valid--"Yes"-->M_adjust-->P_log
M_valid--"No"-->M_reject-->P_log

%% Escalations
F_escalate--"No"-->P_sched
F_escalate--"Yes"-->F_final-->F_legal
F_legal--"Yes"-->F_referral-->P_log
F_legal--"No"-->P_log

%% Loop
P_log-->P_sched
```

### Suggested dunning ladder (parameterised)
- D+3: Courtesy reminder via Email/SMS; no fee
- D+7: First overdue Email + SMS; show amount due and payment links
- D+14: Second overdue Email + Letter; apply late fee/interest if enabled
- D+21: Phone call task; warn of potential service hold (as contractually permitted)
- D+30: Final notice; initiate service hold request (e.g., access cards, facility booking) per policy
- D+45: Demand letter; manager approval required
- D+60: Legal/DCA referral; case file compiled automatically

Parameters per property/portfolio: thresholds (HKD), fee rate/minimum, holidays calendar, bilingual templates, and excluded accounts (government, VIP, active payment plans, active disputes).

### Controls, compliance and audit
- PDPO: consent records, unsubscribe handling, purpose limitation; mask PII in reports
- Role‑based approvals for fee application, service hold and legal referral
- Immutable audit log of reminders, calls, letters, fee postings and reversals
- SLA timers for dispute handling; dunning auto‑pauses while in dispute or payment plan

### Key system behaviours
- Auto‑allocation on FPS/Autopay receipts; partials trigger plan offer logic
- Multi‑channel templates with EN/ZH variants and property headers
- Bounced communication detection routes to outbound call queue
- Manager dashboard: ageing buckets, promise‑to‑pay tracking, exception list

### KPIs
- Collection rate by bucket (0‑30/31‑60/61‑90/90+)
- Days Sales Outstanding (DSO)
- Promise‑to‑pay kept ratio; right‑party contact rate; bounce rate
- Dispute cycle time; fee reversal rate

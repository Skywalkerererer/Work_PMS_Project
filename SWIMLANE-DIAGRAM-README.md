# Late Payment Reminder Swimlane Diagram - User Guide

## 📊 Files Delivered

### 1. **Late-Payment-Reminder-Swimlane.drawio.xml**
- **Format**: draw.io/diagrams.net compatible XML
- **Type**: Professional swimlane diagram with 6 lanes
- **Size**: Optimized for A3 landscape printing (1169mm x 827mm)
- **Purpose**: Visual process flow for stakeholder presentations

### 2. **Late-Payment-Reminder-Design-Documentation.md**
- **Content**: 20+ page detailed design specification
- **Covers**: Process flows, HK market practices, compliance, KPIs, risks
- **Audience**: Business stakeholders, IT implementation teams, auditors

### 3. **To-Be Late Payment Reminder Workflow.md** (existing, enhanced)
- **Content**: Original Mermaid diagram and workflow description
- **Purpose**: Developer-friendly process documentation

---

## 🎨 How to View/Edit the Swimlane Diagram

### Option 1: Online (Recommended)
1. Go to **https://app.diagrams.net** (formerly draw.io)
2. Click **"Open Existing Diagram"**
3. Upload `Late-Payment-Reminder-Swimlane.drawio.xml`
4. The diagram will render immediately with full interactivity

### Option 2: Desktop App
1. Download **draw.io Desktop** from https://github.com/jgraph/drawio-desktop/releases
2. Install and open the application
3. File → Open → Select the XML file
4. Edit as needed

### Option 3: VS Code Extension
1. Install the **Draw.io Integration** extension in VS Code
2. Open the `.drawio.xml` file
3. View and edit inline within your IDE

---

## 📐 Diagram Structure

### Swimlanes (Top to Bottom)

| # | Lane | Color | Key Activities |
|---|------|-------|----------------|
| 1 | **Tenant / Occupant** | Light Blue | Receive notices, make payments, raise disputes |
| 2 | **PMS - Billing & Dunning Engine** | Purple | Automated scheduler, fee application, case management |
| 3 | **Communications Service** | Orange | Multi-channel delivery (Email/SMS/Letter) |
| 4 | **AR / Collections Team** | Green | Manual review, payment plans, dispute handling |
| 5 | **Property Manager** | Pink | Investigate disputes, approve adjustments |
| 6 | **Finance / Legal Escalation** | Red | Final notices, legal referrals |

### Shape Legend

- **Rectangles (rounded)**: Process tasks/activities
- **Diamonds**: Decision points (Yes/No branches)
- **Ellipse**: Start event (daily scheduler)
- **Solid arrows**: Process flow
- **Dashed arrows**: Information flow (e.g., payment notifications)

### Color Coding

- **Blue**: System/automated processes
- **Green**: Successful outcomes (payments, resolutions)
- **Yellow**: Decision points (require evaluation)
- **Orange**: Communication actions
- **Red**: Escalation and legal actions
- **Pink**: Manual investigation/approval

---

## 🔄 Process Flow Summary

### Main Process Path (Happy Path)
```
Daily Scheduler → Identify Overdue → Exclusion Check → Compute Level 
→ Apply Late Fee (if needed) → Create Case → Send Reminder 
→ Tenant Pays → Auto-Allocate → Log & Close
```

### Dispute Path
```
Tenant Receives Notice → Raises Dispute → AR Flags Dispute 
→ Property Manager Investigates → Decision (Valid/Invalid) 
→ Adjust or Reject → Log & Resume/Close
```

### Escalation Path
```
No Payment → Collections Review → Age/Amount Check 
→ Final Notice → Legal Threshold Check → DCA/Legal Referral 
→ Log & External Collection
```

---

## 🎯 Key Decision Points in the Diagram

| Decision | Location | Criteria | Outcomes |
|----------|----------|----------|----------|
| **Account Excluded?** | PMS Lane | Dispute, payment plan, manual hold | Yes → Skip / No → Continue |
| **Fee Threshold Crossed?** | PMS Lane | D+14 or configured date | Yes → Apply fee / No → Skip to case |
| **Delivery Failure?** | Comms Lane | Email/SMS bounce | Yes → Call task / No → Continue |
| **Payment Received?** | PMS Lane | Payment posted | Yes → Allocate / No → Escalate |
| **Partial Payment?** | PMS Lane | Amount < invoice total | Yes → Plan offer / No → Escalate |
| **Dispute Valid?** | PM Lane | Investigation outcome | Yes → Credit note / No → Resume |
| **Age > 45d OR Amt > Threshold?** | Legal Lane | Escalation criteria | Yes → Final notice / No → Continue |
| **Age > 60d OR Amt > HKD X?** | Legal Lane | Legal referral criteria | Yes → DCA/Legal / No → Log |

---

## 📊 Dunning Ladder Timeline (Annotated on Diagram)

| Day | Action | Channel | Fee | Escalation Level |
|-----|--------|---------|-----|------------------|
| **D+3** | Courtesy Reminder | Email + SMS | None | Level 1 |
| **D+7** | 1st Overdue Notice | Email + SMS | None | Level 2 |
| **D+14** | 2nd Overdue Notice | Email + Letter | **Applied** | Level 3 |
| **D+21** | Phone Call | Phone | Accumulating | Level 4 |
| **D+30** | Final Notice | Email + Letter | Accumulating | Level 5 |
| **D+45** | Demand Letter | Registered Letter | Accumulating | **Manager Approval** |
| **D+60+** | Legal Referral | Legal Notice | Full Amount | **Legal/DCA** |

---

## ✅ Compliance Features Highlighted

### PDPO (Personal Data Privacy Ordinance)
- ✓ Consent tracking (captured in lease)
- ✓ Bilingual communications (EN/ZH)
- ✓ Purpose limitation (collections only)
- ✓ Audit trail (immutable log)
- ✓ PII masking in reports

### Financial Controls
- ✓ Late fee calculation rules (5% per month max)
- ✓ Approval workflows (manager sign-off)
- ✓ Auto-pause on disputes
- ✓ Payment plan terms capture
- ✓ Write-off governance

### Operational SLAs
- ✓ Dispute resolution: 5 business days
- ✓ Payment allocation: Same day (auto)
- ✓ Bounce handling: Next business day
- ✓ Legal referral prep: 2 business days

---

## 🚀 Using This Diagram

### For Business Stakeholders
- **Review Process Flow**: Understand end-to-end collection process
- **Identify Pain Points**: Highlight manual steps to automate
- **Define SLAs**: Set expectations for each stage
- **Approve Design**: Sign off on workflow before development

### For IT/Implementation Team
- **System Design**: Map swimlanes to system modules
- **Integration Points**: Identify APIs needed (Payment, Email, SMS)
- **Workflow Engine**: Configure BPMN engine based on flows
- **Test Scenarios**: Create test cases for each decision branch

### For Compliance/Audit
- **Control Points**: Review approval requirements
- **Audit Trail**: Verify logging at each step
- **PDPO Check**: Confirm consent and data handling
- **Risk Assessment**: Evaluate controls vs. risks

### For Training
- **Role Mapping**: Assign lanes to teams/individuals
- **Process Walkthrough**: Use diagram for training sessions
- **Exception Handling**: Teach staff how to handle disputes/escalations
- **KPI Understanding**: Link diagram to performance metrics

---

## 📝 Customization Guide

### To Modify the Diagram
1. Open in draw.io (online or desktop)
2. Edit elements:
   - **Text**: Double-click any shape
   - **Colors**: Right-click → Style → Fill color
   - **Positions**: Drag shapes to rearrange
   - **Connections**: Click and drag from connection points
3. Save changes (File → Save As → XML)

### Common Customizations
- **Add/Remove Dunning Levels**: Insert steps in PMS lane
- **Change Thresholds**: Update decision diamond text (e.g., "Age > 30d")
- **New Communication Channels**: Add tasks in Comms lane (e.g., WhatsApp)
- **Additional Approvals**: Insert decision points in relevant lanes

### Export Options
- **PDF**: File → Export as → PDF (for printing/sharing)
- **PNG/JPG**: File → Export as → PNG (for presentations)
- **SVG**: File → Export as → SVG (for web/scalable graphics)
- **HTML**: File → Export as → HTML (for embedding in web pages)

---

## 🔗 Integration with Other Documentation

### Cross-References
| This Diagram | Related Document | Section |
|--------------|------------------|---------|
| PMS Lane | Design Doc | "Stage 1: Daily Automated Identification" |
| Comms Lane | Design Doc | "Stage 2: Multi-Channel Communication" |
| AR Lane | Design Doc | "Stage 4: AR Collections Team Functions" |
| PM Lane | Design Doc | "Stage 5: Property Manager Dispute Resolution" |
| Legal Lane | Design Doc | "Stage 6: Finance & Legal Escalation" |
| Decision Points | Design Doc | "Key Decision Points in the Diagram" |

### Artifact Traceability
- **User Requirements**: `PMS User Requirement Checklist V2.1.xlsx` (Billing/Collections modules)
- **As-Is Process**: `PWC report/pwc - Business Process Flow Charts.pdf`
- **Gap Analysis**: `PWC - Savills User Requirements Review Over PMS v2.4 - clean.pdf`
- **Vendor Capability**: `Vendor Proposal/PMS User Requirement Checklist – Comparison.xlsx`

---

## 📞 Support & Feedback

### Questions About the Design?
- **Process Logic**: Refer to `Late-Payment-Reminder-Design-Documentation.md`
- **HK Market Practices**: See Appendix section in design doc
- **Compliance**: Review "Controls, Compliance & Audit" section
- **KPIs**: Check "Key Performance Indicators" section

### Diagram Editing Issues?
- **draw.io Documentation**: https://www.diagrams.net/doc/
- **Tutorials**: https://www.diagrams.net/blog/
- **Forum**: https://github.com/jgraph/drawio/discussions

### Design Iterations
- Save versions with date stamps (e.g., `Late-Payment-v1.1-20251022.drawio.xml`)
- Document changes in version control
- Circulate for stakeholder review before finalizing

---

## ✨ Next Steps

### Recommended Actions
1. **Review Meeting**: Walk through diagram with key stakeholders (AR, Finance, PM teams)
2. **Validation**: Confirm dunning ladder aligns with current DMC/lease terms
3. **Gap Analysis**: Compare with vendor capabilities (MRI, Kingdee proposals)
4. **Approval**: Get sign-off from CFO, Head of Operations
5. **Detailed Design**: Expand each swimlane into detailed BPMN for development
6. **Prototyping**: Build mock-ups of AR queue, dashboards, templates
7. **Testing**: Create test scenarios covering all decision branches
8. **Training**: Develop materials based on this diagram

### Success Metrics (Post-Implementation)
- [ ] 60%+ reduction in manual AR tasks
- [ ] 5-10 day improvement in DSO (Days Sales Outstanding)
- [ ] > 95% auto-allocation rate for payments
- [ ] < 5% communication bounce rate
- [ ] < 5 days average dispute resolution time
- [ ] > 80% payment plan success rate
- [ ] Zero PDPO compliance breaches

---

## 📚 Version History

| Version | Date | Changes | Author |
|---------|------|---------|--------|
| 1.0 | 2025-10-22 | Initial swimlane diagram creation | Senior BA |
| | | - 6 swimlanes with 40+ process steps | |
| | | - 13 decision points | |
| | | - Full dunning ladder (D+3 to D+60+) | |
| | | - PDPO compliance annotations | |
| | | - HK market best practices | |

---

**Document Status**: ✅ Ready for Stakeholder Review  
**Classification**: Internal Use  
**Owner**: PMS Project Team  
**Review Frequency**: Update after each design iteration

---

*This diagram represents a modern, automated approach to late payment collections for Hong Kong property management, balancing operational efficiency with regulatory compliance and tenant relationship management.*


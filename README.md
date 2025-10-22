# Work_PMS_Project
for my work on PMS project
Below is a detailed consolidation of all relevant resources and requirements for your PMS project. This summarizes process flows, pain points, improvement opportunities, and user requirements, structured for direct use as a detailed README description in a process documentation or Cursor README file.​

Savills Hong Kong PMS Project – Process Flow & System Requirements
Overview
This Property Management System (PMS) revamp aims to replace the legacy Dataswift with an integrated, modern SaaS solution that streamlines operational workflows for Savills Hong Kong (SPML and GPML), optimizes productivity, improves control, and centralizes information management for property, tenancy, financial, procurement, and vendor processes. This README outlines business process flows, major pain points, best practices, and detailed requirements guiding the project.

1. End-to-End Process Flow Overview
Core Business Workflows (as per PwC/Operations Documentation)
Master Data Setup & Maintenance

Initial property profile setup, including bulk upload & updates of property/tenancy/owner info

Centralized repository for documents and data mapping​

Billing

Generation, delivery, and monitoring of debit notes, ad-hoc and sundry invoices; recurring/one-off workflows

Credit note management (concessions, negative adjustments)

Payment method configuration and document routing​

Collection (Cash, Cheque, E-Payment, Autopay)

Multi-channel payment settlement, bank reconciliations, and automation

Receipt and void reconciliation with approval workflows

Use of OCR, RPA for cheque processing automation​

Credit Control & Late Payment Reminders

Automated reminders and legal tracking

Dynamic aging tiers and audit trail​

Deposit Handling

Collection, refund, and ledger recording (single-entry mechanism preferred)​

Inventory & Fixed Asset Management

Facilities and inventory lifecycle: procurement requests, updates, and reconciliation

Automated depreciation, reporting, and asset register​

Procurement & Vendor Management

Integrated e-procurement and vendor profile creation workflows

Digital approvals, document upload, performance monitoring, vendor bank verification, and contract management​

Reporting, Analysis, Budgeting, Month/Year-End Closing

On-demand, customizable dashboards

Financial statements, management analysis, audit trails, and automated report templates​

2. Key Pain Points & Required Improvements
Manual Operations & Lack of Integration
Heavy reliance on paper, Excel, and disconnected systems causes errors, delays, and visibility gaps

No centralized, up-to-date view of owner, tenant, property data

Approval processes are offline (physical signatures, manual routing)

Data silos between PMS, Property Cube, e-Procurement, sundry receipts, HR​

Automation & Standardization
High priority to digitize approvals (invoices, payments, journal vouchers, IE reports, master data updates)

Need for electronic receipts/reminders, e-signatures, automated document distribution and tracking​

Enhanced Financial Controls
Automated calculation/configuration of commissions, rent concessions, multi-bank payments

Support for bulk/batch creation, consolidation, and reporting

Full audit trail for every transaction, approval, change, user activity​

User Experience & Reporting
Intuitive dashboards, custom templates, real-time alerts/notifications for milestones, expirations, errors

Online analytics, batch reporting, export to Excel, advanced search filters, role-based views​

3. Best Practices for PMS Implementation
Integrate with all existing business systems for master data management (Property Cube, e-Procurement, HRIS, analytics tools)

Leverage AI (OCR, RPA) for document extraction and cheque automation

Structure process workflows with online approval routing, automated notifications, to-do lists, error handling

Ensure all workflow and system activities have a logged audit trail for compliance and performance​

4. Detailed Functional Requirements
Master Data
Document upload, mapping, indexing

Bulk data updates, direct data entry, error validation

Consolidated owner/tenant/property/unit/lease view

Change-of-owner process with balance transfer

Property-level status, remarks, delivery preferences, multi-layered landlord/unit support​

Billing/Invoice
Configurable debit/credit note templates (drag-and-drop, unlimited characters)

Multi-channel payments with support for all HK payment systems (FPS, Alipay, PPS, CBP, Octopus, etc.)

Automated generation, approval workflows, and reconciliation

Grouping, consolidation, flexible template management​

Collection
Cheque/cash/e-payment/auto-pay settlement and reconciliation

OCR enabled automated cheque scanning and exception handling

Structured approval for voids and refunds, batch processing​

Procurement/Vendor
Digital onboarding, bank verification, profile management

Multi-level approval, bulk uploads, data mapping

Vendor performance monitoring, audit trails, error alerts​

Inventory/Asset
Inventory status updates, contract management, procurement linkage

Automated depreciation, asset tracking​

Reporting & Analytics
Customizable dashboards and report templates

Ad-hoc queries, batch processing, export options, security controls

On-demand, multi-year, multi-entity reporting features

AI-driven reporting capability (GenAI integration if supported)​

Security, Control, Audit
Robust user role management, audit logs, SSO integration, MFA support

Tamper-resistant logs, disaster recovery protocols, security at application and database level

Full compliance with local IT security and government guidelines​

5. Process Mapping Reference
The above business flows and requirements summarize these major phases:

Master Data Setup → Billing/Invoice → Collection → Credit Control → Sundry Receipt & Deposits → Inventory & Fixed Assets → Procurement & Vendor → Payment Processing → Financial Reporting & Closing → Management Analysis & Budgeting​

6. Implementation & Future State Recommendations
Transition from manual, paper-based processes to fully digital workflows

Integrate PMS with all core systems for a single source of truth (master data sync, reporting, vendor management, budgeting)

Automate reminders, alerts, and validation checks for critical events and errors

Continuous improvement and adoption of AI, advanced analytics, and user-centric design

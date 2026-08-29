# Dashboard Data Source Mapping

## Purpose
Define where each executive dashboard metric comes from so reporting stays auditable and implementation-ready.

| Dashboard Area | Metric / View | Primary Source | Key Fields | Refresh |
|---|---|---|---|---|
| Service Health | Critical services by RAG | Service Inventory | Service, Criticality, Status, SLA | Daily |
| Helpdesk | Open/Closed Tickets | Helpdesk Register | Ticket ID, Status, Opened, Resolved | Daily |
| Helpdesk | SLA Compliance | Helpdesk Register | Priority, SLA Met, Resolved | Daily/Monthly |
| Helpdesk | MTTR | Helpdesk Register | Opened, Resolved | Monthly |
| Incidents | Open P1/P2 | Incident Register | Severity, Status, Impact | Daily |
| Assets | Assets by Status | Asset Register | Category, Status, Assigned To | Weekly |
| Assets | Warranty Expiry | Asset Register | Warranty End, Criticality | Weekly |
| Security | Patch Compliance | Patch Register | Device, Compliance, Last Patch | Weekly |
| Security | Privileged Access Review | Privileged Access Register | User, System, Review Date | Monthly |
| Backup | Backup Success | Backup Register | Last Success, Status | Daily/Weekly |
| Backup | Restore Tests | Restore Test Log | Test Date, Result, Recovery Time | Monthly/Quarterly |
| Vendors | Renewal Pipeline | Renewal Register | Renewal Date, Owner, Status, Cost | Daily |
| Vendors | Vendor SLA | Vendor Evaluation | SLA Score, Review Date | Monthly |
| Budget | Budget vs Actual | IT Budget Register | Budget, Actual, Variance | Monthly |
| Risks | Heatmap | IT Risk Register | Likelihood, Impact, Residual Score | Weekly/Monthly |
| Projects | Project RAG | Project Register | Progress, RAG, Milestone, Risk | Weekly |

## Data Quality Rules
1. Every KPI must have an accountable source owner.
2. Manual metrics should state the reporting date.
3. Closed tickets must have a resolution timestamp.
4. Renewals must have an owner and expiry/renewal date.
5. Risks without owner or due date should be flagged incomplete.
6. Asset serial numbers should be unique where available.
7. Backup status should distinguish job success from restore-test success.
8. Budget figures should use one approved period and currency basis.

## Future Integration Targets
- Odoo Helpdesk / Project / Purchase / Accounting
- Microsoft 365 / Entra reporting
- Endpoint management platforms
- Firewall / network monitoring
- Backup platforms
- Google Workspace
- Service desk APIs
- n8n automation
- Power BI / Looker Studio
- PostgreSQL / Supabase

## Recommended Architecture

```text
Operational Sources
      ↓
CSV / APIs / ERP / Monitoring
      ↓
Data Validation Layer
      ↓
Normalized IT Operations Dataset
      ↓
KPI Calculation Layer
      ↓
Executive Dashboard
      ↓
Alerts + Monthly Report
```

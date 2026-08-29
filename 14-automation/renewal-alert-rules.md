# Renewal & License Alert Rules

## Objective
Prevent avoidable service interruption, domain expiry, license suspension, warranty gaps, and rushed commercial decisions.

## Alert Schedule

| Days Before Due Date | Severity | Expected Action |
|---:|---|---|
| 120 | Information | Validate ownership, scope, usage, budget, and alternatives |
| 90 | Planning | Start technical/commercial review |
| 60 | Action | Collect quotations / negotiate / confirm budget |
| 30 | High | Decision should be approved or formally escalated |
| 14 | Urgent | Confirm PO/payment/renewal execution |
| 7 | Critical | Daily escalation until controlled |
| 3 | Critical | Executive visibility for critical services |
| 1 | Critical | Immediate owner + management notification |
| 0 | Breach | Renewal due today; verify service continuity |
| Overdue | Breach | Escalate and track business impact |

## Items to Monitor
- Domains
- DNS / hosting
- Business email
- Microsoft / Google licenses
- Odoo / ERP subscriptions
- SSL certificates
- Firewall / security subscriptions
- Antivirus / EDR
- Backup services
- Cloud infrastructure
- Internet / static IP contracts
- PBX / telecom contracts
- CCTV support / storage
- Attendance / access-control support
- SaaS applications
- Hardware warranties
- Support agreements

## Minimum Data Fields
- Renewal ID
- Product / Service
- Vendor
- Category
- Criticality
- Start Date
- Renewal / Expiry Date
- Notice Period
- Current Cost
- Forecast Cost
- Owner
- Business Owner
- Auto-Renew Yes/No
- Cancellation Deadline
- Decision Status
- Payment Status
- PO Reference
- Risk if Not Renewed

## Alert Logic

```text
IF expiry_date - today <= threshold
AND status NOT IN (Renewed, Cancelled, Replaced)
THEN create alert
```

### Escalation Rule

```text
IF criticality = Critical
AND days_remaining <= 30
AND decision_status != Approved
THEN escalate to IT Manager + Business Owner
```

```text
IF days_remaining <= 7
AND payment_status != Completed
THEN alert daily until resolved
```

## Example Automation Workflow

```text
Renewal Register
      ↓
Daily Scheduled Check
      ↓
Calculate Days Remaining
      ↓
Apply Severity Rule
      ↓
Create Alert
      ↓
Email / Teams / Slack / WhatsApp Gateway
      ↓
Update Alert Log
      ↓
Escalate if unresolved
```

## Management Control
No critical service renewal should depend on one person's memory. Renewal ownership and escalation must be system-driven where possible.

# Executive IT Dashboard Specification

## Objective
Provide a single management view of IT service health, operational workload, risk, security, assets, renewals, vendors, projects, and budget.

## Executive Summary Cards

| KPI | Definition | Target / Threshold |
|---|---|---|
| Service Health | % of critical services in Green status | >= 95% |
| SLA Compliance | Tickets closed within SLA | >= 90% |
| Critical Incidents | Open P1 incidents | 0 |
| Backup Success | Successful scheduled backups | >= 98% |
| Patch Compliance | In-scope devices compliant | >= 95% |
| High Risks | Open High/Critical risks | Trend down |
| Renewals Due | Contracts/licenses due within 30 days | 0 unowned |
| Budget Variance | Actual vs budget | Within approved tolerance |

## Dashboard Sections

### 1. Service Health
- Critical services by Green / Amber / Red
- Availability trend
- Open major incidents
- Vendor-related outages

### 2. Helpdesk
- Tickets opened vs closed
- Backlog
- SLA compliance
- MTTR
- Ticket aging buckets
- Top issue categories
- Repeat incidents

### 3. Infrastructure & Security
- Patch compliance
- Endpoint protection coverage
- Backup success
- Restore tests
- Critical vulnerabilities / findings
- Privileged access review status

### 4. Assets
- Total assets
- Assigned / Stock / Repair / Retired
- Warranty expirations
- Devices older than approved lifecycle
- Asset inventory accuracy

### 5. Vendors & Renewals
- Renewals due 120/90/60/30/14/7 days
- Contracts without owner
- Vendor SLA score
- Annual vendor spend
- Critical vendor risks

### 6. Budget
- Annual budget
- YTD actual
- Forecast
- Variance
- CAPEX vs OPEX
- Top cost categories

### 7. Risks
- Risk heatmap
- High/Critical open risks
- Overdue mitigations
- Risks requiring management decision

### 8. Projects
- Project progress
- RAG status
- Next milestone
- Budget status
- Top dependency / blocker

## Filters
- Date range
- Branch / location
- Department
- Service
- Vendor
- Asset category
- Priority / severity
- Project

## Recommended RAG Rules

### Green
Within target and no immediate management action.

### Amber
Target at risk, negative trend, approaching renewal, overdue action, or medium/high residual risk.

### Red
Critical service failure, P1 incident, missed critical renewal, failed recovery control, major security exposure, or approved threshold breach.

## Management Questions the Dashboard Must Answer
1. Is the business currently operationally safe from an IT perspective?
2. What is failing or at risk of failing?
3. Which issue has the highest business impact?
4. What needs management approval or funding?
5. What renewals or deadlines can cause service interruption?
6. Are backup and recovery controls actually working?
7. Is IT spend within plan?
8. Are projects moving toward agreed outcomes?

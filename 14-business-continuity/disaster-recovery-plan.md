# Disaster Recovery Plan Template

## 1. Purpose
Define how critical IT services will be restored after a major outage, cyber incident, infrastructure failure, data loss event, or site disruption.

## 2. Critical Services

| Service | Business Owner | IT Owner | Criticality | RTO | RPO | Recovery Method | Dependencies |
|---|---|---|---|---|---|---|---|
| ERP | Finance / Operations | IT | Critical | 4 hours | 1 hour | Restore / provider recovery | Internet, identity, database |

## 3. Recovery Priorities
1. Identity / authentication
2. Connectivity
3. Core business applications
4. Business email / collaboration
5. File/data services
6. Supporting services

Adapt priorities to the organization.

## 4. Recovery Team
- Incident/DR Lead
- Infrastructure Owner
- Application Owner
- Business Representative
- Vendor Contacts
- Communications Owner

## 5. Recovery Procedure
1. Declare incident / disaster according to agreed criteria.
2. Confirm safety and business impact.
3. Establish command channel.
4. Identify affected systems and dependencies.
5. Select recovery strategy.
6. Restore infrastructure/services in priority order.
7. Validate data integrity.
8. Obtain business validation.
9. Communicate restoration status.
10. Conduct post-incident review.

## 6. Required Evidence
- Backup reports
- Restore-test evidence
- Vendor escalation contacts
- Configuration backups
- Recovery credentials stored securely
- Architecture/network documentation

## 7. Testing
DR plans should be exercised periodically using tabletop tests, component restore tests, or full recovery simulations appropriate to the risk.

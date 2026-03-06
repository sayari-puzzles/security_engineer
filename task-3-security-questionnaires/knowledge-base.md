# Security Knowledge Base (Mock Vanta-Style)

Use only this file as the approved source of truth for drafting responses.

## Company Security Program

1. We maintain a formal information security program reviewed annually.
2. Policies are owned by Security and approved by executive leadership.
3. All employees complete security awareness training at onboarding and annually.

## Access Control

4. Workforce access is managed through SSO with MFA enforced.
5. Privileged access is restricted by least privilege and reviewed quarterly.
6. Access is removed within defined SLA after termination.

## Infrastructure and Encryption

7. Data in transit is encrypted using TLS 1.2+.
8. Data at rest is encrypted using cloud-provider managed keys.
9. Secrets are stored in a centralized secrets manager, not in source code.

## Application Security

10. All production changes require pull request review.
11. CI pipeline runs dependency and secret scans.
12. High-severity findings block release unless risk accepted by Security.
13. External penetration tests are performed at least annually.

## Monitoring and Incident Response

14. Security events are centrally logged and monitored.
15. On-call process exists for high-severity security alerts.
16. Incident response plan is documented and tested at least annually.
17. Customer notification target for confirmed material incidents is 72 hours.

## Compliance and Assurance

18. We maintain a SOC 2 Type II report for in-scope services.
19. We map controls to ISO 27001 and applicable AI governance requirements.
20. We maintain a subprocessor inventory and notify customers of changes per contract.

## Data Governance

21. Customer data retention follows documented policy and contractual obligations.
22. Data deletion requests are supported through documented workflows.
23. Backups are encrypted and periodically tested for restoration.

## AI Governance (If Applicable)

24. Prompt/model changes are reviewed through change management controls.
25. High-impact AI changes require an AI impact assessment.
26. Fairness/bias and transparency checks are part of AI governance review.
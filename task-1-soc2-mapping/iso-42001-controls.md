# Internal ISO 42001 Control Reference (Sample)

Use this as the target control set for mapping SOC 2 evidence.

## Control Domains

### GOV - AI Governance

| ID | Control Objective | Control Statement | Evidence Examples |
|---|---|---|---|
| GOV-01 | Governance framework | Maintain approved AI governance policy and ownership model | Policy doc, RACI |
| GOV-02 | Accountability | Assign accountable owner for each AI system | System inventory, owner register |
| GOV-03 | Risk appetite | Define risk thresholds for model behavior and business use | Risk standard, KRIs |
| GOV-04 | Review cadence | Conduct governance review at defined intervals | Steering committee minutes |

### RSK - AI Risk Management

| ID | Control Objective | Control Statement | Evidence Examples |
|---|---|---|---|
| RSK-01 | Risk identification | Identify AI risks across lifecycle (data, model, prompt, output) | Risk register |
| RSK-02 | Risk scoring | Apply severity/likelihood scoring with clear criteria | Scoring rubric |
| RSK-03 | Risk treatment | Define and track mitigation plans for material risks | Action tracker |
| RSK-04 | Residual risk | Record residual risk and approver for accepted risk | Approval log |

### DSC - Data and Security Controls

| ID | Control Objective | Control Statement | Evidence Examples |
|---|---|---|---|
| DSC-01 | Data provenance | Track source and lineage of training/evaluation data | Data lineage logs |
| DSC-02 | Data quality | Validate quality and suitability before use | Validation reports |
| DSC-03 | Sensitive data handling | Enforce restrictions for personal/sensitive data in AI flows | DLP logs, policy |
| DSC-04 | Access control | Apply least privilege for model, prompt, and data assets | IAM review artifacts |
| DSC-05 | Cryptographic controls | Encrypt AI data at rest/in transit | Config evidence |

### DEV - AI Lifecycle and Change Management

| ID | Control Objective | Control Statement | Evidence Examples |
|---|---|---|---|
| DEV-01 | Change trigger | Require impact assessment for prompt/model/data changes | PR template, workflow |
| DEV-02 | Secure development | Include security checks in AI development pipeline | CI logs |
| DEV-03 | Testing and validation | Run pre-release tests for safety, quality, fairness | Test reports |
| DEV-04 | Deployment approval | Require role-based approvals before production rollout | Approval history |
| DEV-05 | Rollback readiness | Maintain tested rollback plan for high-risk updates | Runbooks |

### IMP - AI Impact Assessment (AIIA)

| ID | Control Objective | Control Statement | Evidence Examples |
|---|---|---|---|
| IMP-01 | Assessment requirement | Perform AIIA for significant AI system changes | Completed forms |
| IMP-02 | Scope definition | Capture impacted users, use cases, and downstream effects | Assessment records |
| IMP-03 | Bias/fairness analysis | Assess disparate impact and fairness risk | Fairness test results |
| IMP-04 | Transparency analysis | Assess explainability and user disclosure impacts | UX/docs evidence |
| IMP-05 | Human oversight | Define human decision points for high-impact outcomes | SOPs |

### MON - Monitoring and Incident Response

| ID | Control Objective | Control Statement | Evidence Examples |
|---|---|---|---|
| MON-01 | Performance monitoring | Monitor drift, degradation, and anomalous behavior | Monitoring dashboards |
| MON-02 | Harm monitoring | Detect and triage potentially harmful outputs | Incident queue |
| MON-03 | Logging and traceability | Log prompts, outputs, model versions, and decisions | Audit logs |
| MON-04 | Incident response | Maintain response process for AI incidents | Playbooks, PIRs |

### TRN - Transparency and Documentation

| ID | Control Objective | Control Statement | Evidence Examples |
|---|---|---|---|
| TRN-01 | System documentation | Maintain current AI system documentation and boundaries | Architecture docs |
| TRN-02 | User transparency | Provide appropriate disclosures on AI usage | Product disclosures |
| TRN-03 | Limitation statements | Document known limitations and failure modes | Model cards |
| TRN-04 | Audit readiness | Keep evidence package for internal/external audit | Control evidence set |

## Mapping Guidance

For each SOC 2 control/evidence item, map to:
1. Most relevant ISO 42001 control ID(s)
2. Mapping confidence (`High`, `Medium`, `Low`)
3. Rationale (1-2 sentences)
4. Gap or follow-up required (if any)

## Expected Output Format

| SOC 2 Ref | SOC 2 Description | ISO 42001 Control(s) | Confidence | Rationale | Gap/Action |
|---|---|---|---|---|---|
| SEC-06 / EV-004 | CI security scan logs | DEV-02, DSC-03 | High | CI evidence shows integrated security checks | Add explicit AI safety test evidence |

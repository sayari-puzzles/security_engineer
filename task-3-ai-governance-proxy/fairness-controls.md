# Internal Fairness, Bias, and Transparency Controls (Sample)

Use these controls as the policy source for your automated governance proxy.

## Fairness Controls

| ID | Requirement | Severity if Violated |
|---|---|---|
| F-01 | System prompts must not instruct differential treatment by protected characteristics (race, religion, sex, gender identity, sexual orientation, disability, age, national origin). | Critical |
| F-02 | Prompts must not include instructions to infer protected traits unless explicitly approved for legal/compliance purpose. | High |
| F-03 | Prompts must not deny service or quality based on inferred socioeconomic status proxies (ZIP code, school, neighborhood) unless policy-approved. | High |
| F-04 | High-impact decisions must include human-review escalation path. | High |
| F-05 | Prompt changes affecting eligibility/recommendation logic require fairness regression testing. | High |

## Bias Risk Controls

| ID | Requirement | Severity if Violated |
|---|---|---|
| B-01 | Prompt changes must not add language that prioritizes or deprioritizes outcomes for specific demographic groups. | Critical |
| B-02 | Prompt changes must preserve neutral phrasing and avoid stereotype reinforcement. | High |
| B-03 | Any use of sensitive attributes in decision logic must be tagged and documented in an approved exception list. | Critical |
| B-04 | If uncertainty is high, prompts must prefer abstain/escalate behavior over speculative claims. | Medium |

## Transparency Controls

| ID | Requirement | Severity if Violated |
|---|---|---|
| T-01 | User-facing AI responses must disclose they are AI-assisted where required by product policy. | Medium |
| T-02 | Prompts must not instruct the model to conceal uncertainty or suppress caveats. | High |
| T-03 | High-impact recommendations must include explanation fields or reason codes. | Medium |
| T-04 | Policy-relevant prompt changes must update changelog metadata (owner, ticket, rationale). | Low |

## Enforcement Suggestion

For each proposed prompt change:
1. Parse diff and classify semantic intent.
2. Check for prohibited patterns and policy keywords.
3. Run LLM-based policy classification with deterministic fallback rules.
4. Return: `allow`, `allow_with_review`, or `block`.
5. Emit machine-readable result (JSON) and human-readable rationale.

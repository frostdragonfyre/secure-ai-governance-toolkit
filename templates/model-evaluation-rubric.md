# Model Evaluation Rubric

This rubric evaluates whether an AI system, model, agent, or AI-enabled workflow performs **reliably enough, safely enough, and transparently enough** to support a specific business, security, legal, ethical, and operational decision.

It is not a general "does it work" checklist. It is a decision instrument: its output is a defensible, evidence-backed recommendation to approve, approve-with-conditions, remediate, or reject.

Complete this rubric before approving a new AI use case, materially changing an existing system, adopting a vendor AI tool, or moving an AI-enabled workflow into production.

> **How depth is decided:** Not every section applies to every system. Complete **Section 0 first** to set the risk tier; the tier determines which sections are mandatory. Applying all 27 sections to a low-risk tool is theater; skipping them on a high-risk one is negligence.

---

## 0. Risk Tier Gate (complete first)

Answer these gating questions. The highest triggered tier governs.

| Trigger | If yes → minimum tier |
|---|---|
| System can take actions autonomously (no human in the loop before effect) | **Tier 3** |
| System processes regulated or sensitive personal data | **Tier 3** |
| Output materially affects a person's rights, access, benefits, employment, or legal standing | **Tier 3** |
| Output is customer- or public-facing | **Tier 2** |
| System informs a human decision but cannot act on its own | **Tier 2** |
| Internal-only, reference/productivity use, human always interprets output, no sensitive data | **Tier 1** |

| Tier | Meaning | Mandatory sections |
|---|---|---|
| **Tier 1 — Low** | Internal, advisory, low blast radius | 1, 2, 3, 5, 8, 9, 12, 20, 21, 23, 24 |
| **Tier 2 — Moderate** | Informs decisions or reaches external users | All Tier 1 + 4, 6, 7, 10, 11, 13, 16, 17, 18, 19, 25, 28 |
| **Tier 3 — High/Critical** | Autonomous, regulated, or rights-affecting | **All sections**, plus mandatory independent reviewer and named risk-owner acceptance |

> **Selected tier:** `Tier 1 / Tier 2 / Tier 3`  ·  **Triggers that set it:** ______

---

## 1. Rubric Information

| Field | Response |
|---|---|
| Evaluation ID *(unique, traceable)* |  |
| Evaluation name |  |
| AI system or model name |  |
| Version or release *(pin the exact build)* |  |
| Risk tier *(from §0)* |  |
| Business owner |  |
| Technical owner |  |
| Security reviewer |  |
| Privacy reviewer |  |
| Legal or compliance reviewer |  |
| Risk owner *(accepts residual risk)* |  |
| Evaluation date |  |
| Approval expiration / next re-review date |  |
| Review status | Draft / In Review / Approved / Approved with Conditions / Rejected |
| Related intake document |  |
| Related risk register entry |  |
| Related model card |  |
| Related security review |  |

## 2. Evaluation Purpose

| Question | Response |
|---|---|
| What decision is this evaluation intended to support? |  |
| Trigger type | New system / Vendor review / Model update / Prompt change / Workflow change / Periodic review |
| What specific approval decision is needed? |  |
| What would cause this system to be rejected or sent back? *(define before testing)* |  |
| What evidence will be used to support the decision? |  |

## 3. System and Use Case Context

| Field | Response |
|---|---|
| Primary use case |  |
| Business process supported |  |
| User group |  |
| Expected users | Internal staff / External users / Customers / Contractors / Public |
| Deployment environment | Development / Test / Pilot / Production |
| Model type | LLM / Classifier / Recommender / Computer vision / Forecasting / Agentic workflow / Other |
| Vendor or provider |  |
| Internal or external model | Internal / External / Hybrid |
| Human decision-maker involved? | Yes / No |
| Automated decision-making involved? | Yes / No |
| High-impact or sensitive use case? | Yes / No |
| Description of high-impact factors |  |

## 4. Model Provenance and Supply Chain *(Tier 2+)*

Weak provenance is itself a risk. You cannot govern what you cannot trace.

| Question | Response |
|---|---|
| Where does the model originate? | Built in-house / Open weights / Vendor closed / Fine-tune of base model |
| Base model and version, if fine-tuned |  |
| Is training-data provenance documented by the provider? | Yes / No / Partial |
| Known training-data licensing or IP concerns? |  |
| Is the model snapshot pinned, or can the vendor change it under us? |  |
| Vendor change-notification commitment | Yes / No / Unknown |
| Supply-chain or dependency risks identified |  |

## 5. Intended Use and Prohibited Use

| Category | Description |
|---|---|
| Intended use |  |
| Approved users |  |
| Approved data types |  |
| Approved output types |  |
| Approved decision context |  |
| Prohibited uses |  |
| Out-of-scope users / data / decisions |  |
| Escalation requirements |  |

## 6. Evaluation Dataset and Sample Adequacy

| Field | Response |
|---|---|
| Dataset name / owner / source |  |
| Creation and refresh dates |  |
| Number of records or examples |  |
| **Is the sample large enough for the reported metrics to be meaningful?** | Yes / No — justify |
| **Reporting confidence intervals on key metrics?** | Yes / No |
| Data classification | Public / Internal / Confidential / Restricted |
| Contains personal / sensitive / regulated data? | Yes / No (each) |
| Synthetic vs. real production data |  |
| Representative of expected use? | Yes / No |
| Known dataset limitations |  |

> **Why this matters:** a high score on a tiny or unrepresentative sample is not evidence. If N is small, report confidence intervals and treat results as provisional.

## 7. Ground Truth and Label Quality *(Tier 2+)*

| Question | Response |
|---|---|
| Ground truth source |  |
| Who created / validated the labels, and what expertise was required? |  |
| More than one reviewer used? | Yes / No |
| Was inter-rater agreement measured? *(e.g., Cohen's/Fleiss' kappa)* | Yes / No — value: ___ |
| How were disagreements resolved? |  |
| Are labels current and valid for the use case? | Yes / No |
| Label quality concerns / assumptions |  |

## 8. Metric Selection

Select metrics by decision context. Do not rely on accuracy alone when data is imbalanced or error costs are asymmetric. For purely generative systems, classification metrics often do not apply — drive the evaluation from §12 (qualitative review) instead, and treat any automated "LLM-as-judge" scoring as needing human validation.

| Metric | Use when | Selected? | Rationale |
|---|---|---:|---|
| Accuracy | Correctness matters and classes are balanced |  |  |
| Precision | False positives are costly |  |  |
| Recall | False negatives are costly |  |  |
| F1 | Precision and recall both matter |  |  |
| Specificity | Correctly identifying negatives matters |  |  |
| False positive rate | Incorrect flags create burden/harm |  |  |
| False negative rate | Missed cases create risk |  |  |
| Calibration *(state method: ECE / Brier)* | Confidence scores drive decisions |  |  |
| Latency *(p50 / p95 / p99 — not average)* | Response time affects usability |  |  |
| Cost per task | Cost affects scale/approval |  |  |
| Human override rate | Reviewers frequently disagree |  |  |
| Escalation rate | System often needs expert review |  |  |

## 9. Threshold Pre-Registration

**Set thresholds before viewing results.** This prevents moving the goalposts to fit the outcome. Tie each threshold to the error cost documented in §11.

| Metric | Pre-registered threshold | Basis for threshold | Set by | Date set (before results?) |
|---|---|---|---|---|
| Primary metric |  |  |  |  |
| Secondary metric |  |  |  |  |
| Hard fail condition |  |  |  |  |

## 10. Core Performance Results

| Metric | Threshold (from §9) | Actual | 95% CI | Pass/Fail | Notes |
|---|---|---|---|---|---|
| Accuracy |  |  |  |  |  |
| Precision |  |  |  |  |  |
| Recall |  |  |  |  |  |
| F1 |  |  |  |  |  |
| False positive rate |  |  |  |  |  |
| False negative rate |  |  |  |  |  |
| Calibration error |  |  |  |  |  |
| Latency p95 |  |  |  |  |  |
| Cost per task |  |  |  |  |  |
| Human override rate |  |  |  |  |  |
| Escalation rate |  |  |  |  |  |

## 11. Error Impact and Baseline Comparison

Document what errors *cost*, and whether the system beats what it replaces. A model can pass every threshold and still be worse than the current process.

| Error type | Example here | Business / Security / Legal / User impact | Severity |
|---|---|---|---|
| False positive |  |  | Low / Med / High / Critical |
| False negative |  |  | Low / Med / High / Critical |
| Hallucinated output |  |  | Low / Med / High / Critical |
| Overconfident output |  |  | Low / Med / High / Critical |

| Baseline question | Response |
|---|---|
| What does this replace or augment? *(human / rules / prior model)* |  |
| Is the AI measurably better than that baseline? | Yes / No / Unclear |
| If not clearly better, why adopt it? |  |

## 12. Qualitative Output Review *(required for generative systems)*

| Review area | Rating | Evidence |
|---|---|---|
| Factual correctness | Poor / Fair / Good / Excellent |  |
| Completeness |  |  |
| Clarity |  |  |
| Consistency |  |  |
| Citation / source quality | … / Not Applicable |  |
| Reasoning quality |  |  |
| Instruction following |  |  |
| Refusal behavior |  |  |
| Appropriate uncertainty |  |  |
| Tone and domain appropriateness |  |  |

## 13. Robustness and Edge-Case Testing *(Tier 2+)*

| Category | Test | Result | Risk | Remediation |
|---|---|---|---|---|
| Ambiguous / incomplete / conflicting inputs |  | Pass / Fail / Partial |  |  |
| Out-of-domain inputs |  | Pass / Fail / Partial |  |  |
| Low-quality / noisy data |  | Pass / Fail / Partial |  |  |
| Rare and boundary cases |  | Pass / Fail / Partial |  |  |
| Sensitive / high-risk scenarios |  | Pass / Fail / Partial |  |  |

## 14. Prompt Injection and Misuse Testing *(Tier 3, or any system using prompts/retrieval/tools/agents/user content)*

| Test area | Result | Notes |
|---|---|---|
| Direct prompt injection | Pass / Fail / Partial / N/A |  |
| Indirect prompt injection (via documents, web, retrieved content) | … |  |
| Tool misuse / unauthorized action | … |  |
| Data exfiltration attempt | … |  |
| System-prompt extraction | … |  |
| Jailbreak / unsafe-content request | … |  |

## 15. Bias, Fairness, and Representational Harm *(Tier 3, or any rights-affecting use)*

| Question | Response |
|---|---|
| Protected/sensitive attributes used directly or inferable indirectly? |  |
| Performance evaluated across relevant groups? |  |
| Disparities identified, and mitigations taken? |  |
| Human review required for sensitive outcomes? |  |
| Who reviewed fairness concerns? |  |

## 16. Privacy and Data Protection *(Tier 2+)*

| Question | Response |
|---|---|
| Processes personal / sensitive / regulated data? |  |
| Data minimized to what is necessary? |  |
| Retention period |  |
| Used for model training or improvement? |  |
| Opt-out available where required? |  |
| Shared with vendor/third party? |  |
| Privacy notices / additional controls required? |  |

## 17. Security Evaluation *(Tier 2+)*

| Area | Question | Result | Notes |
|---|---|---|---|
| Access control | Only authorized users access the system? | Pass / Fail / Partial |  |
| Data access | System reaches only approved sources? | … |  |
| Logging | Prompts, outputs, actions, errors logged? | … |  |
| Secrets handling | Credentials/tokens protected? | … |  |
| Output handling | Outputs protected per classification? | … |  |
| Tool permissions | Tools limited to approved actions? | … / N/A |  |
| Retrieval security | Documents filtered by user permission? | … / N/A |  |
| Incident escalation | Defined AI-incident escalation path? | … |  |

## 18. Human Review and Recourse *(Tier 2+; recourse mandatory for rights-affecting use)*

| Question | Response |
|---|---|
| Human review required before action? Which outputs? |  |
| Reviewer role, criteria, and training required |  |
| Can users override the system, and are overrides logged? |  |
| **Can an affected person contest or appeal an AI-influenced decision?** |  |
| **What is the recourse/remediation path for a wrong decision?** |  |

## 19. Monitoring, Drift, and Re-Review *(Tier 2+)*

| Area | Required? | Owner | Frequency |
|---|---|---|---|
| Accuracy / precision / recall monitoring |  |  |  |
| False positive & negative sampling review |  |  |  |
| Output quality & user-feedback review |  |  |  |
| Bias / fairness monitoring |  |  |  |
| Prompt-injection & misuse monitoring |  |  |  |
| Data & model drift monitoring |  |  |  |
| Vendor-change monitoring |  |  |  |

**Re-review triggers** *(approval is not permanent — any of these forces re-evaluation):*
- [ ] New model or version
- [ ] Vendor terms or model snapshot changed
- [ ] New data type or user group
- [ ] Move from pilot → production, or internal → external
- [ ] Security incident or quality regression
- [ ] Relevant regulatory change
- [ ] Approval expiration date reached

## 20. Evaluation Reproducibility

Weak reproducibility means weak evidence. Anyone should be able to re-run this evaluation and get materially the same result.

| Field | Response |
|---|---|
| Exact model identifier / snapshot / date |  |
| Decoding parameters *(temperature, top-p, max tokens, seed)* |  |
| Evaluation harness / code version or commit |  |
| Prompt templates versioned? |  |
| Can this evaluation be re-run by someone else? | Yes / No |

## 21. Framework Mapping

Map evidence to the frameworks your organization is accountable to. Precision beats breadth — one correct mapping is worth more than a wide, vague crosswalk.

| Rubric area | NIST AI RMF function | ISO/IEC 42001 | EU AI Act | OWASP LLM Top 10 |
|---|---|---|---|---|
| §15 Bias/fairness | Measure / Manage | Impact assessment | Non-discrimination duties | — |
| §14 Prompt injection | Measure | — | — | LLM01 / LLM02 |
| §17 Security | Manage | Controls | — | LLM06 / LLM08 |
| §16 Privacy | Map / Manage | Data governance | Data governance duties | LLM06 |
| §18 Human oversight & recourse | Govern | — | Human oversight; right to explanation | — |
| §19 Monitoring | Manage | Continual improvement | Post-market monitoring | — |
| §4 Provenance | Map | — | Technical documentation | LLM05 (supply chain) |

> Fill the cells that apply to *your* obligations; delete rows that don't. Cite the specific clause/article where you can — that precision is what makes the rubric auditable.

## 22. Risk Rating and Aggregation

Rate each domain, then derive the overall rating by an explicit rule — don't assert it.

| Risk domain | Rating |
|---|---|
| Performance | Low / Med / High / Critical |
| Security | … |
| Privacy | … |
| Legal / compliance | … |
| Fairness / bias | … |
| Operational | … |
| Reputational | … |

**Aggregation rule (state the one you use):**
- Default: **overall residual risk = the highest single domain rating**, unless a documented, accepted mitigation lowers that domain.
- **Any `Critical` domain** blocks routine approval and requires named risk-owner (and, for Tier 3, executive) acceptance with written rationale.
- Multiple `High` domains escalate the overall rating one level.

> **Overall residual risk:** ______  ·  **Derived how:** ______

## 23. Approval Decision

| Decision | Selected? | Notes |
|---|---:|---|
| Approved for production |  |  |
| Approved for limited pilot |  |  |
| Approved with conditions |  |  |
| Requires remediation and re-review |  |  |
| Rejected |  |  |
| Deferred pending evidence |  |  |

**Approval rationale** *(the most important free-text field in this rubric — explain the judgment, including any tradeoff accepted and why):*
```text

```

**Conditions / restrictions / expiration:**
```text

```

## 24. Reviewer Sign-Off

| Role | Name | Decision | Date |
|---|---|---|---|
| Business owner |  | Approve / Reject / Conditional |  |
| Technical owner |  | Approve / Reject / Conditional |  |
| Security reviewer *(Tier 2+)* |  | Approve / Reject / Conditional |  |
| Privacy reviewer *(Tier 2+)* |  | Approve / Reject / Conditional |  |
| Legal / compliance *(Tier 2+)* |  | Approve / Reject / Conditional |  |
| Independent reviewer *(Tier 3)* |  | Approve / Reject / Conditional |  |
| Risk owner |  | Accept / Reject / Conditional |  |

## 25. Required Remediation

| Item | Risk addressed | Owner | Due | Blocks approval? | Status |
|---|---|---|---|---:|---|
|  |  |  |  |  | Not Started / In Progress / Complete |

## 26. Review History

| Version | Date | Reviewer | Change summary |
|---|---|---|---|
| 0.1 |  |  | Initial draft |

## 27. Reviewer Notes

```text

```

## 28. Practical Reviewer Checklist *(Tier 2+)*

| Item | Complete? |
|---|---:|
| Risk tier set and correct sections completed |  |
| Sample size adequate; CIs reported where N is small |  |
| Thresholds pre-registered before results |  |
| Metrics matched to error costs (not accuracy-alone) |  |
| Compared against the baseline it replaces |  |
| Edge cases and (where relevant) injection/misuse tested |  |
| Bias, privacy, and security reviewed at required depth |  |
| Human review, override, and recourse defined |  |
| Monitoring plan and re-review triggers documented |  |
| Evaluation is reproducible (model pinned, params recorded) |  |
| Overall risk derived by stated rule, not asserted |  |
| Residual risk accepted by named owner; rationale written |  |

# Model Card Template

Use this template to document an AI model, AI-enabled system, or AI use case before approval, deployment, procurement, or material change.

This model card is intended to create reviewable governance evidence. It should be completed by the system owner with input from security, privacy, legal, compliance, procurement, engineering, and business stakeholders as needed.

## 1. Basic information

| Field                          | Response                                   |
| ------------------------------ | ------------------------------------------ |
| Model or system name           |                                            |
| Version                        |                                            |
| Date completed                 |                                            |
| Business owner                 |                                            |
| Technical owner                |                                            |
| Risk owner                     |                                            |
| Vendor or provider             |                                            |
| Internal or third-party system |                                            |
| Deployment environment         |                                            |
| Current status                 | Proposed / Pilot / Production / Deprecated |
| Review cadence                 |                                            |
| Next review date               |                                            |

## 2. Purpose and intended use

### Business purpose

Describe the business problem this model or AI system is intended to solve.

```text
[Enter business purpose here]
```

### Intended users

List the expected user groups.

```text
[Enter intended users here]
```

### Intended outputs

Describe the outputs the model or AI system is expected to produce.

```text
[Enter intended outputs here]
```

### Intended decisions or workflows supported

Describe whether the model supports, recommends, automates, or influences any business decision or workflow.

```text
[Enter supported decisions or workflows here]
```

### Out-of-scope uses

List uses that are not approved.

```text
[Enter prohibited or out-of-scope uses here]
```

## 3. System overview

### Model or system type

Select all that apply.

* [ ] Large language model
* [ ] Retrieval-augmented generation system
* [ ] Predictive model
* [ ] Classification model
* [ ] Recommendation system
* [ ] Computer vision model
* [ ] Speech or audio model
* [ ] Agentic AI system
* [ ] AI-enabled SaaS product
* [ ] Internal automation
* [ ] Other:

### System description

Provide a plain-language description of how the system works.

```text
[Enter system description here]
```

### Key components

| Component                     | Description | Owner |
| ----------------------------- | ----------- | ----- |
| Model                         |             |       |
| Application                   |             |       |
| Data source                   |             |       |
| Retrieval system              |             |       |
| Prompt or configuration layer |             |       |
| Logging and monitoring        |             |       |
| Human review process          |             |       |

### External dependencies

List vendors, APIs, cloud services, datasets, plugins, tools, or third-party integrations.

| Dependency | Purpose | Data shared | Contract or review status |
| ---------- | ------- | ----------- | ------------------------- |
|            |         |             |                           |

## 4. Data

### Input data

Describe the data the system receives from users, applications, files, APIs, databases, or other systems.

```text
[Enter input data description here]
```

### Training data

Describe known training data, fine-tuning data, or vendor-provided training information.

```text
[Enter training data description here]
```

### Retrieval or grounding data

For retrieval-augmented generation or knowledge systems, describe the sources used for grounding.

```text
[Enter retrieval or grounding data here]
```

### Output data

Describe the data produced by the system.

```text
[Enter output data description here]
```

### Data classification

Select all that apply.

* [ ] Public
* [ ] Internal
* [ ] Confidential
* [ ] Restricted
* [ ] Regulated
* [ ] Customer data
* [ ] Employee data
* [ ] Financial data
* [ ] Legal data
* [ ] Security data
* [ ] Source code
* [ ] Authentication or access data
* [ ] Personal data
* [ ] Sensitive personal data
* [ ] Other:

### Data handling notes

Document retention, storage, transmission, encryption, access control, and vendor data-use commitments.

```text
[Enter data handling notes here]
```

## 5. Risk classification

### Overall risk rating

Select one.

* [ ] Low
* [ ] Medium
* [ ] High
* [ ] Critical

### Risk rationale

Explain why this risk rating was selected.

```text
[Enter risk rationale here]
```

### Risk factors

Select all that apply.

* [ ] Uses sensitive or regulated data
* [ ] Produces customer-facing output
* [ ] Supports high-impact decisions
* [ ] Used in security, legal, finance, HR, healthcare, or safety workflows
* [ ] Can trigger actions in other systems
* [ ] Has access to internal tools, plugins, APIs, or agents
* [ ] Uses third-party or vendor-hosted models
* [ ] Uses retrieval from internal knowledge sources
* [ ] May produce inaccurate, misleading, or harmful outputs
* [ ] May expose confidential information
* [ ] May be vulnerable to prompt injection or data poisoning
* [ ] May create intellectual property, licensing, or attribution concerns
* [ ] Has limited explainability
* [ ] Has limited monitoring
* [ ] Other:

## 6. Limitations and assumptions

### Known limitations

Describe known model, system, data, process, or vendor limitations.

```text
[Enter known limitations here]
```

### Assumptions

List assumptions relied on during review or approval.

```text
[Enter assumptions here]
```

### Conditions where the model may fail

Describe contexts where performance, safety, accuracy, security, or reliability may degrade.

```text
[Enter failure conditions here]
```

### Required user warnings or disclaimers

List warnings that must be shown to users.

```text
[Enter required warnings here]
```

## 7. Evaluation

### Evaluation summary

Summarize how the model or system was evaluated.

```text
[Enter evaluation summary here]
```

### Evaluation methods

Select all that apply.

* [ ] Functional testing
* [ ] Accuracy testing
* [ ] Security testing
* [ ] Red-team testing
* [ ] Prompt injection testing
* [ ] Bias or fairness testing
* [ ] Privacy review
* [ ] Human review
* [ ] Vendor documentation review
* [ ] Production monitoring review
* [ ] Other:

### Evaluation results

| Evaluation area  | Method | Result | Notes |
| ---------------- | ------ | ------ | ----- |
| Accuracy         |        |        |       |
| Reliability      |        |        |       |
| Security         |        |        |       |
| Privacy          |        |        |       |
| Bias or fairness |        |        |       |
| Explainability   |        |        |       |
| User experience  |        |        |       |
| Monitoring       |        |        |       |

### Minimum acceptable performance

Document the minimum acceptable thresholds for approval or continued use.

```text
[Enter minimum acceptable performance here]
```

### Evaluation gaps

List any evaluation gaps or unresolved concerns.

```text
[Enter evaluation gaps here]
```

## 8. Security review

### Security concerns

Select all that apply.

* [ ] Prompt injection
* [ ] Sensitive data leakage
* [ ] Unauthorized access to retrieved content
* [ ] Insecure plugin, tool, or agent access
* [ ] Model output used without validation
* [ ] Data poisoning
* [ ] Training data exposure
* [ ] Excessive permissions
* [ ] Inadequate logging
* [ ] Inadequate monitoring
* [ ] Vendor security uncertainty
* [ ] Supply-chain or provenance concerns
* [ ] Other:

### Required security controls

| Control                      | Required? | Owner | Status | Notes |
| ---------------------------- | --------: | ----- | ------ | ----- |
| Access control               |           |       |        |       |
| Least privilege              |           |       |        |       |
| Data loss prevention         |           |       |        |       |
| Prompt injection mitigations |           |       |        |       |
| Output validation            |           |       |        |       |
| Human review                 |           |       |        |       |
| Logging                      |           |       |        |       |
| Monitoring                   |           |       |        |       |
| Incident response path       |           |       |        |       |
| Vendor security review       |           |       |        |       |

### Security review notes

```text
[Enter security review notes here]
```

## 9. Privacy, legal, and compliance

### Privacy considerations

```text
[Enter privacy considerations here]
```

### Legal or contractual considerations

```text
[Enter legal or contractual considerations here]
```

### Compliance considerations

```text
[Enter compliance considerations here]
```

### Required approvals

| Function       | Approval required? | Approver | Date | Notes |
| -------------- | -----------------: | -------- | ---- | ----- |
| Security       |                    |          |      |       |
| Privacy        |                    |          |      |       |
| Legal          |                    |          |      |       |
| Compliance     |                    |          |      |       |
| Procurement    |                    |          |      |       |
| Business owner |                    |          |      |       |

## 10. Human oversight

### Human role

Describe how humans review, approve, override, or monitor the model output.

```text
[Enter human oversight process here]
```

### Human review required

Select one.

* [ ] Always required before action
* [ ] Required for high-risk outputs only
* [ ] Required by sampling
* [ ] Not required
* [ ] Not applicable

### Escalation process

Describe how users escalate concerns, errors, unsafe outputs, or incidents.

```text
[Enter escalation process here]
```

## 11. Monitoring and logging

### Monitoring approach

Describe how the system is monitored after deployment.

```text
[Enter monitoring approach here]
```

### Logged events

Select all that apply.

* [ ] User prompts
* [ ] Model responses
* [ ] Retrieved documents or sources
* [ ] Tool or plugin calls
* [ ] User feedback
* [ ] Errors
* [ ] Policy violations
* [ ] Security alerts
* [ ] Administrative changes
* [ ] Model or configuration changes
* [ ] Other:

### Metrics

| Metric | Purpose | Owner | Review frequency |
| ------ | ------- | ----- | ---------------- |
|        |         |       |                  |

### Monitoring gaps

```text
[Enter monitoring gaps here]
```

## 12. Incident response

### Potential incident types

Select all that apply.

* [ ] Sensitive data exposure
* [ ] Unauthorized access
* [ ] Harmful or unsafe output
* [ ] Material hallucination or misinformation
* [ ] Prompt injection
* [ ] Vendor compromise
* [ ] Model or configuration change without review
* [ ] Misuse by authorized user
* [ ] Abuse by external user
* [ ] Other:

### Incident response owner

```text
[Enter incident response owner here]
```

### Escalation path

```text
[Enter escalation path here]
```

### Required response actions

```text
[Enter required response actions here]
```

## 13. Approval decision

### Decision

Select one.

* [ ] Approved
* [ ] Approved with conditions
* [ ] Deferred
* [ ] Rejected

### Decision rationale

```text
[Enter decision rationale here]
```

### Required conditions

List any conditions that must be met before deployment or continued use.

```text
[Enter required conditions here]
```

### Open risks

| Risk | Owner | Mitigation | Due date |
| ---- | ----- | ---------- | -------- |
|      |       |            |          |

### Approval record

| Role                | Name | Decision | Date |
| ------------------- | ---- | -------- | ---- |
| Business owner      |      |          |      |
| Technical owner     |      |          |      |
| Security            |      |          |      |
| Privacy             |      |          |      |
| Legal or compliance |      |          |      |
| Risk owner          |      |          |      |

## 14. Change management

### Material change triggers

A new review is required if any of the following occur.

* [ ] New model or model version
* [ ] New vendor or provider
* [ ] New data source
* [ ] New user group
* [ ] New integration
* [ ] New tool, plugin, or agent capability
* [ ] Expanded permissions
* [ ] Production rollout
* [ ] Material prompt or configuration change
* [ ] Change in retention or logging
* [ ] Security incident
* [ ] Failed evaluation
* [ ] Regulatory, contractual, or policy change
* [ ] Other:

### Review history

| Date | Reviewer | Reason for review | Outcome |
| ---- | -------- | ----------------- | ------- |
|      |          |                   |         |

## 15. Related artifacts

Link related documents.

| Artifact                        | Link |
| ------------------------------- | ---- |
| AI use case intake              |      |
| Threat model                    |      |
| Evaluation rubric               |      |
| Vendor review                   |      |
| Prompt and configuration review |      |
| Incident response playbook      |      |
| Control mapping                 |      |
| Governance decision record      |      |

## 16. Notes

```text
[Enter additional notes here]
```

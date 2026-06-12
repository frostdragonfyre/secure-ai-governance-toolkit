# AI Governance Decision Record

AI governance should produce evidence, not just intent.

Use this record to document the final governance decision for an AI system, model, vendor, or use case. This artifact should be completed after intake, risk review, security review, model documentation, and evaluation evidence have been reviewed.

---

## 1. Decision Summary

| Field | Response |
|---|---|
| AI system / use case name |  |
| Business owner |  |
| Technical owner |  |
| Risk owner |  |
| Decision owner |  |
| Review date |  |
| Decision status | Approved / Approved with Conditions / Deferred / Rejected |
| Final risk tier | Low / Moderate / High / Prohibited |
| Next review date |  |

### Decision statement

Briefly state the governance decision.

Example:

> Approved with conditions for limited internal use by the customer support team. The system may summarize support tickets but may not send customer-facing responses without human review.

---

## 2. Scope of Approval

Describe exactly what is approved.

| Area | Approved Scope |
|---|---|
| Users / teams |  |
| Business process |  |
| Data types |  |
| Model or vendor |  |
| Deployment environment |  |
| Integrations |  |
| Output use |  |
| Human review requirement |  |

### Out of scope

List uses that are not approved.

Examples:

- Use with regulated personal data not included in the intake
- Direct customer-facing output without review
- Autonomous account actions
- Use by teams outside the approved user group
- Model or vendor substitution without re-review

---

## 3. Evidence Reviewed

List the artifacts reviewed before making the decision.

| Evidence Artifact | Location / Link | Reviewed By | Notes |
|---|---|---|---|
| AI use case intake |  |  |  |
| AI risk register |  |  |  |
| AI security review checklist |  |  |  |
| Model card |  |  |  |
| Model evaluation rubric |  |  |  |
| Vendor review / DPA / security docs |  |  |  |
| Framework mapping |  |  |  |
| Other evidence |  |  |  |

---

## 4. Key Risks Considered

Summarize the main risks that influenced the decision.

| Risk | Severity | Disposition | Notes |
|---|---|---|---|
| Data exposure | Low / Moderate / High | Accepted / Mitigated / Blocker |  |
| Inaccurate or harmful output | Low / Moderate / High | Accepted / Mitigated / Blocker |  |
| Prompt injection or misuse | Low / Moderate / High | Accepted / Mitigated / Blocker |  |
| Vendor dependency | Low / Moderate / High | Accepted / Mitigated / Blocker |  |
| Model change or drift | Low / Moderate / High | Accepted / Mitigated / Blocker |  |
| Lack of human oversight | Low / Moderate / High | Accepted / Mitigated / Blocker |  |
| Logging or retention risk | Low / Moderate / High | Accepted / Mitigated / Blocker |  |
| Legal, regulatory, or contractual risk | Low / Moderate / High | Accepted / Mitigated / Blocker |  |

### Risk rationale

Explain why the final risk tier was selected.

---

## 5. Required Controls

List the controls required for approval.

| Control | Required? | Owner | Due Date | Evidence Required |
|---|---|---|---|---|
| Human review before external use | Yes / No |  |  |  |
| Access limited to approved users | Yes / No |  |  |  |
| Sensitive data restrictions | Yes / No |  |  |  |
| Logging and monitoring enabled | Yes / No |  |  |  |
| Output quality testing completed | Yes / No |  |  |  |
| Security review completed | Yes / No |  |  |  |
| Vendor review completed | Yes / No |  |  |  |
| Incident escalation path defined | Yes / No |  |  |  |
| Re-review triggers documented | Yes / No |  |  |  |

### Additional conditions

Document any conditions that must be satisfied before or after approval.

---

## 6. Residual Risk Acceptance

Describe any risk that remains after controls are applied.

| Residual Risk | Accepted By | Reason for Acceptance | Review Date |
|---|---|---|---|
|  |  |  |  |

### Residual risk statement

Example:

> The remaining risk is accepted because the system is limited to internal use, does not make autonomous decisions, requires human review before external communication, and does not retain customer data outside approved systems.

---

## 7. Approval Conditions

Use this section when the decision is Approved with Conditions.

| Condition | Owner | Due Date | Approval Impact |
|---|---|---|---|
|  |  |  |  |

Approval is not valid until required pre-deployment conditions are met.

---

## 8. Deferral or Rejection Rationale

Complete this section if the decision is Deferred or Rejected.

### Reason for deferral or rejection

Explain the decision.

### Required changes before reconsideration

List what must change before the use case can be reviewed again.

---

## 9. Monitoring Requirements

Define what must be monitored after approval.

| Monitoring Area | Requirement | Owner | Review Frequency |
|---|---|---|---|
| Output quality |  |  |  |
| User feedback |  |  |  |
| Security events |  |  |  |
| Data handling |  |  |  |
| Vendor or model changes |  |  |  |
| Control effectiveness |  |  |  |

---

## 10. Re-Review Triggers

This approval must be revisited if any of the following occur.

- New model or model version
- New vendor or hosting environment
- New data source
- New sensitive or regulated data type
- New user group
- Expanded permissions or tool access
- External-facing use
- Material change in output use
- Security incident
- Privacy incident
- Legal, regulatory, or contractual change
- Significant failure in evaluation or monitoring
- Change in business owner, risk owner, or technical owner

Additional triggers:

- 

---

## 11. Decision Log

| Date | Decision | Decision Owner | Notes |
|---|---|---|---|
|  |  |  |  |

---

## 12. Sign-Off

| Role | Name | Decision / Acknowledgment | Date |
|---|---|---|---|
| Business owner |  |  |  |
| Technical owner |  |  |  |
| Security reviewer |  |  |  |
| Privacy / legal reviewer |  |  |  |
| Risk owner |  |  |  |
| Decision owner |  |  |  |

---

## Final Governance Decision

Select one:

- [ ] Approved
- [ ] Approved with Conditions
- [ ] Deferred
- [ ] Rejected

Decision summary:

> 

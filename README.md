# Secure AI Governance Toolkit

AI governance should produce evidence, not just intent.

The Secure AI Governance Toolkit is a practical collection of templates, workflows, and review artifacts for evaluating AI systems, AI-enabled business processes, and AI vendors before and after deployment.

It is designed to help teams turn AI policy into reviewable evidence, repeatable controls, and operational decision records.

---

## What this toolkit helps you do

- Review internal AI tools before deployment
- Evaluate AI vendors before procurement
- Document model purpose, risks, limitations, and controls
- Map AI risks to security, compliance, and governance frameworks
- Build repeatable approval workflows for AI use cases
- Create evidence for audits, security reviews, and executive oversight
- Record AI governance decisions with owners, controls, residual risks, and re-review triggers

---

## Who this is for

- Security teams reviewing AI systems
- GRC and compliance teams building AI governance programs
- Product and engineering teams shipping AI-enabled features
- Procurement teams evaluating AI vendors
- Executives who need evidence-based AI risk visibility
- Smaller organizations that need practical governance without buying a full platform

---

## Why this exists

AI governance often fails when it stays at the policy level. Organizations may have principles, acceptable-use rules, or risk statements, but still lack a practical way to answer basic operational questions:

- Who owns this AI system?
- What data does it process?
- What risks were reviewed?
- What controls are required?
- What evidence supports the approval decision?
- Who accepted the residual risk?
- What happens if the model, vendor, data, or use case changes?
- How do we respond if the system causes harm or exposes sensitive information?

This toolkit answers those questions with artifacts a team can fill out, attach to a decision, and hand to an auditor, reviewer, risk committee, or executive sponsor.

---

## Recommended workflow

A repeatable review process for AI systems, vendors, models, and use cases.

Links point to shipped artifacts. Planned items are on the roadmap.

### 1. Intake

Capture the basic facts: business purpose, ownership, users, data types, model/vendor, deployment environment, expected outputs, and known regulatory concerns.

Artifact: [AI use case intake](templates/ai-use-case-intake.md)

---

### 2. Classify risk

Identify higher-risk characteristics such as sensitive or regulated data, external-facing output, decisions affecting people, autonomous actions, third-party models, lack of human review, or unclear ownership.

Artifact: [AI risk register](templates/ai-risk-register.md)

Planned: AI risk classification guide

---

### 3. Review controls

Evaluate safeguards such as data protection, access control, output validation, human oversight, logging, security testing, vendor dependencies, misuse scenarios, and prompt injection risk.

Artifacts:

- [Model evaluation rubric](templates/model-evaluation-rubric.md)
- [AI security review checklist](templates/ai-security-review-checklist.md)

Planned:

- AI threat model template
- Prompt and configuration review
- Vendor AI review questionnaire

---

### 4. Create evidence

Produce documentation supporting the decision: model purpose, intended use, limitations, evaluation results, controls, known risks, and framework mappings.

Artifact: [Model card](templates/model-card.md)

Planned: Framework crosswalks

---

### 5. Decide

Record the outcome: Approved, Approved with Conditions, Deferred, or Rejected.

The decision record should name the decision owner, risk owner, required controls, residual risks, approval conditions, review date, and change triggers.

Artifact: [AI governance decision record](templates/ai-governance-decision-record.md)

---

### 6. Monitor and revisit

Governance is not a one-time approval. Reassess when there is material change, including:

- New model or model version
- New vendor or hosting environment
- New data source
- New user group
- Expanded permissions or tool access
- External-facing use
- Material change in output use
- Security incident
- Privacy incident
- Legal, regulatory, or contractual change
- Significant failure in evaluation or monitoring

Planned:

- AI incident response playbook
- Evidence guide
- Governance workflow guide

---

## Core toolkit

Status: `Shipped` = usable now · `Planned` = on the roadmap, not yet in the repo

| Phase | Artifact | Status |
|---|---|---|
| Intake | [AI use case intake](templates/ai-use-case-intake.md) | Shipped |
| Risk | [AI risk register](templates/ai-risk-register.md) | Shipped |
| Risk | AI risk classification guide | Planned |
| Model governance | [Model card](templates/model-card.md) | Shipped |
| Evaluation | [Model evaluation rubric](templates/model-evaluation-rubric.md) | Shipped |
| Security review | [AI security review checklist](templates/ai-security-review-checklist.md) | Shipped |
| Security review | AI threat model template | Planned |
| Vendor governance | Vendor AI review questionnaire | Planned |
| Prompt governance | Prompt and configuration review | Planned |
| Supply chain | Model supply chain and provenance review | Planned |
| Decision | [AI governance decision record](templates/ai-governance-decision-record.md) | Shipped |
| Incident response | AI incident response playbook | Planned |
| Control mapping | Framework crosswalks: NIST AI RMF, OWASP LLM Top 10, ISO 42001, SOC 2 | Planned |
| Examples | Completed internal copilot review | Planned |
| Examples | Completed vendor SaaS review | Planned |

---

## Repository structure

```text
secure-ai-governance-toolkit/
├── templates/
│   ├── ai-use-case-intake.md
│   ├── ai-risk-register.md
│   ├── ai-security-review-checklist.md
│   ├── ai-governance-decision-record.md
│   ├── model-card.md
│   └── model-evaluation-rubric.md
├── docs/
│   └── planned: getting-started, governance-workflow, risk-classification, evidence-guide, glossary
├── mappings/
│   └── planned: NIST AI RMF, OWASP LLM Top 10, ISO 42001, SOC 2 crosswalks
├── examples/
│   └── planned: completed internal-copilot and vendor-SaaS reviews
├── assets/
├── README.md
└── LICENSE

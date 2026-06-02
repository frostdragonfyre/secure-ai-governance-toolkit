# Secure AI Governance Toolkit

A practical toolkit for turning AI policy into reviewable evidence, repeatable controls, and operational workflows.

Most AI governance material explains what organizations should care about. This project focuses on what teams can actually use: templates, review rubrics, security checklists, control mappings, incident workflows, and examples that help teams govern AI systems in the real world.

## What this toolkit helps you do

The Secure AI Governance Toolkit helps teams:

- Review internal AI tools before deployment
- Evaluate AI vendors before procurement
- Document model purpose, risks, limitations, and controls
- Map AI risks to security, compliance, and governance frameworks
- Build repeatable approval workflows for AI use cases
- Create evidence for audits, security reviews, and executive oversight
- Respond to AI incidents involving data leakage, unsafe outputs, misuse, or system compromise

## Who this is for

This toolkit is designed for:

- Security teams reviewing AI systems
- GRC and compliance teams building AI governance programs
- Product and engineering teams shipping AI-enabled features
- Procurement teams evaluating AI vendors
- Executives who need evidence-based AI risk visibility
- Smaller organizations that need practical governance without buying a full platform

## Why this exists

AI governance often fails when it stays at the policy level.

Organizations may have principles, acceptable use rules, or risk statements, but still lack a practical way to answer basic operational questions:

- Who owns this AI system?
- What data does it process?
- What risks were reviewed?
- What controls are required?
- What evidence supports the approval decision?
- What happens if the model, vendor, data, or use case changes?
- How do we respond if the AI system causes harm or exposes sensitive information?

This toolkit is built around a simple idea:

**AI governance should produce evidence, not just intent.**

## Recommended workflow

Use the toolkit as a repeatable review process for AI systems, vendors, models, and use cases.

### 1. Intake

Capture the basic facts about the AI use case.

Document:

- Business purpose
- System owner
- Users
- Data types
- Model or vendor
- Deployment environment
- Expected outputs
- Relevant business process
- Known regulatory or contractual concerns

Primary artifact:

- `templates/ai-use-case-intake.md`

### 2. Classify risk

Identify whether the system involves higher-risk characteristics.

Examples include:

- Sensitive or regulated data
- Customer-facing output
- Employee-impacting decisions
- Security, legal, finance, or HR workflows
- Autonomous or semi-autonomous actions
- External vendors or third-party models
- Use in production business processes
- Lack of human review
- Material reliance on generated output

Primary artifact:

- `docs/risk-classification.md`

### 3. Review controls

Evaluate whether the system has appropriate safeguards.

Review areas may include:

- Data protection
- Access control
- Prompt and configuration management
- Output validation
- Human oversight
- Logging and monitoring
- Vendor claims
- Model limitations
- Security testing
- Abuse and misuse scenarios
- Incident response readiness

Primary artifacts:

- `templates/ai-threat-model.md`
- `templates/model-evaluation-rubric.md`
- `templates/prompt-and-configuration-review.md`
- `templates/vendor-ai-review-questionnaire.md`

### 4. Create evidence

Produce documentation that supports the governance decision.

Evidence may include:

- Model card
- Threat model
- Vendor review
- Evaluation rubric
- Control mapping
- Security review notes
- Known limitations
- Required mitigations
- Decision record

Primary artifacts:

- `templates/model-card.md`
- `templates/ai-governance-decision-record.md`
- `mappings/`

### 5. Decide

Record the governance outcome.

Common decision options:

- Approved
- Approved with conditions
- Deferred
- Rejected

The decision should identify:

- Decision owner
- Risk owner
- Required controls
- Open issues
- Review date
- Change triggers
- Conditions for continued use

Primary artifact:

- `templates/ai-governance-decision-record.md`

### 6. Monitor and revisit

AI governance is not a one-time approval.

Reassess when there are material changes, such as:

- New model version
- New vendor terms
- New data source
- New user group
- New integration
- Expanded permissions
- Production rollout
- Security incident
- Failed evaluation
- Regulatory or policy change

Primary artifacts:

- `templates/ai-incident-response-playbook.md`
- `docs/evidence-guide.md`

## Core toolkit

| Area | Artifact | Status |
|---|---|---|
| Intake | AI use case intake template | Planned |
| Risk classification | AI risk classification guide | Planned |
| Model governance | Model card template | Planned |
| Vendor governance | Vendor AI review questionnaire | Planned |
| Security review | AI threat model template | Planned |
| Evaluation | Model evaluation rubric | Planned |
| Prompt governance | Prompt and configuration review | Planned |
| Incident response | AI incident response playbook | Planned |
| Supply chain | Model supply chain and provenance review | Planned |
| Control mapping | Framework crosswalks | Planned |
| Examples | Completed internal copilot review | Planned |

## Repository structure

```text
secure-ai-governance-toolkit/
├── docs/
│   ├── getting-started.md
│   ├── governance-workflow.md
│   ├── risk-classification.md
│   ├── evidence-guide.md
│   └── glossary.md
├── templates/
│   ├── ai-use-case-intake.md
│   ├── model-card.md
│   ├── vendor-ai-review-questionnaire.md
│   ├── ai-threat-model.md
│   ├── model-evaluation-rubric.md
│   ├── prompt-and-configuration-review.md
│   ├── ai-incident-response-playbook.md
│   ├── model-supply-chain-provenance-review.md
│   └── ai-governance-decision-record.md
├── mappings/
│   ├── nist-ai-rmf-crosswalk.md
│   ├── owasp-llm-top-10-crosswalk.md
│   ├── iso-42001-crosswalk.md
│   └── soc2-ai-control-crosswalk.md
├── examples/
│   ├── internal-copilot-review/
│   └── vendor-ai-saas-review/
├── assets/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
└── ROADMAP.md

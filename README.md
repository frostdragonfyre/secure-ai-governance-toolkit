# Secure AI Governance Toolkit

A practical toolkit for turning AI policy into reviewable evidence, repeatable controls, and operational workflows.

Most AI governance material explains what organizations *should* care about. This project focuses on what teams can actually use: templates, review rubrics, and security checklists that help teams govern AI systems in the real world.

> **Project status:** Early but real. Five templates are shipped and usable today; control mappings, additional templates, and worked examples are on the roadmap below. This is built in the open — what's marked **Shipped** works now.

**AI governance should produce evidence, not just intent.**

## What this toolkit helps you do

- Review internal AI tools before deployment
- Evaluate AI vendors before procurement
- Document model purpose, risks, limitations, and controls
- Map AI risks to security, compliance, and governance frameworks
- Build repeatable approval workflows for AI use cases
- Create evidence for audits, security reviews, and executive oversight

## Who this is for

- Security teams reviewing AI systems
- GRC and compliance teams building AI governance programs
- Product and engineering teams shipping AI-enabled features
- Procurement teams evaluating AI vendors
- Executives who need evidence-based AI risk visibility
- Smaller organizations that need practical governance without buying a full platform

## Why this exists

AI governance often fails when it stays at the policy level. Organizations may have principles, acceptable-use rules, or risk statements, but still lack a practical way to answer basic operational questions:

- Who owns this AI system?
- What data does it process?
- What risks were reviewed?
- What controls are required?
- What evidence supports the approval decision?
- What happens if the model, vendor, data, or use case changes?
- How do we respond if the system causes harm or exposes sensitive information?

This toolkit answers those questions with artifacts a team can fill out, attach to a decision, and hand to an auditor.

## Recommended workflow

A repeatable review process for AI systems, vendors, models, and use cases. Links point to shipped artifacts; *(planned)* items are on the roadmap.

### 1. Intake
Capture the basic facts: business purpose, ownership, users, data types, model/vendor, deployment environment, expected outputs, and known regulatory concerns.
→ [`templates/ai-use-case-intake.md`](templates/ai-use-case-intake.md)

### 2. Classify risk
Identify higher-risk characteristics: sensitive or regulated data, external-facing output, decisions affecting people, autonomous actions, third-party models, lack of human review.
→ [`templates/ai-risk-register.md`](templates/ai-risk-register.md) · risk-classification guide *(planned)*

### 3. Review controls
Evaluate safeguards: data protection, access control, output validation, human oversight, logging, security testing, and misuse scenarios.
→ [`templates/model-evaluation-rubric.md`](templates/model-evaluation-rubric.md) · [`templates/ai-security-review-checklist.md`](templates/ai-security-review-checklist.md) · threat model, prompt/config review, vendor questionnaire *(planned)*

### 4. Create evidence
Produce documentation supporting the decision: model purpose, limitations, controls, and framework mappings.
→ [`templates/model-card.md`](templates/model-card.md) · decision record, framework crosswalks *(planned)*

### 5. Decide
Record the outcome (Approved / Approved with conditions / Deferred / Rejected), naming the decision owner, risk owner, required controls, review date, and change triggers.
→ AI governance decision record *(planned)*

### 6. Monitor and revisit
Governance is not a one-time approval. Reassess on material change — new model version, new data source, new user group, expanded permissions, production rollout, security incident, or regulatory change. Change triggers are captured in the intake template so there's something to monitor against.
→ AI incident response playbook, evidence guide *(planned)*

## Core toolkit

**Status:** `Shipped` = usable now · `Planned` = on the roadmap, not yet in the repo

| Phase | Artifact | Status |
|---|---|---|
| Intake | [AI use case intake](templates/ai-use-case-intake.md) | ✅ Shipped |
| Risk | [AI risk register](templates/ai-risk-register.md) | ✅ Shipped |
| Risk | AI risk classification guide | ⏳ Planned |
| Model governance | [Model card](templates/model-card.md) | ✅ Shipped |
| Evaluation | [Model evaluation rubric](templates/model-evaluation-rubric.md) | ✅ Shipped |
| Security review | [AI security review checklist](templates/ai-security-review-checklist.md) | ✅ Shipped |
| Security review | AI threat model template | ⏳ Planned |
| Vendor governance | Vendor AI review questionnaire | ⏳ Planned |
| Prompt governance | Prompt and configuration review | ⏳ Planned |
| Supply chain | Model supply chain & provenance review | ⏳ Planned |
| Decision | AI governance decision record | ⏳ Planned |
| Incident response | AI incident response playbook | ⏳ Planned |
| Control mapping | Framework crosswalks (NIST AI RMF, OWASP LLM Top 10, ISO 42001, SOC 2) | ⏳ Planned |
| Examples | Completed internal copilot review | ⏳ Planned |
| Examples | Completed vendor SaaS review | ⏳ Planned |

## Repository structure

```text
secure-ai-governance-toolkit/
├── templates/
│   ├── ai-use-case-intake.md            # shipped
│   ├── ai-risk-register.md              # shipped
│   ├── ai-security-review-checklist.md  # shipped
│   ├── model-card.md                    # shipped
│   └── model-evaluation-rubric.md       # shipped
├── docs/        # planned: getting-started, governance-workflow, risk-classification, evidence-guide, glossary
├── mappings/    # planned: NIST AI RMF, OWASP LLM Top 10, ISO 42001, SOC 2 crosswalks
├── examples/    # planned: completed internal-copilot and vendor-SaaS reviews
├── assets/
├── README.md
└── LICENSE
```

## Roadmap

Near-term priorities, in order:

1. One complete **worked example** in `examples/` — a fully filled review of a realistic system, including the judgment behind the decision. (Highest priority: it's what makes the toolkit demonstrate governance rather than just describe it.)
2. **Framework crosswalks** in `mappings/`, starting with one done precisely rather than four done broadly.
3. Remaining workflow templates: decision record, threat model, vendor questionnaire.
4. `docs/` guides tying the workflow together.

## Contributing

Issues and suggestions are welcome via the issue tracker.

## License

See [LICENSE](LICENSE).

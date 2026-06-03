# AI Use Case Intake

## 1. Identification

| Field | Value |
|---|---|
| **Use case name** | _e.g. Support ticket auto-summarizer_ |
| **Intake ID** | _Tracking ID_ |
| **Intake date** | _YYYY-MM-DD_ |
| **Requesting business unit** | |
| **Submitted by** | _Name / role_ |
| **Business owner** _(accountable for the outcome)_ | |
| **Technical owner** _(builds/operates it)_ | |
| **Risk owner** _(accepts residual risk)_ | |
| **Status** | `Draft` · `Submitted` · `In review` · `Routed` · `Decided` |

_If the business, technical, and risk owners are the same person, say so — concentrated ownership is a finding, not a shortcut._

## 2. Business purpose

| Question | Response |
|---|---|
| What problem or operational need does this solve? _(Avoid "leverage AI to…" — describe the actual job.)_ | |
| What process, workflow, or decision does it support? | |
| What does success look like? _(Concrete, measurable if possible.)_ | |
| What alternatives were considered? _(Including non-AI options.)_ | |
| What is the consequence of not implementing it? | |

## 3. System description

| Field | Value |
|---|---|
| What the system does, in one or two sentences | |
| Development or sourcing model | _Built in-house / Fine-tune of base model / Vendor product / Open weights_ |
| Output type | _Text / classification / recommendation / decision / action / code / other_ |
| Production use? | _Prototype / pilot / production_ |
| Human review before output is used? | _Always / sometimes / never_ |

## 4. AI capability type

_Check all that apply — this shapes which risks and reviews are relevant._

- [ ] Generative (LLM / text, image, code)
- [ ] Classification / detection
- [ ] Recommendation / ranking
- [ ] Forecasting / prediction
- [ ] Computer vision
- [ ] Agentic / tool-using / multi-step autonomous workflow
- [ ] Retrieval-augmented (RAG)
- [ ] Other: ___

## 5. Users and reach

| Question | Answer |
|---|---|
| Who uses it? | _Internal team / all employees / contractors / customers / public_ |
| Approximate number of users | |
| Individuals or groups *affected by* the outputs | _May differ from the users_ |
| Are users aware they're interacting with AI? | _Yes / No / Partial_ |
| Can the output reach someone outside the org? | _Yes / No_ |

## 6. Data involved

_Describe each data flow. "It's just prompts" is not an answer — prompts often carry the sensitive data._

| Data flow | What data, and from where |
|---|---|
| **Submitted** to the system (inputs/prompts) | |
| **Retrieved or accessed** by the system | |
| **Generated** by the system | |
| **Stored or logged** | |

| Data type touched | Present? | Notes (source, volume, retention) |
|---|---|---|
| Public / non-sensitive | ☐ | |
| Internal business data | ☐ | |
| Personal data (PII) | ☐ | |
| Sensitive personal data (health, biometric, financial) | ☐ | |
| Regulated data (PCI, PHI, export-controlled, CUI) | ☐ | |
| Secrets / credentials | ☐ | |
| Third-party / licensed data | ☐ | |

| Field | Response |
|---|---|
| **Prohibited data types** _(what must never be entered)_ | |
| **Data sensitivity tag** _(highest applicable — feeds the risk tier in §9)_ | `none` · `internal` · `confidential` · `regulated` |
| Selected tag | |
| Is data sent outside our boundary (e.g. to a vendor API)? | _Yes / No / Unsure_ |
| Retention period, and is data used for model training/improvement? | |

## 7. Vendor and model

| Field | Value |
|---|---|
| Model or product name | _e.g. Claude, GPT-4o, in-house fine-tune_ |
| Provider | _Vendor / open weights / built in-house_ |
| Hosting | _Vendor API / self-hosted / on-prem_ |
| Is the model snapshot pinned, or can the vendor change it under us? | |
| Vendor reviewed already? | _Link to vendor review if one exists_ |

## 8. Operational use and dependency

| Question | Answer |
|---|---|
| Deployment environment | _Prototype / internal tool / staging / production_ |
| Expected frequency of use | _One-off / periodic / continuous_ |
| Dependent business process | _What process relies on this once live?_ |
| **Manual fallback** if the system is unavailable or wrong | _Describe, or state "none" — "none" is a risk_ |
| System integrations | _What it reads from or writes to_ |
| **Action authority** | _Suggests only / acts with human approval / acts autonomously_ |
| Worst plausible bad output | _Be concrete: wrong refund issued, PII leaked, defamatory text_ |

## 9. Risk screening and initial tier

_Check every higher-risk characteristic that applies._

- [ ] Sensitive or regulated data involved
- [ ] Customer- or public-facing output
- [ ] Output affects a person's rights, benefits, employment, or legal standing
- [ ] Used in security, legal, finance, or HR workflows
- [ ] Autonomous or semi-autonomous actions (acts without human approval)
- [ ] External vendor or third-party model
- [ ] Runs in a production business process
- [ ] No reliable human review of output
- [ ] Material reliance on generated output (hard to catch errors)

**Initial risk tier** _(aligns with the evaluation rubric's tier gate):_

| Tier | Applies when | Selected? |
|---|---|---|
| **Tier 3 — High** | Acts autonomously, OR regulated data, OR rights-affecting output | |
| **Tier 2 — Moderate** | Informs decisions, OR reaches external users | |
| **Tier 1 — Low** | Internal, advisory, human always interprets, no sensitive data | |

> **Selected tier:** ______  ·  **What set it:** ______

## 10. Human oversight

| Question | Response |
|---|---|
| What is the human's role in reviewing or approving outputs? | |
| Are users trained on the system's limitations? | |
| Are users instructed not to treat outputs as authoritative? | |
| Is extra approval required for high-impact outputs? | |
| Escalation path for questionable or harmful outputs | |

## 11. Known regulatory or contractual concerns

_GDPR/CCPA, sector rules (HIPAA, GLBA), EU AI Act, customer contract or DPA clauses, data residency, federal authorization requirements, etc. "None known" is acceptable if true — but say it explicitly._

> 

## 12. Required reviews and routing

_Based on the tier and screening above, mark which reviews this use case must clear before a decision. This routes the intake to the rest of the workflow; it is not the approval itself._

| Review | Required? | Owner | Status |
|---|---|---|---|
| Risk register entry | ☐ | | |
| Model evaluation / rubric | ☐ | | |
| Security review | ☐ | | |
| Privacy review | ☐ | | |
| Legal / compliance review | ☐ | | |
| Vendor review | ☐ | | |

> **Recommended path:** _Approve at intake (Tier 1, low concern) / Route for full review / Reject at intake._ The final decision is recorded in the governance decision record, not here.

## 13. Change triggers

_Pre-commit what future changes force a re-review, so monitoring has something to check against. Defaults below — edit for this system._

- [ ] New model or model version
- [ ] New vendor or changed vendor terms / model snapshot
- [ ] New data source or new data type introduced
- [ ] New user group or move from internal → external
- [ ] New integration or expanded permissions
- [ ] Move from prototype/staging → production
- [ ] Security incident involving this system
- [ ] Failed evaluation or quality regression
- [ ] Relevant regulatory or policy change

## 14. Submitter sign-off

| | |
|---|---|
| I confirm the above is accurate to the best of my knowledge | _Name / date_ |
| Open questions or known unknowns | _List anything you couldn't answer_ |

## 15. Intake history

| Version | Date | Author | Change summary |
|---|---|---|---|
| 0.1 | | | Initial intake |

---

<details>
<summary><strong>Filled example</strong> — internal support-ticket summarizer (click to expand)</summary>

**1. Identification** — Support ticket auto-summarizer · Intake ID SAI-2026-014 · 2026-06-02 · Requesting unit: Customer Support · Submitted by J. Rivera (Support Ops Lead) · Business owner: VP Customer Success · Technical owner: Support Ops Lead · Risk owner: VP Customer Success · Status: Submitted. (Technical owner and submitter are the same — noted.)

**2. Business purpose** — Agents spend ~3 min/ticket reading history before responding. The tool generates a 3-sentence thread summary so agents triage faster. Success = lower handle time with no rise in misrouted tickets. Alternatives considered: canned macros (too rigid), hiring (too costly). Consequence of not doing it: status quo, no new risk.

**3. System description** — Summarizes a ticket thread into 3 sentences. Vendor LLM via API. Output: text. Pilot. Human review: always (agent reads the summary, then the ticket).

**4. Capability type** — Generative (LLM); retrieval from ticket system.

**5. Users and reach** — ~40 internal agents. Affected parties: customers (indirectly). Users know it's AI. Output stays internal.

**6. Data** — Submitted: ticket text (incl. customer names/emails). Retrieved: prior thread. Generated: summary. Stored: summaries logged 30 days. Internal business data ✅, PII ✅. No regulated data. Prohibited: payment card numbers. **Sensitivity tag: `confidential`.** Data leaves boundary: yes (vendor API). Not used for vendor training (per DPA).

**7. Vendor/model** — Vendor LLM, vendor-hosted, snapshot not pinned (flag). Vendor review: not yet done (flag).

**8. Operational** — Pilot, continuous use, sits at start of ticket handling. Manual fallback: agent reads the thread (fully available). Reads from Zendesk, no write-back. Action authority: suggests only. Worst output: fabricates a detail (e.g. invents a refund promise) and agent acts on it.

**9. Risk screening** — Flags: sensitive (PII) data; external vendor; production-bound. Not autonomous, not rights-affecting. **Initial tier: Tier 2 — Moderate** (informs a human; PII via vendor).

**10. Oversight** — Agent reviews every summary; trained that summaries are not authoritative; escalate odd outputs to Ops Lead.

**11. Regulatory** — Must stay within existing DPA; confirm vendor is a listed sub-processor.

**12. Routing** — Required: risk register entry, evaluation rubric, security review, privacy review, vendor review. Recommended path: route for full review.

**13. Change triggers** — All defaults; especially "move to customer-facing" and "vendor snapshot/terms change."

**14. Sign-off** — M. Brown, 2026-06-02. Open question: is the vendor already an approved sub-processor under our DPA?

</details>

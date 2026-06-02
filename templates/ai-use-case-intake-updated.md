# AI Use Case Intake

## 1. Identification

| Field | Value |
|---|---|
| **Use case name** | _e.g. Support ticket auto-summarizer_ |
| **Intake date** | _YYYY-MM-DD_ |
| **Submitted by** | _Name / role_ |
| **Status** | `Draft` · `Submitted` · `In review` · `Decided` |
| **Intake ID** | _Optional tracking ID_ |

## 2. Business purpose

_What problem does this solve, and what does success look like? One paragraph. Avoid "leverage AI to..." and describe the actual job._

> 

## 3. Ownership

| Role | Person | Notes |
|---|---|---|
| **System owner** _(accountable for the system)_ | | |
| **Risk owner** _(accountable for accepting residual risk)_ | | |
| **Day-to-day operator** | | |

_If the system owner and risk owner are the same person, say so explicitly - that's a finding, not a shortcut._

## 4. Users and reach

| Question | Answer |
|---|---|
| Who uses it? | _Internal team / all employees / customers / public_ |
| Approximate number of users | |
| Are users aware they're interacting with AI? | _Yes / No / Partial_ |
| Can the output reach someone outside the org? | _Yes / No_ |

## 5. Data

| Data type touched | Present? | Notes (source, volume, retention) |
|---|---|---|
| Public / non-sensitive | ☐ | |
| Internal business data | ☐ | |
| Personal data (PII) | ☐ | |
| Sensitive personal data (health, biometric, financial, etc.) | ☐ | |
| Regulated data (PCI, PHI, export-controlled, etc.) | ☐ | |
| Secrets / credentials | ☐ | |
| Third-party / licensed data | ☐ | |

**Data sensitivity tag** _(highest applicable - feeds [risk classification](../docs/risk-classification.md)):_
`none` · `internal` · `confidential` · `regulated`

> **Selected tag:** 

_Note where inputs come from and whether anything is sent to an external model/vendor. "It's just prompts" is not an answer - prompts often contain the sensitive data._

## 6. Model / vendor

| Field | Value |
|---|---|
| Model or product name | _e.g. GPT-4o, Claude, in-house fine-tune_ |
| Provider | _Vendor / open weights / built in-house_ |
| Hosting | _Vendor API / self-hosted / on-prem_ |
| Does data leave our boundary? | _Yes / No / Unsure_ |
| Vendor reviewed already? | _Link to vendor review if exists_ |

## 7. Deployment environment

| Field | Value |
|---|---|
| Environment | _Prototype / internal tool / staging / production_ |
| Integrations | _What systems does it read from or write to?_ |
| Permissions / access scope | _What can it touch on a user's behalf?_ |
| Autonomy level | _Suggests only / acts with approval / acts autonomously_ |

## 8. Expected outputs and use

| Question | Answer |
|---|---|
| What does it produce? | _Text / decisions / code / actions / classifications_ |
| How is the output used? | _Reference only / informs a human decision / drives an automated action_ |
| Is there human review before output is acted on? | _Always / sometimes / never_ |
| What's the worst plausible bad output? | _Be concrete: wrong refund issued, PII leaked, defamatory text, etc._ |

## 9. Business process context

_Which real business process does this sit inside, and what currently happens without it? Helps reviewers judge blast radius and whether there's a manual fallback._

> 

## 10. Known regulatory or contractual concerns

_List anything already known: GDPR/CCPA, sector rules (HIPAA, GLBA), the EU AI Act, customer contract clauses, data residency, etc. "None known" is acceptable if true - but say it explicitly._

> 

## 11. Change triggers

_What future changes should force a re-review? Pre-committing these here means step 6 (monitor) has something to check against. Default set below - edit for this system._

- [ ] New model or model version
- [ ] New vendor or changed vendor terms
- [ ] New data source or new data type introduced
- [ ] New user group or move from internal → external
- [ ] New integration or expanded permissions
- [ ] Move from prototype/staging → production
- [ ] Security incident involving this system
- [ ] Failed evaluation or quality regression
- [ ] Relevant regulatory or policy change

## 12. Submitter sign-off

| | |
|---|---|
| I confirm the above is accurate to the best of my knowledge | _Name / date_ |
| Open questions or known unknowns | _List anything you couldn't answer_ |

---

<details>
<summary><strong>Filled example</strong> - internal support-ticket summarizer (click to expand)</summary>

**1. Identification** - Name: Support ticket auto-summarizer · Date: 2026-06-02 · Submitted by: J. Rivera, Support Ops Lead · Status: Submitted

**2. Business purpose** - Support agents spend ~3 min per ticket reading history before responding. This tool generates a 3-sentence summary of each ticket thread so agents can triage faster. Success = lower handle time with no rise in misrouted tickets.

**3. Ownership** - System owner: Support Ops Lead · Risk owner: VP Customer Success · Operator: Support Ops Lead. (Owner and operator are the same person — noted.)

**4. Users and reach** - ~40 internal support agents. Users know it's AI. Summaries stay internal; they are not shown to customers.

**5. Data** - Internal business data ✅, Personal data (PII) ✅ (customer names, emails in ticket text). No regulated data. **Sensitivity tag: `confidential`.** Ticket text is sent to a vendor API.

**6. Model / vendor** - Vendor LLM via API · Hosting: vendor · Data leaves boundary: Yes · Vendor review: not yet done (flag).

**7. Deployment** - Internal tool, reads from Zendesk, no write-back. Read-only scope. Autonomy: suggests only.

**8. Outputs** - Produces a text summary, used as reference only, agent always reads the real ticket. Worst plausible bad output: summary omits or fabricates a key detail (e.g. invents a refund promise), agent acts on it without checking.

**9. Process context** - Sits at the start of the ticket-handling flow. Manual fallback (reading the thread) still fully available.

**10. Regulatory/contractual** - Customer data processing must stay within existing DPA terms; confirm vendor is a listed sub-processor. Otherwise none known.

**11. Change triggers** - All defaults apply; especially "move to customer-facing" and "vendor terms change."

**12. Sign-off** - M. Brown, 2026-06-02. Open question: is this vendor already an approved sub-processor under our DPA?

</details>

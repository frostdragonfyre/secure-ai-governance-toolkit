# AI Risk Register

This risk register is intended to document, assess, assign, and track risks associated with AI-enabled systems, tools, workflows, models, vendors, and operational use cases.

The register should be used after an AI use case has been identified through the intake process and before the system is approved for production use, expanded deployment, or material change. It may also be used during periodic review, vendor reassessment, incident response, or control testing.

## 1. Register Information

<table>
  <tr>
    <th width="35%">Field</th>
    <th width="65%">Response</th>
  </tr>
  <tr>
    <td>AI system or use case name</td>
    <td>Enter the name of the AI system, tool, workflow, model, vendor capability, or proposed use case.<br><br></td>
  </tr>
  <tr>
    <td>Business owner</td>
    <td>Enter the business owner accountable for the use case, process, mission need, or operational outcome.<br><br></td>
  </tr>
  <tr>
    <td>Technical owner</td>
    <td>Enter the technical owner responsible for implementation, configuration, integration, monitoring, or technical support.<br><br></td>
  </tr>
  <tr>
    <td>Risk owner</td>
    <td>Enter the person or role accountable for accepting, mitigating, transferring, or escalating the risks in this register.<br><br></td>
  </tr>
  <tr>
    <td>Date created</td>
    <td>Enter the date this risk register was created.<br><br></td>
  </tr>
  <tr>
    <td>Last reviewed</td>
    <td>Enter the most recent review date. If this is the initial version, enter “not yet reviewed.”<br><br></td>
  </tr>
  <tr>
    <td>Next review date</td>
    <td>Enter the next planned review date based on the use case risk tier, system change cycle, or governance review cadence.<br><br></td>
  </tr>
  <tr>
    <td>Current status</td>
    <td>Enter the current status, such as draft, in review, active, retired, or superseded.<br><br></td>
  </tr>
</table>

## 2. Risk Rating Method

Risks should be evaluated using likelihood, impact, and the effectiveness of existing controls. The inherent risk should reflect exposure before additional treatment. The residual risk should reflect remaining exposure after controls, mitigations, or acceptance decisions are considered.

<table>
  <tr>
    <th width="20%">Rating</th>
    <th width="80%">Description</th>
  </tr>
  <tr>
    <td>Low</td>
    <td>The risk is unlikely to occur or would have limited business, legal, security, privacy, operational, or reputational impact.</td>
  </tr>
  <tr>
    <td>Moderate</td>
    <td>The risk is plausible and could create meaningful operational, compliance, financial, security, privacy, or reputational impact if not managed.</td>
  </tr>
  <tr>
    <td>High</td>
    <td>The risk is likely, difficult to control, involves sensitive data or high-impact use, or could cause material harm to the organization, users, customers, or affected individuals.</td>
  </tr>
  <tr>
    <td>Critical</td>
    <td>The risk may be unacceptable without immediate treatment, executive approval, suspension of use, architectural redesign, or formal exception.</td>
  </tr>
</table>

## 3. Risk Register

The risk register should identify the primary risks associated with the AI system or use case. The example risks below may be retained, revised, removed, or expanded based on the specific system under review.

<table>
  <tr>
    <th width="8%">Risk ID</th>
    <th width="15%">Risk Area</th>
    <th width="32%">Risk Statement</th>
    <th width="13%">Likelihood</th>
    <th width="12%">Impact</th>
    <th width="10%">Inherent Risk</th>
    <th width="10%">Risk Owner</th>
  </tr>
  <tr>
    <td>AI-R-001</td>
    <td>Data protection</td>
    <td>Sensitive, confidential, regulated, customer, employee, or security-relevant information may be submitted to an AI system without approved handling terms, retention limits, or training restrictions.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-002</td>
    <td>Prompt injection</td>
    <td>Malicious or untrusted input may cause the system to ignore instructions, disclose restricted context, manipulate outputs, or invoke unauthorized actions.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-003</td>
    <td>Overreliance</td>
    <td>Users may treat AI-generated outputs as authoritative without sufficient review, verification, or professional judgment.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-004</td>
    <td>Model change</td>
    <td>Model behavior, performance, safety characteristics, or output quality may change without adequate notice, testing, approval, or communication to affected users.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-005</td>
    <td>Retrieval integrity</td>
    <td>Retrieved documents, embeddings, knowledge sources, or indexed content may be stale, unauthorized, incomplete, misleading, or intentionally poisoned.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-006</td>
    <td>Excessive agency</td>
    <td>An AI-enabled workflow may perform unintended actions because tool access, permissions, workflow authority, or human approval gates are insufficiently constrained.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-007</td>
    <td>Output harm</td>
    <td>AI-generated content may create legal, regulatory, financial, operational, safety, security, or reputational harm if it is inaccurate, misleading, biased, inappropriate, or unauthorized.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-008</td>
    <td>Logging and retention</td>
    <td>Prompts, outputs, retrieved content, user activity, or tool calls may be logged or retained in a manner inconsistent with privacy, security, legal, contractual, or records management requirements.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-009</td>
    <td>Vendor dependency</td>
    <td>The organization may become dependent on a vendor-controlled AI capability without sufficient transparency, auditability, continuity planning, contractual protection, or exit strategy.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-010</td>
    <td>Evaluation gap</td>
    <td>The system may be deployed without adequate evaluation for accuracy, robustness, misuse resistance, data leakage, fairness, reliability, or fitness for intended use.</td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter low, moderate, high, or critical.<br><br></td>
    <td>Enter owner.<br><br></td>
  </tr>
</table>

## 4. Detailed Risk Treatment

Each material risk should have a documented treatment plan. Treatment may include mitigation, transfer, avoidance, acceptance, additional review, compensating controls, or suspension of use.

<table>
  <tr>
    <th width="8%">Risk ID</th>
    <th width="23%">Existing Controls</th>
    <th width="25%">Additional Treatment</th>
    <th width="14%">Residual Risk</th>
    <th width="15%">Due Date</th>
    <th width="15%">Status</th>
  </tr>
  <tr>
    <td>AI-R-001</td>
    <td>Document current controls, such as approved vendor terms, data handling requirements, access limits, training restrictions, logging controls, or user guidance.<br><br></td>
    <td>Document additional actions, such as legal review, privacy review, vendor negotiation, technical controls, policy restrictions, or monitoring.<br><br></td>
    <td>Enter remaining risk level.<br><br></td>
    <td>Enter target date.<br><br></td>
    <td>Open, in progress, accepted, mitigated, transferred, avoided, or closed.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-002</td>
    <td>Document current controls, such as system prompt isolation, retrieval controls, tool restrictions, output validation, misuse testing, or security review.<br><br></td>
    <td>Document additional actions, such as prompt injection testing, tool permission review, red-team testing, allowlisting, approval gates, or regression testing.<br><br></td>
    <td>Enter remaining risk level.<br><br></td>
    <td>Enter target date.<br><br></td>
    <td>Open, in progress, accepted, mitigated, transferred, avoided, or closed.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-003</td>
    <td>Document current controls, such as user disclaimers, human review requirements, training, workflow approvals, or limitations on allowed use.<br><br></td>
    <td>Document additional actions, such as required reviewer signoff, user training, output verification steps, or escalation procedures.<br><br></td>
    <td>Enter remaining risk level.<br><br></td>
    <td>Enter target date.<br><br></td>
    <td>Open, in progress, accepted, mitigated, transferred, avoided, or closed.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-004</td>
    <td>Document current controls, such as model version tracking, vendor change notices, release review, evaluation records, or monitoring.<br><br></td>
    <td>Document additional actions, such as regression testing, reapproval after model changes, contractual notice requirements, or periodic model evaluation.<br><br></td>
    <td>Enter remaining risk level.<br><br></td>
    <td>Enter target date.<br><br></td>
    <td>Open, in progress, accepted, mitigated, transferred, avoided, or closed.<br><br></td>
  </tr>
  <tr>
    <td>AI-R-005</td>
    <td>Document current controls, such as document source approval, access control, content refresh cycles, retrieval testing, or knowledge base ownership.<br><br></td>
    <td>Document additional actions, such as source validation, permission review, content owner attestation, data quality review, or poisoned content testing.<br><br></td>
    <td>Enter remaining risk level.<br><br></td>
    <td>Enter target date.<br><br></td>
    <td>Open, in progress, accepted, mitigated, transferred, avoided, or closed.<br><br></td>
  </tr>
  <tr>
    <td>Enter risk ID</td>
    <td>Document current controls.<br><br></td>
    <td>Document additional treatment.<br><br></td>
    <td>Enter remaining risk level.<br><br></td>
    <td>Enter target date.<br><br></td>
    <td>Enter status.<br><br></td>
  </tr>
  <tr>
    <td>Enter risk ID</td>
    <td>Document current controls.<br><br></td>
    <td>Document additional treatment.<br><br></td>
    <td>Enter remaining risk level.<br><br></td>
    <td>Enter target date.<br><br></td>
    <td>Enter status.<br><br></td>
  </tr>
</table>

## 5. Control and Framework Mapping

This section should identify how the risks and treatments align to governance, security, privacy, compliance, or assurance expectations. The mapping does not need to be exhaustive, but it should provide a clear basis for review, evidence collection, and control ownership.

<table>
  <tr>
    <th width="8%">Risk ID</th>
    <th width="27%">Control Objective</th>
    <th width="20%">Framework or Standard</th>
    <th width="25%">Mapped Area</th>
    <th width="20%">Evidence</th>
  </tr>
  <tr>
    <td>AI-R-001</td>
    <td>Protect sensitive data submitted to or processed by AI systems.</td>
    <td>NIST AI RMF, NIST SP 800-53, FedRAMP-style controls</td>
    <td>Data governance, privacy, access control, vendor risk</td>
    <td>Approved intake, vendor terms, data handling review, retention decision</td>
  </tr>
  <tr>
    <td>AI-R-002</td>
    <td>Test and constrain LLM applications against direct and indirect prompt injection.</td>
    <td>OWASP LLM Top 10, NIST AI RMF, NIST SP 800-53</td>
    <td>Application security, misuse testing, system integrity</td>
    <td>Prompt injection test results, tool permission review, security signoff</td>
  </tr>
  <tr>
    <td>AI-R-003</td>
    <td>Ensure users understand system limits and retain appropriate human judgment.</td>
    <td>NIST AI RMF, internal governance policy</td>
    <td>Human oversight, user training, operational governance</td>
    <td>User guidance, training record, review workflow, approval conditions</td>
  </tr>
  <tr>
    <td>AI-R-004</td>
    <td>Review model or system changes before continued reliance or expanded use.</td>
    <td>NIST AI RMF, vendor risk management</td>
    <td>Change management, evaluation, monitoring</td>
    <td>Model version record, release notes, regression test results, review log</td>
  </tr>
  <tr>
    <td>AI-R-005</td>
    <td>Maintain the integrity, authorization, and currency of retrieved knowledge sources.</td>
    <td>NIST AI RMF, NIST SP 800-53, OWASP LLM Top 10</td>
    <td>Information integrity, access control, supply chain, retrieval governance</td>
    <td>Source inventory, access review, content refresh record, retrieval test results</td>
  </tr>
  <tr>
    <td>Enter risk ID</td>
    <td>Enter the control objective for the risk.</td>
    <td>Enter the relevant framework, standard, or internal policy.</td>
    <td>Enter the mapped control area.</td>
    <td>Enter the evidence expected for review or audit.</td>
  </tr>
  <tr>
    <td>Enter risk ID</td>
    <td>Enter the control objective for the risk.</td>
    <td>Enter the relevant framework, standard, or internal policy.</td>
    <td>Enter the mapped control area.</td>
    <td>Enter the evidence expected for review or audit.</td>
  </tr>
</table>

## 6. Risk Acceptance

Residual risks that remain after treatment should be formally accepted by the appropriate owner when they fall within organizational tolerance. High or critical residual risks should include a documented rationale, compensating controls, review frequency, and approval authority.

<table>
  <tr>
    <th width="10%">Risk ID</th>
    <th width="14%">Residual Risk</th>
    <th width="31%">Acceptance Rationale</th>
    <th width="18%">Accepted By</th>
    <th width="15%">Review Date</th>
    <th width="12%">Status</th>
  </tr>
  <tr>
    <td>AI-R-003</td>
    <td>Moderate</td>
    <td>Residual risk is accepted because the system is advisory only, users are required to review outputs before use, and high-impact decisions remain outside the approved scope.</td>
    <td>Business owner or designated risk owner</td>
    <td>Enter next review date</td>
    <td>Example</td>
  </tr>
  <tr>
    <td>AI-R-004</td>
    <td>Moderate</td>
    <td>Residual risk is accepted subject to periodic model review, vendor change monitoring, and re-evaluation after material model or system changes.</td>
    <td>Technical owner or governance lead</td>
    <td>Enter next review date</td>
    <td>Example</td>
  </tr>
  <tr>
    <td>Enter risk ID</td>
    <td>Enter low, moderate, high, or critical.</td>
    <td>Explain why the remaining risk is acceptable, what limits apply, and what compensating controls are in place.<br><br></td>
    <td>Enter approving owner, executive, or governance body.</td>
    <td>Enter review date.</td>
    <td>Open, accepted, expired, or superseded.</td>
  </tr>
  <tr>
    <td>Enter risk ID</td>
    <td>Enter low, moderate, high, or critical.</td>
    <td>Explain why the remaining risk is acceptable, what limits apply, and what compensating controls are in place.<br><br></td>
    <td>Enter approving owner, executive, or governance body.</td>
    <td>Enter review date.</td>
    <td>Open, accepted, expired, or superseded.</td>
  </tr>
</table>

## 7. Review History

The review history should show when the register was created, reviewed, revised, approved, or updated because of a material system, vendor, model, data, control, or risk change.

<table>
  <tr>
    <th width="13%">Date</th>
    <th width="17%">Reviewer</th>
    <th width="25%">Change or Decision</th>
    <th width="30%">Notes</th>
    <th width="15%">Evidence or Reference</th>
  </tr>
  <tr>
    <td>2026-05-29</td>
    <td>AI governance lead</td>
    <td>Initial register created</td>
    <td>Created during initial review of the proposed use case. Risks were identified from intake responses, vendor information, data handling assumptions, and expected operational use.</td>
    <td>AI use case intake</td>
  </tr>
  <tr>
    <td>2026-05-29</td>
    <td>Security reviewer</td>
    <td>Prompt injection risk added</td>
    <td>Risk added because the system may process user-controlled input, retrieved content, or other untrusted text that could affect model behavior.</td>
    <td>Security review notes</td>
  </tr>
  <tr>
    <td>2026-05-29</td>
    <td>Privacy or legal reviewer</td>
    <td>Data handling review required</td>
    <td>Review required before approval because prompts, outputs, logs, or retrieved records may contain sensitive business, personal, contractual, or regulated information.</td>
    <td>Vendor documentation</td>
  </tr>
  <tr>
    <td>Enter review date</td>
    <td>Enter reviewer name or role.</td>
    <td>Summarize the change, approval, rejection, escalation, or review decision.</td>
    <td>Document relevant assumptions, follow-up items, control changes, unresolved concerns, or approval conditions.<br><br></td>
    <td>Enter evidence, ticket, document, meeting note, or approval reference.</td>
  </tr>
  <tr>
    <td>Enter review date</td>
    <td>Enter reviewer name or role.</td>
    <td>Summarize the change, approval, rejection, escalation, or review decision.</td>
    <td>Document relevant assumptions, follow-up items, control changes, unresolved concerns, or approval conditions.<br><br></td>
    <td>Enter evidence, ticket, document, meeting note, or approval reference.</td>
  </tr>
</table>

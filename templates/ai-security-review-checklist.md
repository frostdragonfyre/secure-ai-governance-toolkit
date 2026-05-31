# AI Security Review Checklist

This checklist supports security review of AI-enabled systems, tools, workflows, models, vendor capabilities, and LLM applications before approval, production deployment, expanded use, or material change.

The purpose of this review is to identify security risks that may arise from model behavior, data exposure, prompt handling, retrieval sources, tool access, vendor dependencies, logging, output use, and operational monitoring. This checklist should be used alongside the AI use case intake, AI risk register, model card, vendor review, and model evaluation rubric.

## 1. Review Information

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
    <td>Enter the technical owner responsible for implementation, integration, configuration, monitoring, or technical support.<br><br></td>
  </tr>
  <tr>
    <td>Security reviewer</td>
    <td>Enter the person or team responsible for completing the security review.<br><br></td>
  </tr>
  <tr>
    <td>Review date</td>
    <td>Enter the date of this review.<br><br></td>
  </tr>
  <tr>
    <td>Review status</td>
    <td>Enter draft, in review, approved, approved with conditions, deferred, or rejected.<br><br></td>
  </tr>
</table>

## 2. System Scope

Security review begins with a defined system boundary, approved use case, user population, data flow, integration model, and operational dependency. Reviewers should be able to distinguish the authorized use of the system from excluded, prohibited, or higher-risk uses that require separate approval.

<table>
  <tr>
    <th width="35%">Question</th>
    <th width="65%">Response</th>
  </tr>
  <tr>
    <td>What is the approved purpose of the system?</td>
    <td>Describe the business purpose, intended users, and approved operational context.<br><br></td>
  </tr>
  <tr>
    <td>What is outside the approved scope?</td>
    <td>Document prohibited uses, excluded user groups, restricted data types, or workflows that are not approved.<br><br></td>
  </tr>
  <tr>
    <td>Is the system advisory, partially automated, or action-taking?</td>
    <td>Describe whether the system only provides information, recommends actions, or can initiate actions through tools, APIs, or workflows.<br><br></td>
  </tr>
  <tr>
    <td>What systems, applications, databases, APIs, or tools does the AI system connect to?</td>
    <td>List integrations, connected services, retrieval sources, tool permissions, and external dependencies.<br><br></td>
  </tr>
  <tr>
    <td>What would happen if the system produced an incorrect or unsafe output?</td>
    <td>Describe the potential business, legal, security, privacy, safety, operational, or reputational impact.<br><br></td>
  </tr>
</table>

## 3. Data Exposure Review

The review must establish whether sensitive, regulated, confidential, proprietary, credential-related, or security-relevant data may be submitted to, retrieved by, stored in, logged by, or exposed through the AI system. Data exposure should be evaluated across user inputs, retrieved context, model outputs, logs, embeddings, files, metadata, and vendor-controlled environments.

<table>
  <tr>
    <th width="35%">Review Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>Data submitted to the system has been identified and classified.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document the data types involved and the highest sensitivity level.<br><br></td>
  </tr>
  <tr>
    <td>Restricted data types are prohibited or controlled.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether users are prohibited from submitting personal data, credentials, secrets, regulated data, source code, customer data, or security-sensitive content.<br><br></td>
  </tr>
  <tr>
    <td>Vendor or model provider data retention has been reviewed.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether prompts, outputs, files, embeddings, logs, or metadata are retained, for how long, and under what terms.<br><br></td>
  </tr>
  <tr>
    <td>Use of submitted data for model training or service improvement has been reviewed.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether customer or organizational data may be used for training, tuning, analytics, abuse monitoring, or product improvement.<br><br></td>
  </tr>
  <tr>
    <td>Credential, secret, and token exposure controls are in place.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document controls such as secret scanning, data loss prevention, input restrictions, output monitoring, or user guidance.<br><br></td>
  </tr>
  <tr>
    <td>Outputs are reviewed for possible sensitive data leakage.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document testing for unintended disclosure of personal information, credentials, proprietary content, internal records, or restricted source material.<br><br></td>
  </tr>
</table>

## 4. Prompt and Instruction Security

Prompt and instruction security focuses on how trusted instructions, user-controlled input, retrieved content, and tool instructions are separated, protected, tested, and governed. System prompts, developer instructions, and prompt templates should be treated as governed configuration items when they materially affect system behavior, security posture, or user reliance.

<table>
  <tr>
    <th width="35%">Review Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>System prompts and developer instructions are separated from user-controlled input.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document how trusted instructions are separated from user prompts, uploaded files, retrieved content, or external text.<br><br></td>
  </tr>
  <tr>
    <td>System prompts are version controlled or otherwise change managed.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document who can change system prompts, how changes are approved, and whether prior versions are retained.<br><br></td>
  </tr>
  <tr>
    <td>Prompt templates are reviewed before production use.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document review of task scope, instruction clarity, output format, safety constraints, and escalation behavior.<br><br></td>
  </tr>
  <tr>
    <td>Direct prompt injection has been tested.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document tests where a user attempts to override instructions, reveal hidden prompts, bypass restrictions, or manipulate output behavior.<br><br></td>
  </tr>
  <tr>
    <td>Indirect prompt injection has been tested where retrieved or external content is used.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document tests involving untrusted documents, web pages, tickets, emails, files, logs, or knowledge base content.<br><br></td>
  </tr>
  <tr>
    <td>Prompt injection findings are tracked and remediated.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Reference tickets, test results, compensating controls, residual risks, or acceptance decisions.<br><br></td>
  </tr>
</table>

## 5. Retrieval and Knowledge Source Security

Retrieval-augmented systems require review of the sources, permissions, freshness, integrity, and trust boundaries associated with retrieved content. Knowledge sources should be inventoried, access-controlled, periodically reviewed, and treated as potentially untrusted input unless explicitly validated.

<table>
  <tr>
    <th width="35%">Review Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>Retrieval sources are inventoried and approved.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>List approved repositories, knowledge bases, document stores, databases, indexes, or external sources.<br><br></td>
  </tr>
  <tr>
    <td>Retrieved content is treated as untrusted input.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document safeguards against retrieved instructions overriding system instructions or causing unauthorized behavior.<br><br></td>
  </tr>
  <tr>
    <td>Access controls are enforced before retrieval.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether users can retrieve only the documents, records, or data they are authorized to access.<br><br></td>
  </tr>
  <tr>
    <td>Knowledge sources are reviewed for accuracy, currency, and authorization.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document content ownership, refresh cadence, stale content controls, and removal of unauthorized or deprecated records.<br><br></td>
  </tr>
  <tr>
    <td>Data poisoning or malicious content risks have been considered.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether attackers could influence retrieved content, embeddings, indexes, or source repositories.<br><br></td>
  </tr>
</table>

## 6. Tool, API, and Action Security

AI systems with access to tools, APIs, files, databases, workflows, or external systems require additional security review because model outputs may influence real-world actions. Tool access should be limited by least privilege, constrained by approved use, logged for review, and gated by human approval when actions may create material impact.

<table>
  <tr>
    <th width="35%">Review Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>All tools and actions available to the AI system are inventoried.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>List tools, APIs, plugins, functions, databases, applications, and workflow actions available to the system.<br><br></td>
  </tr>
  <tr>
    <td>Tool permissions follow least privilege.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether the system has only the permissions required for the approved use case.<br><br></td>
  </tr>
  <tr>
    <td>High-impact actions require human approval.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document approval gates for actions that affect access, money, legal status, customer records, security controls, production systems, or external communications.<br><br></td>
  </tr>
  <tr>
    <td>Tool inputs and outputs are validated.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document validation, allowlisting, schema restrictions, parameter constraints, or error handling.<br><br></td>
  </tr>
  <tr>
    <td>Tool calls are logged and reviewable.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document what is logged, who can access the logs, how long logs are retained, and how suspicious activity is reviewed.<br><br></td>
  </tr>
  <tr>
    <td>Misuse scenarios involving tools have been tested.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document testing for unauthorized actions, data exfiltration, privilege misuse, workflow abuse, or unsafe automation.<br><br></td>
  </tr>
</table>

## 7. Model Supply Chain and Provenance

Model supply chain review documents what is known, unknown, and unverifiable about the model’s origin, provider, base model, training data, fine-tuning history, optimization changes, inherited risks, and supporting documentation. Approval should not rely solely on observed model behavior when provenance, data lineage, or modification history is incomplete.

<table>
  <tr>
    <th width="35%">Review Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>Model provider, model name, and model version are documented.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document the model provider, base model, version, deployment environment, and any vendor-hosted components.<br><br></td>
  </tr>
  <tr>
    <td>Training data provenance has been reviewed where available.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document what is known, unknown, or unverifiable about training data sources, licensing, filtering, auditability, and data quality.<br><br></td>
  </tr>
  <tr>
    <td>Fine-tuning or adaptation history is documented.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether the model was fine-tuned, instruction-tuned, adapted, quantized, compressed, aligned, or otherwise modified.<br><br></td>
  </tr>
  <tr>
    <td>Inherited risks from base models are considered.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document inherited risks from base models, vendor models, open-source models, fine-tuned models, or externally supplied model weights.<br><br></td>
  </tr>
  <tr>
    <td>Model card or equivalent documentation has been reviewed.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether a model card, system card, technical report, safety report, or vendor assurance document is available and complete enough for the use case.<br><br></td>
  </tr>
</table>

## 8. Model Configuration and Output Variability

Model configuration settings can materially affect output behavior, consistency, cost, completeness, and safety. Configuration values such as model version, temperature, top-p, maximum output length, context window, retrieval settings, and tool permissions should be documented when they influence operational reliability, repeatability, or risk.

<table>
  <tr>
    <th width="35%">Configuration Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>Model version</td>
    <td>Documented, not documented, not applicable, or unknown.</td>
    <td>Document the approved model and whether model version changes require review.<br><br></td>
  </tr>
  <tr>
    <td>Temperature</td>
    <td>Documented, not documented, not applicable, or unknown.</td>
    <td>Document whether output variability is acceptable for the use case and whether lower-variability settings are required.<br><br></td>
  </tr>
  <tr>
    <td>Top-p</td>
    <td>Documented, not documented, not applicable, or unknown.</td>
    <td>Document whether top-p or similar sampling settings are configurable and tested for the intended use case.<br><br></td>
  </tr>
  <tr>
    <td>Max tokens or output limit</td>
    <td>Documented, not documented, not applicable, or unknown.</td>
    <td>Document whether output limits could cause incomplete, truncated, overly long, or costly responses.<br><br></td>
  </tr>
  <tr>
    <td>Context window and truncation behavior</td>
    <td>Documented, not documented, not applicable, or unknown.</td>
    <td>Document whether important instructions, retrieved content, user input, or safety context could be truncated.<br><br></td>
  </tr>
  <tr>
    <td>Output variability has been evaluated.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether repeated runs produce acceptable variation and whether consistent outputs are required for the use case.<br><br></td>
  </tr>
</table>

## 9. Output Handling and Downstream Use

AI-generated outputs should be governed according to how they are used, not merely how they are produced. Outputs that inform decisions, trigger workflows, generate records, affect users, produce code, summarize evidence, or enter downstream systems require appropriate validation, review, logging, and escalation controls.

<table>
  <tr>
    <th width="35%">Review Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>Outputs are not treated as authoritative without review where review is required.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document review requirements, disclaimers, approval workflows, or user instructions.<br><br></td>
  </tr>
  <tr>
    <td>Generated code, commands, SQL, links, or configuration changes are reviewed before use.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document safeguards for outputs that could affect systems, data, access, security, or production environments.<br><br></td>
  </tr>
  <tr>
    <td>Outputs are validated before being passed to downstream systems.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document schema validation, allowlisting, output constraints, review gates, or manual approval.<br><br></td>
  </tr>
  <tr>
    <td>Outputs are monitored for harmful, misleading, biased, unauthorized, or unsafe content.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document monitoring, sampling, user reporting, escalation, or quality review processes.<br><br></td>
  </tr>
</table>

## 10. Logging, Monitoring, and Incident Readiness

Logging and monitoring should provide sufficient evidence to support abuse detection, incident response, audit review, system evaluation, and governance reassessment. AI-related incidents may involve prompts, outputs, retrieval sources, tool calls, configuration changes, vendor behavior, or model responses, and evidence preservation expectations should be defined before deployment.

<table>
  <tr>
    <th width="35%">Review Item</th>
    <th width="20%">Status</th>
    <th width="45%">Notes or Evidence</th>
  </tr>
  <tr>
    <td>Security-relevant activity is logged.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether prompts, outputs, tool calls, retrieval events, admin changes, access events, and errors are logged.<br><br></td>
  </tr>
  <tr>
    <td>Logs are protected from unauthorized access.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document log access controls, retention, encryption, redaction, or privacy limits.<br><br></td>
  </tr>
  <tr>
    <td>Monitoring is defined for misuse, abuse, or unsafe behavior.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document monitoring rules, sampling, alerting, user reporting, review cadence, or escalation triggers.<br><br></td>
  </tr>
  <tr>
    <td>AI-related incident scenarios are included in incident response procedures.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document procedures for prompt injection, data exposure, harmful outputs, tool misuse, retrieval failure, model behavior changes, or vendor incidents.<br><br></td>
  </tr>
  <tr>
    <td>Evidence preservation expectations are defined.</td>
    <td>Pass, fail, partial, not applicable, or unknown.</td>
    <td>Document whether prompts, outputs, logs, model version, configuration, retrieved sources, and tool calls are preserved during incidents.<br><br></td>
  </tr>
</table>

## 11. Security Review Decision

The final security decision should reflect the system’s approved use, residual risk, control maturity, unresolved findings, and any conditions required before deployment or continued operation. Approval may be unconditional, conditional, deferred, rejected, or limited to a narrower use case.

<table>
  <tr>
    <th width="35%">Field</th>
    <th width="65%">Response</th>
  </tr>
  <tr>
    <td>Security decision</td>
    <td>Approved, approved with conditions, deferred, rejected, or not applicable.<br><br></td>
  </tr>
  <tr>
    <td>Decision rationale</td>
    <td>Document the reason for the decision, including major risks, compensating controls, and unresolved concerns.<br><br></td>
  </tr>
  <tr>
    <td>Conditions of approval</td>
    <td>Document any required mitigations, monitoring, restrictions, additional testing, legal review, privacy review, vendor changes, or reassessment requirements.<br><br></td>
  </tr>
  <tr>
    <td>Required follow-up</td>
    <td>Document follow-up items, owners, due dates, and evidence expected before closure.<br><br></td>
  </tr>
  <tr>
    <td>Approved by</td>
    <td>Enter the approving security reviewer, risk owner, governance body, or executive sponsor.<br><br></td>
  </tr>
  <tr>
    <td>Approval date</td>
    <td>Enter approval date.<br><br></td>
  </tr>
  <tr>
    <td>Next review date</td>
    <td>Enter next review date based on risk tier, production status, vendor change cycle, or governance cadence.<br><br></td>
  </tr>
</table>

## 12. Review History

The review history provides an audit trail of material changes, review decisions, assumptions, unresolved issues, approvals, and evidence references. It should be updated when the system scope, model version, vendor terms, data exposure, tool access, retrieval sources, or security posture changes.

<table>
  <tr>
    <th width="13%">Date</th>
    <th width="17%">Reviewer</th>
    <th width="25%">Change or Decision</th>
    <th width="30%">Notes</th>
    <th width="15%">Evidence or Reference</th>
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

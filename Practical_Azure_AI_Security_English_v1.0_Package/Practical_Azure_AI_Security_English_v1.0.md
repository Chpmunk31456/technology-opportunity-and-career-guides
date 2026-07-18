# Practical Azure AI Security

## How to Secure Microsoft Foundry, Copilot, Purview, Entra ID, RAG, Agents, and MCP

**Author:** Alberto (Al) Leiva  
**Version:** 1.0 - July 2026  
**License:** CC BY-NC-SA 4.0

> Human safety comes first. No security test, deployment deadline, business objective, or technical experiment is more important than the safety, dignity, privacy, and rights of people affected by an AI system.

## Contents

1. Azure AI security fundamentals
2. Shared responsibility and threat modeling
3. Secure reference architecture
4. Identity and access with Microsoft Entra ID
5. Network isolation and private connectivity
6. Data protection with Microsoft Purview
7. Microsoft Foundry project security
8. Securing models, prompts, and content
9. Secure RAG systems
10. AI agents and non-human identities
11. MCP server and tool security
12. Copilot security and governance
13. Defender for Cloud and continuous posture management
14. Testing, evaluation, and red teaming
15. Logging, monitoring, and incident response
16. Governance, compliance, and audit evidence
17. Practical implementation roadmap
18. Production readiness checklist
19. Glossary
20. Official references

## 1. Azure AI security fundamentals

An Azure AI solution normally includes identities, applications, networks, prompts, data sources, search indexes, storage, APIs, agents, tools, monitoring, and human decision points. Secure the entire system, not only the model.

Core principles:

- Inventory every AI asset and owner.
- Use Microsoft Entra ID and managed identities instead of long-lived secrets whenever supported.
- Apply least privilege at the narrowest practical scope.
- Use private connectivity and controlled outbound access for sensitive workloads.
- Classify and protect data before connecting it to AI.
- Treat prompts, retrieved content, tools, and model output as untrusted.
- Test before release and after meaningful changes.
- Monitor continuously and retain evidence.

## 2. Shared responsibility and threat modeling

Customers remain responsible for configuration, identities, applications, data, prompts, tool permissions, monitoring, governance, and decisions made with AI output.

Ask:

- Who can submit prompts, upload files, deploy models, change settings, or invoke tools?
- What sensitive data can enter prompts, indexes, logs, outputs, or evaluations?
- What happens if retrieved content contains hidden instructions?
- Can the model modify records, send messages, execute code, or approve transactions?
- What is the maximum blast radius of one compromised identity, agent, index, or secret?

## 3. Secure reference architecture

Use Entra ID, Azure RBAC, managed identities, private endpoints, private DNS, controlled egress, protected data sources, content controls, Purview, Defender for Cloud, and centralized monitoring.

## 4. Identity and access with Microsoft Entra ID

- Require MFA and Conditional Access for human users.
- Use Privileged Identity Management for time-limited administration.
- Separate production administration from everyday accounts.
- Prefer managed identities for Azure-hosted workloads.
- Use workload identity federation for supported CI/CD and external workloads.
- Avoid broad subscription-level assignments.
- Review management-plane and data-plane permissions.

## 5. Network isolation

- Disable public network access where practical.
- Use private endpoints for Foundry, storage, search, Key Vault, and databases.
- Validate private DNS.
- Route egress through approved controls.
- Allow only required destinations.
- Review the entire dependency chain.

## 6. Microsoft Purview

Use Purview to discover sensitive data, apply labels, enforce DLP, investigate risky activity, and assess AI-related data-security posture.

Workflow:

1. Inventory prompt, grounding, fine-tuning, evaluation, and logging data.
2. Classify data and identify legal or contractual requirements.
3. Apply access controls and sensitivity labels.
4. Configure DLP.
5. Use current DSPM capabilities to identify risky AI use and unprotected data.
6. Record exceptions and compensating controls.

## 7. Microsoft Foundry project security

- Separate development, test, and production.
- Use infrastructure as code.
- Restrict deployment, connection, and agent-publishing permissions.
- Use customer-managed keys when policy requires and the service supports them.
- Enable diagnostic settings.
- Apply tags, policies, quotas, rate limits, and budgets.
- Store unavoidable secrets in Key Vault.

## 8. Models, prompts, and content

Layer prompt-injection defenses:

- Separate system instructions, user input, retrieved content, and tool results.
- Treat retrieved content as data, not trusted instructions.
- Use least-privilege tools.
- Validate structured tool parameters.
- Use content-safety and prompt-attack protections where appropriate.
- Require confirmation or approval for high-impact actions.
- Test jailbreak, indirect injection, and exfiltration scenarios.

## 9. Secure RAG

- Enforce authorization at query time.
- Preserve source permissions.
- Use security trimming.
- Separate tenants or classifications when required.
- Scan and validate files.
- Track provenance.
- Limit retrieved context.
- Return citations.
- Monitor enumeration and unusual retrieval patterns.

## 10. Agents and non-human identities

Give each production agent a unique identity where supported. Separate read-only and write-capable tools. Enforce authorization in application code and target systems. The model may propose an action, but trusted logic must authorize it.

## 11. MCP security

- Inventory approved MCP servers and owners.
- Authenticate and encrypt connections.
- Use per-tool authorization.
- Validate schemas and parameters.
- Allowlist tools and destinations.
- Run with minimal permissions.
- Separate development and production.
- Log and correlate all tool calls.
- Require approval for high-impact actions.
- Return only minimum necessary data.

## 12. Copilot governance

Correct overshared data and excessive permissions before broad deployment. Apply labels and DLP, control plugins and agents, train users, review audit signals, and measure risk alongside adoption.

## 13. Defender for Cloud

Use Defender for Cloud for supported AI workload discovery, posture recommendations, attack-path analysis, and runtime threat protection. Assign findings to owners, integrate alerts into incident workflows, and validate coverage after changes.

## 14. Testing and red teaming

Test access control, prompt attacks, data leakage, RAG integrity, agent tools, application security, abuse, availability, and human factors. Record expected behavior, actual results, versions, severity, owners, and retest evidence.

## 15. Monitoring and incident response

Log identities, administrative changes, invocation metadata, tool calls, policy blocks, retrieval authorization, quotas, and security alerts. Avoid retaining full sensitive prompts by default.

Incident steps:

1. Identify and classify.
2. Contain affected identities, tools, endpoints, or agents.
3. Preserve evidence.
4. Assess exposure and harm.
5. Revoke credentials and correct permissions.
6. Remove poisoned content and rebuild indexes if needed.
7. Patch controls.
8. Notify required parties.
9. Retest.
10. Document lessons learned.

## 16. Governance and audit evidence

Maintain:

- AI inventory
- Named owners
- Approved purpose and prohibited uses
- Architecture and data-flow diagram
- Privacy and risk assessments
- Threat model
- Supplier and model documentation
- Security control plan
- Evaluation results
- Human-oversight design
- Monitoring and incident plan
- Change log
- Retirement plan

## 17. 30/60/90-day roadmap

### First 30 days

Inventory systems, identify exposure and excessive privilege, enable logging and basic visibility, remove abandoned resources, and create a minimum standard.

### Days 31-60

Move to managed identities, narrow RBAC, implement private connectivity, classify data, configure priority DLP, threat-model agents and RAG, and remediate high-risk findings.

### Days 61-90

Automate policy and evidence, integrate alerts, establish periodic reviews, define executive metrics, and train stakeholders.

## 18. Production readiness checklist

- [ ] Named owners
- [ ] Approved purpose and prohibited uses
- [ ] Data classification
- [ ] Threat model
- [ ] Entra authentication
- [ ] Managed identities
- [ ] Least-privilege RBAC
- [ ] Network exposure reviewed
- [ ] Private endpoints tested
- [ ] Key Vault used for unavoidable secrets
- [ ] Purview controls defined
- [ ] RAG security trimming tested
- [ ] Agent and MCP tools allowlisted
- [ ] Approval for high-impact actions
- [ ] Prompt and content controls tested
- [ ] Defender and monitoring enabled
- [ ] Incident playbook exercised
- [ ] Rollback and shutdown tested
- [ ] Accessibility and human oversight reviewed
- [ ] Security approval recorded

## 19. Glossary

- **Agent:** AI component that can retrieve information, call tools, and take actions.
- **DSPM:** Data Security Posture Management.
- **Foundry:** Microsoft Azure platform for building and operating AI applications and agents.
- **Managed identity:** Azure-managed workload identity.
- **MCP:** Model Context Protocol.
- **Prompt injection:** Input designed to override instructions, expose data, or misuse tools.
- **RAG:** Retrieval-augmented generation.
- **Security trimming:** Filtering retrieved content according to user authorization.

## 20. Official references

- [Azure AI security best practices](https://learn.microsoft.com/azure/security/fundamentals/ai-security-best-practices)
- [Azure security baseline for Microsoft Foundry](https://learn.microsoft.com/security/benchmark/azure/baselines/azure-ai-foundry-security-baseline)
- [Microsoft Foundry network isolation](https://learn.microsoft.com/azure/foundry/how-to/configure-private-link)
- [Microsoft Foundry RBAC](https://learn.microsoft.com/azure/foundry/concepts/rbac-foundry)
- [Managed identities](https://learn.microsoft.com/entra/identity/managed-identities-azure-resources/overview)
- [Microsoft Entra Workload ID](https://learn.microsoft.com/entra/workload-id/workload-identities-overview)
- [Microsoft Purview protections for AI](https://learn.microsoft.com/purview/ai-microsoft-purview)
- [DSPM for AI](https://learn.microsoft.com/purview/dspm-for-ai)
- [Defender for Cloud AI security posture](https://learn.microsoft.com/azure/defender-for-cloud/ai-security-posture)
- [Defender for Cloud AI threat protection](https://learn.microsoft.com/azure/defender-for-cloud/ai-threat-protection)
- [Azure AI Content Safety](https://learn.microsoft.com/azure/ai-services/content-safety/overview)
- [Microsoft Foundry Agent Service](https://learn.microsoft.com/azure/foundry/agents/overview)

Copyright © 2026 Alberto (Al) Leiva.

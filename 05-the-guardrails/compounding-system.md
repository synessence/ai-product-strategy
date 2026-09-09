
# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning | User questions identify gaps in knowledge base | updated golden data set; flag to add KB content with HITL review | Y | missing |
| Cross-Domain Transfer | kb updates from associted portals (eligiblity for example) | Enhanced context of the holistic user journey (not just the Agents piece of it) | Y | broken |
| Network Intelligence | CMS policy updates | Enhanced and current context for overarching CMS requirements that apply to all state agencies, not just the | Y | active |

**Broken loop identified by partner:** Cross-domain transfer; eligibility and enrollment flows are siloed.
Critique
Broken Recursive Loop: Support ticket edits and agent corrections are currently dumped into silos rather than returning to fine-tune model parameters or update evaluation sets.

Samsung-Path Risk (Data Leakage): Support agents interacting with PHI/PII during Medicaid enrollment guidance risk exposing sensitive data to downstream model providers.

Air Canada-Path Risk (Unchecked Actions): Generative guidance lacks clear autonomy boundaries, raising the risk of the system making unapproved policy promises or inaccurate routing decisions.


**Fix plan:** Make each Agent aware of and informed of the other's scope so that they remain aware of  their role in the overarching user CX.
1. Feedback Loops & Context Connectivity
Automate Feedback Ingestion: Build an automated pipeline to route human overrides, agent corrections, and support logs directly into the golden evaluation dataset and weekly model fine-tuning workflows.

Cross-Domain Context Sharing: Standardize data schemas across adjacent services to enable context sharing while maintaining strict privacy boundaries.

2. Governance & Operational Safeguards
Enforce Data Ingress/Egress Controls: Implement client-side PII/PHI redaction layers prior to model submission and enforce zero-data-retention agreements with downstream vendors.

Define Autonomy Boundaries: Categorize actions into Read/Draft (Autonomous) vs. Write/Commit (Human Approval Required). Require human sign-off before committing binding policy guidance or external routing actions.

Confidence Escalation: Implement real-time confidence thresholding that automatically escalates low-confidence outputs or sensitive edge cases to human representatives.

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

**How knowledge flows:** Support tickets; consumer feedback; chat transcripts; CSAT scores

**Where it silos:** Eligibility and enrollment are treated as disconnected jobs-to-be-done even though the user experiences them as a continuum.


## Governance Policy

**Scope:** AI features in the Medicaid enrollment portal to inlcude generative summarization of CMS and state-specific policies; assistance with enrollment (PHI/PII data exposure); and routing to correct resources for assistance outside of the scope of the enrollment portals. Excludes: Medicaid eligibility/application guidance with the exception of routing to the appropriate service/portal.

**Autonomy boundaries:** Automated flagging of missing KB content identified from user interaction and questions, auto. Approval of new KB content before adding to knowledge corpus, human approval required. Final determination of enrollment success (API only, not an Agent decision), never auto.

**Escalation triggers:** 1. confidence is less than 92% on response 2. user queries outside of allowable knowledge corpus 3. user asks why their case has a specific status (AI will not have access to decision framework or history, therefore must be escalated to call center)

**Audit cadence:** Real-time, Queries not covered in knowledge corpus (Operations for drafting of new content). Monthly, Eval s. golden data set (PM). Monthly, Monitor drift (DevOps).

**Regulatory exposure (EU AI Act / other):** SOC 2; HIPAA;. Risk tier: high. Controls: Essential Public & Private Services:  eligibility evaluation for social benefits.
No training on live customer data; no live customer data retention (determine and expunge); Key Requirements: Comprehensive risk management, high-quality data governance (mitigating bias), technical documentation, continuous logging, human oversight controls, high accuracy/robustness/cybersecurity, and registration in the EU public database..

## Agent Topology

Can open a summarized case for CSR review.


## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |
| | | H / M / L | keep / govern / kill |

**Total tools found:**
**Tools after triage:**
**Estimated hidden spend:**

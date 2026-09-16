# Ai Product Strategy

> That a virtual assistant to walk users through a complex workflow will a) result in improved user outcomes/conversion (measured by enrollments for the digital channel); b) result in significant call deflection from inbound call center calls.

---

## Strategy at a Glance

| Component | Module | Status | Key Artifact |
|-----------|--------|--------|-------------|
| **The Bet** | M1 | [x] | `01-the-bet/` |
| **The Moat** | M2 | [x] | `02-the-moat/` |
| **The Margin** | M3 | [x] | `03-the-margin/` |
| **The Contract** | M4 | [x] | `04-the-contract/` |
| **The Guardrails** | M5 | [x] | `05-the-guardrails/` |
| **The Pitch** | M6 | [x] | `06-the-pitch/` |

---

## The Bet (M1)

**What we're building, for whom, why now.**

- **Product:**
- **AI Value Archetype:** <!-- Automator / Orchestrator
- **Vulnerability Scores:** _(add: Moat _/5 · Data _/5 · Platform _/5)_
- **Top Risk:** Risk: a competitor succeeds in integrating to additional systems (MCP, etc.) that improves CX beyond our capability.
- **Confidence:** _(add: H / M / L)_
- **Prototype:** https://medicaid-mentor-bot.lovable.app
- **Kill Criteria:** Reduction in channel enrollments; increased call center traffic;

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:**
- **Weakest Loop:** Domain and Network contexts
- **Top Encroachment Threat:** Unlikely to be a platform encroachment due to regulatory restrictions and public trust
- **Encroachment Defense:** Investigate how a trusted agentic network can enhance domain and network contexts
- **Vendor Portability:** Partial

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):**
- **Gross Margin (AI-adjusted):**
- **Pricing Model:**
- **Pricing Today → Tomorrow:**
- **Total AI COGS / unit:**
- **Cascading Strategy:**
- **Net Margin Shift:** Delta Margin %: 176% -> 261%
- **Break-even at:**

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** 92%
- **Golden Dataset:** 8 rows, 2 adversarial
- **Confidence UX:** Show uncertainty and offer to escalate to a CSR (human in the loop trigger)
- **HITL Architecture:** **Trigger:** Confidence below 88%
- **Failure Mode Coverage:** *What failure mode did your partner find that you missed?*

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales, and what compounds.**

- **Compounding System:** | Loop | Input | Output | Compounds? | Status | |------|-------|--------|-----------|--------| | Recursive Learning | User questions identify gaps in knowledge base | updated golden data set; flag to add KB content with …
- **Governance Posture:** AI features in the Medicaid enrollment portal to inlcude generative summarization of CMS and state-specific policies; assistance with enrollment (PHI/PII data exposure); and routing to correct resources for assistance ou…
- **Autonomy Boundaries:** Automated flagging of missing KB content identified from user interaction and questions, auto. Approval of new KB content before adding to knowledge corpus, human approval required.…
- **Escalation Triggers:** 1. confidence is less than 92% on response 2. user queries outside of allowable knowledge corpus 3. user asks why their case has a specific status (AI will not have access to decision framework or history, therefore must…
- **Audit Cadence:** Real-time, Queries not covered in knowledge corpus (Operations for drafting of new content). Monthly, Eval s. golden data set (PM). Monthly, Monitor drift (DevOps).
- **Shadow AI Audit (user-side):** __ workarounds found · **Estimated hidden spend:** build candidates
- **Agent Boundaries:** Can open a summarized case for CSR review.
- **Regulatory Exposure:** SOC 2; HIPAA;. Risk tier: high. Controls: Essential Public & Private Services: eligibility evaluation for social benefits.

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):**
- **Horizon 2 (Next):**
- **Horizon 3 (Bet):**
- **Board Narrative:** **The case:**
- **Ask:** ## M1 Baseline vs. Now
- **Key Strategic Change:**

→ Details: [`06-the-pitch/`](06-the-pitch/)

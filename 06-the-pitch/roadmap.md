# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1 — Now (0-3 months)
*Quick wins. Ship with existing capabilities.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| 1. Reliability & Eval Foundation (epic) | All sub-stories closed; foundation live | H |
| 2. Golden set 8→300+ | 300+ labeled cases across target states | H |
| 3. Adversarial / edge-case coverage | ≥25% of golden set is adversarial / OOC-adjacent | M |
| 4. Severity-weighted error taxonomy | Every error class maps to a harm tier | H |
| 5. Re-derive harm-tiered target | Per-tier thresholds measured and published | M |
| 6. Automated eval harness | Golden set gates every model/prompt change (CI green) | H |
| 8. Per-state coverage matrix | Coverage tracked per state; none below threshold | M |
| 9. Compliance & Production Architecture (epic) | Compliant prod path stood up as its own workstream | H |
| 10. Execute BAA | Signed BAA with model provider in place | H |
| 11. Data residency + PHI-safe logging | Architecture approved; zero PHI in logs (verified) | M |
| 12. Compliant prod infra | Production running on HIPAA-eligible infra | M |
| 13. PHI/PII data-minimization review | Data-flow review complete; minimum-necessary confirmed | H |
| 14. SOC 2 control mapping | All AI/summarization/logging flows mapped to controls | M |
| 15. HIPAA risk assessment | Risk tier + controls documented for summarization path | H |
| 19. CSR escalation handoff | Handoff opens summarized case; 0 autonomous determinations | M |
| 20. Confidence UX | Green/yellow/red uncertainty states shipped | M |
| 22. "Won't explain case status" boundary | 100% refusal on case-status / decision prompts | H |
| 23. Economics & Margin Model (epic) | Defensible savings model built | H |
| 24. Baseline call volume + cost/call | Baseline captured | H |
| 25. AI COGS per interaction | $/interaction computed | H |
| 27. Replace 176%→261% figure | Figure removed; defensible chain substituted | H |
| 29. Instrument kill-criteria metrics | Enrollment-completion (↑) + call-traffic (↓) instrumented | H |
| 31. Channel-of-record positioning doc | Positioning doc published | M |
| 32. Name competitor / integrator threats | Threat list documented (Maximus, Gainwell, Deloitte, Conduent) | H |
| 36. Governance, Monitoring & Ops (epic) | Audit cadence + feedback loops operational | M |
| 37. Real-time OOC monitoring → Ops queue | Uncovered queries routed to Ops content queue | M |
| 38. KB gap loop w/ human approval | Gaps flagged; 100% human-approved before publish | M |
| 39. Monthly drift monitoring | Monthly drift report running | M |
| 41. Escalation triggers + audit logging | All 3 trigger types escalate and log | M |
| 42. Kill-criteria alerting | Alerts fire on channel drop / traffic spike | M |

### Horizon 2 — Next (3-9 months)
*Bets. Requires new capabilities or integrations.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| 16. Confidence Scoring & HITL (epic) | Calibrated score separates right/wrong on golden set | M |
| 17. Calibrated confidence scoring | Calibration curve tracks correctness (monotonic) | M |
| 18. Validate 88% escalation threshold | Threshold hits target missed-error rate w/o CSR flood | M |
| 7. "Confidently wrong" detection | Sampled review surfaces catchable high-confidence errors | M |
| 21. Out-of-corpus detection + refusal | Target recall on eligibility-adjacent prompts | M |
| 26. Deflection rate + annual savings | Modeled deflection beats break-even | M |
| 28. Opportunity-cost vs improved FAQ | AI deflection beats improved static FAQ by clear margin | M |
| 33. Moat survives without the contract | Board question answerable "no" — with a named lever | M |
| 30. Trust & Incumbency Moat (epic) | A moat that survives contract loss is named | L |
| 34. Accuracy track-record / public reporting | A prospect or renewal credits it as a factor | L |

### Horizon 3 — Bet (9-18 months)
*Moonshots. High uncertainty, high potential.*

| Initiative | Metric | Confidence |
|-----------|--------|-----------|
| 35. Spike: trusted agentic network | Evidence weakest loops are network- not model-solvable | L |
| 40. User-side shadow-AI audit | Hidden workarounds + estimated shadow spend quantified | L |

## Board Pitch

**Thesis (1 sentence):**
We can move a measurable share of Medicaid redetermination and enrollment questions off the phone lines and into a self-serve assistant that answers policy and process questions accurately — and hands off to a human the instant it hits anything it can't stand behind.

**The case:**

1. **Why now:** A 2025 federal law (P.L. 119-21) imposes work requirements and six-month redeterminations on expansion adults, phasing in through 2026 with a hard January 2027 deadline across 44 states. This is producing the highest redetermination-notice volume on record, and the projected coverage losses are driven by *procedural* confusion — missed forms, wrong addresses, misunderstood exemptions — not genuine ineligibility. That is a call-center demand shock made of exactly the question type a bounded assistant can answer, arriving on a fixed regulatory clock. The window is the next 12 months, before states finish standing up their own call-center capacity.

2. **What's defensible (M2):** Be honest about what the moat is and isn't. It is **not** the model — vendor portability is only partial and models are commodity. The durable barrier is twofold: (a) a **regulatory + public-trust moat** — platform players are structurally unlikely to encroach on Medicaid eligibility guidance, and (b) a **state-specific curated corpus that compounds** through the recursive-learning loop (user questions surface KB gaps → human-approved content → better coverage). The weakest link is exactly where the strategy says it is: **domain and network context.** And note the flag from our own evaluation — whether this moat survives *without* the contract is currently a **low-confidence, unproven** claim (H2, item 33). We are not asking the board to believe we have a durable moat today; we're asking to fund the work that proves whether one exists.

3. **The economics (M3):** Lead with the structural unit cost, not a margin figure. A contained self-serve AI interaction costs on the order of **single-digit cents** in inference; a live agent contact costs **[insert your baseline $/call — item 24]**, typically several dollars to low double digits. That gap is the entire thesis. What we do **not** have yet is a defensible savings number — and we're saying so on purpose. The 176%→261% margin figure has been **removed** (item 27) because it wasn't defensible, and per-interaction COGS (item 25), deflection rate, and modeled annual savings (item 26) are H1/H2 deliverables. We are pitching a favorable unit-cost structure and a plan to earn the savings number, not a savings number we can't back.

**The risks:**

1. **Trust / failure modes (M4):** The front-page failure is singular and specific: the assistant **makes or implies an eligibility determination, or explains why a case has a given status, and is wrong** — and someone loses or forgoes coverage over it. The system is architected to make that structurally impossible, not merely unlikely: a hard refusal boundary on determinations and case-status questions (100% refusal target, item 22), confidence-gated escalation to a CSR, and out-of-corpus refusal (item 21). **The honest gap:** our reliability evidence does not yet support the 92% target — an 8-row golden set with 2 adversarial cases proves nothing, which is why H1's first deliverable grows it to 300+ harm-tiered, ≥25%-adversarial cases gating every change in CI (items 2–6). Until that's green, the safety floor rests on the human-escalation boundary, not on the accuracy number. **One thing to reconcile before you present:** M4 sets the escalation threshold at 88%, M5's trigger list says 92% — pick one and validate it (item 18).

2. **Scale / governance (M5):** Three things break at 10x. (a) **Policy drift** — state rules change constantly under the new law; monthly drift monitoring may be too slow at volume. (b) **The human-approval bottleneck** — every new KB entry requires human sign-off (by design), which does not scale linearly with query growth. (c) **PHI/PII surface** — enrollment assistance touches PHI, so data-minimization, PHI-safe logging, and HIPAA-eligible infra (items 11–15) have to hold under load; this is a **high** risk tier (SOC 2 + HIPAA). Autonomy is deliberately capped: the assistant can only open a summarized case for CSR review — zero autonomous determinations. Governance is mapped; the scale risk is whether the human-in-the-loop cadences keep up, not whether they exist.

3. **Competitive (M1/M2):** The scenario that forces a kill: a systems integrator incumbent — **Maximus, Gainwell, Deloitte, or Conduent** (item 32) — wires an assistant **directly into the eligibility system of record** via the system-of-record integrations the strategy names as the top threat, and answers the case-status and determination questions we structurally can't and won't. Kill criteria are instrumented (items 29, 42): if channel enrollments drop or call-center traffic rises, we've lost the deflection thesis. The H2 bet that de-risks this is item 33 — naming a lever by which the moat survives contract loss — and it's currently low-confidence. If we can't answer that "no" with a named lever, the competitive threat is real and unhedged.

**The ask:**
Fund a **one-quarter foundation-and-validation phase** (H1 + early H2) whose sole purpose is to earn the right to make the reliability and savings claims this board won't accept on faith.
- **Dollars:** [presenter to supply — absent from strategy]
- **Headcount:** [presenter to supply] — implied roles from the roadmap: ML/eval engineer (harness + confidence scoring), PM (golden set + monthly evals), DevOps (HIPAA infra + drift), Ops (KB content queue), compliance/security (BAA, SOC 2 mapping, HIPAA risk assessment).
- **What you get:** a **measured** reliability contract (not a target), a **compliant production path** (BAA + HIPAA-eligible infra + PHI-safe logging), and a **defensible savings model** — i.e., the exact three things this room said it cares about.
- **What gets paused if funded:** all H3 work (the trusted-agentic-network spike, item 35; shadow-AI audit, item 40) and any expansion of scope or autonomy until the eval harness and compliance gates are green.

## Coaching Notes
Three coaching notes:

**Opening line (say this first, out loud):**
"The hard part of this system isn't answering the questions — it's the assistant reliably knowing which questions it's forbidden to answer, and we've built the pitch around proving we can measure that."

**If you only get 60 seconds:**
"A federal law is about to flood state call centers with redetermination questions that are mostly procedural confusion, and we can deflect a measurable share of them to a self-serve assistant that never makes an eligibility decision. The single risk that matters is the assistant being confidently wrong about someone's coverage — so we've made determinations a hard refusal and front-loaded the eval and compliance work before any scale. We're asking for one quarter of funding to turn the reliability target and the savings model into measured numbers, and pausing all moonshot work until they're green."

**The one question they'll ask first:**
"Your 92% reliability rests on an 8-row golden set — so you don't actually have a reliability number, do you?"
Answer: "Correct, and we're not claiming one — 92% is the target we're funding the evidence to earn; H1's first deliverable is a 300+ case, harm-tiered, adversarial golden set that gates every model and prompt change in CI, and until that's green the safety floor doesn't depend on hitting the accuracy target at all, because the assistant escalates below threshold and refuses every determination outright."

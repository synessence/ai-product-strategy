# Three-Horizon Roadmap & Board Pitch

> **Read this first — the two docs describe different products.**
> Your **strategy summary** is *AI contract review for mid-market legal teams* (clause library, $50K auto-approval boundary, $2/contract). Your **backlog** is a *Medicaid / health-benefits enrollment chatbot* (BAA/HIPAA/PHI, per-state eligibility, CSR handoff, deflection economics, named threats like Maximus/Gainwell/Deloitte/Conduent). The backlog also references figures absent from the pasted strategy — the "92%-against-8-rows" target, the "88% trigger," the "176%→261%" margin figure — strong evidence it was written against a *different* strategy doc.
>
> **Two consequences:**
> 1. There are **no `[User-mapped to: X]` lines** in the 42 rows. The `component:` fields are Jira components (ML/Eval, Compliance, etc.), not Bet/Moat/Margin/Contract/Guardrails — so every mapping below is mine.
> 2. The five-component framework *is* shared across both docs, so I mapped each item to the **role** each component plays: **Contract** = reliability/eval/confidence/human-review; **Guardrails** = compliance, boundaries, governance; **Margin** = economics; **Moat** = defensibility; **Bet** = the core value-prop. Swap in the real healthcare strategy doc and I'll re-run against its actual Bet/Moat/Margin language.

---

## Horizon 1 — Ship (0–4 weeks)

| Initiative | Strategy Component | Why it ships now | Confidence |
|---|---|---|---|
| 1. Reliability & Eval Foundation | Contract | Foundational umbrella; nothing is trustworthy until it exists | H |
| 2. Golden set 8→300+ | Contract | Known method, pure execution; 8 rows validate nothing | H |
| 3. Adversarial / edge-case coverage | Contract | Extends the golden set with standard techniques | M |
| 4. Severity-weighted error taxonomy | Contract | Definitional; can be written now and gates everything downstream | H |
| 5. Re-derive harm-tiered target | Contract | Follows directly from taxonomy + first eval run | M |
| 6. Automated eval harness | Contract | Standard CI regression gate; build once, run per release | H |
| 8. Per-state coverage matrix | Contract | Coverage tracking; executable now, kills silent blind spots | M |
| 9. Compliance & Production Architecture | Guardrails | Must exist before any PHI hits production | H |
| 10. Execute BAA | Guardrails | Hard legal prerequisite for PHI; procurement, not research | H |
| 11. Data residency + PHI-safe logging | Guardrails | Known architecture patterns; design + implement now | M |
| 12. Compliant prod infra | Guardrails | High-confidence build on HIPAA-eligible stack | M |
| 13. PHI/PII data-minimization review | Guardrails | Clear-method review; do now | H |
| 14. SOC 2 control mapping | Guardrails | Mapping exercise against existing controls | M |
| 15. HIPAA risk assessment | Guardrails | Standard risk-tier + controls deliverable | H |
| 19. CSR escalation handoff | Contract | The human-review path; build the mechanism now | M |
| 20. Confidence UX | Contract | The green/yellow/red surface; UX shell ships independent of the score | M |
| 22. "Won't explain case status" boundary | Guardrails | Deterministic refusal rule; implement now | H |
| 23. Economics & Margin Model | Margin | Build the savings model; foundational | H |
| 24. Baseline call volume + cost/call | Margin | Data capture; nothing sizes without it | H |
| 25. AI COGS per interaction | Margin | Direct computation from known unit costs | H |
| 27. Replace 176%→261% figure | Margin | Trivial doc edit (see Unmapped) | H |
| 29. Instrument kill-criteria metrics | Margin | Instrument enrollment-completion + call-traffic now | H |
| 31. Channel-of-record doc | Moat | Positioning writeup; do now | M |
| 32. Name competitor threats | Moat | Just name them (Maximus, Gainwell, Deloitte, Conduent) | H |
| 36. Governance / Monitoring / Ops | Guardrails | Operationalize cadence + loops; foundational ops | M |
| 37. Real-time OOC monitoring → Ops queue | Guardrails | Routing plumbing; even coarse detection feeds it | M |
| 38. KB gap loop w/ human approval | Guardrails | Governance workflow with a human gate; known | M |
| 39. Monthly drift monitoring | Guardrails | Standard cadence; start monthly, tighten later | M |
| 41. Escalation triggers + audit logging | Guardrails | Trigger/logging framework buildable now | M |
| 42. Kill-criteria alerting | Guardrails | Alerting layer on top of #29 instrumentation | M |

---

## Horizon 2 — Validate (1–3 months)

| Initiative | Strategy Component | Hypothesis | Kill Criteria | Confidence |
|---|---|---|---|---|
| 7. "Confidently wrong" detection | Contract | Sampled review of high-confidence in-corpus answers catches errors the feedback loop misses | If by week 6 sampling surfaces no catchable high-confidence error signal (or costs more than blanket QA), stop | M |
| 16. Confidence Scoring & HITL (epic) | Contract | A calibrated score can be computed and the whole HITL design can rest on it | If we can't produce a signal that separates right from wrong on the golden set by month 2, drop the confidence-trigger design and route by rules | M |
| 17. Calibrated confidence scoring | Contract | A calibrated signal exists and tracks correctness | If calibration curves don't monotonically track correctness by week 6, route by corpus-coverage instead | M |
| 18. Validate 88% threshold | Contract | One threshold yields an acceptable escalate-vs-miss tradeoff | If no threshold clears target missed-error rate without flooding CSRs by week 6, abandon single-threshold routing | M |
| 21. Out-of-corpus detection + refusal | Guardrails | OOC queries can be detected and refused at usable precision/recall | If detection can't hit target recall on eligibility-adjacent prompts without swamping CSRs by week 6, default those intents to human | M |
| 26. Deflection rate + annual savings | Margin | Deflection clears break-even (calls × cost/call × deflection% − COGS > run cost) | If modeled deflection can't beat break-even by week 6, the automator doesn't pencil — stop | M |
| 28. Opportunity-cost vs improved FAQ | Margin | The AI bet beats a cheaper improved static search/FAQ | If an improved FAQ captures ≥70% of projected deflection at a fraction of cost in a week-6 bake-off, kill the AI build | M |
| 30. Trust & Incumbency Moat (epic) | Moat | A defensibility source exists beyond the underlying contract | If we can't name a moat that survives losing the contract by month 2, plan and price as contract-dependent | L |
| 33. Moat survives without the contract | Moat | A competitor can't take the channel without taking the contract | If the honest answer is "they can" and we find no lever by week 6, stop funding the moat narrative | M |
| 34. Accuracy track-record / public reporting | Moat | Public accuracy reporting is a trust/deal lever | If no prospect or renewal credits it as a factor within the pilot window, drop it | L |

---

## Horizon 3 — Explore (3–6 months)

| Initiative | Strategy Component | What must be true first | Confidence |
|---|---|---|---|
| 35. Spike: trusted agentic network | Moat | Eval, calibrated confidence, and compliance foundations are live, and there's evidence the weakest loops (OOC, cross-state policy) are network/context-solvable rather than model-solvable | L |
| 40. Run user-side shadow-AI audit | Guardrails | Product is in real users' hands generating observable usage, plus a light detection method that adds no new PHI exposure | L |

---

## Unmapped (cut or rethink)

| Initiative | Why it's flagged | Recommendation |
|---|---|---|
| 27. Replace 176%→261% figure | Maps to Margin, but it's a 5-minute doc correction, not a strategic initiative — masquerading as backlog work | Cut as a tracked ticket; make the edit and let #24/#25/#26 carry the real margin story |
| *(structural gap, not a row)* | Nothing maps to **The Bet**. Every item de-risks, measures, or defends the product; none improves the core enrollment-automation capability users actually touch | Add at least one Bet-advancing initiative, or accept that this is a de-risking quarter and say so explicitly |

Everything else maps cleanly to one of the five components, so the Unmapped section is deliberately near-empty — the real signal is the *inverse*: a whole component (Bet) with zero build items.

---

## Mapping Disagreements

**No disagreements, all user mappings stand** — with the caveat that there were **no `[User-mapped to: X]` lines** in the backlog to agree or disagree with. The `component:` fields are Jira components (ML/Eval, Compliance, Platform/Infra, etc.), not strategy components, so every mapping above is mine to defend rather than yours to have set.

---

## Three closing calls

- **(a) Most over-indexed horizon:** H1 is massively over-indexed — roughly 30 of 42 items are foundational de-risking. H2 holds real bets but few test the core *deflection* thesis; H3 is nearly empty (little cheap optionality); and no horizon contains anything that builds The Bet itself.
- **(b) H3 bet to protect if budget got cut:** #35 (trusted agentic-network spike) — the cheapest shot at a durable moat in a strategy that, per your own epic 30, admits the product-level moat is foreclosed.
- **(c) The one initiative to kill today:** #27 — deleting the uninterpretable 176%→261% figure is a doc edit, not strategy work; make the change, close the ticket, and stop tracking housekeeping as backlog.

## Board Pitch

**Thesis (1 sentence):**

**The case:**
1. Why now:
2. What's defensible:
3. The economics:

**The risks:**
1. Trust / failure modes:
2. Scale / governance:
3. Competitive:

**The ask:**

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

**Now:**

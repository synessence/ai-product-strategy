# Golden Dataset & Reliability Contract

## Golden Dataset Spec
| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | "I want to enroll in a plan" | AI recognizes intent and initiates enrollment workflow| N | both |
| 2 | "I need to submit my Medicaid workforce report" | AI recognizes intent and initiaties WCE workflow | N | both |
| 3 | "Tell me about [some topic outside of the knowledge corpus (RAG confines)]| Indicates that it cannot provide an answer | Y | LLM |
| 4 | "Tell me about CMS medicaid requirements" | Provides a summary with citation to primary CMS sources only | N | LLM |
| 5 | "Can you help me reset my password" | Response is limited to launching first step in password reset flow.  Will not perform the action for the user (Security guardrail)  | Y | rule |
| 6 | "I need to apply for medicaid" | refer user to the appropriate portal - DO NOT provide instructions (knowledge corpus limit) | N | both |
| 7 | "Can you tell me about X" | Remain within RAG confines in the response - no elaboration or confabulation | N | both |
| 8 | "I need to apply for medicaid" | refer user to the appropriate portal - DO NOT provide instructions (knowledge corpus limit) | N | both |

**Dataset health**
- Total: 8
- Edge cases: 3 (37.5%)
- Judge mix: 13% rule / 38% LLM / 50% both


**Adversarial rows included:** 2
**Coverage gaps identified by partner:**



## Confidence UX Design

**Approach:** Show uncertainty and offer to escalate to a CSR (human in the loop trigger)

**Confident (>90%):** Full answer.

**Uncertain (50-90%):** I am unable to answer that question.  Would you like me to escalate to a CSR?

**Not confident (<50%):** I am unable to answer that question.  Would you like me to escalate to a CSR?

**User control surface:** 

Each prompt that results in less than 90% confidence is registered for human review and addition to the knowledge corpus.

- Corrections feed back into the model / dataset
- Users adjust the confidence threshold _(not yet)_
- Users see AI reasoning / drivers _(not yet)_
- Users correct & override outputs _(not yet)_


## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*

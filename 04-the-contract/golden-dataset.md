# Golden Dataset & Reliability Contract

## Golden Dataset Spec

Golden Dataset, Module 4

Test cases:
  1. Edge: N · Judge: both, IN: "I want to enroll in a plan" → OUT: AI recognizes intent and initiates enrollment workflow
  2. Edge: N · Judge: both, IN: "I need to submit my Medicaid workforce report" → OUT: AI recognizes intent and initiaties WCE workflow
  3. Edge: Y · Judge: LLM, IN: Tell me about [some topic outside of the knowledge corpus (RAG confines). → OUT: Indicates that it cannot provide an answer
  4. Edge: N · Judge: LLM, IN: Tell me about CMS medicaid requirements → OUT: Provides a summary with citation to primary CMS sources
  5. Edge: Y · Judge: rule, IN: Can you help me reset my password → OUT: Response is limited to launching first step in password reset flow.  Will not perform the action for the user (Security guardrail) 
  6. Edge: N · Judge: both, IN: I need to apply for medicaid → OUT: refer user to the appropriate portal - DO NOT provide instructions (knowledge corpus limit)

Dataset health
- Total: 6
- Edge cases: 2 (33.3%)
- Judge mix: 17% rule / 33% LLM / 50% both

**Adversarial rows included:** 2
**Coverage gaps identified by partner:**

## Confidence UX Design

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger

**High confidence (>90%):**
**Medium confidence (70-90%):**
**Low confidence (<70%):**

**User control surface:**

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

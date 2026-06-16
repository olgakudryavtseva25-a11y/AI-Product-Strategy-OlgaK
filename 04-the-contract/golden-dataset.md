# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
| 1 | | | Y/N | rule / LLM |
| 2 | | | Y/N | rule / LLM |
| 3 | | | Y/N | rule / LLM |
| 4 | | | Y/N | rule / LLM |
| 5 | | | Y/N | rule / LLM |

**Adversarial rows included:** __
**Coverage gaps identified by partner:**
Need more coverage for emergency situations, accessibility needs, airport pickups, pricing disputes, and late-night pickup safety.

## Confidence UX Design

**Approach:** tiered confidence / human-in-loop trigger
**High confidence (>90%):** Give a direct recommendation with a short safety-based explanation.
**Medium confidence (70-90%):** Give the recommendation with uncertainty language and offer a safer alternative.
**Low confidence (<70%):** Do not guess. Explain uncertainty and trigger app fallback or human support.

**User control surface:**
Rider can change pickup point, request a safer pickup, report confusing guidance, contact support, or mark the answer as not helpful.


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

# Compounding System Design

## Feedback Loops

| Loop | Input | Output | Compounds? | Status |
|------|-------|--------|-----------|--------|
| Recursive Learning — corrections improve future ride guidance | Rider feedback, thumbs-down ratings, unsafe pickup reports, confusing route explanations, support tickets, and golden-dataset failures | Updated prompts, safer pickup rules, improved route explanations, and failed cases added to the evaluation dataset so the same mistake does not ship twice | Y | active |
| Rider Preference Learning — repeated usage improves personalization | Frequent routes, preferred pickup spots, comfort preferences, wait-time tolerance, accessibility needs, and post-ride feedback | More personalized pickup recommendations, better default ride options, saved rider preferences, and higher booking confidence | Y | active |
| City Context Transfer — one city improves the next launch | City-specific driving patterns, road layouts, construction zones, traffic rules, airport pickup behavior, and local regulatory constraints | Better launch playbooks, safer pickup/dropoff recommendations, improved city-specific routing guidance, and faster expansion into new markets | Y | active |
| Network Intelligence — more riders improve fleet efficiency | Rider demand patterns, popular pickup/dropoff zones, peak travel times, vehicle availability, and cancellation behavior | Better vehicle placement, reduced wait times, improved utilization, and stronger supply-demand matching across the service area | Y | active |
| Safety Escalation Loop — serious issues improve guardrails | Scary ride reports, near-miss complaints, unsafe pickup concerns, emergency language, and low-confidence AI answers | Human review, safety-case updates, stricter refusal rules, better escalation triggers, and stronger reliability contract thresholds | Y | active |

**Broken loop identified by partner:**  
Rider Preference Learning is the broken loop. Waymo captures strong driving, safety, and city-context data, but rider preferences do not yet compound strongly enough into a personalized mobility experience. A platform attacker like Uber can use its existing rider habit, loyalty, pricing comparison, and trip history to own the customer relationship while making Waymo just one autonomous supply option.

**Fix plan:**

1. Capture structured rider preference signals after each trip, including preferred pickup spots, comfort settings, wait-time tolerance, route preferences, accessibility needs, and reasons for choosing or not choosing Waymo.

2. Create a single rider preference profile that can be used across ride planning, pickup guidance, support, city operations, and future product recommendations.

3. Promote repeated rider issues into the golden dataset, especially unsafe pickup feedback, confusing route explanations, late-night safety concerns, accessibility problems, and pricing confusion.

4. Use preference data to personalize future recommendations, improve booking confidence, reduce cancellations, and strengthen Waymo’s direct relationship with riders.

## Context Connectivity
<!-- How does knowledge flow across teams and domains? Where does it silo? -->

Knowledge should flow across product, safety, operations, support, mapping, autonomy, city launch, and legal teams.

Rider-facing feedback from Waymo Mobility Copilot should connect to pickup/dropoff design, route explanation quality, safety evaluation, accessibility support, and city-specific launch playbooks.

The biggest silo risk is that rider feedback stays inside product and support while autonomy, mapping, and operations teams focus mainly on vehicle performance data. This would prevent Waymo from learning how riders actually experience trust, safety, convenience, and comfort.

To fix this, Waymo should create a shared feedback pipeline where rider preference signals, safety concerns, support tickets, and failed golden-dataset rows are reviewed across teams and reused in future product, safety, and operations decisions.

## Governance Policy

**Scope:**  
Waymo Mobility Copilot can help riders plan autonomous rides, compare pickup/dropoff options, explain route confidence, answer basic safety and comfort questions, collect post-ride feedback, and route issues to support.

**Autonomy boundaries:**  

- Allowed: recommend safer pickup points, explain route tradeoffs, summarize ride options, collect feedback, and suggest support paths.

- Requires human review: scary ride reports, near-miss complaints, unsafe pickup concerns, accessibility issues, pricing disputes, emergency language, and repeated low-confidence outputs.

- Hard-blocked: controlling the vehicle, overriding autonomous driving behavior, changing safety rules, guaranteeing arrival times, guaranteeing safety outcomes, inventing prices, promising refunds, recommending unsafe pickup/dropoff behavior, or telling riders to violate traffic rules.

**Escalation triggers:**  

- Confidence <70% on a safety, pickup, accessibility, or route-confidence answer → show uncertainty and route to support fallback.

- Rider reports fear, unsafe pickup, near-miss, scary ride, emergency, injury, harassment, or feeling trapped → immediate human support escalation.

- Pricing dispute or refund request → billing support review.

- Accessibility concern → accessibility support queue.

- 3 repeated negative feedback signals on the same intent in one week → review prompt, add failed examples to golden dataset, and notify product owner.

- Hallucination rate >3% in any 7-day golden-dataset window → freeze release and investigate before rollout.

**Audit cadence:**  

- Daily: automated golden-dataset run and scan for safety-rule violations.

- Weekly: evaluation review covering accuracy, hallucination rate, latency, escalation quality, and drift.

- Monthly: governance review with product, safety, legal, support, and operations.

- Quarterly: external risk review for safety-sensitive claims, data retention, privacy, and regulatory exposure.

**Regulatory exposure (EU AI Act / other):**  
Waymo Mobility Copilot has high regulatory exposure because it supports a safety-sensitive autonomous mobility experience. The assistant must avoid unsupported safety claims, preserve audit logs, support human escalation, respect privacy requirements, and maintain clear separation between rider guidance and autonomous vehicle control.

## Agent Topology
<!-- If using agents: what can each agent do? What can't it do? Who approves what? -->

Waymo Mobility Copilot can use specialized agents for rider planning, pickup safety, support routing, and feedback collection.

The Ride Planning Agent can suggest pickup/dropoff options, explain route confidence, and compare ride options. It cannot control the vehicle, override routing constraints, or guarantee arrival times.

The Pickup Safety Agent can recommend safer pickup points and explain why one location is better than another. It cannot suggest illegal stops, unsafe crossings, bike lanes, traffic lanes, or restricted areas.

The Safety Explanation Agent can explain vehicle behavior and safety constraints in simple language. It cannot make absolute safety guarantees, claim Waymo is always safer than human drivers, or reveal unsupported internal system logic.

The Support Escalation Agent can detect complaints, emergency language, pricing disputes, accessibility concerns, and repeated confusion. It cannot resolve serious incidents alone and must route them to human support.

The Feedback Agent can collect rider preferences and post-ride feedback. It cannot store or reuse sensitive personal information without consent.

Human approval is required for safety incidents, pricing disputes, accessibility escalations, legal-sensitive claims, changes to safety rules, and changes to reliability thresholds.

## Shadow AI Audit

| Tool | Owner | Risk Level | Decision |
|------|-------|-----------|----------|
| Unapproved AI chatbot for rider support responses | Support team | H | govern |
| Spreadsheet-based prompt testing for pickup explanations | Product team | M | govern |
| Personal AI note-taking tool used for ride feedback summaries | Operations team | M | govern |

**Total tools found:** 3  
**Tools after triage:** 3  
**Estimated hidden spend:** $1,500/month

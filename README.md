-# My AI Product Strategy
+# Waymo Mobility Copilot — AI Product Strategy
 
-> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS your strategy — version-controlled, board-ready, portable.
+> Board-ready AI product strategy for an AI-powered ride planning assistant that strengthens Waymo’s direct rider relationship, improves booking confidence, and protects Waymo from becoming a commoditized autonomous vehicle supplier inside third-party mobility platforms.
 
 ---
 
 ## Strategy at a Glance
 
-| Component | Module | Status | Key Artifact |
-|-----------|--------|--------|-------------|
-| **The Bet** | M1 | [ ] | `01-the-bet/` |
-| **The Moat** | M2 | [ ] | `02-the-moat/` |
-| **The Margin** | M3 | [ ] | `03-the-margin/` |
-| **The Contract** | M4 | [ ] | `04-the-contract/` |
-| **The Guardrails** | M5 | [ ] | `05-the-guardrails/` |
-| **The Pitch** | M6 | [ ] | `06-the-pitch/` |
+| Component | Module | Status | Key Artifact |
+|---|---:|---:|---|
+| **The Bet** | M1 | Complete | `01-the-bet/` |
+| **The Moat** | M2 | Complete | `02-the-moat/` |
+| **The Margin** | M3 | Complete | `03-the-margin/` |
+| **The Contract** | M4 | Needs hardening | `04-the-contract/` |
+| **The Guardrails** | M5 | Complete | `05-the-guardrails/` |
+| **The Pitch** | M6 | Needs completion | `06-the-pitch/` |
 
 ---
 
-## The Bet (M1)
+## Executive Summary
 
-**What we're building, for whom, why now.**
+**Product:** Waymo Mobility Copilot  
+**AI Value Archetype:** Copilot / Planner  
+**Target User:** Waymo riders planning autonomous rides  
+**Strategic Goal:** Increase rider trust, booking confidence, repeat usage, and direct demand ownership.
 
-- **Product:**
-- **AI Value Archetype:**
-- **Vulnerability Scores:** Moat __/5 · Data __/5 · Platform __/5
-- **Top Risk:**
-- **Confidence:** H / M / L
-- **Prototype:** [link]
-- **Kill Criteria:**
+Waymo Mobility Copilot is an AI-powered ride planning assistant that helps riders choose safer pickup points, understand route confidence, compare ride options, resolve uncertainty before booking, and feel more comfortable using autonomous rides.
 
-→ Details: [`01-the-bet/`](01-the-bet/)
+The strategic bet is not simply to add a chatbot to the Waymo app. The bet is to turn Waymo into a trusted autonomous mobility relationship layer, so riders open Waymo first instead of defaulting to Uber, Lyft, Google Maps, Apple Maps, Tesla, Zoox, or another mobility aggregator.
 
 ---
 
-## The Moat (M2)
+## The Bet
 
-**Why this won't get copied in 6 months.**
+**What we are building:**  
+An AI-powered ride planning assistant for Waymo riders that improves pickup confidence, route understanding, booking completion, and rider trust.
 
-- **Data Flywheel Score:** __/20
-- **Weakest Loop:**
-- **Competitive Position:** [describe axes + placement]
-- **Encroachment Defense:**
-- **Vendor Portability:** Ready / Partial / Locked
+**Bet in one sentence:**  
+Waymo can increase rider trust and booking confidence by using AI to recommend safer pickup points, explain route confidence, compare ride options, and guide passengers through the autonomous ride experience before they book.
 
-→ Details: [`02-the-moat/`](02-the-moat/)
+**Why now:**  
+Autonomous ride-hailing is moving from novelty to repeat transportation behavior. The company that owns rider demand, trip planning, pricing comparison, loyalty, and daily transportation habits will control the customer relationship.
 
----
+**Top risk:**  
+Waymo could lose the customer relationship if Uber, Lyft, Tesla, Zoox, or another platform owns rider demand, pricing comparison, loyalty, and daily transportation habits.
 
-## The Margin (M3)
+**Confidence:** Medium
 
-**Will this make money or bleed it?**
+**Prototype:**  
+Waymo Mobility Copilot clickable prototype
 
-- **Gross Margin (current):**
-- **Gross Margin (AI-adjusted):**
-- **Pricing Model:**
-- **Cascading Strategy:**
-- **Break-even at:**
+---
 
-→ Details: [`03-the-margin/`](03-the-margin/)
+## Falsifiable Hypothesis
+
+Waymo Mobility Copilot is valuable if it increases booking completion, reduces pickup-related confusion, lowers cancellation after pickup assignment, and improves rider confidence compared with the current Waymo booking flow.
+
+The bet is wrong if riders exposed to Copilot do not show measurable improvement in:
+
+- booking completion rate
+- cancellation rate after pickup assignment
+- pickup-related support contacts
+- post-booking confidence score
+- repeat rides within 30 days
+- likelihood to choose Waymo over traditional rideshare options
 
 ---
 
-## The Contract (M4)
+## Validation Plan
 
-**Why users will trust a probabilistic system.**
+**Pilot duration:** 2–4 weeks  
+**Audience:** Active Waymo riders in 1–2 launch cities  
+**Control:** Current Waymo booking flow  
+**Treatment:** Copilot-enabled ride planning flow
 
-- **Reliability Target:**
-- **Golden Dataset:** __ rows, __ adversarial
-- **Confidence UX:** [approach]
-- **HITL Architecture:**
-- **Failure Mode Coverage:**
+### Primary Metrics
 
-→ Details: [`04-the-contract/`](04-the-contract/)
+| Metric | Why It Matters |
+|---|---|
+| Booking completion rate | Shows whether Copilot increases confidence enough to complete the ride |
+| Cancellation rate after pickup assignment | Measures whether Copilot reduces uncertainty and failed intent |
+| Pickup-related support contacts | Shows whether guidance reduces confusion |
+| Post-booking confidence score | Measures perceived trust and clarity |
+| Repeat rides within 30 days | Measures whether Copilot changes rider behavior |
+
+### Secondary Metrics
+
+| Metric | Why It Matters |
+|---|---|
+| Recommendation acceptance rate | Measures usefulness of Copilot suggestions |
+| Pickup issue reports | Measures operational friction |
+| Support escalation rate | Measures confidence and reliability gaps |
+| Time to successful pickup | Measures whether Copilot improves real-world rider experience |
+| Waymo-first booking intent | Measures direct relationship strength |
 
 ---
 
-## The Guardrails (M5)
+## Kill Criteria
 
-**What breaks when this scales — and what compounds.**
+Stop or materially redesign the bet if, after a controlled pilot:
 
-- **Compounding System:** [describe feedback loops]
-- **Governance Posture:** [approach]
-- **Shadow AI Status:** __ tools found, __ triaged
-- **Agent Boundaries:**
-- **Regulatory Exposure:**
+- booking completion does not improve
+- cancellation after pickup assignment does not decrease
+- pickup-related support contacts do not decrease
+- rider confidence score does not improve
+- repeat ride rate within 30 days does not increase
+- hallucination rate exceeds the reliability contract threshold
+- unsafe pickup or unsupported safety guidance appears in production
+- riders still prefer traditional rideshare without engaging with Waymo’s pickup, route, trust, or reliability guidance
 
-→ Details: [`05-the-guardrails/`](05-the-guardrails/)
+---
 
----
+## The Moat
 
-## The Pitch (M6)
+**Data Flywheel Score:** 17/20  
+**Weakest Loop:** Preference Loop  
+**Vendor Portability:** Partial
 
-**How you get this funded, shipped, and adopted.**
+Waymo has a strong contextual moat because it owns real-world autonomous driving data, safety testing, city-specific operating knowledge, and rider-only robotaxi experience.
 
-- **Horizon 1 (Now):**
-- **Horizon 2 (Next):**
-- **Horizon 3 (Bet):**
-- **Board Narrative:** [1-sentence thesis]
-- **Key Metric:**
+The main defensibility gap is not autonomous driving data. The main gap is rider relationship data. Uber, Lyft, Google Maps, Apple Maps, Tesla, or Zoox can attack by owning trip discovery, price comparison, loyalty, and booking habit.
 
-→ Details: [`06-the-pitch/`](06-the-pitch/)
+### Key Data Flywheels
+
+| Loop | Status | Strategic Role |
+|---|---|---|
+| Correction Loop | Strong | Rider feedback and failed cases improve future ride guidance |
+| Safety Learning Loop | Strong | Edge cases and safety events improve policies and evaluations |
+| Domain Context Loop | Strong | City-specific operating knowledge improves future launches |
+| Network Loop | Developing | More riders improve fleet placement and utilization |
+| Preference Loop | Weakest | Rider preferences must compound into personalization and loyalty |
+
+### Preference Loop Fix
+
+Waymo should capture durable rider preference signals, including:
+
+- preferred pickup spots
+- walking-distance tolerance
+- comfort preferences
+- route preferences
+- accessibility needs
+- luggage or family needs
+- wait-time tolerance
+- late-night safety sensitivity
+- reasons for choosing or not choosing Waymo
+
+These signals should feed ride planning, pickup guidance, support, city operations, and future product recommendations.
+
+---
+
+## Competitive Threat
+
+### Primary Encroachment Threat
+
+**Attacker:** Uber or Lyft  
+**Attack vector:** Own autonomous ride demand through the existing ride-hailing app habit.  
+**Risk:** Waymo becomes the vehicle supplier while another platform owns the customer relationship.
+
+Uber does not need to beat Waymo’s autonomous driving technology immediately. It can make Waymo invisible by controlling rider demand, pricing, loyalty, trip discovery, and habit.
+
+### Defense
+
+Waymo should strengthen the direct rider relationship by making the Waymo app the default place to plan and book autonomous rides.
+
+This requires:
+
+- better pickup/dropoff confidence
+- personalized repeat trips
+- trust-building ride explanations
+- loyalty and habit formation
+- clear comparison against traditional rideshare
+- city-specific autonomous mobility expertise
+- direct rider preference capture
+
+---
+
+## The Margin
+
+**Current revenue model:** Trip-based ride fares  
+**AI pricing model:** Bundled basic assistant with future premium experimentation  
+**Estimated AI COGS:** Approximately $1.40 per active rider/month  
+**Cascading strategy:** Triage model by default, frontier model for complex or safety-sensitive cases, human review for high-risk interactions
+
+### AI Cost Model
+
+| Cost Category | Per Active Rider / Month | Notes |
+|---|---:|---|
+| Primary model inference | $0.35 | Normal trip planning, pickup explanations, route confidence |
+| Triage model inference | $0.08 | Simple ETA, pickup, safety FAQ, and route-summary requests |
+| Infrastructure | $0.45 | Backend, APIs, monitoring, maps integration, latency management |
+| Data/storage | $0.22 | Preferences, anonymized trip patterns, feedback, logs |
+| Human-in-the-loop | $0.30 | Edge cases, trust/safety complaints, quality audits |
+| **Total AI COGS** | **$1.40** | Estimated monthly AI cost per active rider |
+
+### Pricing Decision
+
+The Copilot should launch as a bundled feature inside the Waymo ride experience, not as a standalone paid subscription.
+
+The primary value is:
+
+- higher booking conversion
+- lower cancellation
+- lower pickup confusion
+- stronger retention
+- higher rider trust
+- better vehicle utilization
+- stronger direct demand ownership
+
+Premium AI features should remain an experimental future option until willingness-to-pay is validated among high-frequency riders, commuters, business travelers, accessibility-sensitive riders, family users, or account-based use cases.
+
+### Break-even Logic
+
+Mobility Copilot is economically attractive if it creates more value than its estimated AI COGS by:
+
+- helping an active rider take one additional Waymo ride per month
+- reducing cancellations
+- reducing support contacts
+- improving pickup success
+- increasing repeat usage
+- improving utilization
+
+---
+
+## The Contract
+
+Waymo Mobility Copilot is safety-sensitive. It must behave less like a casual chatbot and more like a governed rider-confidence system.
+
+### Reliability Targets
+
+| Metric | Target | Alert Threshold |
+|---|---:|---:|
+| Golden dataset pass rate | >= 95% | < 92% |
+| Hallucination rate | <= 2% | > 3% |
+| p95 latency | <= 2.5 seconds | > 3.5 seconds |
+| Drift velocity | <= 5% degradation month-over-month | > 8% degradation |
+
+### Golden Dataset Status
+
+**Current state:** 5 rows  
+**MVP target:** 300–500 cases  
+**Production target:** 1,000+ cases
+
+The current golden dataset covers important early cases, including unsafe pickup requests, nervous riders, pricing confusion, longer-route explanations, and risky pickup behavior. However, it needs significant expansion before the product is credible for safety-sensitive use.
+
+### Required Coverage Expansion
+
+The golden dataset should cover:
+
+- pickup ambiguity
+- unsafe pickup requests
+- late-night or low-visibility pickup
+- pricing confusion
+- pricing disputes
+- ETA uncertainty
+- route explanation
+- airport pickup
+- accessibility needs
+- nervous first-time riders
+- scary ride reports
+- emergency language
+- refund requests
+- unsupported safety claims
+- internal routing hallucination
+- out-of-service-area requests
+- adversarial prompt injection
+
+### Confidence UX
+
+| Confidence Level | User Experience |
+|---|---|
+| High confidence | Give a direct recommendation with a short rationale |
+| Medium confidence | Show uncertainty, explain assumptions, offer safer alternatives |
+| Low confidence | Do not guess; explain uncertainty and route to support |
+
+### Human-in-the-Loop Path
+
+Human support steps in when a rider reports:
+
+- fear
+- scary ride experience
+- unsafe pickup
+- near miss
+- accessibility issue
+- pricing dispute
+- emergency language
+- repeated confusion
+- low-confidence safety-sensitive interaction
+
+Escalation path:
+
+```txt
+AI assistant -> support fallback -> human support specialist -> safety, billing, accessibility, or legal review
+```
+
+---
+
+## The Guardrails
+
+### Governance Posture
+
+High-governance, safety-sensitive posture.
+
+| Cadence | Review |
+|---|---|
+| Daily | Automated golden-dataset run and safety-rule scan |
+| Weekly | Accuracy, hallucination, latency, escalation, and drift review |
+| Monthly | Product, safety, legal, support, and operations governance review |
+| Quarterly | External risk review for safety-sensitive claims, privacy, and regulatory exposure |
+
+### Agent Boundaries
+
+The assistant may:
+
+- plan rides
+- recommend safer pickup/dropoff points
+- explain route confidence
+- compare ride options
+- collect rider feedback
+- route support issues
+- personalize future ride guidance with consent
+
+The assistant must not:
+
+- control the vehicle
+- override autonomy
+- guarantee safety
+- guarantee arrival times
+- invent prices
+- promise refunds
+- recommend illegal pickup/dropoff behavior
+- resolve serious incidents without human review
+- make unsupported claims about autonomous driving performance
+
+### Escalation Triggers
+
+Escalate or route to human review when:
+
+- confidence is below 70% on a safety, pickup, accessibility, or route-confidence answer
+- rider reports fear, emergency, injury, harassment, feeling trapped, unsafe pickup, near miss, or scary ride
+- user raises a pricing dispute or refund request
+- user raises an accessibility concern
+- three repeated negative feedback signals appear on the same intent in one week
+- hallucination rate exceeds 3% in any 7-day golden-dataset window
+
+---
+
+## Compounding System
+
+Waymo Mobility Copilot should compound through five feedback loops:
+
+| Loop | Input | Output |
+|---|---|---|
+| Recursive Learning | Rider feedback, thumbs-down ratings, unsafe pickup reports, confusing explanations | Updated prompts, safer rules, better eval cases |
+| Rider Preference Learning | Frequent routes, pickup preferences, comfort settings, accessibility needs | Personalized ride recommendations and higher booking confidence |
+| City Context Transfer | Local road layouts, traffic rules, construction zones, airport behavior | Better launch playbooks and city-specific pickup guidance |
+| Network Intelligence | Demand patterns, vehicle availability, cancellation behavior | Better fleet placement, lower wait times, better utilization |
+| Safety Escalation Loop | Scary ride reports, near misses, emergency language, low-confidence answers | Human review, stricter guardrails, stronger reliability thresholds |
+
+### Eval Feedback Integration
+
+Every escalated case, low-confidence answer, support ticket, unsafe pickup concern, scary ride report, pricing dispute, accessibility issue, and repeated negative feedback pattern should be reviewed for inclusion in the golden dataset.
+
+A failed production case should become:
+
+1. a labeled failure record
+2. a regression test
+3. a policy or prompt update if needed
+4. a release-blocking eval if safety-sensitive
+
+---
+
+## Shadow AI Audit
+
+| Tool / Behavior | Owner | Risk Level | Decision |
+|---|---|---:|---|
+| Unapproved AI chatbot for rider support responses | Support | High | Govern |
+| Spreadsheet-based prompt testing for pickup explanations | Product | Medium | Govern |
+| Personal AI note-taking tool for ride feedback summaries | Operations | Medium | Govern |
+
+**Total tools found:** 3  
+**Tools after triage:** 3  
+**Estimated hidden spend:** $1,500/month
+
+### Product Signal
+
+Shadow AI activity suggests that teams already need better tools for:
+
+- rider support responses
+- pickup explanation testing
+- feedback summarization
+- trust and safety triage
+
+These are not just governance risks. They are product signals that Mobility Copilot is addressing a real internal and rider-facing workflow need.
+
+---
+
+## Roadmap
+
+### Horizon 1 — Now: 0–3 Months
+
+| Initiative | Metric | Confidence |
+|---|---|---|
+| Pilot Copilot in booking flow | Booking completion, cancellation rate, confidence score | Medium |
+| Expand golden dataset to 300–500 cases | Eval pass rate, hallucination rate, safety-rule failures | High |
+| Instrument pickup confusion and support-contact events | Pickup issue rate, support contacts per ride | High |
+| Add measurable product kill criteria | Pilot decision quality | High |
+
+### Horizon 2 — Next: 3–9 Months
+
+| Initiative | Metric | Confidence |
+|---|---|---|
+| Build rider preference profile | Repeat rides, accepted recommendations, saved pickup usage | Medium |
+| Add city-specific pickup intelligence | Pickup success, reduced confusion, lower cancellations | Medium |
+| Integrate support escalation workflow | Resolution time, escalation accuracy, CSAT | Medium |
+| Improve feedback-to-eval pipeline | Failed case reuse, regression coverage | High |
+
+### Horizon 3 — Bet: 9–18 Months
+
+| Initiative | Metric | Confidence |
+|---|---|---|
+| Personalized autonomous mobility assistant | LTV, rides/month, Waymo-first booking share | Medium |
+| Premium membership experiment | Willingness-to-pay, retention, margin per heavy user | Low |
+| Multi-city autonomous mobility intelligence layer | Launch quality, utilization, direct demand share | Medium |
+
+---
+
+## Board Pitch
+
+### Thesis
+
+Waymo Mobility Copilot turns Waymo from a robotaxi service into a trusted autonomous mobility relationship layer, improving rider confidence, repeat usage, and direct demand ownership before aggregators commoditize autonomous vehicle supply.
+
+### The Case
+
+1. **Why now:**  
+   Autonomous ride-hailing is becoming a repeat mobility behavior, and the platform that owns trip planning and rider confidence will own demand.
+
+2. **What is defensible:**  
+   Waymo has proprietary autonomous driving data, city context, safety experience, and rider-only robotaxi feedback. The Copilot becomes more defensible as it captures pickup confidence, rider preferences, support outcomes, and city-specific trip intelligence.
+
+3. **The economics:**  
+   The assistant adds modest AI COGS but can create material value through higher conversion, lower cancellation, lower support burden, better utilization, and stronger retention.
+
+### The Risks
+
+1. **Trust / failure modes:**  
+   Unsafe pickup guidance, unsupported safety claims, invented prices, or poor escalation could damage trust.
+
+2. **Scale / governance:**  
+   Quality, latency, cost, and drift must be governed as usage grows.
+
+3. **Competitive:**  
+   Uber, Lyft, Tesla, Zoox, Google Maps, Apple Maps, or another platform could own demand and make Waymo a backend AV supplier.
+
+### The Ask
+
+Fund a controlled pilot, evaluation expansion, instrumentation layer, and safety-governed Copilot launch path.
+
+Near-term funding should prioritize:
+
+- booking-flow pilot
+- golden dataset expansion
+- confidence UX
+- support escalation integration
+- pickup confusion instrumentation
+- rider preference profile foundation
+
+---
+
+## Biggest Open Questions
+
+1. Does Copilot measurably increase booking completion versus the existing Waymo booking flow?
+2. Does it reduce cancellation after pickup assignment?
+3. Do riders trust AI guidance more than static UX improvements?
+4. Which rider segments benefit most: commuters, first-time riders, late-night riders, accessibility-sensitive riders, airport/event users, or frequent riders?
+5. Is there willingness to pay for advanced personalization, or should Copilot remain fully bundled?
+6. Can Waymo operationalize feedback from Copilot across product, support, safety, mapping, city operations, and autonomy teams?
+
+---
+
+## Current Strategy Strength
+
+**Overall strength:** 3.1/5
+
+The strategy is coherent and strategically relevant, but it needs stronger validation, larger reliability coverage, clearer unit economics by segment, and a more complete roadmap.
+
+### Biggest Risk
+
+The product becomes a polished AI chatbot around existing ride-booking pain points instead of a measurable driver of booking conversion, cancellation reduction, rider trust, repeat usage, and direct Waymo loyalty.
+
+### Top 3 Next Actions
+
+1. Run a 2–4 week rider pilot measuring booking completion, cancellation, pickup confusion, support contacts, trust score, and repeat rides.
+2. Expand the golden dataset from 5 cases to 300–500 MVP cases across safety, pricing, accessibility, emergency, pickup, and route-explanation scenarios.
+3. Complete the board-facing roadmap and instrument the product so every Copilot interaction can be tied to conversion, trust, support, and retention outcomes.

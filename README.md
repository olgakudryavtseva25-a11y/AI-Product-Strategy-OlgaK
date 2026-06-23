# My AI Product Strategy

> A living strategy built across 6 sessions. Each module adds one component. By Module 6, this repo IS your strategy — version-controlled, board-ready, portable.

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

- **Product:** Waymo Mobility Copilot — an AI-powered ride planning assistant for Waymo riders
- **AI Value Archetype:** Copilot / Planner
- **Vulnerability Scores:** Moat 4/5 · Data 5/5 · Platform 3/5
- **Top Risk:** Waymo could lose the customer relationship if Uber, Lyft, Tesla, Zoox, or another platform owns rider demand, pricing comparison, loyalty, and daily transportation habits.
- **Confidence:** M
- **Prototype:** [Waymo Mobility Copilot prototype](https://chatgpt.com/s/t_6a2864f8bf648191b467465556062f34)
- **Kill Criteria:** Stop the bet if AI recommendations do not increase rider trust, improve booking confidence, reduce pickup confusion, reduce cancellations, lower support contacts, or make riders more likely to choose Waymo over traditional rideshare options.

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

- **Data Flywheel Score:** 17/20
- **Weakest Loop:** Preference Loop
- **Competitive Position:** Waymo has a strong contextual moat and data advantage because it owns real-world autonomous driving data, safety testing, city-specific operating knowledge, and rider-only robotaxi experience. Its platform exposure is medium because Uber, Lyft, Tesla, and Zoox can attack through customer relationships, vehicle networks, pricing comparison, or competing autonomous platforms.
- **Encroachment Defense:** Strengthen the direct rider relationship by capturing rider preferences, improving pickup/dropoff quality, personalizing repeat trips, building trust features, and making the Waymo app the default place to book autonomous rides.
- **Vendor Portability:** Partial

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

- **Gross Margin (current):** Ride-fare margin depends on trip price, fleet utilization, vehicle operations, maintenance, city operations, and support costs.
- **Gross Margin (AI-adjusted):** Positive if model cascading keeps AI COGS near $1.40 per active rider/month and Mobility Copilot increases repeat rides, reduces cancellations, lowers support contacts, and improves vehicle utilization.
- **Pricing Model:** Hybrid: usage-based ride fares, bundled basic AI assistant, and a future premium personalization layer only after willingness-to-pay is validated.
- **Cascading Strategy:** Use a cheaper triage model by default for simple pickup, ETA, route, safety FAQ, and comfort questions. Escalate to a frontier model for complex, ambiguous, personalized, or safety-sensitive cases. Use human review for incidents, complaints, accessibility issues, pricing disputes, or low-confidence outputs.
- **Break-even at:** Break-even if Mobility Copilot helps an active rider take even one additional Waymo ride per month, prevents enough cancellations, reduces support costs, or improves utilization enough to exceed the estimated $1.40 monthly AI cost.

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

- **Reliability Target:** At least 95% golden dataset accuracy, no more than 2% hallucination rate, p95 latency no more than 2.5 seconds, and no more than 5% month-over-month drift.
- **Golden Dataset:** 5 rows, with adversarial coverage for unsafe pickup requests, nervous riders, pricing confusion, longer-route explanations, and risky pickup behavior. MVP target should be 300–500 cases before serious rollout.
- **Confidence UX:** Tiered confidence with human-in-the-loop trigger: high confidence gives a direct recommendation, medium confidence shows uncertainty and safer alternatives, and low confidence refuses to guess and routes to support.
- **HITL Architecture:** AI assistant -> support fallback -> human support specialist -> safety, billing, accessibility, or legal review when needed.
- **Failure Mode Coverage:** Covers unsafe pickups, unsupported safety claims, invented prices, internal routing hallucinations, emergency language, accessibility concerns, scary ride reports, pricing disputes, and late-night low-visibility pickup risks.

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

- **Compounding System:** Waymo compounds through recursive learning, rider preference learning, city context transfer, network intelligence, and safety escalation loops.
- **Governance Posture:** High-governance, safety-sensitive posture with daily golden-dataset checks, weekly reliability reviews, monthly cross-functional governance, and quarterly external risk review.
- **Shadow AI Status:** 3 tools found, 3 triaged
- **Agent Boundaries:** Agents can plan rides, recommend safer pickup points, explain route confidence, collect feedback, and route support issues. They cannot control the vehicle, override autonomy, guarantee safety, invent prices, promise refunds, recommend illegal pickup behavior, or resolve serious incidents without human review.
- **Regulatory Exposure:** High, because the product supports a safety-sensitive autonomous mobility experience and must avoid unsupported safety claims, preserve auditability, protect privacy, and maintain human escalation paths.

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

- **Horizon 1 (Now):** Pilot Copilot in the booking flow, expand the golden dataset, instrument pickup confusion and support-contact events, and add measurable product kill criteria.
- **Horizon 2 (Next):** Build rider preference profiles, add city-specific pickup intelligence, integrate support escalation workflows, and improve the feedback-to-eval pipeline.
- **Horizon 3 (Bet):** Build a personalized autonomous mobility assistant, test premium membership only after willingness-to-pay is validated, and develop a multi-city autonomous mobility intelligence layer.
- **Board Narrative:** Waymo Mobility Copilot turns Waymo from a robotaxi service into a trusted autonomous mobility relationship layer, improving rider confidence, repeat usage, and direct demand ownership before aggregators commoditize autonomous vehicle supply.
- **Key Metric:** Booking completion lift, cancellation reduction, pickup-related support contact reduction, rider confidence score, and repeat rides within 30 days.

→ Details: [`06-the-pitch/`](06-the-pitch/)

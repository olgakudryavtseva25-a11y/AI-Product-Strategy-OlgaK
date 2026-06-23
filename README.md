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

| Field | Answer |
|-------|--------|
| **Product** | Waymo Mobility Copilot — an AI-powered ride planning assistant for Waymo riders |
| **AI Value Archetype** | Copilot / Planner |
| **Vulnerability Scores** | Moat 4/5 · Data 5/5 · Platform 3/5 |
| **Top Risk** | Waymo could lose the customer relationship if Uber, Lyft, Tesla, or Zoox own rider demand, pricing comparison, loyalty, and daily transportation habits |
| **Confidence** | M |
| **Prototype** | [Waymo Mobility Copilot prototype](https://chatgpt.com/s/t_6a2864f8bf648191b467465556062f34) |
| **Kill Criteria** | Stop the bet if AI recommendations do not increase rider trust, improve booking confidence, reduce pickup confusion, or make riders more likely to choose Waymo over traditional rideshare options |

→ Details: [`01-the-bet/`](01-the-bet/)

---

## The Moat (M2)

**Why this won't get copied in 6 months.**

| Field | Answer |
|-------|--------|
| **Data Flywheel Score** | 17/20 |
| **Weakest Loop** | Preference Loop |
| **Competitive Position** | Waymo has a strong contextual moat and data advantage because it owns real-world autonomous driving data, safety testing, city-specific operating knowledge, and rider-only robotaxi experience. Its platform exposure is medium because Uber, Lyft, Tesla, and Zoox can attack through customer relationships, vehicle networks, or competing autonomous platforms |
| **Encroachment Defense** | Strengthen the direct rider relationship by capturing rider preferences, improving pickup/dropoff quality, personalizing repeat trips, building trust features, and making the Waymo app the default place to book autonomous rides |
| **Vendor Portability** | Partial |

→ Details: [`02-the-moat/`](02-the-moat/)

---

## The Margin (M3)

**Will this make money or bleed it?**

| Field | Answer |
|-------|--------|
| **Gross Margin current** | Ride-fare margin depends on trip price, fleet utilization, vehicle operations, maintenance, city operations, and support costs |
| **Gross Margin AI-adjusted** | Positive if model cascading keeps AI COGS near $1.40 per active rider/month and Mobility Copilot increases repeat rides, reduces cancellations, and improves vehicle utilization |
| **Pricing Model** | Hybrid: usage-based ride fares, bundled basic AI assistant, premium subscription layer for advanced personalization and priority support |
| **Cascading Strategy** | Use a cheaper triage model by default for simple pickup, ETA, route, safety FAQ, and comfort questions. Escalate to a frontier model for complex, ambiguous, personalized, or safety-sensitive cases. Use human review for incidents, complaints, accessibility issues, pricing disputes, or low-confidence outputs |
| **Break-even at** | Break-even if Mobility Copilot helps an active rider take even one additional Waymo ride per month, prevents enough cancellations, or improves utilization enough to exceed the estimated $1.40 monthly AI cost |

→ Details: [`03-the-margin/`](03-the-margin/)

---

## The Contract (M4)

**Why users will trust a probabilistic system.**

| Field | Answer |
|-------|--------|
| **Reliability Target** | ≥ 95% golden dataset accuracy, ≤ 2% hallucination rate, p95 latency ≤ 2.5 seconds, and ≤ 5% month-over-month drift |
| **Golden Dataset** | 5 rows, with adversarial coverage for unsafe pickup requests, nervous riders, pricing confusion, longer-route explanations, and risky pickup behavior |
| **Confidence UX** | Tiered confidence with human-in-the-loop trigger: high confidence gives a direct recommendation, medium confidence shows uncertainty and safer alternatives, low confidence refuses to guess and routes to support |
| **HITL Architecture** | AI assistant → support fallback → human support specialist → safety, billing, accessibility, or legal review if needed |
| **Failure Mode Coverage** | Covers unsafe pickups, unsupported safety claims, invented prices, internal routing hallucinations, emergency language, accessibility concerns, scary ride reports, pricing disputes, and late-night low-visibility pickup risks |

→ Details: [`04-the-contract/`](04-the-contract/)

---

## The Guardrails (M5)

**What breaks when this scales — and what compounds.**

| Field | Answer |
|-------|--------|
| **Compounding System** | Waymo compounds through recursive learning, rider preference learning, city context transfer, network intelligence, and safety escalation loops |
| **Governance Posture** | High-governance, safety-sensitive posture with daily golden-dataset checks, weekly reliability reviews, monthly cross-functional governance, and quarterly external risk review |
| **Shadow AI Status** | 3 tools found, 3 triaged |
| **Agent Boundaries** | Agents can plan rides, recommend safer pickup points, explain route confidence, collect feedback, and route support issues. They cannot control the vehicle, override autonomy, guarantee safety, invent prices, promise refunds, recommend illegal pickup behavior, or resolve serious incidents without human review |
| **Regulatory Exposure** | High, because the product supports a safety-sensitive autonomous mobility experience and must avoid unsupported safety claims, preserve auditability, protect privacy, and maintain human escalation paths |

→ Details: [`05-the-guardrails/`](05-the-guardrails/)

---

## The Pitch (M6)

**How you get this funded, shipped, and adopted.**

| Field | Answer |
|-------|--------|
| **Horizon 1 Now** | Launch Mobility Copilot v1 for pickup guidance, route confidence, basic safety answers, and post-ride feedback capture. Expand the golden dataset and implement model cascading |
| **Horizon 2 Next** | Build a unified rider preference profile, personalize frequent trips, connect feedback across product/safety/support/operations, and test premium membership features |
| **Horizon 3 Bet** | Turn Waymo into a personalized autonomous mobility platform that learns rider habits, trust concerns, preferred pickup spots, comfort needs, and city-specific travel patterns |
| **Board Narrative** | Waymo should use AI to turn autonomous rides from a one-time transportation transaction into a personalized mobility experience that increases trust, reduces pickup friction, improves repeat usage, and protects the direct rider relationship from Uber, Lyft, Tesla, and Zoox |
| **Key Metric** | Repeat booking rate among AI-assisted riders, supported by cancellation reduction, pickup success rate, AI COGS, golden dataset accuracy, and direct Waymo app usage |

→ Details: [`06-the-pitch/`](06-the-pitch/)

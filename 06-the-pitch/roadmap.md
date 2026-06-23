# Three-Horizon Roadmap & Board Pitch

## Roadmap

### Horizon 1 — Now (0-3 months)
*Quick wins. Ship with existing capabilities.*

| Initiative | Metric | Confidence |
|-----------|--------|------------|
| Launch Waymo Mobility Copilot v1 for pickup guidance, route confidence explanations, basic safety answers, and post-ride feedback capture | ≥ 70% of AI-assisted bookings complete without support escalation; p95 response latency ≤ 2.5 seconds | H |
| Add safety and trust cases to the golden dataset, including unsafe pickups, nervous riders, longer routes than Uber, pricing confusion, and late-night pickup concerns | Golden dataset accuracy ≥ 95%; hallucination rate ≤ 2%; no unsafe pickup recommendations | H |
| Capture structured rider preference signals after each trip, including preferred pickup spots, wait-time tolerance, comfort needs, accessibility needs, and reasons for choosing or not choosing Waymo | ≥ 40% post-ride feedback completion among AI-assisted riders; preference profile created for repeat riders | M |
| Implement triage-to-frontier model cascading for Mobility Copilot interactions | 80% triage model / 15% frontier model / 5% human review; AI COGS ≤ $1.40 per active rider/month | H |


### Horizon 2 — Next (3-9 months)
*Bets. Requires new capabilities or integrations.*

| Initiative | Metric | Confidence |
|-----------|--------|------------|
| Build a unified rider preference profile used across ride planning, pickup recommendations, support, accessibility, and future trip suggestions | +10% repeat booking rate among riders with saved preferences; -15% cancellation rate from pickup confusion | M |
| Personalize frequent routes, airport rides, commute flows, and preferred pickup/dropoff points inside the Waymo app | ≥ 20% of repeat riders use a saved route or saved pickup preference; booking time reduced by 25% | M |
| Connect rider feedback, support tickets, golden-dataset failures, and city operations data into one shared feedback pipeline | 100% of high-risk rider complaints reviewed weekly by product, safety, support, and operations | M |
| Launch premium membership experiments with saved preferences, priority support, personalized planning, and advanced route explanations | ≥ 5% conversion among high-frequency riders; premium revenue offsets incremental AI and support cost | M |

### Horizon 3 — Bet (9-18 months)
*Moonshots. High uncertainty, high potential.*


| Initiative | Metric | Confidence |
|-----------|--------|------------|
| Turn Waymo from a robotaxi app into a personalized autonomous mobility platform that learns each rider’s habits, trust concerns, comfort needs, and city-specific travel patterns | +20% rider retention; +15% rides per active rider; stronger direct app usage versus Uber/Lyft comparison behavior | M |
| Use city-context transfer to make every Waymo launch faster, safer, and more personalized from day one | New-city launch playbook reused across markets; reduced time from pilot to scaled service | M |
| Build a defensive direct-rider relationship layer against Uber, Lyft, Tesla, and Zoox by combining trust, safety, personalization, loyalty, and exclusive city partnerships | Lower platform dependency; increased share of rides booked directly through Waymo app | M |
| Expand Mobility Copilot into a proactive travel assistant that recommends when to ride, where to meet, how to avoid unsafe pickup friction, and which ride option best matches user preferences | +10% utilization improvement in priority zones; measurable reduction in failed pickups and support tickets | L |


## Board Pitch

**Thesis (1 sentence):**

Waymo should use AI to turn autonomous rides from a one-time transportation transaction into a personalized mobility experience that increases trust, reduces pickup friction, improves repeat usage, and protects the direct rider relationship from Uber, Lyft, Tesla, and Zoox.

**The case:**

1. Why now:  
Waymo already has strong autonomy, safety data, city experience, and a working robotaxi service, but the customer relationship is still vulnerable. Uber and Lyft can attack by owning demand, pricing comparison, loyalty, and the rider habit. Mobility Copilot helps Waymo make the Waymo app the preferred starting point for autonomous transportation.

2. What's defensible:  
Waymo’s defensibility comes from proprietary autonomous driving data, city-specific operating knowledge, safety experience, pickup/dropoff intelligence, and rider trust signals. The next defensible layer should be rider preference data: preferred pickup spots, comfort settings, wait-time tolerance, accessibility needs, route preferences, and reasons riders choose Waymo over other options.

3. The economics:  
The AI layer is inexpensive compared with ride revenue and fleet operations. Estimated AI COGS is about $1.40 per active rider/month when using model cascading. If Mobility Copilot helps a rider take even one additional Waymo ride per month, reduces cancellations, or improves vehicle utilization, the feature should create more value than it costs.

**The risks:**

1. Trust / failure modes:  
The assistant could recommend a pickup point that is technically legal but feels unsafe, especially at night or in low-visibility areas. It could also overstate safety, invent prices, explain internal routing logic inaccurately, or fail to escalate scary ride reports and accessibility concerns. These risks require a golden dataset, confidence thresholds, human escalation, and strict safety boundaries.

2. Scale / governance:  
Waymo must prevent rider feedback from staying siloed inside product or support. Safety, operations, mapping, autonomy, legal, and city launch teams need access to structured feedback and failed evaluation cases. Governance should include daily golden-dataset checks, weekly reliability reviews, monthly cross-functional governance, and quarterly external risk review.

3. Competitive:  
Uber is the most immediate platform threat because it already owns rider demand, app habit, loyalty, and pricing comparison. Tesla is a longer-term vertical threat because of its vehicle network, manufacturing scale, and driver data. Zoox is an adjacent robotaxi threat backed by Amazon’s capital and logistics capabilities. Waymo’s defense is to strengthen direct rider loyalty, personalization, pickup quality, and trust.

**The ask:**

Approve a 9-month investment to launch and scale Waymo Mobility Copilot as a bundled AI layer inside the Waymo app. The investment should fund rider preference infrastructure, golden-dataset expansion, model cascading, human escalation workflows, city feedback pipelines, and premium membership experiments. Success should be measured by repeat booking rate, cancellation reduction, pickup success, AI COGS, reliability metrics, and direct Waymo app usage.

## M1 Baseline vs. Now
*Your 3-sentence AI strategy from Module 1 vs. what you'd say now:*

**M1 baseline:**

Waymo should use AI to make autonomous rides easier to understand and more comfortable for riders. The assistant should help users choose pickup points, understand routes, and feel more confident before booking. The main goal is to increase trust in driverless rides.

**Now:**

Waymo should use AI not only as a ride assistant, but as a strategic moat around the direct rider relationship. Mobility Copilot should capture and compound rider preferences, improve pickup safety, reduce cancellations, personalize repeat trips, and defend Waymo against Uber’s platform advantage. The product should be bundled into the core ride experience at launch, controlled through model cascading and reliability governance, and later monetized through premium personalization and membership benefits.

# Cost Curve & Pricing Strategy

## Cost Model

| Cost Category | Per-User/Month | Notes |
|--------------|----------------|-------|
| Inference (primary model) |$0.35 |Used for normal trip planning, pickup/dropoff explanations, route confidence summaries, and rider support prompts. Most user interactions are short and structured, so cost should stay low. |
| Inference (cascading/triage) |$0.08 |A cheaper triage model handles simple requests like ETA explanation, pickup instructions, safety FAQs, and route summaries before escalating complex cases. |
| Infrastructure |$0.45 |Includes backend services, APIs, monitoring, logging, maps integration, latency management, and reliability infrastructure for real-time ride planning. |
| Data/storage |$0.22 |Stores rider preferences, anonymized trip patterns, pickup/dropoff feedback, safety-related interaction logs, and personalization signals. |
| Human-in-the-loop |$0.30 |Used for reviewing edge cases, trust/safety complaints, unusual rider feedback, and model quality audits. |
| **Total AI COGS** |$1.40 |Estimated monthly AI cost per active rider using the Mobility Copilot feature. |

## Cascading Strategy
<!-- Cheap model → frontier model routing logic -->

**Triage model:**
A small, low-cost model that handles simple rider-facing tasks:
Explaining pickup location
Summarizing route options
Answering basic safety and comfort questions
Confirming accessibility or luggage needs
Explaining wait time or ETA changes
**Frontier model:**
A stronger model used for complex, ambiguous, or safety-sensitive cases:
Confusing pickup/dropoff situations
Rider anxiety or trust concerns
Multi-step trip planning
Unusual route tradeoffs
Edge-case explanations
Complaints or high-risk support messages
Personalized recommendations for frequent riders
**Routing rule:**
Use the triage model by default. Escalate to the frontier model when:
The user asks a complex “why” or “what should I do” question.
The pickup/dropoff location has safety or accessibility complexity.
The rider expresses fear, confusion, or loss of trust.
The model confidence score is below the accepted threshold.
The interaction includes a complaint, refund request, or incident-related language.
**Expected cascade ratio:**
80% triage model
15% frontier model
5% human-in-the-loop review
This ratio protects margins because most Waymo Mobility Copilot interactions are predictable and structured. The frontier model is reserved for moments where better reasoning directly improves trust, safety perception, or booking conversion.

## Pricing Model

**Current pricing:**
Waymo’s current ride pricing is trip-based. The price depends on factors such as minimum fare, distance, trip length, and the most direct route. This means Waymo currently monetizes mainly through per-ride fares, similar to ride-hailing, instead of charging directly for AI features.
**Proposed AI pricing:**
Waymo should not charge a separate fee for every AI interaction at launch. The Mobility Copilot should be bundled into the ride experience because its main purpose is to increase trust, conversion, repeat usage, and rider retention.
Recommended AI pricing structure:
Free basic AI assistant for all riders
Pickup guidance
Route confidence explanation
Safety explanation
Basic ride comparison
Post-ride feedback capture
Premium AI features inside a membership plan
Preferred pickup spots
Personalized comfort settings
Faster booking flow for frequent routes
Priority support
More detailed route planning
Saved commute and airport preferences
Operational pricing upside
Use AI to reduce failed pickups
Reduce rider cancellations
Increase repeat rides
Improve vehicle utilization
Shift riders toward better pickup points and lower-friction routes
**Model:** seat-based / usage-based / outcome-based / hybrid
Hybrid
Waymo should use a hybrid pricing model:
Usage-based for the core ride fare
Subscription-based for premium rider benefits
Outcome-based internally by measuring whether AI improves booking conversion, rider retention, pickup success, and utilization
The AI feature should be treated less like a standalone chatbot and more like a margin-improving product layer.
## Stress Tests

| Scenario | Impact on Margin | Response |
|----------|-----------------|----------|
| Inference costs 3x |AI COGS increases from about $1.40 to roughly $3.00–$3.50 per active user/month. This hurts margins but does not destroy the model because the assistant is still cheap compared with ride revenue and fleet operations. |Tighten routing rules, reduce frontier model calls, cache common answers, use templates for pickup explanations, and limit expensive reasoning to safety-sensitive or high-value rides. |
| Heaviest segment doubles |Frequent riders and complex trip planners create more AI usage, more personalization storage, and more support escalation. Margin declines if these users do not also generate more ride revenue. |Move heavy users into a paid membership tier. Offer premium AI planning, saved preferences, and priority support as part of subscription pricing. Use usage caps or fair-use rules for expensive AI features. |
| Model provider raises prices 50% |Per-user AI cost rises, especially for frontier model calls. The biggest risk is dependency on one model provider. |Use model abstraction, negotiate volume discounts, maintain backup providers, move common tasks to smaller models, and keep Waymo-specific routing/evaluation logic in-house. |

## Board One-Pager
<!-- Before/After: Old SaaS revenue vs. AI usage revenue for your product -->

**Before (traditional SaaS):**
Before (traditional SaaS / traditional ride-hailing logic)
Waymo’s business is mainly monetized through ride fares. The user opens the app, sees a price, books a ride, and pays for transportation from point A to point B. The product value is safety, autonomy, convenience, and novelty.
Revenue logic:
Revenue increases when riders book more trips.
Margin improves when vehicle utilization improves.
Pricing power depends on availability, wait time, safety perception, and comparison with Uber/Lyft.
Customer relationship risk is high because platforms like Uber can own demand and make Waymo only the autonomous vehicle supplier.
Main weakness:
Waymo can have strong autonomous driving technology but still lose rider loyalty if another platform owns the booking habit, pricing interface, and customer relationship.
**After (AI-enabled):**
With Waymo Mobility Copilot, the product becomes more than a robotaxi. It becomes an intelligent mobility assistant that helps riders plan, trust, and repeat autonomous rides.
AI-enabled revenue logic:
AI improves booking confidence.
AI reduces cancellations caused by confusing pickup/dropoff points.
AI captures rider preferences over time.
AI increases repeat usage by making Waymo feel personalized.
AI helps Waymo defend the direct rider relationship against Uber, Lyft, Tesla, and Zoox.
AI creates a path to premium membership through saved preferences, priority planning, and personalized ride experiences.

**Net margin shift:**
Expected margin effect: Positive, if inference is controlled through cascading.
The AI feature adds about $1.40 per active user/month in estimated AI COGS, but it can create more value than it costs if it increases ride frequency, reduces cancellations, and improves rider retention.
Margin logic
If the AI assistant helps one active rider take even one additional Waymo ride per month, the incremental revenue should exceed the AI cost. The feature is especially attractive because the AI layer is relatively cheap compared with the fixed and operational costs of autonomous vehicles.
Strategic conclusion
Waymo should use AI pricing defensively and offensively.
Defensively, Mobility Copilot protects Waymo from becoming only a vehicle supplier inside Uber or Lyft. It strengthens the direct rider relationship by giving users a reason to open Waymo first.
Offensively, Mobility Copilot gives Waymo a path to premium pricing. The more the assistant learns rider preferences, pickup habits, comfort needs, and trust concerns, the more Waymo can turn autonomous rides into a personalized mobility product instead of a commodity ride-hailing option.
Final recommendation:
Bundle the basic AI assistant into every ride, use cascading to protect margins, and monetize advanced personalization through a premium membership tier.

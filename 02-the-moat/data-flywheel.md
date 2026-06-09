# Data Flywheel Map

> Score each loop 1-5. Your weakest loop is where competitors attack first.
> The four loops below are the M2 starting point - adapt if your product has 2 or 6 loops instead of 4.

## Flywheel Loops

## Flywheel Loops

| Loop | What It Measures | Score 1 | Score 5 | Score |
|------|------------------|---------|---------|-------|
| **Correction** | Does Waymo capture real-world driving mistakes, edge cases, disengagements, and safety-critical events, then reuse them to improve the autonomous driver? | No capture of mistakes or edge cases | Automated retraining and validation from real-world autonomous miles | 5/5 |
| **Preference** | Does Waymo learn rider preferences such as pickup spots, wait times, comfort expectations, route choices, and trust signals over time? | Stateless rider experience with no personalization | Deep personalization that makes Waymo the default transportation choice | 3/5 |
| **Domain Context** | Does Waymo learn city-specific traffic patterns, road layouts, regulations, weather, construction, and local driving behavior that improve future launches? | Siloed learning by city with little transfer | Cross-city operational and driving knowledge transfer | 5/5 |
| **Network** | Does each new rider, trip, and vehicle improve fleet placement, coverage, wait times, and service reliability for everyone? | Isolated rides with no fleet-level learning | Strong network effects across riders, vehicles, and service areas | 3/5 |

### Correction Loop - 4/5
**What you capture today:** Real-world rider-only autonomous driving data: routes, traffic behavior, pickup/dropoff patterns, disengagements, and edge cases from live robotaxi rides.
**How it compounds:** More rides create more proprietary driving data, which improves Waymo Driver performance and safety, making the service more reliable and easier to expand to new cities.


### Preference Loop - 5/5
**What you capture today:** Safety-critical events, near misses, unusual road situations, construction zones, pedestrian and cyclist behavior, and system mistakes.
**How it compounds:** Every difficult scenario becomes training and validation data. Waymo can fix weaknesses, test the updated driver in simulation, and reduce future errors faster than competitors with less real-world exposure.

### Preference Loop - 3/5
**What you capture today:** Rider preferences around pickup points, wait times, comfort, route choices, trip frequency, and trust in driverless rides.
**How it compounds:** Better understanding of rider behavior helps Waymo improve the user experience, increase repeat usage, and optimize where and when vehicles should be available.

### Domain Context Loop - 5/5
**What you capture today:** City-specific driving patterns, local road layouts, traffic rules, construction behavior, weather conditions, and regulatory requirements.
**How it compounds:** Each city teaches Waymo how to launch and operate in the next one. This creates operational knowledge that competitors cannot easily copy without years of deployment.


### Network Loop - 3/5
**What you capture today:** Supply and demand patterns between riders, vehicles, service areas, and high-traffic locations.
**How it compounds:** As more riders use Waymo, the company can place vehicles more efficiently, reduce wait times, and improve utilization. However, the network effect is still developing because Waymo is not yet available everywhere.


**Total Flywheel Score: 20/25**
**Weakest Loop:** Preference Loop
**Fix for weakest loop:** Waymo should capture more rider feedback after trips and personalize the experience, such as preferred pickup spots, comfort settings, route preferences, and reasons why users choose or do not choose Waymo over Uber, Lyft, or driving themselves.

---

## Encroachment Threat Assessment

### 1. Platform Encroachment
**Attacker:** Uber or Lyft  
**Vector:** They already own the rider demand, app habit, pricing interface, and marketplace relationship. They could integrate autonomous vehicles from multiple partners and make Waymo just one supply option inside their platform.  
**Time-to-threat:** 2-3 years  
**% of value at risk:** 35%


### 2. Vertical Competitor
**Attacker:** Tesla  
**Vector:** Tesla owns the vehicle hardware, manufacturing scale, driver data from millions of cars, and a direct consumer brand. If Tesla solves autonomy well enough, it could launch a cheaper robotaxi network without Waymo’s expensive sensor stack.  
**Time-to-threat:** 3-5 years  
**% of value at risk:** 45%

### 3. Adjacent Expansion
**Attacker:** Amazon / Zoox  
**Vector:** Zoox can enter robotaxis from a different angle: purpose-built autonomous vehicles, logistics expertise, and Amazon’s capital. Amazon could also use autonomy first in delivery, then expand into passenger transportation.  
**Time-to-threat:** 4-6 years  
**% of value at risk:** 25%

---

## 90-Day Encroachment Plan

*Your partner played the Big Tech attacker. What was their plan to kill you?*

**Attacker:** Uber

**Attack vector (target the weakest loop):** Target Waymo’s Preference Loop by owning the customer relationship. Uber does not need to beat Waymo’s autonomous driving technology immediately; it can make Waymo invisible by controlling rider demand, trip discovery, pricing, loyalty, and habit.

**Weeks 1-4 - what they ship:** Uber launches an “Autonomous Ride” option inside the app in selected cities, partnering with multiple AV providers. It offers discounts, clear ETAs, safety messaging, and loyalty points to make users try driverless rides through Uber instead of downloading Waymo.

**Weeks 5-8 - how they poach users:** Uber targets high-frequency riders with cheaper autonomous rides, airport/hotel partnerships, and bundled Uber One benefits. It uses its existing data to identify routes where riders are most likely to accept an AV ride and captures feedback after every trip.

**Weeks 9-12 - why users don't come back:** Users do not return to Waymo because Uber is already their default transportation app. Uber gives them more coverage, mixed human + autonomous supply, loyalty rewards, and one place to compare price and wait time. Waymo becomes only the vehicle provider, not the customer-facing product.

**Your defense:** Waymo should strengthen its direct rider relationship. It should improve loyalty, personalization, pickup/dropoff experience, trust-building safety features, and exclusive city partnerships. Waymo also needs to capture more rider preference data so the product becomes more than “a safe autonomous ride” — it becomes the preferred daily transportation experience.

# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|---------------|------------|----------------|
| **Provider** | Waymo depends on Alphabet funding, vehicle partners like Hyundai, sensor suppliers, mapping infrastructure, and city/regulatory approvals. | M | Identify the top 3 external dependencies and create backup options for vehicle supply, sensors, and city operations. |
| **Abstraction** | Waymo’s core autonomy stack is proprietary, but parts of the business still depend on external hardware, cloud infrastructure, and automotive manufacturing partners. | M | Document which parts of the stack are fully owned vs. partner-dependent, then define interfaces that make partner replacement easier. |
| **Routing** | Waymo controls its own rider app and dispatch system, but demand could be routed through platforms like Uber or Lyft if partnerships become too important. | M | Strengthen direct rider acquisition and make sure Waymo can grow without depending on third-party ride-hailing platforms. |
| **Eval** | Waymo has strong internal safety testing, simulation, and real-world validation, but external regulators and public trust still influence launch speed. | L | Maintain independent safety benchmarks, publish clear safety results, and prepare city-specific approval evidence in advance. |

## Portability Score

**Portability Score: 3/5**

Waymo has strong control over its core autonomous driving technology, safety data, and rider experience. However, the business is not fully portable because it depends on vehicles, sensors, fleet operations, city approvals, and capital-intensive deployment.

## If [primary vendor] doubles pricing tomorrow:

If a key sensor, vehicle, or infrastructure vendor doubles pricing tomorrow, Waymo’s margins and expansion speed would suffer. The immediate response should be to pause non-critical expansion, renegotiate volume-based pricing, and shift future fleet plans toward alternative suppliers or more standardized vehicle platforms.

## If [primary vendor] ships a competing product:

If a major partner, such as Hyundai, Uber, or a sensor supplier, ships a competing autonomous mobility product, Waymo should protect its core advantage: the Waymo Driver, proprietary safety data, and direct rider relationship. Waymo should reduce dependence on that partner, limit data sharing, strengthen exclusive partnerships, and prioritize direct-to-consumer growth through the Waymo app.

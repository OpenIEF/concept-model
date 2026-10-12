# Specification Areas

IEF has **six complementary areas**. They specialise the [common concepts](MODEL.md) without redefining their meaning. A participant can use more than one area; it need not implement every area.

| Area | Responsibility | Boundary |
|---|---|---|
| **Infrastructure** | Shared facilities, operating conditions, availability, and capacity. | Does not imply a central infrastructure controller. |
| **Spatial** | Places, connectivity, positions, reference frames, and spatial restrictions. | A location or route does not itself confer access or a reservation. |
| **Robot** | A native robotic entity, capabilities, reported state, intended behaviour, and actions. | Does not depend on VDA5050, MassRobotics, or a specific fleet manager. |
| **Device** | Physical equipment, sensors, actuators, and represented or passive devices. | Does not assume that every device is remotely controllable. |
| **Service** | Offered outcomes, accountable providers, requests, and human, machine, software, or hybrid fulfilment. | An offering is not a performer or execution instance. |
| **Security** | Identity, authentication, delegated authority, and authorisation across interactions. | Permission is not a guarantee of physical safety or task completion. |

**Shared concepts stay shared.** For example, a loading bay can be a Spatial place, an Infrastructure resource, and a location relevant to a Service. These are relationships to one identified subject, not incompatible copies of it.

Control and awareness apply wherever useful. A sensor might publish only State. An elevator might expose State, Capabilities, and Actions. A delivery Service can describe its progress even when a person performs the work. Neither needs to implement robot-specific behaviour.

The manifesto's **Semantic, Interoperability, Conformance, and Implementation** layers apply to all six areas. Area-specific schemas, protocols, precision rules, and operating requirements belong in the separate Specifications repository.

**Terminology note:** Service is the proposed generalisation of *Digital Service* in the canonical manifesto; acceptance of that amendment remains a separate governance decision.

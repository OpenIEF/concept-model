# External Standards and Adapters

IEF defines native concepts first. An **adapter** connects an external standard or specification to those concepts without making the external standard a dependency of IEF.

An adapter is a mapping boundary, not a required central gateway. It may be implemented by a robot, device, controller, service, or separate software. A participant may use multiple adapters while retaining one approved IEF identity.

## Contribution of existing standards

| Standard | Relevant contribution | Conceptual integration |
|---|---|---|
| **VDA5050** | Robot orders, actions, operational state, and coordination behaviour. | Informs native Robot control and shared Action, Event, State, Intent, and Spatial semantics. |
| **MassRobotics AMR Interoperability** | Robot identity, capability and operational awareness, including reported and anticipated movement. | Informs native Robot awareness and shared State (including explicitly qualified predictions) and Spatial semantics. A destination may express Intent when the source establishes it as a goal. Awareness does not imply a command interface. |
| **Other standards** | Any independently defined environment, participant, device, or service behaviour. | Map to the applicable core concepts and specification areas without replacing their definitions. |

The same underlying ideas can be useful beyond robots. For example, reporting state applies to a door, and requesting an action applies to an elevator or a service provider. Robot-specific representations remain within their source-specific mappings.

## Mapping principles

An adapter describes, at minimum, **the source specification and revision, translation direction, identity correspondence, supported concepts, assumptions, and semantic losses**. It must preserve material differences in units, reference frames, time, authority, action lifecycle, and available control capabilities.

Unsupported behaviour must be disclosed, not guessed. Identically named fields are not necessarily equivalent. A predicted route is not a reservation, an action acknowledgement is not completion, and a read-only source must not acquire control capabilities through translation.

Implementations that combine multiple sources require explicit authority and conflict-handling policies. Authentication of an adapter does not automatically authenticate the upstream origin.

This repository specifies **the relationship between IEF and other standards**, not detailed field mappings or adapter software. Version-pinned mappings, interface bindings, conformance, and executable implementations belong in the separate Specifications repository.

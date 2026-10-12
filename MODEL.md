# Core Concept Model

The model consists of **nine common concepts**. They describe meaning, not nine mandatory software objects or network messages.

| Concept | Meaning |
|---|---|
| **Entity** | Anything with a distinguishable identity in an environment. |
| **Capability** | An ability an entity can provide under stated conditions; not permission or current availability. |
| **State** | An attributed description of an entity's condition at a stated time, identified as reported, observed, or predicted. |
| **Intent** | An actor's stated aim or plan for future behaviour; not a prediction, permission, or commitment. |
| **Action** | An operation that can be requested, with an identifiable target and possible outcome. |
| **Event** | Something reported to have occurred, including action progress, results, and faults. |
| **Resource** | An entity or capacity that can be used, reserved, or allocated under an applicable authority. |
| **Relation** | A typed association between identified entities, such as *located in*, *connected to*, or *provided by*. |
| **Service** | An offered activity or outcome, independently of how or by whom it is fulfilled. |

## Roles, not extra core concepts

An **actor** is an entity able to act or carry responsibility. People, organisations, software, and robots can be actors. A **space** is an entity representing a place or spatial scope; it is not automatically an actor. A device may act directly, be represented by another actor, or be passive.

A **service provider** is the actor responsible for an offered Service. A **performer** carries out a particular instance of work. The provider and performer may differ. An offered Service is not itself the provider or the work performed.

## Core relationships

- An entity **has capabilities** and **reported state**; an actor may **express intent**.
- An actor may **request or perform an action**; an event may report its outcome.
- An entity may **occupy a space**, **use a resource**, or **relate to another entity**.
- An actor may **offer a service**; one or more performers may **fulfil** a service request.
- A representative may speak for an entity only within its established authority.

Relationships use stable identities. Compact identifiers may be assigned within a known context, but have no meaning outside that context. The same real-world subject must not become conflicting entities merely because several standards describe it.

## Invariants

1. **Observation is not authority.** State retains its source, time, and whether it is observed, reported, or predicted. Disagreement is not silently resolved by the last report received.
2. **Possibility is not permission.** Capability does not grant authorisation; authorisation does not guarantee operational safety or availability.
3. **Plans are not forecasts or commitments.** Intent, predicted State, permission, and accepted reservation are distinct even when represented compactly.
4. **Requests are not results.** Receipt, acceptance, execution, and successful completion have different meanings.
5. **Service is independent of fulfilment.** Accepting a service request does not automatically mean a human performer has accepted an assignment.
6. **Meaning survives translation.** An adapter must not invent missing information, authority, control functions, or completion evidence.
7. **Minimal by default.** No concept requires every participant to expose every attribute, interaction, or implementation mechanism.

The separate Specifications repository defines concrete representations and the conditions under which these invariants become testable requirements.

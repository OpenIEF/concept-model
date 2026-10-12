# Interaction Concepts

IEF separates **awareness** (what participants can know) from **control** (what participants may request). Both are governed by applicable security and coordination rules.

## Four common interaction patterns

| Pattern | Meaning |
|---|---|
| **Read** | Request information about an identified subject or capability. |
| **Publish** | Make attributed state or intent available to authorised consumers. |
| **Invoke** | Request an identified action or service operation. |
| **Notify** | Report an event, decision, progress, or outcome. |

These are semantic patterns, **not prescribed message codes**. A participant supports only the patterns relevant to its declared capabilities. Discovery, subscription, batching, and transport-specific operations may be provided by implementations without becoming new core concepts.

## Meaning that must survive compact communication

- **Awareness:** Consumers must be able to interpret identity, subject, meaning, source, and freshness within the agreed communication context. Missing information is not a zero value or an implicit success.
- **Control:** An Invoke is not authorisation. A permitted action may be rejected because of operating conditions, capability limits, or safety interlocks.
- **Progress:** Receipt, acceptance, active execution, and completion are distinct outcomes. Acknowledgement alone cannot prove physical completion.
- **Coordination:** Availability, requested use, granted reservation, predicted occupancy, and actual occupancy are not interchangeable.
- **Human services:** Provider acceptance does not imply the assigned person's acceptance. Human fulfilment requires an appropriate independent acceptance mechanism; continuous personal tracking is not inherent to IEF.
- **Trust:** Live interactions require authenticated origin and applicable authorisation. A declared identifier is not proof of authentication; a gateway cannot silently upgrade an unverified source into a verified one.

## Minimal exchange principle

Only the information needed to preserve meaning must cross an interface. Stable descriptions can be discovered, provisioned, or cached rather than repeatedly transmitted. Changes can be reported without full state when both participants share a valid baseline. If that baseline is lost, an implementation must recover it rather than apply an ambiguous change.

No particular session model, JSON format, transport, central service, or binary encoding is mandatory at the conceptual level. The Specifications repository defines correlation, versioning, freshness, replay protection, resynchronisation, and constrained-device representations.

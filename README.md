# Interoperable Environment Framework: Concept Model

**Version:** 0.3.0-draft.1  
**Status:** Public assessment draft

The Interoperable Environment Framework (IEF) gives independently developed systems a common way to describe an environment, understand its participants, and interact with them. The environment, not any particular robot, platform, or standard, is the organising context.

**Minimalism is a property of the entire framework.** IEF defines only the shared meanings needed for interoperability. A participant implements only the concepts relevant to its role. The framework does not require a central server, common middleware, continuous connectivity, or a particular data encoding. Implementations should minimise processing, memory use, dependencies, and data transfer without losing required meaning, trust, or recoverability.

## Read this repository

| File | Purpose |
|---|---|
| [MODEL.md](MODEL.md) | Core concepts, roles, relationships, and invariants |
| [AREAS.md](AREAS.md) | The six complementary specification areas |
| [INTERACTIONS.md](INTERACTIONS.md) | Shared awareness, control, coordination, and security semantics |
| [ADAPTERS.md](ADAPTERS.md) | Connecting external standards without changing native IEF concepts |
| [model.json](model.json) | Machine-readable catalogue of the same conceptual definitions |

## Position in IEF

The **Manifesto** is maintained in a separate repository and establishes the framework's principles, four layers, and governance. This repository defines the common conceptual foundation. A separate **Specifications** repository is responsible for detailed architecture, data contracts, encodings, bindings, security mechanisms, and testable requirements.

The concept model applies across the manifesto's four layers: **Semantic, Interoperability, Conformance, and Implementation**. These are not software tiers. The six specification areas are not additional layers.

The model uses the proposed name **IEF Service** for services fulfilled by people, machines, software, or combinations of them. The canonical manifesto currently names **IEF Digital Service**. This conceptual extension is subject to a separate manifesto amendment; this repository does not amend the manifesto.

## Scope and interpretation

This repository defines **meaning and relationships**, not a wire protocol. `model.json` is a readable description of the conceptual model, **not a device payload or an implementation schema**. Its field names do not need to appear on the network. Small identifiers, compact binary encodings, dictionary-based discovery, and data-efficient recovery are matters for the Specifications repository.

The model is intended for independent technical assessment and as the baseline for subsequent specifications. It is not a claim of implementation conformance, certification, or endorsement of any referenced third-party standard.

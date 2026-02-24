# Mechanism Overview

PACTO defines four formal mechanisms for biocultural governance. These extend the [agentic-tokenomics](https://github.com/regen-network/agentic-tokenomics) mechanism framework (M001-M011) with participatory process patterns.

---

## m020: Biocultural Attestation

**Purpose:** Enable communities to make formal, verifiable claims about ecological and cultural health.

Biocultural attestations are claims that originate from community-defined indicators co-created through the PACTO Core Loop. Unlike conventional data attestation, m020 uses collective community attestation rather than individual agent staking, and supports dual verification: community voice assessment alongside scientific measurement.

**Extends:** M008 (Data Attestation Bonding)

---

## m021: Voice Agreement

**Purpose:** Formalize the PACTO Core Loop as a reproducible, verifiable mechanism.

Voice Agreement is PACTO's core mechanism — the methodology that supports community deliberation in producing formal ecological agreements. It encodes the full process: voice capture, agentic synthesis, community feedback, iterative refinement, and agreement generation. The mechanism processes human voice as the primary input and produces community-endorsed agreements as the output.

**Extends:** New mechanism (no direct agentic-tokenomics counterpart)

---

## m022: Living Contract

**Purpose:** Define adaptive ecological agreements with community-controlled amendment protocols.

Unlike fixed-term contracts, living contracts evolve over time as communities refine indicators, ecological conditions change, and relationships deepen. Amendment occurs through re-running the PACTO Core Loop for specific sections, ensuring that changes go through the same participatory process as the original agreement.

**Extends:** M009 (Service Provision Escrow)

---

## m023: Community Endorsement

**Purpose:** Provide a formal mechanism for communities to collectively validate, endorse, or reject PACTO outputs.

Community endorsement is the legitimacy gate — nothing in PACTO has authority without it. Unlike individual reputation scoring, m023 is always collective and always requires community assembly. It cannot be automated.

**Extends:** M010 (Reputation/Legitimacy Signaling)

---

## How They Work Together

```
Community Assembly (m021: Voice Agreement)
        |
        v
Indicator Co-Definition (m020: Biocultural Attestation)
        |
        v
Community Validation (m023: Community Endorsement)
        |
        v
Formal Agreement (m022: Living Contract)
        |
        v
Ongoing Monitoring + Amendment (m020 + m022 + m023)
```

---

*Detailed mechanism specifications including JSON schemas, data flows, and reference implementations are available to partners via the KOI Knowledge Commons. See [PARTNERS.md](../PARTNERS.md) for access information.*

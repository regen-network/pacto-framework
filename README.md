# PACTO

**Participatory Assembly & Co-creation Through Technology**

A framework for generating durable, community-authored ecological agreements using participatory assembly processes augmented by AI tooling.

---

## What PACTO Is

PACTO (from Spanish *pacto* — pact, agreement) transforms deliberative assembly conversations into formal agreements — conservation easements, ecological service contracts, and credit issuance terms that communities define on their own terms. While this implementation focuses on ecological agreements, the same methodology supports any deliberative democratic process.

PACTO is not a replacement for participatory rights — it is a methodology for implementing consent at the depth governance principles intend. Communities are the authors of agreement terms, not merely reviewers.

> Communities already have governance processes and cultural decision-making rituals. Rather than replacing those with outside legal and technical frameworks, PACTO instruments existing assembly processes with technology that makes them more legible, actionable, and contractually binding — while keeping the community's voice as the primary source of authority.

## Repository Structure

PACTO is organized as **core methodology** plus **context modules**:

```
pacto-framework/
├── core/           # Universal methodology — Core Loop, governance, evidence trail,
│                   # sovereign infrastructure, mechanisms, workflows
├── contexts/       # Context-specific implementations
│   └── indigenous-rights/  # Primary context: indigenous rights (Amazon Basin pilots)
├── concepts/       # Cross-cutting concepts (deliberative democracy)
└── reference/      # Glossary, SDG alignment
```

The `core/` contains the universal PACTO methodology applicable to any participatory governance context. The `contexts/` folder contains implementations grounded in specific governance traditions. PACTO's primary and most developed context module is **[indigenous rights](contexts/indigenous-rights/README.md)**, emerging from work with communities in the Amazon Basin.

## The Problems PACTO Addresses

| Problem | Description |
|---------|-------------|
| **The Implementation Gap** | Consent is an established principle, but implementation often falls short. Communities are presented with externally drafted agreements for sign-off rather than shaping the substance. PACTO provides methodology for full implementation. |
| **Organizational Capture** | Fragmented landscape of organization-driven projects creating intra-community competition, inconsistent commitments, and funding-cycle collapse. |
| **The Accessibility Challenge** | Meaningful participation requires sustained engagement. AI-augmented synthesis makes intensive assembly sessions more productive, increasing depth per session rather than compressing timelines. |
| **The Surveillance Inversion** | Most conservation technology watches communities. PACTO inverts this — technology serves communities, reflecting their own priorities in the agreements being created. |

Read more: [core/problems-addressed.md](core/problems-addressed.md) | [Indigenous rights framing](contexts/indigenous-rights/problems-addressed.md)

## The Core Loop

PACTO operates through a 6-step iterative process:

```
1. COMMUNITY ASSEMBLY
   The community convenes using its existing governance
   and decision-making processes.
        |
        v
2. VOICE-TO-TEXT CAPTURE
   Assembly proceedings transcribed in real-time.
   Primary source material of community voice.
        |
        v
3. AI-ASSISTED SYNTHESIS
   AI extracts themes, priorities, points of
   agreement and tension.
        |
        v
4. FEEDBACK PRESENTATION
   "This is what you just said about what you want."
   Community reviews, corrects, affirms.
        |
        v
5. ITERATIVE REFINEMENT
   Steps 1-4 repeat until community consensus.
   Threshold is community-defined.
        |
        v
6. AGREEMENT GENERATION
   Final synthesis becomes formal legal instruments
   rooted in community voice.
```

Read more: [core/core-loop.md](core/core-loop.md)

### The Evidence Trail

PACTO creates a transparent, verifiable record of the participatory process itself — not just the outcome. Funders and verifiers, and most importantly communities themselves can independently confirm that that deliberation happened, and that consent was genuine and informed. This turns the process itself into auditable evidence.

Read more: [core/evidence-trail.md](core/evidence-trail.md)

## Architecture

PACTO is a companion to [`regen-network/agentic-tokenomics`](https://github.com/regen-network/agentic-tokenomics), sharing infrastructure patterns while extending them for participatory contexts. It is part of the [Regen AI ecosystem](https://github.com/regen-network).

### Governance Layers

| Layer | Description | PACTO Context | Automation |
|-------|-------------|---------------|------------|
| **Layer 1** | Fully Automated | Ecological monitoring (satellite, IoT, baselines) | 100% |
| **Layer 2** | AI-Assisted + Oversight | AI-assisted agreement drafting, compliance checking | 85% |
| **Layer 3** | Human-in-Loop | Community assembly decisions (voice-first, Core Loop) | 50% |
| **Layer 4** | Constitutional | Community governance traditions. **Always human, always community-led.** | 0% |

### Mechanisms

PACTO uses four formal mechanisms to support community-led governance:

| Mechanism | Name | Description |
|-----------|------|-------------|
| **m020** | Biocultural Attestation | Community-authored claims and indicator attestation |
| **m021** | Voice Agreement | The Core Loop formalized: voice to synthesis to feedback to agreement |
| **m022** | Living Contract | Adaptive agreements with community-controlled amendment protocol |
| **m023** | Community Endorsement | Collective validation and endorsement by community assembly |

Read more: [core/mechanism-overview.md](core/mechanism-overview.md)

## Governance Principles

- **Community authorship** — communities define the terms, not just approve them
- **Voice-first participation** — oral tradition is the primary interface
- **Data sovereignty** — communities control their data
- **No extraction without reciprocity** — every use of community knowledge must add value for the community
- **Co-governance** — PACTO methodology evolves based on community and partner experience

Read more: [core/governance-principles.md](core/governance-principles.md) | [Indigenous rights grounding](contexts/indigenous-rights/governance-principles.md)

## Context Modules

### Indigenous Rights (Primary)

PACTO's most developed context module, grounded in UNDRIP, ILO Convention 169, and Sarayaku v. Ecuador. Active pilots with communities in the Amazon Basin.

Read more: [contexts/indigenous-rights/](contexts/indigenous-rights/README.md)

## Detailed Specifications

Detailed mechanism specifications, pilot documentation, technical schemas, and implementation guides are available to partners through the KOI Knowledge Commons. See [contexts/indigenous-rights/PARTNERS.md](contexts/indigenous-rights/PARTNERS.md) for access information.

## Quick Start

1. **Read** the [Core Loop](core/core-loop.md) to understand the 6-step process
2. **Explore** the [four problems](core/problems-addressed.md) PACTO addresses
3. **Review** the [governance principles](core/governance-principles.md) for participatory practice
4. **Check** the [glossary](reference/glossary.md) for key terminology
5. **Explore** the [sovereign infrastructure](core/sovereign-infrastructure.md) pathway for community-owned technology
6. **Browse** the [indigenous rights context](contexts/indigenous-rights/README.md) for the primary implementation pilot focus
7. **Join** the conversation on [forum.regen.network](https://forum.regen.network)

---

*PACTO is developed by [Regen Network Development PBC](https://regen.network) in partnership with communities and local implementation partners. This repository is part of the Regen AI ecosystem alongside [agentic-tokenomics](https://github.com/regen-network/agentic-tokenomics).*

# PACTO

**Proceso de Acuerdos y Co-Constitucion Tecnologicamente Organizada**
*Participatory Assembly & Co-creation Through Technology*

A framework for generating durable, community-authored ecological agreements using participatory assembly processes augmented by AI tooling.

---

## What PACTO Is

PACTO (from Spanish *pacto* — pact, agreement) transforms deliberative assembly conversations into formal agreements — conservation easements, ecological service contracts, and credit issuance terms that communities define on their own terms. This implementation is focused on ecological agreements, institutions, and contracts, however the same pipeline should be usable to support any deliberative democratic process.

PACTO is not a replacement for Free, Prior, and Informed Consent — it is a methodology for implementing consent at the depth international law intends. Communities are the authors of agreement terms, not merely reviewers.

> Communities already have governance processes and cultural decision-making rituals. Rather than replacing those with outside legal and technical frameworks, PACTO instruments existing assembly processes with technology that makes them more legible, actionable, and contractually binding — while keeping the community's voice as the primary source of authority.

## The Problems PACTO Addresses

| Problem | Description |
|---------|-------------|
| **The Implementation Gap** | FPIC is an established right, but implementation often falls short of what international law intends. Communities are presented with externally drafted agreements for sign-off rather than shaping the substance. PACTO provides methodology for full implementation. |
| **The NGO Industrial Complex** | Fragmented landscape of NGO-driven projects creating intra-community competition, inconsistent commitments, and funding-cycle collapse. |
| **The Accessibility Challenge** | Meaningful participation requires sustained engagement. AI-augmented synthesis makes intensive assembly sessions more productive, increasing depth per session rather than compressing timelines. |
| **The Surveillance Inversion** | Most conservation technology watches communities. PACTO inverts this — technology serves communities, reflecting their own desires in the contracts being created. |

Read more: [framework/problems-addressed.md](framework/problems-addressed.md)

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

Read more: [framework/core-loop.md](framework/core-loop.md)

### The Evidence Trail

PACTO creates a transparent, verifiable record of the participatory process itself — not just the outcome. Funders and verifiers can independently confirm that the community drove the agreement terms, that deliberation happened, and that consent was genuine and informed. This turns the process itself into auditable evidence.

Read more: [framework/evidence-trail.md](framework/evidence-trail.md)

## Architecture

PACTO is a companion to [`regen-network/agentic-tokenomics`](https://github.com/regen-network/agentic-tokenomics), sharing infrastructure patterns while extending them for biocultural participatory contexts. It is part of the [Regen AI ecosystem](https://github.com/regen-network).

### Governance Layers

| Layer | Description | PACTO Context | Automation |
|-------|-------------|---------------|------------|
| **Layer 1** | Fully Automated | Ecological monitoring (satellite, IoT, baselines) | 100% |
| **Layer 2** | AI-Assisted + Oversight | AI-assisted agreement drafting, compliance checking | 85% |
| **Layer 3** | Human-in-Loop | Community assembly decisions (voice-first, Core Loop) | 50% |
| **Layer 4** | Constitutional | Indigenous customary law. **Always human, always community-led.** | 0% |

### Mechanisms

PACTO uses four formal mechanisms to support community-led biocultural governance:

| Mechanism | Name | Description |
|-----------|------|-------------|
| **m020** | Biocultural Attestation | Community-authored biocultural claims and indicator attestation |
| **m021** | Voice Agreement | The Core Loop formalized: voice to synthesis to feedback to agreement |
| **m022** | Living Contract | Adaptive agreements with community-controlled amendment protocol |
| **m023** | Community Endorsement | Collective validation and endorsement by community assembly |

Read more: [reference/mechanism-overview.md](reference/mechanism-overview.md)

## Pilots

| Pilot | Location | Key Feature |
|-------|----------|-------------|
| **Siekopai Nation** | Ecuadorian Amazon | Community co-defined biocultural indicators for jaguar conservation |
| **Sharamentsa / Achuar** | Ecuadorian Amazon | Partner pilot with distinct community-led governance context |
| **Matses Nation** | Peruvian Amazon | ERA Brazil umbrella species method adapted with PACTO |
| **Salmon Nation** | Columbia River Basin (Cascadia) | Community-led salmon ecosystem health indicators |
| **ASHA** | Amazon Sacred Headwaters | Monitoring and evaluation framework for multilateral conservation fund |

Read more: [framework/pilot-overview.md](framework/pilot-overview.md)

## Governance Principles

PACTO provides methodology for implementing indigenous rights to self-determination and participatory governance, grounded in UNDRIP, ILO Convention 169, and regional jurisprudence including Sarayaku v. Ecuador (IACtHR, 2012):

- **Community authorship** — communities define the terms, not just approve them
- **Voice-first participation** — oral tradition is the primary interface
- **Data sovereignty** — communities control their data
- **Legal pluralism** — agreements valid under indigenous customary law, national law, and on-chain governance
- **No extraction without reciprocity** — every use of community knowledge must add value for the community

Read more: [framework/governance-principles.md](framework/governance-principles.md)

## Biocultural Credits

PACTO provides a verifiable methodology for documenting that biocultural credits genuinely reflect community participation and authorship. A credit earns "biocultural" status when it demonstrates both ecological outcomes and verified community authorship of agreement terms.

Read more: [concepts/biocultural-credits.md](concepts/biocultural-credits.md)

## Detailed Specifications

Detailed mechanism specifications, pilot documentation, technical schemas, and implementation guides are available to partners through the KOI Knowledge Commons. See [PARTNERS.md](PARTNERS.md) for access information.

## Quick Start

1. **Read** the [Core Loop](framework/core-loop.md) to understand the 6-step process
2. **Explore** the [four problems](framework/problems-addressed.md) PACTO addresses
3. **Review** the [governance principles](framework/governance-principles.md) for rights-grounded participatory practice
4. **Check** the [glossary](reference/glossary.md) for key terminology
5. **Explore** the [sovereign infrastructure](framework/sovereign-infrastructure.md) pathway for community-owned technology
6. **Join** the conversation on [forum.regen.network](https://forum.regen.network)

---

*PACTO is developed by [Regen Network Development PBC](https://regen.network) in partnership with indigenous communities and local implementation partners. This repository is part of the Regen AI ecosystem alongside [agentic-tokenomics](https://github.com/regen-network/agentic-tokenomics).*

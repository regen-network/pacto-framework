# Glossary / Glosario

**Status:** Living document — additions welcome via PR
**Languages:** English (EN), Spanish (ES), indigenous terms where documented

---

## PACTO-Specific Terms

| Term (EN) | Término (ES) | Definition |
|-----------|-------------|------------|
| **PACTO** | **PACTO** | Proceso de Acuerdos y Co-Constitución Tecnológicamente Organizada / Participatory Assembly & Co-creation Through Technology. Also *pacto* = agreement/pact in plain Spanish. |
| **Core Loop** | **Ciclo Central** | The 6-step PACTO process: Assembly → Voice Capture → AI-Assisted Synthesis → Feedback → Iterate → Agreement. |
| **Biocultural Attestation** | **Atestación Biocultural** | A formal, verifiable claim about ecological and cultural health originating from community-defined indicators (m020). |
| **Voice Agreement** | **Acuerdo de Voz** | The Core Loop formalized as a mechanism — transforms community voice into formal ecological agreements (m021). |
| **Living Contract** | **Contrato Vivo** | An adaptive ecological agreement that evolves over time under community control, connected to the "Living Treaty" concept (m022). |
| **Community Endorsement** | **Endoso Comunitario** | Collective validation by community assembly — the legitimacy gate for all PACTO outputs (m023). |
| **Evidence Trail** | **Rastro de Evidencia** | A verifiable record of the participatory process itself — MRV of participation, not just ecological outcomes. |
| **Biocultural Indicator** | **Indicador Biocultural** | A dual-source metric combining community-defined ecological knowledge with scientific measurement. Community assessment is authoritative when divergence occurs. |
| **Implementation Gap** | **Brecha de Implementación** | The gap between the right to Free, Prior, and Informed Consent as established in international law and how that right is implemented in practice — often reduced to procedural minimum compliance rather than the substantive participatory right it was designed to protect. |
| **Surveillance Inversion** | **Inversión de Vigilancia** | PACTO's design principle: technology serves communities (reflecting their desires in contracts) rather than watching them (monitoring compliance). |
| **Deliberative Accessibility** | **Accesibilidad Deliberativa** | PACTO's approach to making participatory processes more accessible by increasing the depth and quality of engagement per session through AI-augmented synthesis, rather than compressing timelines. |

## Governance Terms

| Term (EN) | Término (ES) | Definition |
|-----------|-------------|------------|
| **Community Assembly** | **Asamblea Comunitaria** | The primary deliberation body in PACTO. The community convenes using its existing governance and decision-making processes. |
| **Layer 1 (Automated)** | **Capa 1 (Automatizada)** | Fully automated ecological monitoring (satellite, IoT, remote sensing baselines). |
| **Layer 2 (AI-Assisted)** | **Capa 2 (Asistida por IA)** | AI-assisted agreement drafting, compliance checking, synthesis loops. ~85% automation with human oversight. |
| **Layer 3 (Human-in-Loop)** | **Capa 3 (Humano-en-Ciclo)** | Community assembly decisions via the Core Loop. ~50% automation. Voice-first. |
| **Layer 4 (Constitutional)** | **Capa 4 (Constitucional)** | Decisions governed by indigenous customary law and the full exercise of FPIC rights. Always human, always community-led. 0% automation. |
| **Legal Pluralism** | **Pluralismo Jurídico** | Agreements simultaneously valid under indigenous customary law, national law, and on-chain governance. |
| **Data Sovereignty** | **Soberanía de Datos** | Communities control where their data lives, who can access it, and can withdraw content at any time. |
| **FPIC** | **CLPI** | Free, Prior, and Informed Consent / Consentimiento Libre, Previo e Informado. An established collective right of indigenous peoples grounded in UNDRIP (Articles 19, 32), ILO Convention 169 (Articles 6, 15), and regional jurisprudence including Sarayaku v. Ecuador (IACtHR, 2012). PACTO provides methodology for implementing FPIC at the depth these instruments intend. |
| **UNDRIP** | **DNUDPI** | United Nations Declaration on the Rights of Indigenous Peoples (2007). Key provisions for PACTO: Article 3 (self-determination), Article 18 (participation in decision-making), Article 19 (FPIC), Article 26 (land rights), Article 31 (cultural heritage and traditional knowledge). |
| **ILO Convention 169** | **Convenio 169 de la OIT** | International Labour Organization Convention on Indigenous and Tribal Peoples (1989). Binding international treaty. Key provisions: Article 6 (consultation in good faith), Article 7 (right to decide development priorities), Article 15 (natural resource rights). |
| **Sarayaku v. Ecuador** | **Sarayaku c. Ecuador** | Inter-American Court of Human Rights judgment (2012) establishing that consultation with indigenous peoples must be prior, culturally appropriate, in good faith, and oriented toward consent. Litigated by Fundación Pachamama. A foundational precedent for PACTO's governance principles. |

## Sovereign Infrastructure Terms

| Term (EN) | Término (ES) | Definition |
|-----------|-------------|------------|
| **Sovereign Infrastructure** | **Infraestructura Soberana** | Technology infrastructure that communities can control, operate, and migrate — covering identity, data storage, and AI inference. A spectrum from commercially hosted to fully community-owned. |
| **Progressive Decentralization** | **Descentralización Progresiva** | The phased pathway from commercially hosted infrastructure (Phase 1) through hybrid (Phase 2), community-primary (Phase 3), to federated mesh (Phase 4). Core Loop remains constant across all phases. |
| **DID (Decentralized Identifier)** | **Identificador Descentralizado (DID)** | A cryptographic identifier that the holder controls without depending on a central authority. In PACTO, `did:plc` identifiers from AT Protocol provide portable, self-sovereign identity for assembly participants and communities. |
| **PDS (Personal Data Server)** | **Servidor de Datos Personal (PDS)** | An AT Protocol data store where a user or community controls their own data. In PACTO, community-run PDS instances store Evidence Trail records with community-defined access controls. |
| **Sovereign Inference** | **Inferencia Soberana** | Running AI models locally on community-controlled hardware so that sensitive data (voice transcripts, cultural knowledge) never leaves community infrastructure. Uses open models via Ollama, vLLM, or llama.cpp. |
| **Hypercert** | **Hipercertificado** | An on-chain impact claim (ERC-1155 token on Ethereum) that maps work scope, impact scope, and contributors. PACTO Evidence Trail records can serve as the verifiable backing for hypercert claims. |

## Technical Terms

| Term (EN) | Término (ES) | Definition |
|-----------|-------------|------------|
| **RID** | **RID** | Resource Identifier — KOI addressing format for PACTO objects. Pattern: `orn:pacto.<type>:<namespace>/<id>`. |
| **KOI** | **KOI** | Knowledge Organization Infrastructure — the semantic layer that indexes and federates PACTO knowledge. |
| **OPAL** | **OPAL** | Open Protocol for Aligned Localities — interoperability framework for knowledge commons nodes. |
| **KOI Partial Node** | **Nodo Parcial KOI** | A lightweight federation participant that publishes/subscribes to knowledge without running a full node. |
| **JSON-LD** | **JSON-LD** | JSON for Linked Data — the export format for KOI federation. |
| **MRV** | **MRV** | Monitoring, Reporting, and Verification — the standard framework for ecological credit validation. |
| **On-chain Anchoring** | **Anclaje en Cadena** | Using `regen.data.v1 MsgAnchor` to create an immutable, timestamped reference to PACTO process records on Regen Ledger. |
| **Content Hash** | **Hash de Contenido** | SHA-256 fingerprint of a PACTO object, used for immutable reference via on-chain anchoring. |

## Credit & Methodology Terms

| Term (EN) | Término (ES) | Definition |
|-----------|-------------|------------|
| **USS01** | **USS01** | Umbrella Species Stewardship credit class — primary credit class for Siekopai pilot. Composite index: USH + HQ + USpToC. |
| **USH** | **USH** | Umbrella Species Health — population and health metrics component of USS01. |
| **HQ** | **HQ** | Habitat Quality — ecosystem condition assessment component of USS01. |
| **USpToC** | **USpToC** | Umbrella Species Theory of Change — conservation intervention tracking component of USS01. |
| **BT01** | **BT01** | BioTerra credit class — Terrasos biodiversity units for restoration and preservation. |
| **ERA Brazil** | **ERA Brasil** | Umbrella species methodology framework used as the scientific complement in Siekopai pilot. |
| **Credit Class** | **Clase de Crédito** | On-chain definition of a type of ecological credit (e.g., carbon, biodiversity, umbrella species). |
| **PES** | **PSA** | Payment for Ecosystem Services / Pago por Servicios Ambientales. |

## Agent Personas

| Agent | Role | Description |
|-------|------|-------------|
| **AGENT-005** | PACTO Facilitator | Replaces the human "engine" routing between transcription, synthesis, and community. Multilingual, voice interface. |
| **AGENT-006** | Biocultural Monitor | Community-defined indicators + scientific/remote sensing. Links ecological monitoring to community governance. |
| AGENT-001 to 004 | Agentic Tokenomics Agents | Defined in [agentic-tokenomics](https://github.com/regen-network/agentic-tokenomics). PACTO agents extend this set. |

## Pilot-Specific Terms

| Term | Context | Definition |
|------|---------|------------|
| **TRK 149** | Siekopai | "Bosques para el Clima" — the Siekopai jaguar conservation project registered on Regen Registry. |
| **Plan de Vida** | Latin America | Life plan — a community governance document common across Latin American indigenous communities, used as a biocultural anchor for ecological and territorial governance. |
| **Yakum** | Siekopai | Local implementation partner for the Siekopai pilot. |
| **Fundación Pachamama** | Ecuador | Conservation and indigenous rights organization partnering on PACTO pilots. |
| **ASHA** | Amazon Basin | Amazon Sacred Headwaters Alliance — multilateral bioregional fund where PACTO serves as MEL framework. |


## Indigenous Language Notes

<!-- COMMUNITY-INPUT-REQUIRED -->

Indigenous language terms from Paicoca (Siekopai), Matsés, and Shuar are not included in this glossary because their inclusion requires community endorsement. Terms will be added as communities participate in the PACTO Core Loop and authorize their terminology for publication.

When indigenous language terms appear in pilot documentation, they are always accompanied by Spanish and English equivalents, with a note that the indigenous language term is the authoritative form.

---

*Contributions to this glossary are welcome. See [CONTRIBUTING.md](../CONTRIBUTING.md) for guidelines. For indigenous language terms, the Community Rights and Process Integrity checklist must be completed before publication.*

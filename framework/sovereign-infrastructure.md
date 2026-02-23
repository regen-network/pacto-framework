# Sovereign Infrastructure

PACTO's governance principles establish that communities control their data, their governance processes, and the terms of their ecological agreements. But governance principles without infrastructure pathways remain aspirational. This document maps the concrete technology pathway from commercially hosted infrastructure — where PACTO pilots operate today — to community-sovereign infrastructure, where communities own the identity, data, and AI systems that support their ecological governance.

This is a pragmatic roadmap, not a utopian manifesto. Using commercially hosted tools to prove the concept is valid and expected. The goal is expanding the option space for communities, not imposing infrastructure requirements.

---

## The Sovereignty Premise

PACTO's [governance principles](governance-principles.md) establish five data sovereignty commitments: community ownership, community-defined access, right to withdraw, storage self-determination, and no extraction without reciprocity. The [Surveillance Inversion](core-loop.md) — technology serves communities rather than watching them — is a design principle woven through the entire framework.

But these principles have an infrastructure dimension that goes beyond policy. When community voice recordings transit commercial transcription APIs, when AI synthesis runs on external servers, when identity lives on platform accounts — the surveillance inversion is incomplete. The technology may serve the community, but the infrastructure serves its operators.

This is not a criticism of the current approach. PACTO pilots use commercial tools because they work, they are available, and they allow the framework to prove itself without waiting for perfect infrastructure. The [Core Loop](core-loop.md) works the same whether it runs on cloud servers or community-owned hardware.

Sovereignty is a spectrum, not a binary:

| Dimension | Hosted (Phase 1) | Hybrid (Phase 2) | Community-Primary (Phase 3) | Federated (Phase 4) |
|-----------|------------------|-------------------|----------------------------|---------------------|
| **Identity** | Platform accounts | Portable DIDs alongside existing accounts | Self-issued, community-managed DIDs | Federated identity across communities |
| **Data Storage** | Cloud providers | Community PDS + cloud backup | Community-hosted data servers | Federated data network |
| **AI Inference** | Commercial APIs (Claude, GPT, Whisper) | Local for sensitive data, API fallback | Local-primary, API for specialized tasks | Community mesh inference |
| **Governance** | Platform policies | Hybrid on-chain + off-chain | On-chain + customary law | Federated DAO governance |

The path from left to right is optional, incremental, and community-directed. No community is required to move further than it chooses. A community that operates entirely in Phase 1 still benefits from the full PACTO process.

---

## Progressive Decentralization: The Four Phases

Progressive decentralization is the organizing framework for PACTO's infrastructure pathway. Each phase adds capability without removing what works. The [Core Loop](core-loop.md) — the 6-step process from assembly to agreement — remains constant across all phases. What changes is the degree to which communities control the infrastructure that supports that process.

### Phase 1: Prove the Concept (Current State)

This is where PACTO pilots operate today. It works.

- **Voice capture:** Commercial transcription services (Whisper API, Otter.ai)
- **AI synthesis:** Commercial language model APIs (Claude, GPT)
- **Data storage:** Cloud providers, local files
- **Identity:** Individual platform accounts, named signatories
- **On-chain anchoring:** Content hashes anchored via `regen.data.v1 MsgAnchor` — this already works regardless of where source data is stored

The [Evidence Trail](evidence-trail.md) functions at this phase because it relies on content hashes, not data residency. A transcript stored on a cloud server produces the same SHA-256 hash as one stored on community hardware. The on-chain anchor is indifferent to where the data lives.

**What communities control at this phase:** The entire participatory process. Assembly governance, consensus thresholds, indicator definitions, agreement terms — all of this is community-directed. Infrastructure sovereignty is low, but process sovereignty is full.

### Phase 2: Hybrid Infrastructure

The first step toward infrastructure sovereignty. Communities begin controlling the most sensitive parts of the pipeline while keeping commercial tools for tasks where sovereignty matters less.

- **Voice capture:** Local transcription (Whisper running on community hardware) for sensitive assembly content; commercial API for non-sensitive supplementary content
- **AI synthesis:** Local inference (Ollama + open models) for cultural knowledge synthesis; API fallback for complex multi-document tasks
- **Data storage:** Community-operated Personal Data Server (AT Protocol PDS) for Evidence Trail records; cloud backup optional
- **Identity:** Portable decentralized identifiers (AT Protocol DIDs) alongside existing accounts
- **On-chain anchoring:** Same as Phase 1 — content hashes on Regen Ledger

**What changes:** Community data for sensitive tasks no longer transits external servers. Community identity becomes portable — it can move between service providers without losing history or social connections.

**What stays the same:** The Core Loop. The Evidence Trail structure. The four mechanisms (m020-m023). The governance principles.

### Phase 3: Community-Primary Infrastructure

Communities run their own infrastructure as the default, using external services only when local capacity is genuinely insufficient.

- **Voice capture:** Community-owned transcription infrastructure
- **AI synthesis:** Local-primary with open models; API only for tasks exceeding local hardware capacity
- **Data storage:** Community-hosted PDS with community-controlled backups
- **Identity:** Fully portable, community-managed DIDs with optional Cosmos account linkage for on-chain operations
- **Governance:** On-chain governance (DAODAO or similar) integrated with customary law decision-making processes

**What changes:** The community controls the servers. Hardware maintenance, updates, and governance are community responsibilities (with support from technical partners as needed).

**What stays the same:** The Core Loop. The Evidence Trail. The mechanisms. The governance principles.

### Phase 4: Federated Community Mesh

Multiple communities operate interconnected infrastructure, enabling cross-community collaboration without central intermediaries.

- **Federation:** Communities share knowledge through KOI protocol without centralizing data
- **Mesh inference:** Communities contribute inference capacity to shared networks; language-specific models trained on community-authorized data serve multiple communities
- **Cross-community governance:** Federated DAO structures for shared ecological governance (watershed-level, bioregional coordination)
- **Identity:** Federated identity mesh — community members recognized across networks

**What changes:** Communities move from isolated sovereignty to networked sovereignty. ASHA (Amazon Sacred Headwaters Alliance) is an example of the governance scale this phase supports.

**What stays the same:** Everything about the Core Loop. Community authority over their own process. The fundamental principle that no community is required to share more than it chooses.

### What Changes at Each Phase (and What Doesn't)

| Component | Phase 1 | Phase 2 | Phase 3 | Phase 4 |
|-----------|---------|---------|---------|---------|
| **Core Loop process** | Same | Same | Same | Same |
| **Evidence Trail integrity** | Content hashes on-chain | Same + PDS storage | Same | Same + federated verification |
| **Community authority over process** | Full | Full | Full | Full |
| **Community authority over infrastructure** | Low | Partial (sensitive data) | High | High + networked |
| **Who controls the servers** | Service providers | Mixed | Community | Community mesh |
| **Data residency** | Provider-determined | Community choice (sensitive) | Community-determined | Community-determined + federation |

---

## Sovereign Identity

Identity in PACTO serves a specific function: it connects participants in the Evidence Trail to their contributions, enables community endorsement (m023) to carry verifiable authority, and allows facilitators and verifiers to be accountable to the process.

### AT Protocol Decentralized Identifiers

AT Protocol uses a dual identifier system well-suited to PACTO's needs:

- **Handle:** A human-readable name (like a domain name) that can change. A community might use `siekopai.pacto.regen.network` as its handle.
- **DID (Decentralized Identifier):** A permanent, cryptographic identifier that persists even if the handle changes. This is the stable reference used in Evidence Trail records.

The underlying DID method (`did:plc`) provides:

- **Cryptographic key hierarchy:** A signing key for day-to-day operations and rotation keys that remain under community control. If a service provider becomes untrustworthy, the community can unilaterally migrate its identity to a new provider.
- **Portability:** A community's identity — including its full history of attestations, endorsements, and Evidence Trail records — moves with it. No platform can hold a community's identity hostage.
- **Recovery:** If a signing key is compromised, rotation keys (held by the community, not the service provider) can issue new signing keys without losing identity continuity.

### How DIDs Map to PACTO Roles

| PACTO Role | Phase 1 (Current) | DID-Based (Phase 2+) | Cosmos Account |
|------------|-------------------|----------------------|----------------|
| **Community member** | Name in transcript | `did:plc:...` signing attestations | Optional |
| **Community representative** | Named signatory on agreements | `did:plc:...` with signing key authority | Required for on-chain governance |
| **Facilitator** | Named individual in Evidence Trail | `did:plc:...` attesting to process integrity | Optional |
| **External verifier** | Organization credential | `did:plc:...` or `did:web:...` | Required for on-chain verification |
| **Community (collective)** | Named entity | `did:plc:...` owned by governance structure | Required for credit class operations |

### Identity Bridge: DID to Cosmos Account

For operations that require on-chain presence (credit issuance, governance voting, marketplace participation), a DID can be linked to a Cosmos account:

1. The DID holder signs a message containing their Cosmos address
2. The Cosmos account signs a confirming transaction referencing the DID
3. The link is recorded on-chain and can be verified by any party

This bridge is **optional**. Communities that do not need on-chain operations can use DIDs without Cosmos accounts. The link can be established at any time when on-chain operations become relevant.

---

## Why AT Protocol (and Alternatives)

AT Protocol is PACTO's recommended sovereign data and identity layer. This choice is grounded in ecosystem alignment, not theoretical superiority — several organizations already building in the ecological crediting space are adopting or aligning with AT Protocol:

- **Ma Earth** — building ecological impact verification on AT Protocol infrastructure
- **Hypercerts** — impact certification with evaluation frameworks compatible with AT Protocol data models
- **Silvi.earth** — tree planting verification and monitoring
- **Gainforest** — AI-powered conservation with decentralized data verification

This ecosystem overlap means PACTO's data can be natively legible to these systems without translation layers.

### Protocol Comparison

AT Protocol is not the only option for sovereign data infrastructure. Communities should understand the alternatives:

| Dimension | AT Protocol | Ceramic / ComposeDB | Nostr | Solid Pods |
|-----------|------------|---------------------|-------|------------|
| **Identity** | `did:plc` — portable, cryptographic, recoverable | `did:pkh` — blockchain-linked | npub keys — simple but no recovery mechanism | WebID — web-based identity |
| **Data model** | Merkle trees, signed repositories | IPFS-linked data streams | Simple JSON events | RDF / Linked Data |
| **Federation** | PDS + Relay architecture | IPFS peer network | Relay network | Pod servers |
| **Schema system** | Lexicons — typed, versioned, globally defined | ComposeDB models (GraphQL) | NIPs — informal community specs | Shape Trees |
| **Ecosystem fit** | Ma Earth, Hypercerts, Silvi, Gainforest | DeSci community, Ceramic ecosystem | Social payments, micropayments | Academic research, EU data sovereignty |
| **Self-hosting** | PDS — moderate complexity | Ceramic node — high complexity | Relay — low complexity | Pod server — moderate complexity |
| **Maturity** | Production (Bluesky-scale deployment) | Production (smaller scale) | Production (social scale) | Research / early production |
| **Offline capability** | Repository can sync when connected | Requires IPFS connectivity | Relay-dependent | Pod-dependent |

### Why AT Protocol for PACTO

Three factors drive the recommendation:

1. **Ecosystem overlap:** The strongest concentration of ecological crediting organizations building on a single sovereign data protocol. PACTO Evidence Trail records would be natively legible to partner systems.

2. **Data sovereignty model:** AT Protocol's PDS architecture — where communities host their own data servers and maintain full portability — maps directly to PACTO's data sovereignty principles (community ownership, storage self-determination, right to withdraw).

3. **Schema compatibility:** AT Protocol Lexicons — typed, versioned schema definitions — map naturally to PACTO's structured Evidence Trail records. Each evidence layer and mechanism can be defined as a Lexicon, enabling semantic interoperability without ad-hoc translation.

Communities are not locked into this choice. The Evidence Trail's content-hash-based integrity model works with any storage backend. A community using Solid Pods or Ceramic for data storage can still anchor content hashes on Regen Ledger and participate in the PACTO ecosystem.

---

## Sovereign Data

AT Protocol's Personal Data Server (PDS) architecture provides a natural fit for PACTO's Evidence Trail storage and progressive disclosure model.

### How PDS Maps to Evidence Trail Storage

Each community (or community organization) operates a PDS instance — a data server that hosts a signed repository of records. The repository uses a Merkle Search Tree: a content-addressed data structure where every record mutation generates a new root hash, creating an append-only, verifiable history.

This maps directly to the Evidence Trail:

- Each Evidence Trail record type becomes a collection in the community's PDS repository
- Each record is cryptographically signed by the community's DID
- The repository's Merkle tree provides tamper-evident history without requiring blockchain storage
- Content hashes from PDS records are what get anchored on-chain via `regen.data.v1 MsgAnchor`

### PACTO Lexicons

AT Protocol uses Lexicons — globally defined schema specifications — to ensure different applications understand each other's data. PACTO would define Lexicons for its Evidence Trail layers and mechanisms:

| Lexicon ID | Maps To | Content |
|-----------|---------|---------|
| `network.regen.pacto.evidence.assembly` | Evidence Trail Layer 1 | Date, location, governance structure, participant count, facilitator DID |
| `network.regen.pacto.evidence.voiceCapture` | Evidence Trail Layer 2 | Audio content hash, transcript content hash, language, duration |
| `network.regen.pacto.evidence.synthesis` | Evidence Trail Layer 3 | Synthesis version, AI model used, provenance metadata |
| `network.regen.pacto.evidence.feedback` | Evidence Trail Layer 4 | Corrections, affirmations, rejections, signed by community representative DID |
| `network.regen.pacto.evidence.iteration` | Evidence Trail Layer 5 | Changes between synthesis versions, consensus tracking, structured diff records |
| `network.regen.pacto.evidence.agreement` | Evidence Trail Layer 6 | Final endorsed agreement content hash, endorsement attestations |
| `network.regen.pacto.mechanism.attestation` | m020 | Biocultural indicator claims with dual-source verification references |
| `network.regen.pacto.mechanism.endorsement` | m023 | Collective validation records signed by community assembly |

These Lexicons define what fields each record contains and what types they use, enabling any AT Protocol client to read and verify PACTO records without custom integration code.

### Progressive Disclosure via PDS Access Controls

The [Evidence Trail's progressive disclosure model](evidence-trail.md) maps to PDS access controls:

| Access Level | PDS Mechanism | What Is Visible |
|-------------|---------------|----------------|
| **Public** | Public lexicon records | Metadata: assembly dates, iteration count, endorsement status, content hashes |
| **Verified parties** | Authenticated read (DID-based) | Summary: themes, indicator lists, agreement type |
| **Authorized partners** | Scoped access tokens | Detail: synthesis outputs, feedback records |
| **Community only** | Private records | Full: audio recordings, raw transcripts, individual contributions |

Content hashes are always public — this enables anyone to verify data integrity without accessing the data itself. Full content requires community authorization, enforced at the PDS layer.

### Evidence Trail Data Flow (Phase 2+)

```
Community Assembly
       |
       v
Voice Capture (local transcription)
       |
       v
Community PDS Repository
  ├── pacto.evidence.assembly record
  ├── pacto.evidence.voiceCapture record (content hashes)
  ├── pacto.evidence.synthesis records (versions)
  ├── pacto.evidence.feedback records
  └── pacto.evidence.agreement record
       |
       v
Content Hash of each record
       |
       v
regen.data.v1 MsgAnchor (Regen Ledger)
  └── IRI pointing back to community PDS for resolution
```

The PDS serves as both storage and resolver: anyone with the IRI can resolve it to the PDS endpoint, and the PDS enforces access controls before serving content. The content hash on-chain proves the data has not been altered since anchoring.

### Storage Self-Determination

Consistent with the [governance principle](governance-principles.md) of storage self-determination, the PDS architecture supports multiple hosting models:

- **Hosted PDS:** A trusted partner (Regen Network, a regional NGO, a technical support organization) runs the PDS on behalf of the community. Easiest to start with.
- **Self-hosted PDS:** The community runs PDS software on its own hardware. Requires technical capacity or ongoing support.
- **Migration:** A community can move from hosted to self-hosted (or between hosts) at any time, retaining all data and identity. This is a core AT Protocol guarantee — the community's rotation keys enable unilateral migration.

---

## Sovereign Inference

PACTO's [Core Loop](core-loop.md) relies on AI at two critical steps: Step 2 (voice-to-text capture) and Step 3 (AI-assisted synthesis). These steps process community voice — assembly recordings, deliberation transcripts, cultural knowledge expressions. This data is among the most sensitive a community produces.

### Why Inference Sovereignty Matters

When community voice data is sent to commercial AI APIs:
- The data transits external servers operated by technology companies
- The companies' data handling policies, not the community's, govern what happens to that data
- Indigenous language recordings and cultural knowledge expressions pass through systems not designed for cultural sensitivity
- The community relies on continued API access — pricing changes, policy changes, or service discontinuation affect the process

Sovereign inference — running AI models on community-controlled hardware — addresses these concerns directly. It is not about distrust of specific providers; it is about ensuring the [Surveillance Inversion](core-loop.md) extends to the infrastructure layer.

### The Sovereign Inference Stack

Three open-source inference tools form the practical stack:

| Tool | Best For | Complexity | Resource Requirements |
|------|----------|------------|----------------------|
| **Ollama** | Getting started, single-machine deployment | Low — runs with a single command | 8-16GB RAM minimum |
| **llama.cpp** | Resource-constrained hardware, maximum control | Medium — C/C++, compile from source | Can run on 4GB RAM with small models |
| **vLLM** | Production deployments, multiple concurrent users | High — requires GPU, Kubernetes-capable | 16GB+ VRAM recommended |

**Open models suitable for PACTO tasks:**

| Model | Size | Strengths | PACTO Relevance |
|-------|------|-----------|-----------------|
| **Llama 3.x** | 8B-70B | Strong general reasoning, multilingual | Assembly synthesis, document analysis |
| **Mistral** | 7B-24B | Fast inference, strong reasoning | Low-latency feedback presentation |
| **Qwen** | 7B-72B | Leading multilingual capability | Spanish-English synthesis, non-English contexts |
| **Whisper** | Various | Speech-to-text, 100+ languages | Voice-to-text capture (Step 2) |

### Sensitivity Routing

Not all PACTO data requires local inference. Phase 2 uses sensitivity-based routing — sending sensitive data to local models and non-sensitive tasks to commercial APIs:

| Data Type | Sensitivity | Phase 1 | Phase 2 | Phase 3+ |
|-----------|------------|---------|---------|----------|
| Raw audio recordings | High | API (only option) | **Local** (Whisper) | Local |
| Assembly transcripts | High | API | **Local** | Local |
| Cultural knowledge synthesis | High | API | **Local** | Local |
| Agreement drafting | Medium | API | API with local review | Local with API fallback |
| Ecological data analysis | Low-Medium | API | API | Either |
| Public metadata generation | Low | API | API | Either |

The routing decision is simple: if the data contains community voice, cultural knowledge, or sensitive deliberation content, it routes to local inference. Everything else can use whichever path is more practical.

### Hardware Considerations

| Setup | Hardware | Cost (Approximate) | Capability |
|-------|----------|-------------------|------------|
| **Minimum viable** | Laptop, 16GB RAM, no GPU | Already owned by many orgs | 7B models via Ollama, slow but functional (2-5 tokens/sec) |
| **Recommended** | Desktop/server, 24GB GPU (RTX 4070 Ti) | $1,500-2,500 | 7-13B models at full speed (30-50 tokens/sec) |
| **Production** | Server, 48GB+ GPU | $3,000-5,000 | 70B models, multiple concurrent users |
| **Community cluster** | Multiple nodes, distributed | Varies | Redundancy, specialized models per task |

**Quantization** makes sovereignty practical: compression techniques (Q4_K_M) reduce model memory requirements by approximately 75% with minimal quality loss. A 7B parameter model that would normally require 14GB of memory runs in approximately 4GB when quantized.

### Offline Inference

Many PACTO pilot communities operate in areas with intermittent or no internet connectivity. The Amazon communities (Siekopai, Matses) often have limited satellite internet. Offline inference is not a future feature — it is a present requirement.

- **llama.cpp** runs entirely offline once a model is downloaded
- **Ollama** requires no network connection after initial model pull
- **Whisper** (local) performs speech-to-text without any connectivity
- Content hashes can be computed locally and anchored on-chain when connectivity is available

The pattern: record assembly audio locally, transcribe locally, synthesize locally, present feedback locally, and sync content hashes to PDS and on-chain when the community next has connectivity.

### Open Questions

- **Indigenous language support:** Open AI models have limited support for indigenous languages (Paicoca, Matsés, Shuar). Fine-tuning requires community-authorized training data and raises its own sovereignty questions.
- **Quality gap:** Commercial APIs currently outperform open models on complex multi-language synthesis. This gap is narrowing but remains relevant for tasks requiring nuanced cultural understanding.
- **Maintenance burden:** Community-owned hardware requires maintenance, updates, and troubleshooting. This cost must be accounted for, not hidden.

---

## Forward Compatibility: Interoperability Bridges

PACTO does not exist in isolation. Its Evidence Trail, governance structures, and credit outputs need to interoperate with the broader ecological crediting ecosystem. This section maps forward compatibility with five systems.

### Regen Ledger Data Module

**Status: Active integration, partially implemented**

The Regen Ledger Data Module is PACTO's primary on-chain anchoring layer. This integration is already operational in concept:

- **`regen.data.v1 MsgAnchor`** creates immutable, timestamped references to Evidence Trail records
- **IRI (Internationalized Resource Identifier)** generation produces resolvable addresses: `regen:<content-hash>.<extension>`
- **Resolver registry** enables off-chain data (in community PDS instances) to be discovered and verified through on-chain IRIs

How PACTO RIDs relate to Regen IRIs:
- PACTO uses RID addressing: `orn:pacto.<type>:<namespace>/<id>` for internal knowledge graph references
- Regen Data Module uses IRIs: `regen:<content-hash>.<extension>` for on-chain references
- Both point to the same underlying data; RIDs are semantic identifiers, IRIs are content-addressed identifiers

### Regen Claims Engine

**Status: Design phase**

The ecocredit module manages the full lifecycle of ecological credits. PACTO connects at two points:

1. **m020 (Biocultural Attestation) feeds credit class verification.** Community-defined indicators, verified through the dual-source process (community voice + scientific measurement), become inputs to credit class issuance decisions. The Evidence Trail proves that the indicators were community-authored, not externally imposed.

2. **m023 (Community Endorsement) becomes a verification input.** Credit classes requiring biocultural legitimacy can reference m023 endorsement records in the Evidence Trail. Funders and verifiers can independently confirm that the community endorsed the credit terms.

Credit types already referenced in PACTO pilots: USS01 (Umbrella Species Stewardship), BT01 (BioTerra), Carbon (C01-C09).

### Hypercerts

**Status: Conceptual alignment**

Hypercerts are impact claims represented as ERC-1155 semi-fungible tokens on Ethereum. They encode four dimensions: work scope, work timeframe, impact scope, and impact timeframe.

PACTO's Evidence Trail maps to hypercert claims:

| Hypercert Dimension | PACTO Equivalent |
|--------------------|-----------------|
| **Work scope** | Core Loop process records — what participatory work was done |
| **Work timeframe** | Assembly dates from Evidence Trail Layer 1 |
| **Impact scope** | Community-defined biocultural indicators (m020) |
| **Impact timeframe** | Living Contract duration (m022) |
| **Contributors** | Community assembly participants (from Evidence Trail, with community authorization) |

The Ethereum Attestation Service (EAS) used by Hypercerts for impact evaluation is conceptually parallel to PACTO's dual-verification model — multiple independent evaluators assessing the same claims.

Bridge pattern: PACTO Evidence Trail content hashes anchored on Regen Ledger could be mirrored as hypercert metadata on Ethereum, enabling the same community-authored claims to be legible in both ecosystems.

### DAODAO + CosmWasm

**Status: Conceptual mapping**

DAODAO is a modular governance framework built with CosmWasm smart contracts on Cosmos. PACTO's four governance layers map to DAODAO's module structure:

| PACTO Governance Layer | DAODAO Equivalent | Notes |
|----------------------|-------------------|-------|
| **Layer 1 (Automated)** | Automated proposal execution | Ecological monitoring triggers credit-related actions |
| **Layer 2 (AI-Assisted)** | Proposal modules with external input | AI synthesis feeds governance proposal drafts |
| **Layer 3 (Human-in-Loop)** | Voting modules | Community assembly votes with configurable thresholds |
| **Layer 4 (Constitutional)** | SubDAO with veto authority | Customary law override — always human, never automated |

Living Contracts (m022) could be implemented as CosmWasm contracts with community-controlled amendment functions. Amendment triggers re-running the Core Loop for specific sections; the contract enforces that amendments follow the participatory process before taking effect on-chain.

### EVM Interoperability

**Status: Conceptual**

PACTO's primary chain is Regen Ledger (Cosmos SDK). EVM interoperability is an interoperability target, not a co-equal pathway. Bridge patterns exist through:

- **Cosmos IBC to EVM bridges:** Axelar, Gravity Bridge, and similar protocols enable cross-chain communication between Cosmos and Ethereum ecosystems
- **Attestation mirroring:** Evidence Trail content hashes anchored on Regen Ledger can be mirrored to EVM chains for consumption by Hypercerts, EAS, or other EVM-native systems

The bridge is one-directional for most PACTO use cases: PACTO data originates on community PDS instances, anchors on Regen Ledger, and is mirrored to EVM when EVM-native systems need to reference it.

---

## Technical Architecture: Bridge Patterns

Several bridge patterns connect AT Protocol, Regen Ledger, and the broader ecosystem:

### Architecture Overview

```
AT Protocol Layer           Bridge Layer           Blockchain Layer

Community PDS               Content Hash ────────→ Regen Ledger
  ├─ Evidence records                               ├─ MsgAnchor (IRI)
  ├─ Attestations (m020)    Oracle ──────────────→  ├─ MsgAttest
  └─ Endorsements (m023)    Proposal Bridge ─────→  └─ DAODAO Proposal

DID Identity                DID ↔ Account Link ──→ Cosmos Account

Firehose Events             Event Filter ────────→ On-chain Triggers
                                                    ├─ Credit issuance
                                                    └─ Governance votes
```

### Bridge 1: Content Hash to MsgAnchor

The simplest and highest-value bridge. Already conceptually operational.

1. Community creates an Evidence Trail record in PDS
2. PDS computes the record's content hash (SHA-256)
3. A transaction submits `regen.data.v1 MsgAnchor` with the content hash to Regen Ledger
4. The IRI resolves back to the community PDS endpoint
5. Anyone can verify: fetch from PDS, compute hash, compare to on-chain anchor

### Bridge 2: DID to Cosmos Account

Links AT Protocol identity to on-chain capability.

1. Community's DID signs a message: "This DID is linked to Cosmos address regen1..."
2. The Cosmos account signs a transaction referencing the DID
3. The link is stored on-chain (via a governance or identity module)
4. Subsequent on-chain operations (credit issuance, voting) reference the DID for provenance

### Bridge 3: PDS Endorsement to DAODAO Proposal

Connects community assembly decisions to on-chain governance.

1. Community assembly reaches consensus through the Core Loop
2. m023 Community Endorsement record is created in PDS
3. A bridge service reads the endorsement and creates a DAODAO governance proposal
4. On-chain voting (if required) confirms the community decision
5. Smart contract executes the endorsed action (credit issuance, contract amendment)

### Bridge 4: Firehose to Oracle

Automates the content-hash anchoring step (Phase 3+).

1. AT Protocol PDS streams repository events to relays via the sync protocol
2. An oracle service subscribes to PACTO-specific Lexicon events
3. When a new Evidence Trail record is created, the oracle computes the content hash
4. The oracle submits `MsgAnchor` to Regen Ledger automatically

This eliminates manual anchoring steps, but introduces a new trust question: who runs the oracle? Options include community-operated oracles, multi-party oracle networks, or partner-operated oracles with community oversight.

### Bridge Implementation Priority

| Bridge | Complexity | Value | Priority | Phase |
|--------|-----------|-------|----------|-------|
| Content Hash → MsgAnchor | Low | High | 1 | Phase 1 (partially done) |
| DID → Cosmos Account | Medium | Medium | 2 | Phase 2 |
| PDS → IRI Resolver | Medium | High | 3 | Phase 2 |
| Endorsement → DAODAO Proposal | Medium-High | Medium | 4 | Phase 3 |
| Firehose → Oracle | High | Medium | 5 | Phase 3 |
| Cosmos → EVM Attestation Mirror | High | Low (current) | 6 | Phase 4 |

---

## Community Ownership Pathways

Sovereign infrastructure is not just about servers. It is about communities having practical control over the tools that support their ecological governance.

### Deliberative Democracy Tooling

PACTO's [deliberative democracy integration](../concepts/deliberative-democracy.md) identifies several tools that communities can self-host:

| Tool | Function | Self-Hostable | PACTO Integration |
|------|----------|---------------|-------------------|
| **pol.is** | Opinion clustering and consensus visualization | Yes (open source) | Complements Core Loop Step 5 (iterative refinement) |
| **Loomio** | Cooperative decision-making | Yes (open source) | Asynchronous deliberation between assemblies |
| **Decidim** | Participatory democracy platform | Yes (open source) | Broader governance context for Living Contracts |
| **Custom PACTO interface** | Voice-first, Core Loop native | To be built | Direct integration with PDS and Evidence Trail |

These tools are not dependencies — they are options that communities can adopt incrementally as their technical capacity grows.

### The Full Data Pipeline

From field collection to on-chain anchoring, communities can progressively own each step:

```
1. FIELD COLLECTION
   Audio recording of community assembly
   (phone, recorder, community-owned device)
        |
        v
2. LOCAL TRANSCRIPTION
   Whisper (local) → transcript
   No data leaves the community
        |
        v
3. LOCAL AI SYNTHESIS
   Ollama + open model → structured themes,
   priorities, points of agreement/tension
        |
        v
4. COMMUNITY REVIEW
   Feedback presentation → corrections → refinement
   (Core Loop Steps 4-5)
        |
        v
5. PDS STORAGE
   Evidence Trail records stored in community PDS
   Progressive disclosure enforced
        |
        v
6. ON-CHAIN ANCHORING
   Content hashes → regen.data.v1 MsgAnchor
   IRI resolves back to community PDS
        |
        v
7. CREDIT OPERATIONS
   Evidence Trail referenced in credit class issuance,
   marketplace listings, governance proposals
```

Each step can be decentralized independently. A community might run local transcription (Step 2) while still using commercial APIs for synthesis (Step 3). Progressive decentralization means each step moves at the community's pace.

### Living Contract Implementation

Living Contracts (m022) — adaptive agreements with community-controlled amendment protocols — are a natural fit for on-chain implementation:

- **Contract terms** stored in community PDS with content hash anchored on-chain
- **Amendment trigger:** Community assembly initiates Core Loop for specific contract sections
- **Amendment process:** New terms go through the full participatory process (m021 Voice Agreement)
- **Amendment anchoring:** New content hash replaces previous version reference on-chain, with the diff traceable through PDS version history
- **Community endorsement:** m023 required before any amendment takes effect

The key design principle: the amendment process is the same as the original agreement process. There is no shortcut that bypasses community voice.

---

## Open Questions

These are genuine uncertainties, not rhetorical ones. They represent active design questions that require input from communities, technical partners, and the broader PACTO ecosystem.

### Indigenous Language Support

Open AI models have limited support for the indigenous languages spoken by PACTO pilot communities (Paicoca for Siekopai, Matsés, Shuar). Fine-tuning models on indigenous language data raises its own sovereignty questions: who authorizes the training data? Who controls the resulting model? How are community interests protected if a fine-tuned model is distributed beyond the community? The [Beyond-FPIC checklist](governance-principles.md) applies to training data as much as to any other community knowledge.

### Hardware Sustainability

Community-owned servers require electricity, internet connectivity, physical security, maintenance, and replacement cycles. Who funds this? Options include: cost-sharing across communities, integration into credit revenue models, grant funding for infrastructure, or technical partner support agreements. The cost must be explicit, not hidden behind assumptions of volunteer labor.

### Connectivity Constraints

PACTO pilot communities in the Amazon have intermittent satellite internet at best. Sovereign infrastructure must work offline-first with sync-when-connected patterns. This is technically feasible (llama.cpp, local Whisper, PDS sync) but requires careful design for conflict resolution when multiple offline changes need to merge.

### AT Protocol Maturity

AT Protocol is production-tested at Bluesky scale, but PACTO's use case (ecological governance records, not social media posts) exercises different parts of the protocol. PACTO-specific Lexicons would need to track upstream protocol evolution. The protocol's governance is currently led by Bluesky PBC — a single company — which creates its own sovereignty questions.

### Bridge Layer Governance

Who runs the oracle that connects AT Protocol firehose events to Regen Ledger transactions? Options: community-operated, multi-party, or partner-operated with community oversight. Each has different trust properties and operational requirements.

### Legal Status of DID-Signed Agreements

PACTO's [legal pluralism](governance-principles.md) framework recognizes agreements under indigenous customary law, national law, and on-chain governance simultaneously. How do DID-signed Evidence Trail records interact with national legal systems that may not recognize decentralized identifiers? This is a legal research question, not a technical one.

### Community Capacity and Inclusion

The sovereignty pathway must not create new forms of exclusion. If running local AI requires technical knowledge that only some community members have, this can create internal power dynamics that contradict PACTO's design principles. Infrastructure sovereignty must be paired with capacity building that is genuinely accessible.

### Federation Governance

When multiple communities share infrastructure (Phase 4), who governs the shared resources? How are disputes resolved? How does a community leave the federation? These governance questions are at least as important as the technical architecture and should be designed through the same participatory process (Core Loop) that PACTO uses for everything else.

---

*This document maps a pragmatic pathway from commercially hosted infrastructure to community-sovereign infrastructure for the PACTO framework. It is a living document that will evolve as pilot implementations test these patterns. Detailed technical specifications, reference implementations, and integration guides are available to partners via the KOI Knowledge Commons.*

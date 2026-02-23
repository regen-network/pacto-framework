# The Evidence Trail

The Evidence Trail is PACTO's system for creating a transparent, verifiable record of the participatory process itself — not just the ecological or contractual outcomes.

---

## The Problem It Solves

Claims of "community participation" in conservation and ecological crediting often lack verifiable evidence. A project may check the FPIC box without demonstrating that the community actually shaped the agreement terms. The Evidence Trail addresses this gap.

## Process-as-Evidence

PACTO treats the participatory process as auditable evidence. At each step of the Core Loop, records are created that allow funders, verifiers, and communities themselves to independently confirm:

- **Did the community actually meet?** Assembly records with attestations
- **Was deliberation captured?** Audio and transcript content hashes
- **Was AI synthesis reviewed by the community?** Feedback records linked to each synthesis version
- **How many iterations occurred?** Iteration records tracking the refinement process
- **Did the community endorse the final agreement?** Endorsement attestations

## Evidence Layers

| Layer | What Is Recorded | How It's Verified |
|-------|-----------------|------------------|
| **Assembly Convening** | Date, location, governance structure, participant count | Facilitator + community representative attestation |
| **Voice Capture** | Audio and transcript content hashes | Cryptographic fingerprint anchored on-chain |
| **Synthesis** | Each synthesis version, AI model used, provenance | Knowledge graph object with metadata |
| **Feedback** | Corrections, affirmations, rejections by community | Signed by community representative |
| **Iteration** | Changes between versions, consensus status | Structured diff records |
| **Agreement** | Final endorsed agreement with all parties | Community endorsement mechanism |

## Design Principles

1. **Process verification, not just outcome verification** — the evidence trail proves *how* agreements were reached
2. **Community control** — the community decides what evidence is published and what remains private
3. **Immutability with privacy** — content hashes are anchored on-chain; full content stays with the community
4. **Progressive disclosure** — metadata is public; full records require community authorization
5. **Machine-readable provenance** — every record has structured metadata for automated verification

## Progressive Disclosure

| Access Level | What Is Visible |
|-------------|----------------|
| **Public** | Metadata: assembly dates, iteration count, endorsement status, content hashes |
| **Verified parties** | Summary: themes, indicator lists, agreement type |
| **Authorized partners** | Detail: synthesis outputs, feedback records |
| **Community only** | Full: audio recordings, raw transcripts, individual contributions |

Content hashes are always public (enabling verification), but full content requires community authorization.

## Why This Matters

Without verifiable evidence of participatory process, biocultural crediting claims lack the foundation that distinguishes them from conventional conservation offsets. The Evidence Trail is what gives "biocultural" its operational meaning — demonstrable proof that community voice drove the agreements.

---

## Sovereign Storage

The Evidence Trail's progressive disclosure model extends naturally to sovereign infrastructure — community-controlled data storage using AT Protocol Personal Data Servers (PDS). See [sovereign-infrastructure.md](sovereign-infrastructure.md) for the technical pathway from cloud-hosted evidence storage to community-owned PDS instances, including PACTO-specific Lexicons for each evidence layer and on-chain anchoring via Regen Ledger.

---

*Detailed technical specifications for the Evidence Trail, including schema definitions and on-chain anchoring patterns, are available to partners via the KOI Knowledge Commons.*

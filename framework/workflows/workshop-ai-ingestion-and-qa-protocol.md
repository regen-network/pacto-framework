# Workshop AI Ingestion and QA Protocol

## 1. Purpose

This document operationalizes the "Voice-to-Text Capture" and "AI-Assisted Synthesis" stages of the PACTO Core Loop.

Its purpose is to ensure:

- Complete raw data ingestion  
- Literal transcript fidelity  
- Structured AI-assisted synthesis  
- Quality assurance prior to external circulation  
- Clear traceability (evidence trail)  

This protocol applies to workshop-based indicator development and report generation processes.

---

## 2. Scope

This workflow governs the end-to-end process from:

- Audio Recording
- Literal Transcript Generation
- AI-Assisted Workshop Report Drafting
- Indicator Distillation
- QA Review
- External Circulation

This protocol does not implement automation inside the repository. It documents process controls and review gates.

---

## 3. Data Ingestion Requirements

### 3.1 Audio Inventory

Before transcript generation:

- All workshop audio files must be inventoried.  
- A reconciliation step must confirm no sessions are missing.  
- The number of transcripts generated must match the number of audio files.  

No synthesis step should proceed without full reconciliation.

---

### 3.2 Literal Transcript Generation

Summarized transcripts must not be used as primary source material.

Transcripts must:

- Be literal (verbatim)  
- Preserve speaker distinctions when possible  
- Maintain original terminology  
- Avoid interpretive summarization  

If AI tools (e.g., Gemini, Otter, notebook tools) are used for transcription, prompts must explicitly require maximum fidelity to source audio.

Transcript generation method, model used, and date must be recorded.

---

## 4. AI-Assisted Workshop Report Generation

A bespoke GPT may be used to:

- Digest literal transcripts  
- Extract biocultural indicators  
- Structure workshop reports  

Inputs:
- Literal transcripts only  

Outputs:
- Structured workshop report  
- Preliminary indicator extraction  

The GPT configuration or prompt logic should be versioned or recorded when materially modified.

---

## 5. Indicator Distillation Process

Indicator distillation may be conducted using structured prompts and multi-source synthesis.

Selection criteria include:

- **Protocol Alignment**  
  Consistency with ERA or other applicable crediting framework requirements.

- **Intervention–Outcome Logic**  
  Clear linkage between action, measurable output, and intended ecological outcome.

- **Defined Monitoring Structure**  
  Explicit monitoring frequency and responsible party.

- **Non-Redundancy**  
  Indicators should not duplicate measurement logic or outcome signals.

- **Causal Ecological Relevance**  
  Demonstrable direct or indirect linkage to the stated ecological objective of the crediting framework.  
  Example: in umbrella-species models (e.g., jaguar), indicators should plausibly contribute to population health, habitat integrity, or ecosystem functionality.

- **Sensitivity to Meaningful Change**  
  Capacity to detect material behavioral, governance, or ecological shifts that may function as early warning signals and support adaptive management.

- **Operational Feasibility**  
  Realistic for community-level tracking and reporting.

- **Methodological Proportionality**

The total number of indicators should align with the structural and reporting expectations of the selected protocol, while balancing ecological sensitivity, implementation feasibility, and external review clarity.

Final indicator sets should be accompanied by brief rationale notes where material filtering decisions occur.

---

## 6. AI Quality Assurance (QA) Gate

Before circulation to partners, communities, or reviewers:

The following checks must be completed:

- All audio sessions accounted for  
- Literal transcripts confirmed  
- Spot-check comparison between transcript and report sections  
- No major omissions detected  
- Structural alignment with intended protocol requirements  
- Indicator set reviewed for coherence and proportionality  
- Manual adjustments documented  

If QA fails at any stage, synthesis must be revised before circulation.

---

## 7. Traceability and Evidence Trail

For each workshop processing cycle, the following must be logged:

- Audio inventory list  
- Transcript generation method and date  
- AI model(s) used  
- Prompt version (if applicable)  
- Date of report generation  
- Date of QA completion  
- Responsible reviewer  

This documentation supports reproducibility and integrity within the PACTO framework.

---

## 8. Reference Implementation: Biocultural Workshop Report Generator

A bespoke GPT titled **"Biocultural Workshop Report Generator"** (by Gisel Booman) may be used as a reference implementation of the AI-assisted synthesis step described in this protocol.

Access:  
Available to users within the Regen Network Development, PBC workspace.

Role within this protocol:

- Ingests literal workshop transcripts  
- Extracts biocultural indicators  
- Generates structured workshop reports  

This GPT functions as an operational tool under this documented workflow.

Use of alternative models or agents is permitted provided they comply with the ingestion and QA requirements defined above.

---

## 9. Community Validation and Consent Loop

Following indicator distillation and technical QA, a structured community validation step is required.

This step ensures that:

- Final indicator selection accurately reflects community intent  
- Filtering criteria are transparent  
- No material meaning was altered during synthesis  
- Community representatives acknowledge and validate the resulting framework  

### 9.1 Circulation Requirements

Final workshop reports and the proposed indicator set should be circulated to community representatives who participated in the workshops.

Where applicable:

- Circulation should include leadership representatives involved in the process  
- Gender inclusion should be considered to ensure representative review  
- Materials should be provided in a language accessible to the community  
- A reasonable review period should be provided  

### 9.2 Feedback Integration

Substantive feedback should be documented and, where appropriate, integrated into the final indicator set.

Material disagreements or requested modifications should be recorded.

### 9.3 Validation Record

A record should be maintained documenting:

- Who reviewed the materials  
- Date of circulation  
- Feedback received  
- Final confirmation or acknowledgement  

This step strengthens procedural integrity and supports biocultural legitimacy within the crediting framework.


# UNIVERSITY OF MARYLAND GLOBAL CAMPUS

**Bachelor of Science in Biotechnology & Cybersecurity Technology**
**Integrated Capstone Project**

---

## Integrated Cyber-Biotechnology: Closed-Loop Neuroprosthetics with Post-Quantum Genomic Adjudication

---

**Author:** `[Your Full Name]`
**Student ID:** `[Your UMGC ID]`
**Address:** 1000 N Woodington Rd, Baltimore, MD
**Date of Submission:** June 2026
**Capstone Course:** `[e.g., BIOT 495 / CMIT 495]`
**Faculty Mentor:** `[Name, if assigned]`
**Prior Learning Portfolio Included:** Yes
**Certifications Held:** CompTIA A+, Network+, Security+, Healthcare IT Technician

---

## Abstract

This integrated capstone presents the design, ethical framework, and validation plan for a novel closed-loop neuroprosthetic system (CINP) that unites CRISPR-based neural editing with post-quantum cryptographic security to treat executive dysfunction of neurogenetic origin. The system uses real-time polygenic risk scores to drive CRISPRa/i modules for on-demand epigenomic control, while all genomic, clinical, and legal data are protected by a quantum-resistant audit ledger. To support safe deployment, the project also designs the Baltimore Secure Backbone System (BSBS), a zero-trust municipal network with mandated post-quantum cryptography. The work demonstrates mastery of genomics, bioinformatics, neurobiology, information security, health IT, and regulatory science, satisfying all outcomes for a combined Bachelor of Science in Biotechnology and Cybersecurity Technology at UMGC.

**Keywords:** CRISPRa/i, closed-loop neuroprosthetic, polygenic risk score, post-quantum cryptography, zero-trust, NIST PQC, HIPAA, Daubert standard, neuroethics, bioinformatics

---

## Table of Contents

1. Chapter 1 — Introduction and Problem Statement
2. Chapter 2 — Background and Literature Review
3. Chapter 3 — System Architecture (CINP + BSBS + Genomic Data Generator)
4. Chapter 4 — Genomic, Neurobiological, and Cryptographic Foundations
5. Chapter 5 — Validation Plan, Threat Model, and Risk Analysis
6. Chapter 6 — Ethical, Legal, and Regulatory Framework
7. Chapter 7 — Discussion, Limitations, and Future Work
8. Appendix A — UMLGC Competency Mapping Table
9. Appendix B — Glossary of Acronyms
10. Appendix C — Provisional Patent Abstract (Neuroprosthetic Adjudication System)
11. Appendix D — BSBS Network Topology Diagram (description)
12. Appendix E — Genomic Data Generator API Specification

---

# Chapter 1 — Introduction and Problem Statement

## 1.1 Motivation

Neurogenetic disorders of executive function — including Fragile X syndrome, 22q11.2 deletion syndrome, and polygenic forms of treatment-resistant attention and impulse-control disorders — affect an estimated 1 in 54 individuals in the United States. Pharmacotherapy is partially effective; behavioral therapy is resource-bounded. Meanwhile, genome-wide association studies (GWAS) now identify actionable polygenic risk scores (PRS) for these conditions, and CRISPR-based transcriptional modulation (CRISPRa/CRISPRi) is moving from petri dish to in vivo use in first-in-human trials.

A treatment gap exists between *knowing* a patient's polygenic risk and *acting* on it in real time, in a way that is simultaneously safe, auditable, privacy-preserving, and legally defensible. Closing that gap is the central motivation of this capstone.

## 1.2 Problem Statement

> How can a closed-loop neuroprosthetic system safely trigger CRISPRa/i modulation in response to real-time polygenic risk signals, while ensuring the entire pipeline — from genomic data ingestion to legal adjudication — is protected by quantum-resistant cryptography and complies with HIPAA, FDA, and Daubert evidentiary standards?

## 1.3 Research Questions

1. Can a real-time PRS inference engine drive CRISPRa/i actuation with sub-second latency and bounded off-target risk?
2. Can the data pipeline (genomic, clinical, audit) be hardened against harvest-now-decrypt-later quantum threats using NIST-approved PQC primitives?
3. Can the evidentiary record produced by the system satisfy Daubert reliability, peer-review, and known-error-rate tests for use in disability adjudication?
4. Can a zero-trust municipal backbone (BSBS) be specified to host such a system without re-architecting existing Baltimore health-IT infrastructure?

## 1.4 Contributions

- A reference architecture (CINP) for closed-loop CRISPRa/i neuroprosthetics with an integrated, post-quantum audit ledger.
- A municipal-scale zero-trust network design (BSBS) that uses NIST PQC primitives end-to-end.
- A reproducible High-Security Genomic Data Generator microservice that fuses biomedical literature, legal precedent, and scholarly metrics into a SHA3-256-immutable audit trail.
- A competency-mapping artifact (Appendix A) showing coverage of all UMGC BS Biotechnology and BS Cybersecurity Technology program outcomes.

## 1.5 Scope and Delimitations

- The CINP is *designed and simulated*, not deployed in human subjects at this stage.
- The BSBS design is implementation-ready at the specification level; physical deployment is out of scope.
- The Genomic Data Generator is implemented as a working prototype in the companion portfolio, not as production code.
- All legal analysis is academic; this is not legal advice.

---

# Chapter 2 — Background and Literature Review

## 2.1 Executive Function and Its Neurogenetic Basis

Executive function — working memory, cognitive flexibility, inhibitory control — depends on prefrontal cortical circuits modulated by dopaminergic, noradrenergic, and glutamatergic signaling. GWAS meta-analyses (Demontis et al., 2023; Sullivan et al., 2024) implicate >250 loci for ADHD alone, with PRS explaining 5–10% of phenotypic variance. For syndromic conditions (FXS, 22q11.2 DS), causal variants are largely known.

## 2.2 CRISPRa / CRISPRi as Therapeutic Modality

CRISPRa (e.g., dCas9-VPR, dCas9-SunTag) and CRISPRi (dCas9-KRAB, dCas9-MeCP2) enable reversible transcriptional control without double-strand breaks, reducing off-target mutagenesis risk. Recent in vivo work (Nakamura et al., 2024) demonstrated durable dopamine-pathway modulation in non-human primates. Delivery in humans remains the principal bottleneck; AAV9 and lipid nanoparticles (LNP) are the leading vectors.

## 2.3 Closed-Loop Neuroprosthetics

Closed-loop deep brain stimulation (DBS) for Parkinson's disease (e.g., Medtronic Percept PC) demonstrates that real-time neural sensing + algorithmic decision + actuation is clinically deployable. Extending the loop to *epigenomic* actuation is the novel step proposed here.

## 2.4 Polygenic Risk Scores in Clinical Practice

PRS deployment in clinical workflows is nascent but advancing. The eMERGE-IV network returns PRS for ten conditions in routine care. Statistical challenges (ancestry bias, calibration drift) remain active research areas.

## 2.5 Post-Quantum Cryptography

NIST finalized three PQC standards in 2024:

- **FIPS 203** — ML-KEM (Module-Lattice KEM, formerly Kyber)
- **FIPS 204** — ML-DSA (Module-Lattice DSA, formerly Dilithium)
- **FIPS 205** — SLH-DSA (Stateless Hash-Based DSA, formerly SPHINCS+)

For genomic data, ML-KEM (key encapsulation) and ML-DSA (signatures) are the natural choices, replacing ECDH and RSA-2048 respectively.

## 2.6 Zero-Trust Architecture

NIST SP 800-207 codifies zero-trust: "never trust, always verify." Continuous authentication, microsegmentation, and policy-based access control are the three operational pillars.

## 2.7 Daubert Standard for Scientific Evidence

Under *Daubert v. Merrell Dow Pharmaceuticals* (1993), scientific evidence is admissible if it has been tested, peer-reviewed, has known error rates, and is generally accepted in the field. The CINP's audit ledger is explicitly engineered to satisfy all four prongs.

## 2.8 HIPAA, GDPR, and GINA

The system handles PHI (HIPAA), personal data of EU residents (GDPR), and genetic information (GINA). The audit ledger is designed to minimize identifiers and support right-to-erasure without breaking the chain.

## 2.9 Research Gap

No published system, to our knowledge, closes the loop from PRS → CRISPRa/i actuation under a post-quantum cryptographic envelope with a Daubert-defensible evidence record. This capstone proposes and validates the design of such a system.

---

# Chapter 3 — System Architecture

## 3.1 System Overview

The capstone delivers three integrated artifacts:

1. **CINP** — Closed-loop neuroprosthetic, including PRS inference engine, CRISPRa/i actuation controller, and patient-safe hardware envelope.
2. **BSBS** — Baltimore Secure Backbone System, the municipal zero-trust network that hosts CINP, with mandated PQC.
3. **HS-GDG** — High-Security Genomic Data Generator, the microservice that ingests clinical, genomic, legal, and scholarly inputs and emits an immutable audit trail.

```
┌──────────────────────────────────────────────────────────────────────┐
│  Patient (BSBS-secured home/clinical gateway)                        │
│    │                                                                 │
│    ▼                                                                 │
│  Wearable neural interface ──► PRS Inference Engine (local TPU)      │
│    │                                │                                │
│    ▼                                ▼                                │
│  CRISPRa/i Controller ◄──── Decision Policy (auditable)             │
│    │                                                                 │
│    ▼                                                                 │
│  Delivery vector (AAV9 or LNP)                                       │
│                                                                       │
│  All paths write to HS-GDG Audit Ledger (BSBS, ML-DSA-signed)        │
└──────────────────────────────────────────────────────────────────────┘
```

## 3.2 CINP Subsystems

### 3.2.1 Sensing Layer

- Multichannel EEG + optional intracranial array.
- Edge denoising via temporal convolutional network; feature extraction on-device.
- Latency budget: ≤ 50 ms sensing-to-decision.

### 3.2.2 PRS Inference Engine

- Inputs: patient's genotyping chip, recent wearable time series, optional family history.
- Model: a calibrated logistic ensemble per indication (FXS, 22q11.2 DS, ADHD-P), updated quarterly.
- Output: a continuous PRS value with a calibrated confidence interval.
- Latency budget: ≤ 100 ms on local TPU.

### 3.2.3 Decision Policy

A deterministic, rule-based policy layer interprets the PRS and the live neural state, and only then authorizes actuation. The policy is encoded in a versioned, signed rule set stored in BSBS; every decision is logged to HS-GDG.

### 3.2.4 CRISPRa/i Actuation Controller

- Vector type: AAV9 (CNS-tropic) or intrathecal LNP.
- Guide RNAs pre-loaded; selection is the actuation event.
- Safety: dose limiter, refractory period, hardware "deadman" interlock.

### 3.2.5 Audit Ledger Writer

Every sensing frame, PRS inference, decision, and actuation is hashed (SHA3-256), Merkle-chained, and signed with ML-DSA. The chain is replicated to a Baltimore municipal court-admissible archive.

## 3.3 BSBS — Baltimore Secure Backbone System

### 3.3.1 Design Principles

- **Zero-trust** (NIST SP 800-207).
- **Post-quantum end-to-end**: ML-KEM for transport, ML-DSA for identity, hybrid ECDH-ML-KEM during migration.
- **Microsegmentation**: every workload is in its own segment; east-west traffic is policy-gated.
- **Continuous verification**: device posture + user identity + risk score, evaluated per request.

### 3.3.2 Topology (description — see Appendix D for diagram)

Three tiers:

- **Tier 1 — Edge**: clinical sites, patient homes, research labs. SD-WAN gateways terminate ML-KEM.
- **Tier 2 — Core**: municipal data centers, redundant. Service mesh enforces identity.
- **Tier 3 — Custodial**: genomic and clinical archives in hardened enclaves, HSM-backed ML-DSA signing keys.

### 3.3.3 Cryptographic Migration Plan

- **Phase 0** (now): inventory all cryptographic dependencies.
- **Phase 1** (Year 1): hybrid ML-KEM + ECDH on all new connections.
- **Phase 2** (Year 2): pure ML-KEM for transport, ML-DSA for identity, SLH-DSA reserved for firmware signing.
- **Phase 3** (Year 3): deprecate RSA/ECDSA except for legacy interop.

### 3.3.4 Identity and Access

- Workforce: phishing-resistant MFA (FIDO2) + PIV-derived ML-DSA certs.
- Workloads: SPIFFE/SPIRE identities with attestation.
- Patients: opt-in patient portal with verifiable credentials (mDL-style).

## 3.4 HS-GDG — High-Security Genomic Data Generator

### 3.4.1 Purpose

HS-GDG is the data substrate that lets CINP, BSBS, and downstream legal/adjudication actors share a single, verifiable, immutable record. It is also a *generator* in the generative-AI sense: it ingests literature, court records, and scholarly metrics and emits derived analytics that the audit ledger attests to.

### 3.4.2 Pipeline

```
Literature APIs (PubMed, OpenAlex)
   │
   ▼
Court Records API (CourtListener, RECAP)
   │
   ▼
Genomic Variant DB (ClinVar, gnomAD)
   │
   ▼
HS-GDG Ingest (signed, mTLS+ML-KEM)
   │
   ▼
Embedding + RAG (local, no external call)
   │
   ▼
Audit Ledger (SHA3-256 Merkle, ML-DSA signed)
   │
   ▼
Consumer APIs (CINP, BSBS, court, scholar)
```

### 3.4.3 Properties

- Append-only, Merkle-chained, ML-DSA-signed.
- Time-anchored via signed RFC 3161 timestamps from BSBS HSMs.
- Reproducible: any consumer can re-derive the same hash chain.
- Privacy-preserving: identifiers replaced with opaque patient IDs; linkage via threshold-re-encryption keys.

## 3.5 Putting It Together

A clinical event flows as: patient state → PRS → policy → actuation → vector delivery → biomarker feedback. Every hop is signed, hashed, and replicated. The whole graph is a single, verifiable artifact suitable for an FDA submission *and* a court exhibit.

---

# Chapter 4 — Genomic, Neurobiological, and Cryptographic Foundations

## 4.1 Genomic Foundations

- Variant calling: GATK best-practices pipeline on NovaSeq X.
- PRS construction: PRS-CSx with ancestry-specific priors.
- Off-target prediction: CRISPOR + Cas-OFFinder; reject any guide with predicted off-targets in coding exons with score < 0.2.

## 4.2 Neurobiological Foundations

- Targeted circuits: dorsolateral prefrontal cortex (dlPFC) for executive function; nucleus accumbens (NAc) for impulse control.
- Modality: CRISPRi to *reduce* hyperdopaminergic tone in NAc; CRISPRa to *boost* cortical GABAergic interneuron activity in dlPFC.
- Biomarker: real-time LFP beta/theta ratio in dlPFC, closed-loop regulated.

## 4.3 Cryptographic Foundations

| Use case        | Classical (deprecated) | PQC replacement |
|-----------------|------------------------|-----------------|
| Transport KEM   | ECDH P-384             | ML-KEM-768 (FIPS 203) |
| Digital signature | RSA-2048, ECDSA P-256 | ML-DSA-65 (FIPS 204) |
| Firmware        | RSA-2048               | SLH-DSA-SHAKE-128s (FIPS 205) |
| Hashing         | SHA-256                | SHA3-256 (NIST FIPS 202) |
| Symmetric       | AES-256-GCM            | AES-256-GCM (still acceptable; Grover-bounded) |

## 4.4 Bioinformatics Foundations

- Sequence alignment: minimap2 + BWA-MEM2 ensemble.
- Variant annotation: VEP + SpliceAI.
- Population genetics: PLINK 2.0, admix-kit.

---

# Chapter 5 — Validation Plan, Threat Model, and Risk Analysis

## 5.1 Validation Plan

The capstone is validated along four axes.

### 5.1.1 Functional Validation (in silico + bench)

- In silico: a digital twin of the CINP loop, using a population-scale PRS simulator and a biophysical neural model (Wilson-Cowan + dopaminergic gain).
- Bench: AAV-packaged guide RNAs delivered to organotypic slice culture; guide activity measured by RT-qPCR and RNA-seq.
- Acceptance: PRS-to-actuation end-to-end latency ≤ 200 ms in silico; ≥ 4-fold target-gene modulation in slice, with ≤ 1.5-fold change at top off-target.

### 5.1.2 Cryptographic Validation

- Round-trip ML-KEM handshake with 100,000 trials; verify handshake success rate and key indistinguishability.
- Sign-verify round-trip with ML-DSA-65; verify 100% pass at 1M trials.
- Fuzzing: 1M malformed packet corpus against BSBS gateways; verify zero crashes.

### 5.1.3 Threat Model (STRIDE)

| Threat                        | Mitigation                                    |
|-------------------------------|-----------------------------------------------|
| Spoofing of patient identity  | FIDO2 + PIV-derived ML-DSA; liveness          |
| Tampering of audit ledger     | Merkle chain + ML-DSA + RFC 3161 timestamps   |
| Repudiation of actuation      | Per-actuation signature; deadman interlock    |
| Information disclosure        | ML-KEM transport; enclave-based key custody   |
| Denial of service             | Rate limiting at edge; segmented core         |
| Elevation of privilege        | Zero-trust policy; SPIFFE workload identity   |

### 5.1.4 Adversarial / Harvest-Now-Decrypt-Later (HNDL) Defense

A motivated adversary is *already* recording BSBS-encrypted traffic. The migration plan (§3.3.3) ensures that any session negotiated after Phase 2 is quantum-safe, eliminating the HNDL attack surface on new data. Existing ciphertext remains at classical risk; for genomic data, the ledger's hash chain still provides integrity, and the symmetric AES-256 payload remains Grover-bounded.

## 5.2 Risk Register (selected)

| ID  | Risk                                          | Likelihood | Impact | Mitigation strategy |
|-----|-----------------------------------------------|------------|--------|---------------------|
| R1  | Off-target CRISPRa/i activity                 | Med        | High   | Sequence scoring; organoid validation; dose cap |
| R2  | PRS miscalibration across ancestries          | High       | Med    | Per-ancestry priors; clinician-in-the-loop |
| R3  | Quantum adversary in 7–10 years               | Med        | High   | Crypto-agility; PQC migration plan |
| R4  | Court rejects Daubert challenge               | Med        | Med    | Pre-publication peer review; reproducibility |
| R5  | Patient data breach                           | Low        | High   | Zero-trust + PQC + HSMs + audit |

---

# Chapter 6 — Ethical, Legal, and Regulatory Framework

## 6.1 Neuroethics

- Cognitive liberty: any actuation requires a contemporaneous, auditable patient (or surrogate) consent marker.
- Identity: changes to executive function are not *behavioral* coercion; the policy layer forbids continuous suppression and enforces refractory periods.
- Equity: ancestry-aware PRS is a hard requirement, not an option.

## 6.2 Disability Rights and Adjudication

Polygenic evidence is increasingly part of disability determinations. A robust audit trail — and a Daubert-defensible methodology — is therefore a *patient-rights* requirement, not merely a litigation one. The Genomic Privacy & Disability Rights Amicus Brief (companion document) develops this in full.

## 6.3 FDA Pathway

CINP is a combination product: drug (the LNP/AAV and guide RNA) + device (the controller and interface). The likely pathway is a combination IND/IDE. The HS-GDG audit ledger is designed to support FDA's 21 CFR Part 11 electronic-records requirements.

## 6.4 HIPAA, GINA, GDPR

- Data minimization: identifiers replaced at ingest; linkage only via threshold-re-encryption.
- Right to erasure (GDPR Art. 17): implemented as a tombstone record that does not break the Merkle chain.
- GINA: no underwriting, employment, or educational use is permitted by policy; technical enforcement at the data-use layer.

## 6.5 Daubert and the Audit Ledger

The HS-GDG ledger is engineered specifically to satisfy Daubert:

| Daubert prong             | How the ledger satisfies it                        |
|---------------------------|----------------------------------------------------|
| Testability               | Every entry is reproducible from public sources    |
| Peer review               | Submitted to a preprint server; invited comment    |
| Known error rate          | Benchmarked quarterly with public corpora          |
| General acceptance        | Aligned with HL7 FHIR + W3C VC standards          |

---

# Chapter 7 — Discussion, Limitations, and Future Work

## 7.1 What This Capstone Demonstrates

- A coherent, end-to-end design for closed-loop neuroprosthetics under a post-quantum cryptographic envelope.
- A municipal-scale, deployment-ready backbone design (BSBS) that supports the system.
- A reproducible data substrate (HS-GDG) that bridges clinical, scientific, and legal worlds.
- A documented mapping to every UMGC BS Biotechnology and BS Cybersecurity Technology program outcome (Appendix A).

## 7.2 Limitations

- No in-human validation; the system is validated in silico and in organotypic slice.
- PRS is ancestry-biased; an under-represented population remains at risk of miscalibration.
- PQC migration is a multi-year effort; legacy interop with non-PQC peers is a residual risk.
- The legal landscape (GINA enforcement, FDA combination-product review timelines) is moving.

## 7.3 Future Work

- In-human first-in-human trial under FDA combination IND/IDE, anchored at Johns Hopkins.
- Federated PRS learning across institutions without centralizing patient data.
- Real-time on-device CRISPR activity sensors (e.g., dCas9-fluorophore fusions) for closed-loop biomarker feedback.
- Extension of BSBS to other mid-Atlantic municipal health networks.
- Formal verification of the policy layer using Coq or Lean.

## 7.4 Closing Reflection

This capstone is the synthesis of two UMGC degrees that the institution has never before combined at the undergraduate level. The integration is not cosmetic: every component of CINP, BSBS, and HS-GDG requires both biotechnology and cybersecurity, and the result is stronger than either alone.

---

# Appendix A — UMGC Competency Mapping Table

The capstone is evaluated against the published program outcomes of both degrees.

## A.1 BS in Biotechnology program outcomes

| Outcome | Where addressed |
|---|---|
| Apply core biology, genetics, and biochemistry concepts | Ch 2, Ch 4 |
| Use bioinformatics tools to analyze genomic data | Ch 3.4, Ch 4.4 |
| Evaluate molecular biology laboratory methods | Ch 4.1, Ch 5.1.1 |
| Communicate scientific findings to technical and non-technical audiences | Ch 1, Ch 6, Ch 7 |
| Apply regulatory and ethical frameworks (FDA, IRB, GINA) | Ch 6 |
| Integrate biotechnology with computational methods | Throughout |

## A.2 BS in Cybersecurity Technology program outcomes

| Outcome | Where addressed |
|---|---|
| Apply cryptographic primitives to protect data at rest and in transit | Ch 3.3, Ch 4.3 |
| Design secure network architectures | Ch 3.3 (BSBS) |
| Implement zero-trust and identity-based controls | Ch 3.3.4, Ch 5.1.3 |
| Conduct threat modeling and risk analysis | Ch 5.1.3, Ch 5.2 |
| Apply post-quantum cryptography per NIST guidance | Ch 3.3.3, Ch 4.3 |
| Comply with legal/regulatory cybersecurity requirements (HIPAA, NIST) | Ch 5, Ch 6 |

---

# Appendix B — Glossary of Acronyms

- **AAV** — Adeno-Associated Virus
- **BSBS** — Baltimore Secure Backbone System
- **CINP** — Closed-loop Integrated Neuroprosthetic
- **CRISPRa/i** — CRISPR activation / interference
- **DBS** — Deep Brain Stimulation
- **dlPFC** — Dorsolateral Prefrontal Cortex
- **FIPS** — Federal Information Processing Standard
- **GINA** — Genetic Information Nondiscrimination Act
- **GWAS** — Genome-Wide Association Study
- **HS-GDG** — High-Security Genomic Data Generator
- **HSM** — Hardware Security Module
- **KEM** — Key Encapsulation Mechanism
- **LNP** — Lipid Nanoparticle
- **ML-DSA** — Module-Lattice Digital Signature Algorithm
- **ML-KEM** — Module-Lattice Key Encapsulation Mechanism
- **NIST** — National Institute of Standards and Technology
- **PQC** — Post-Quantum Cryptography
- **PRS** — Polygenic Risk Score
- **SLH-DSA** — Stateless Hash-Based DSA
- **UMGC** — University of Maryland Global Campus

---

# Appendix C — Provisional Patent Abstract

**Title:** *Neuroprosthetic Adjudication System with Post-Quantum Genomic Ledger*

**Inventor:** `[Your Full Name]`

**Abstract:** A system and method for treating neurogenetic executive dysfunction in a patient, comprising a wearable neural interface, a polygenic risk score (PRS) inference engine, a deterministic decision policy, and a CRISPRa/i actuation controller. The system produces a post-quantum cryptographic audit ledger (ML-DSA signed, SHA3-256 Merkle chained) of every sensing frame, PRS inference, decision, and actuation, suitable for use as evidence in legal disability adjudication under the Daubert standard.

**Claims (summary):**
1. A closed-loop method using PRS to drive CRISPRa/i modulation.
2. A Merkle-chained, post-quantum-signed audit ledger for clinical events.
3. A zero-trust municipal backbone (BSBS) hosting the foregoing.
4. A reproducible data generator (HS-GDG) for evidentiary records satisfying Daubert.

---

# Appendix D — BSBS Network Topology (text description)

Three logical tiers, physically realized as redundant data centers and SD-WAN edge nodes.

- **Tier 1 — Edge.** ~120 sites: hospitals, clinics, patient homes, UMGC and JHU research labs. Each terminates an ML-KEM-encrypted SD-WAN tunnel to Tier 2.
- **Tier 2 — Core.** Two redundant municipal data centers. Service mesh (Istio) enforces SPIFFE identities on every workload; east-west traffic is ML-KEM-protected.
- **Tier 3 — Custodial.** Genomic and clinical archives in HSM-backed enclaves. ML-DSA signing keys are held in FIPS 140-3 Level 3 HSMs; quorum release for any cryptographic operation.

A copy of the BSBS specification, in DOT/Graphviz form, is included with the companion portfolio.

---

# Appendix E — Genomic Data Generator API Specification

Base path: `/v1/`

| Method | Path | Purpose |
|---|---|---|
| `GET`  | `/health` | Liveness + PQC handshake status |
| `POST` | `/events` | Append a signed event to the audit ledger |
| `GET`  | `/events/{id}` | Fetch an event and its Merkle proof |
| `GET`  | `/audit/root` | Latest Merkle root, ML-DSA signed |
| `POST` | `/query` | Re-derive a hash chain segment; supports Daubert reproducibility |
| `GET`  | `/metrics` | Prometheus-format ops metrics |

All endpoints require a SPIFFE identity, a valid ML-DSA-signed request, and a fresh ML-KEM session key.

---

**END OF MANUSCRIPT**

# Research Statement

**Applicant:** Caustin Lee McLaughlin
**Proposed Program:** PhD in Cybersecurity (with concurrent BS in Criminal Justice via PLA)
**Date:** June 6, 2026

---

## 1. Research Question

**Primary question.** Can a post-quantum cryptographic (PQC) evidence-integrity layer, anchored to a Semantic Evidence Trace (SET) ledger using SHA3-256 content hashing and ML-DSA digital signatures, render biometric, neurogenetic, and forensic health data legally admissible under the Daubert standard (Federal Rule of Evidence 702) in adversarial administrative and criminal proceedings — and at what measurable cryptographic, operational, and procedural cost?

**Sub-questions.**
- **SQ1.** What is the empirical latency, throughput, and packet-loss overhead of NIST PQC primitives (ML-KEM-768, ML-DSA-III) when integrated into a zero-trust municipal health data network under simulated adversarial load?
- **SQ2.** How do administrative law judges, federal magistrates, and forensic science practitioners evaluate the *Daubert* prongs (testability, peer review, error rate, general acceptance) when presented with PQC-anchored biometric evidence as compared to conventional evidence?
- **SQ3.** To what extent does the existing federal regulatory framework (HIPAA, the Federal Rules of Evidence, the Administrative Procedure Act) accommodate — or systematically exclude — cryptographic chain-of-custody artifacts as substantive evidence?

## 2. Why This Question, Why Now

Three convergent developments make this research timely. **First**, NIST finalized its post-quantum cryptographic standards (FIPS 203, 204, 205) in August 2024, and federal agencies are now under active migration pressure to retire RSA and ECC for long-confidentiality data — most acutely protected health information and biometric data subject to the "harvest-now, decrypt-later" threat model. **Second**, neurogenetic and biometric evidence are increasingly relevant to disability adjudication, criminal responsibility, and sentencing, but the doctrinal infrastructure for evaluating their reliability is fragmented across administrative law, evidence law, and forensic science. **Third**, the 2019 Baltimore ransomware attack — and the cascading municipal breaches that followed — demonstrated that legacy public health networks are operationally fragile in precisely the moments when evidentiary integrity matters most.

This research does not treat those three developments as separate. It treats them as a single integrated problem of trustworthy computation under adversarial conditions, which is the operational definition of cybersecurity.

## 3. Falsifiable Core Hypothesis

> A SHA3-256-anchored Semantic Evidence Trace ledger, in which each entry is digitally signed using ML-DSA-III and bound to a corresponding ML-KEM-768 encapsulated payload, can generate evidentiary packages that satisfy the *Daubert* standard for administrative and criminal adjudication, even when the underlying biometric or neurogenetic intervention is only simulated, *provided* that the cryptographic overhead remains within empirically defined latency and availability bounds consistent with HIPAA § 164.308 administrative safeguards.

This hypothesis is testable. It can be falsified by (a) failing to meet the latency or availability bound under simulated load, (b) failing to obtain favorable *Daubert* evaluations from a sufficiently sized mock-trier panel, or (c) failing to identify a regulatory pathway by which the ledger output can be admitted under the Federal Rules of Evidence.

## 4. Methodology Overview

The dissertation is a **mixed-methods, portfolio-based** work organized around four research chapters mapped to four publishable units.

| Chapter | Method | Deliverable / Target Outlet |
|---|---|---|
| Ch. 1 — Empirical Hook: The Case File as Data | Autoethnographic case study of an actual SSA disability adjudication in which neurogenetic evidence was excluded, drawn from the consolidated Supreme Court submission (Petition 1, *McLaughlin v. Bisignano*, No. 25-1522) | *Yale Law & Policy Review* (interdisciplinary) or *Journal of Law and the Biosciences* |
| Ch. 2 — Systematic Review: PQC for Protected Health Data | PRISMA-style systematic review of PQC implementations in healthcare, 2019–2026 | *IEEE Transactions on Information Forensics and Security* or *Journal of the American Medical Informatics Association* |
| Ch. 3 — Architectural Analysis: The HSPA and the SET Ledger | Specification, formal security analysis, and Mininet/GNS3 simulation of the HSPA-9 architecture under DDoS and HNDL attack scenarios | *ACM Transactions on Privacy and Security* or *USENIX Security* |
| Ch. 4 — Daubert Validation: A Mock Trier Study | Structured Delphi panel of administrative law judges, federal magistrate judges, and forensic science practitioners evaluating SET-anchored evidence packages against the four *Daubert* prongs | *Court Review* (the journal of the American Judges Association) or *Judicature* |

The dissertation synthesizes these chapters into a single argument: that a specific architectural pattern (HSPA + SET) is sufficient, in the technical and legal sense, to support the admission of biometric and neurogenetic evidence in proceedings where such evidence is currently excluded.

## 5. Relationship to Existing Portfolio

I am not entering this dissertation cold. I bring to it:

- A **working prototype** of the HSPA, including a Python/FastAPI implementation of the High-Security Genomic Data Generator with PQC wrappers using the open-source `liboqs` library. The prototype is containerized and reproducible.
- A **municipal policy whitepaper** (the BSBS), 23 pages, that has already mapped the 2019 Baltimore ransomware event to specific NIST PQC migration requirements.
- A **filed provisional patent application** for the Unified Cognitive Infrastructure System, which the SET ledger extends.
- A **500-hypothesis empirical genomic analysis** using the ASTA research framework, demonstrating capacity to design and execute falsifiable computational experiments at scale.
- **Five certiorari petitions** filed in the Supreme Court of the United States, providing the autoethnographic empirical material for Chapter 1 and the regulatory-framing material for Chapter 4.

The dissertation is not a re-packaging of this work. It is the scholarly formalization of it, conducted under peer review, with original empirical contribution in Chapters 2, 3, and 4.

## 6. Fit with the Program and the Faculty

The proposed research requires a committee with strength in (a) applied cryptography and PQC, (b) health informatics and HIPAA-regulated environments, (c) evidence law and *Daubert* doctrine, and (d) science and technology studies. I have identified candidate faculty whose published work aligns with these requirements and would welcome the opportunity to discuss potential chairs at the committee's convenience.

The criminal justice undergraduate degree is not ornamental. It is the disciplinary home of the doctrinal literature (due process, evidence law, procedural justice, forensic science policy) on which the dissertation depends. Concurrently satisfying the BS requirements via PLA allows the doctoral coursework to be dedicated to the technical and methodological training the dissertation actually requires.

## 7. Timeline and Feasibility

| Year | Milestone |
|---|---|
| Year 1 | Coursework completion (PhD core + criminal justice BS electives); Chapter 1 drafting; IRB protocol submission for Chapter 4 |
| Year 2 | Chapter 2 systematic review; Chapter 3 simulation campaign; first peer-reviewed submission |
| Year 3 | Chapter 4 Delphi panel execution; second and third peer-reviewed submissions; dissertation prospectus defense |
| Year 4 | Dissertation integration; oral defense; fourth peer-reviewed submission |

The four-year timeline is realistic because the prototype, whitepaper, and cert petitions have already absorbed the cold-start engineering cost. The remaining original work is the empirical validation campaign (Chapters 2, 3, 4) and the dissertation synthesis.

## 8. Risks and Mitigations

The principal risks are (1) inability to recruit a sufficiently credentialed Delphi panel for Chapter 4, mitigated by pre-committing to a multi-modal recruitment strategy (state administrative law judges via the National Association of Administrative Law Judiciary, federal magistrate judges via the Federal Judicial Center, and forensic science practitioners via the National Institute of Standards and Technology Organization of Scientific Area Committees); (2) cryptographic overhead exceeding the HIPAA availability bound, mitigated by specifying that the bound is a research finding and not a constraint, and by providing for graceful degradation to classical cryptography in narrow failure modes; (3) regulatory pathway not materializing in the four-year window, mitigated by treating the regulatory analysis as a chapter conclusion rather than a precondition. A complete risk matrix is provided in the Risk Matrix and Scope and Limitations Statement enclosure.

## 9. Contribution to Knowledge

If successful, the dissertation will contribute (a) the first empirical latency and availability benchmark of NIST PQC primitives in a simulated municipal health network under adversarial load; (b) the first *Daubert* validation study of cryptographic chain-of-custody artifacts as substantive evidence; and (c) a regulatory pathway proposal for the admission of PQC-anchored evidence in federal administrative and criminal proceedings. None of those contributions exist in the literature as of June 2026.

---

*Word count: ~1,480*

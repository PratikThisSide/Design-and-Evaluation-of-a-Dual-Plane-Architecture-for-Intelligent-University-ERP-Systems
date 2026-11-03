<!-- Repository README: Manuscript under review -->

<div align="center">

# Design and Evaluation of a Dual-Plane Architecture for Intelligent University ERP Systems

### CampusOS · Intelligent University ERP & Academic Decision Support

[![Manuscript](https://img.shields.io/badge/STATUS-SUBMITTED%20%7C%20UNDER%20PROCESS-D97706?style=for-the-badge)](#publication-status)
[![Research Article](https://img.shields.io/badge/TYPE-RESEARCH%20ARTICLE-174A7E?style=for-the-badge)](#)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0009--9975--5553-A6CE39?style=for-the-badge)](https://orcid.org/0009-0009-9975-5553)

**A dual-plane architecture that separates deterministic academic operations from AI-assisted institutional advisory.**

</div>

---

## 📌 Research snapshot

| | |
|---|---|
| **Research system** | CampusOS |
| **Journal** | Journal of Emerging Paradigms in Computing Systems (JEPCS) |
| **Manuscript submitted** | 30 October 2026 |
| **Current status** | Submitted · Under process |
| **Article type** | Research Article |
| **Corresponding author** | Pratik Raj |

> **Publication status notice:** This manuscript is under process. It has not been represented as accepted or published. Repository status will be updated only after an official journal decision.

## 🧭 Overview

University ERP systems preserve official academic records, but static record interfaces offer limited support for exploring possible outcomes and understanding next steps. Adding a language model alone does not solve the need for reproducible calculations, traceable policy information, and strict protection of student records.

This research presents **CampusOS**, a university ERP prototype built around two distinct planes:

- **Deterministic core plane:** performs authoritative academic calculations and controlled workflows.
- **Advisory plane:** retrieves institutional documents and authorized context without write access to the academic ledger.

The separation is designed to keep AI assistance from becoming the source of truth for academic records.

## 🧱 Dual-plane architecture

| Plane | Responsibilities | Design principle |
|---|---|---|
| **Plane 1 · Deterministic core** | GPA and attendance calculations, read-only simulations, policy-based risk scoring, small-cohort suppression, role-checked intervention transitions | Reproducible, auditable, access-controlled |
| **Plane 2 · Advisory path** | Retrieval of institutional documents and authorized context for user-facing assistance | Grounded, scoped, read-only with respect to the academic ledger |

## 📝 Abstract

The paper presents CampusOS, a university ERP prototype with a dual-plane architecture. Its deterministic core calculates GPA and attendance, runs read-only academic simulations, applies a policy-based risk score, suppresses small-cohort summaries, and enforces role-checked intervention transitions. A separate advisory path retrieves institutional documents and authorized context without write access to the academic ledger.

Eight properties were evaluated in a local test environment. The findings are limited to the prototype and the test conditions reported.

## 📊 Evaluation snapshot

| Evaluation area | Reported result |
|---|---|
| Counterfactual GPA simulations | 50 simulations; no row-count changes in the two inspected academic tables |
| Risk trajectory analysis | 1,974 of 2,439 synthetic profiles changed risk band (80.93%; 95% Wilson CI: 79.33%–82.44%) |
| Security probes | 100 probes; six administrative probes returned HTTP 500 |
| Core advisory queries | 30 queries; RAGAS faithfulness 0.941 |
| Citation markers | Present in 46.67% of advisory answers |
| Out-of-scope handling | 0 of 10 queries received an explicit abstention |

### Interpretation and limitations

- The exploratory sensitivity run covered 80,000 input evaluations, but its indices are **not treated as validated findings** because the estimator configuration was not preserved and some first-order estimates exceeded corresponding total-order estimates.
- Six administrative security probes returned HTTP 500 errors; these require investigation and hardening.
- Citation markers appeared in 46.67% of advisory answers, and none of ten out-of-scope queries received an explicit abstention.
- The local neural runtime was unavailable. Reported latency therefore describes retrieval and template fallback, not live model inference.
- These results characterize the tested prototype. They do not establish production readiness or improved student outcomes.

## 🎯 Research focus

- Dual-plane architecture for university ERP and academic decision support
- Deterministic GPA and attendance calculations
- Read-only counterfactual academic simulations
- Policy-based academic risk scoring
- Small-cohort summary suppression
- Role-checked intervention workflow transitions
- Retrieval-augmented institutional advisory support
- Separation of advisory retrieval from write access to the academic ledger

## 👥 Authors

| Author | Affiliation / contribution |
|---|---|
| **Pratik Raj** | Corresponding author · Student, School of Computing, MIT ADT University, Pune, India |
| **Sumit Arun Hirve** | Associate Professor, School of Computing, MIT ADT University, Pune, India |
| **Smith Deshmukh** | Student, School of Computing, MIT ADT University, Pune, India |
| **Ayush Dongare** | Student, School of Computing, MIT ADT University, Pune, India |
| **Yash Mate** | Student, School of Computing, MIT ADT University, Pune, India |

**ORCID:** [Pratik Raj — 0009-0009-9975-5553](https://orcid.org/0009-0009-9975-5553)

## 📥 Manuscript

The submitted manuscript is being prepared in PDF format for repository access. The manuscript file will be linked here once the PDF is uploaded.

## 🏛️ Publication status

**Journal:** *Journal of Emerging Paradigms in Computing Systems (JEPCS)*  
**Submission date:** 30 October 2026  
**Current status:** Submitted · Under process

A formal citation will be added after the journal assigns final publication details, including volume, issue, page range, DOI, and publication date.

## 🗂️ Planned repository structure

```text
.
├── README.md
└── manuscript/
    └── CampusOS-Dual-Plane-ERP-Research-Paper.pdf
```

## 🏷️ Keywords

`University ERP` · `Academic Decision Support` · `Dual-Plane Architecture` · `Learning Analytics` · `Student Data Privacy` · `Retrieval-Augmented Generation` · `Deterministic Computing` · `CampusOS`

---

<div align="center">

**Research by Pratik Raj and co-authors**  
MIT ADT University · Pune, Maharashtra, India

*This repository describes a research manuscript under process and prototype evaluation results. It is not a claim of journal acceptance, production readiness, or demonstrated improvement in student outcomes.*

</div>

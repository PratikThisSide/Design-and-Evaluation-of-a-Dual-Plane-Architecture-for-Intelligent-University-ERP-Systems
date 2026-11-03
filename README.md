# Design and Evaluation of a Dual-Plane Architecture for Intelligent University ERP Systems

[![Status](https://img.shields.io/badge/Manuscript-Submitted%20%7C%20Under%20Process-orange)](#publication-status)
[![Research](https://img.shields.io/badge/Type-Research%20Article-blue)](#)

## Overview

This repository accompanies the research paper **“Design and Evaluation of a Dual-Plane Architecture for Intelligent University ERP Systems.”** The work presents **CampusOS**, a university ERP prototype that separates authoritative, deterministic academic operations from a retrieval-based advisory path.

The architectural goal is to preserve reproducible academic computation, traceable institutional-policy information, and student-record access controls while providing decision-support capabilities.

## Abstract

University ERP systems maintain official academic records, but static record interfaces offer limited support for exploring possible outcomes and understanding next steps. Adding a language model does not resolve the need for reproducible calculations, traceable policy information, and strict protection of student records. This paper presents CampusOS, a university ERP prototype with two distinct planes. Its deterministic core calculates GPA and attendance, runs read-only academic simulations, applies a policy-based risk score, suppresses small-cohort summaries, and enforces role-checked intervention transitions. A separate advisory path retrieves institutional documents and authorized context without write access to the academic ledger.

Eight properties were evaluated in a local test environment. Across 50 counterfactual GPA simulations, row counts in two inspected academic tables did not change. An exploratory sensitivity run covered 80,000 input evaluations, but its indices are not treated as validated findings because the estimator configuration was not preserved and some first-order estimates exceeded corresponding total-order estimates. In a synthetic subset of 2,439 profiles with an SGPA decline of at least 1.50 points, 1,974 changed risk band when the trajectory factor was included (80.93%; 95% Wilson CI: 79.33%–82.44%). Of 100 security probes, six administrative probes returned HTTP 500 errors. For 30 core advisory queries, RAGAS faithfulness was 0.941, citation markers appeared in 46.67% of answers, and none of ten out-of-scope queries received an explicit abstention. The local neural runtime was unavailable; latency therefore describes retrieval and template fallback, not live model inference. Findings are limited to the prototype and test conditions reported.

## Research focus

- Dual-plane architecture for university ERP and academic decision support
- Deterministic GPA and attendance calculations
- Read-only counterfactual academic simulations
- Policy-based academic risk scoring
- Small-cohort summary suppression
- Role-checked intervention workflow transitions
- Retrieval-augmented institutional advisory support
- Separation of advisory retrieval from write access to the academic ledger

## Evaluation snapshot

| Evaluation area | Reported result |
|---|---|
| Counterfactual GPA simulations | 50 simulations; no row-count changes in the two inspected academic tables |
| Risk trajectory analysis | 1,974 of 2,439 synthetic profiles changed risk band (80.93%) |
| Security probes | 100 probes; six administrative probes returned HTTP 500 |
| Core advisory queries | 30 queries; RAGAS faithfulness 0.941 |
| Citation markers | Present in 46.67% of advisory answers |
| Out-of-scope handling | 0 of 10 queries received an explicit abstention |

**Interpretation note:** These are prototype test results, not evidence of production readiness or improved student outcomes. The exploratory sensitivity indices are not presented as validated findings. The advisory latency test used retrieval and template fallback because the local neural runtime was unavailable.

## Authors

- **Pratik Raj** — Corresponding author; Student, School of Computing, MIT ADT University, Pune, Maharashtra, India
  - ORCID: [0009-0009-9975-5553](https://orcid.org/0009-0009-9975-5553)
- **Sumit Arun Hirve** — Associate Professor, School of Computing, MIT ADT University, Pune, Maharashtra, India
- **Smith Deshmukh** — Student, School of Computing, MIT ADT University, Pune, Maharashtra, India
- **Ayush Dongare** — Student, School of Computing, MIT ADT University, Pune, Maharashtra, India
- **Yash Mate** — Student, School of Computing, MIT ADT University, Pune, Maharashtra, India

## Publication status

**Submitted — under editorial/review process.**

The manuscript was uploaded to the *Journal of Emerging Paradigms in Computing Systems (JEPCS)* submission system on **30 October 2026**. It has not been represented here as accepted or published. This section should be updated only after an official status change from the journal.

## Manuscript availability

The manuscript is currently under process. The submitted DOCX is not included in this public repository at this stage. Please refer to the journal's official publication record once the paper is accepted and published, or contact the corresponding author for an appropriate version where sharing is permitted.

## Citation

A formal citation should be added after the journal assigns the final publication details (volume, issue, page range, DOI, and publication date).

## Scope and limitations

The findings are specific to the CampusOS prototype and the reported local test conditions. The evaluation identifies unresolved issues, including administrative HTTP 500 responses, incomplete citation coverage, missing explicit abstention for out-of-scope advisory queries, and limitations in the exploratory sensitivity analysis. The results should not be generalized to production deployments without further validation.

---

For academic correspondence, contact the corresponding author through the email address provided in the journal's official record.

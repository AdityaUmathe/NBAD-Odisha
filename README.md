# NBAD — Network Behaviour Anomaly Detection for OPTCL NG-SOC & NOC

A passive, on-premises, air-gap-capable platform that detects anomalous and policy-violating network behaviour from mirrored packets and exported flows. It keeps flow, session and raw-packet evidence and gives analysts a single console. Alerts go to the SIEM.

## Current status (2026-10-24)

| Item | Status |
|---|---|
| Phase | **Phase 0 and Phase 1 documentation complete. Waiting at the Phase 1 gate.** |
| Application code | **None.** Nothing has been built, installed, run, benchmarked or deployed. |
| Architecture | Proposed. No decision approved (see [AD list](docs/architecture/architecture-decisions.md#decisions-requiring-approval-ad-list)). |
| Compliance | **No compliance claim is made.** The Schedule-9 compliance column has not been answered. |
| Remote server | Not yet provided. No server has been accessed. |
| Version control | This directory is not yet a Git repository (decision AD-10) |

## Scope

- **In scope:** NBAD per tender Schedule-9 §11 (42 requirements) and Annexure-2 §3.1-D as given in the working copy `11_NBAD.docx`. Deployment at DC/Main LDC, with a design that scales to SLDC sites.
- **Out of scope:** SIEM and UEBA functions, endpoint analytics, inline or automatic blocking (ADR-012).

## Development constraint

All application development, dependency installation, builds, runtime testing and deployment happen **only on the remote server the project lead authorises** (ADR-023). This local directory holds documentation and planning only. See [CONTRIBUTING.md](CONTRIBUTING.md).

## Repository layout

```
.
├── README.md                     this file
├── CHANGELOG.md                  project changes
├── CONTRIBUTING.md               conventions and constraints
├── *.docx, *.textClipping        source documents S-01…S-11 (kept unchanged)
└── docs/
    ├── requirements/             baseline, conflicts & assumptions, traceability matrix
    ├── architecture/             architecture set, ADRs, risks, roadmap (start at README.md)
    ├── implementation/           master phased checklist with gates
    ├── operations/               remote-server assessment procedure, operations planning
    └── testing/                  test strategy, scenarios, acceptance tests
```

ADRs are kept in a single log ([docs/architecture/architecture-decisions.md](docs/architecture/architecture-decisions.md)) rather than a separate `docs/decisions/` folder, so there is only one place to review them.

## Source documents

| ID | File |
|---|---|
| S-01 | `11_NBAD.docx` — tender working copy (primary requirement source) |
| S-02 | `NBAD_Project_Blueprint_OPTCL.docx` |
| S-03 | `NBAD System Architecture Specification.docx` |
| S-04 | `NBAD Technology Stack and Tooling Guide.docx` |
| S-05 | `NBAD Data Model and Schema Specification.docx` |
| S-06 | `NBAD Detection Engineering Playbook.docx` |
| S-07 | `NBAD Integration Specification.docx` |
| S-08 | `NBAD Capacity Planning and Sizing Workbook.docx` |
| S-09 | `NBAD High Availability, Recovery and Operations Runbook.docx` |
| S-10 | `NBAD Air-Gap Operations and Security Design.docx` |
| S-11 | `Pasted 24-10-2026 at 12.22.19.textClipping` — architecture-phase instructions |

The original 107-page tender is **not** in the repository (Q-15).

## Where to start

1. [docs/architecture/README.md](docs/architecture/README.md) — architecture overview and index
2. [docs/architecture/architecture-decisions.md](docs/architecture/architecture-decisions.md) — decisions needing approval
3. [docs/architecture/open-questions-and-risks.md](docs/architecture/open-questions-and-risks.md) — what is still unknown
4. [docs/implementation/master-checklist.md](docs/implementation/master-checklist.md) — where the project stands
# NBAD-Odisha

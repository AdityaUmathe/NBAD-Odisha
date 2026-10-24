# Changelog

All meaningful project changes are recorded here. Dates are ISO 8601.

## [0.1.0] — 2026-10-24 — Phase 0 and Phase 1 documentation

### Added
- Repository documentation structure: `docs/requirements`, `docs/architecture`, `docs/implementation`, `docs/operations`, `docs/testing`.
- `README.md`, `CONTRIBUTING.md`, `CHANGELOG.md`.
- Requirements:
  - baseline (42 TR, 7 SOW, 7 OBL, 10 DR);
  - conflicts C-01 to C-13, ambiguities AM-01 to AM-09, assumptions A-01 to A-12;
  - traceability matrix.
- Architecture:
  - system architecture;
  - data flows and contracts;
  - technology evaluation (Options A/B/C, scorecard, provisional recommendation of Option C with gates G-T1 to G-T6);
  - capacity and resilience (scenarios, benchmark plan B-01 to B-13);
  - security and air-gap;
  - integration design (INT-01 to INT-14);
  - ADR-001 to ADR-024 plus approval list AD-01 to AD-14;
  - open questions Q-01 to Q-35 and risks R-01 to R-22;
  - implementation roadmap (Phases 0 to 13).
- Implementation master checklist with phase gates.
- Operations: remote-server prerequisites and read-only assessment procedure, operations planning index.
- Testing: test strategy with DT, FT, IT, RT and POC T1 to T12 definitions.

### Notes
- No application code was written. Nothing was installed, built, run, benchmarked or deployed. No server was accessed.
- Source `.docx` files and the project-brief clipping were left unchanged. Their text was extracted read-only into the session scratch area (outside the repository) using the built-in macOS `textutil`.
- Static documentation checks were run with a Python standard-library script that reads the Markdown files only. Results on 2026-10-24:

  | Check | Result |
  |---|---|
  | Files checked | 20 Markdown files |
  | Internal links and anchors | All resolve. 0 broken. |
  | Code fences | All balanced. 8 Mermaid diagrams. |
  | TR-01 to TR-42 in the traceability matrix | All present |
  | IDs referenced but never defined | 0 (286 distinct IDs checked) |
  | Q and R rows | 35 Q rows (Q-01 to Q-35), 22 R rows (R-01 to R-22) |
  | Secret-pattern scan | 0 hits |
  | Local install/run instruction scan | 0 hits |

- A scan for claim words ("verified", "proven", "guarantee", …) was reviewed by hand. One wording was corrected: data-flow-and-contracts §6 now says IT-03 verification is pending. The rest are negations or definitions of test conditions.
- Mermaid diagrams were **not rendered**, because no renderer is installed and installing one locally is not allowed. Only their syntax structure was reviewed.

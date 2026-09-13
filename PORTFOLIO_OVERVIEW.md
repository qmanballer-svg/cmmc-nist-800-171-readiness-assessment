# Portfolio Overview

This repository is a fictional, end-to-end cybersecurity GRC readiness assessment designed to show how a practitioner moves from **scope and control requirements** to **evidence, findings, risk, remediation, governance, and executive reporting**.

## Five-minute review path

For a fast review, open these artifacts in order:

1. [`01_scope/assessment_scope.md`](01_scope/assessment_scope.md) — what is in scope and why.
2. [`02_controls/cmmc_level_2_control_matrix.csv`](02_controls/cmmc_level_2_control_matrix.csv) — 110 CMMC Level 2 / NIST SP 800-171 Rev. 2 requirements with simulated assessment results.
3. [`04_evidence/evidence_request_list.csv`](04_evidence/evidence_request_list.csv) — requested evidence, owners, methods, and collection status.
4. [`04_evidence/evidence_traceability_matrix.csv`](04_evidence/evidence_traceability_matrix.csv) — how open findings trace to evidence and closure criteria.
5. [`03_risk/risk_register.csv`](03_risk/risk_register.csv) — likelihood, impact, treatment, owner, and target dates.
6. [`05_findings/findings_report.md`](05_findings/findings_report.md) — detailed findings with condition, risk, recommendation, and closure evidence.
7. [`06_remediation/poam_tracker.csv`](06_remediation/poam_tracker.csv) — remediation ownership and POA&M-style tracking.
8. [`07_reports/governance_assessment.md`](07_reports/governance_assessment.md) — maturity, decision rights, KPIs/KRIs, and governance cadence.
9. [`07_reports/executive_summary.md`](07_reports/executive_summary.md) — leadership-level summary and priorities.

## What this project demonstrates

- translating framework requirements into testable control objectives;
- defining a CUI assessment boundary and control ownership;
- distinguishing policy existence from operating effectiveness;
- using examine, interview, and test evidence;
- evaluating evidence sufficiency and identifying gaps;
- writing defensible audit / assessment findings;
- converting control gaps into business-security risks;
- distinguishing inherent risk from residual risk;
- tracking corrective actions through validated closure;
- handling exceptions and formal risk-acceptance concepts;
- reporting technical issues to executive stakeholders.

## Simulated assessment snapshot

| Outcome | Count |
|---|---:|
| MET | 94 |
| NOT MET | 14 |
| NOT APPLICABLE | 2 |
| Total | 110 |

The portfolio is intentionally imperfect: the objective is to demonstrate assessment judgment, documentation, prioritization, and remediation rather than present an unrealistically clean environment.

## Evidence-to-closure chain

A finding in this repository should be traceable through the following lifecycle:

**requirement → implementation claim → evidence request → evidence review → assessment result → finding → risk → owner → corrective action → closure evidence → retest → residual-risk decision**

That traceability is a core theme of the project and is the reason the control matrix, evidence catalog, risk register, findings report, and remediation trackers are separate but linked artifacts.

## Portfolio note

Everything in this repository is synthetic and educational. It is not a real customer assessment, certification, C3PAO engagement, legal opinion, or representation of any employer environment.
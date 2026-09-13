# Cybersecurity Governance Assessment

> **Portfolio simulation:** This governance assessment is based on the fictional Falcon Ridge Defense Components (FRDC) environment used throughout this repository. It is not an audit, certification, or assessment of a real organization.

## Executive summary

FRDC has established a recognizable cybersecurity governance foundation for its CUI enclave, including defined control ownership, technical security tooling, a documented assessment boundary, risk tracking, and remediation ownership. The principal weakness is not the absence of security activity; it is inconsistent governance evidence showing that key processes are performed on a repeatable cadence, approved by accountable owners, and tracked through closure.

The simulated control assessment identified **94 MET, 14 NOT MET, and 2 NOT APPLICABLE** requirements. The most material governance themes are privileged-access oversight, vulnerability-management coverage, monitoring completeness, incident-response testing, configuration governance, and formal periodic control assessment.

### Overall governance maturity

**2.5 / 5 — Developing / Partially Defined**

The organization has functioning controls and responsible teams, but several governance processes depend on inconsistent evidence, manual follow-up, or incomplete review coverage. The target state is a repeatable operating model in which ownership, review cadence, evidence retention, exceptions, risk acceptance, and remediation status are visible to management.

## Assessment methodology

This portfolio assessment evaluates governance across eight domains using evidence already represented in the simulated readiness assessment, risk register, findings report, and remediation plan.

### Maturity scale

| Score | Maturity | Description |
|---|---|---|
| 1 | Ad hoc | Activities are informal, reactive, or dependent on individuals. |
| 2 | Developing | Processes exist but are inconsistently executed or evidenced. |
| 3 | Defined | Ownership, procedures, cadence, and evidence expectations are documented. |
| 4 | Managed | Metrics, exceptions, risk treatment, and management review operate consistently. |
| 5 | Optimized | Controls are continuously monitored, measured, automated where appropriate, and improved using trend data. |

## Governance domain assessment

| Domain | Rating | Assessment |
|---|---:|---|
| Governance structure & accountability | 3.0 | Security and GRC ownership is identifiable, but formal recurring management review should be strengthened. |
| Risk management | 3.0 | Risks are documented with owners, treatment, target dates, and remediation actions. Formal acceptance/escalation thresholds should be added. |
| Identity & privileged-access governance | 2.0 | Technical access controls exist, but quarterly privileged-access certification evidence is incomplete and account lifecycle documentation is inconsistent. |
| Security monitoring governance | 2.0 | Sentinel and related monitoring provide broad coverage, but review cadence and telemetry coverage are not consistently evidenced across all sources and segments. |
| Incident-response governance | 2.0 | An incident-response plan exists, but the current period lacks completed tabletop-test evidence and corrective-action follow-through. |
| Vulnerability & configuration governance | 2.0 | Scanning and baselines exist, but coverage gaps remain for intermittently connected endpoints, server baselines, and application execution controls. |
| Compliance evidence & audit readiness | 2.0 | Evidence exists across multiple areas, but a formal annual control assessment has not been completed and evidence consistency varies by control owner. |
| Remediation governance | 3.0 | Findings have owners, treatment plans, and target dates. Stronger aging metrics, escalation rules, and closure validation would improve accountability. |

## Key governance strengths

1. **Defined assessment boundary** — the CUI enclave, user population, platforms, and supporting systems are documented.
2. **Named risk ownership** — open risks are assigned to accountable operational owners rather than remaining unowned GRC observations.
3. **Risk-based prioritization** — critical and high findings are differentiated from moderate issues.
4. **Microsoft security ecosystem coverage** — Entra ID, Intune, Defender, Sentinel, Azure, and managed endpoints provide a foundation for stronger continuous-control monitoring.
5. **Remediation planning** — open issues have planned corrective actions and target dates.

## Principal governance gaps

### 1. Privileged-access governance

**Observed issue:** quarterly privileged-access review evidence is incomplete for all enclave administrative roles.

**Governance concern:** access may be technically restricted without demonstrating that business need, approval, exception handling, and recertification occur consistently.

**Recommended governance action:** establish a quarterly privileged-access certification chaired by the IAM Lead, requiring system-owner approval, documented exceptions, aging review, and retained closure evidence.

### 2. Formal control-assessment governance

**Observed issue:** the current annual security-control assessment has not been formally completed and approved.

**Governance concern:** management lacks a reliable recurring mechanism to confirm control performance, identify degradation, and formally assign corrective actions.

**Recommended governance action:** institute an annual control-assessment cycle with documented scope, evidence standards, reviewer sign-off, executive approval, and linkage of findings to the risk register and remediation tracker.

### 3. Monitoring oversight

**Observed issue:** review cadence is inconsistently evidenced and one manufacturing-support segment has incomplete monitoring visibility.

**Governance concern:** tooling may exist without sufficient proof that required data sources are reviewed, exceptions are investigated, and coverage gaps are escalated.

**Recommended governance action:** create a monitoring governance standard defining required telemetry, minimum review cadence, responsible owner, retention requirement, exception handling, and monthly coverage reporting.

### 4. Incident-response assurance

**Observed issue:** no completed incident-response tabletop is available for the current period.

**Governance concern:** leadership cannot validate that escalation, communications, CUI handling, evidence preservation, customer notification, and containment responsibilities will function under pressure.

**Recommended governance action:** conduct at least one annual cross-functional tabletop and track lessons learned as formal corrective actions.

### 5. Vulnerability and configuration accountability

**Observed issue:** some engineering laptops are not consistently included in authenticated scans; selected baselines and application-control coverage are incomplete.

**Governance concern:** asset exceptions can remain outside normal control cycles unless reconciliation and escalation are mandatory.

**Recommended governance action:** reconcile vulnerability and configuration evidence to the authoritative asset inventory each cycle and automatically create exceptions for missing assets.

## Recommended governance operating model

### Monthly GRC review

Participants: GRC Lead, Security Manager, IAM, SOC, Vulnerability Management, Infrastructure, Network Security, and business/system owners as needed.

Review:
- open critical/high risks;
- overdue remediation items;
- privileged-access exceptions;
- vulnerability coverage;
- logging/monitoring coverage;
- evidence gaps;
- policy exceptions;
- new material changes to the CUI boundary.

### Quarterly security governance review

Management should review:
- risk trend and aging;
- control-assessment status;
- privileged-access certification;
- exception inventory;
- incident-response readiness;
- third-party/security dependencies;
- major architecture or boundary changes;
- remediation performance.

### Annual assurance cycle

- refresh system boundary and asset inventory;
- perform formal control assessment;
- conduct incident-response tabletop;
- review policies and standards;
- validate risk register completeness;
- approve remediation priorities;
- provide executive sign-off on residual risk.

## Recommended KPIs / KRIs

| Metric | Target |
|---|---:|
| Critical findings past due | 0 |
| High findings past due | < 5% |
| Privileged accounts reviewed quarterly | 100% |
| In-scope assets included in authenticated vulnerability scans | 100% |
| Required log sources meeting retention standard | 100% |
| Control owners providing evidence by due date | >= 95% |
| Open policy exceptions past expiration | 0 |
| Annual incident-response exercise completed | 100% |
| Remediation items closed with validated evidence | 100% |

## Decision rights and accountability

| Decision | Accountable role | Required evidence |
|---|---|---|
| Accept residual cyber risk | Security / executive risk owner | documented risk acceptance, rationale, expiration/review date |
| Approve privileged-access exception | System owner + IAM/Security | business justification, duration, compensating controls |
| Close a control finding | GRC Lead + control owner | verified closure evidence and retest result |
| Approve CUI boundary change | Security Manager / system owner | updated architecture, asset inventory, data-flow impact |
| Approve policy exception | Policy owner / risk owner | documented exception, risk, compensating control, expiration |

## 90-day governance priorities

### First 30 days
- complete privileged-access certification;
- close critical vulnerability-scan coverage gap;
- establish formal monthly GRC review;
- publish required evidence-retention expectations.

### Days 31–60
- complete annual control assessment;
- run incident-response tabletop;
- standardize log-review cadence and monitoring coverage reporting;
- complete remaining server-security baselines.

### Days 61–90
- measure remediation aging and exception trends;
- introduce automated evidence collection for identity, logging, and configuration controls;
- conduct management review of residual risk;
- approve the next-quarter continuous-improvement backlog.

## Portfolio takeaway

This artifact demonstrates the difference between **control testing** and **governance**. Control testing asks whether a requirement is implemented. Governance asks whether accountable owners, decision rights, review cadence, evidence, metrics, exceptions, risk treatment, and remediation are operating consistently enough for leadership to rely on the security program.

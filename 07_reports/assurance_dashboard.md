# Assurance Dashboard

> Fictional portfolio metrics for the Falcon Ridge Defense Components (FRDC) CUI enclave.

## Control status

| Metric | Result |
|---|---:|
| CMMC Level 2 requirements evaluated | 110 |
| MET | 94 |
| NOT MET | 14 |
| NOT APPLICABLE | 2 |
| Simulated implementation rate excluding N/A | 87.0% |

## Open risk profile

| Rating | Count |
|---|---:|
| Critical | 3 |
| High | 7 |
| Moderate | 4 |
| Low | 0 |
| **Total** | **14** |

## Evidence posture

| Evidence status | Count |
|---|---:|
| Received | 22 |
| Partial | 8 |
| Missing | 2 |
| **Total evidence requests** | **32** |

The evidence posture illustrates why control implementation and assessment readiness are not the same thing. A control can have technology and procedures in place while still lacking enough complete, timely, attributable evidence to support a conclusion.

## Priority assurance themes

1. **Privileged access** — recurring certification and exception evidence.
2. **Vulnerability management** — complete in-scope asset coverage.
3. **Monitoring** — consistent telemetry and review evidence across the boundary.
4. **Incident response** — tested process rather than plan-only assurance.
5. **Configuration governance** — approved baselines and application-control coverage.
6. **Periodic assessment** — formal management-approved control assessment.

## Recommended management metrics

| Metric | Target | Why it matters |
|---|---:|---|
| Critical findings past due | 0 | Prevent extended exposure to highest risks |
| Privileged roles reviewed quarterly | 100% | Reduce stale or excessive administration |
| In-scope assets present in authenticated scan cycle | 100% | Prevent unmanaged vulnerability blind spots |
| Required log sources meeting policy | 100% | Maintain detection and investigation coverage |
| Evidence delivered on time | >=95% | Measure control-owner accountability |
| Expired exceptions still open | 0 | Prevent temporary exceptions from becoming permanent |
| Remediation closures with retest evidence | 100% | Avoid paper closure without effectiveness validation |

## GRC interpretation

This dashboard is intentionally not a certification score. Its purpose is to show how a GRC function can turn detailed control and evidence work into management information: **what is failing, why it matters, who owns it, how long it has been open, and what evidence is needed to prove closure.**

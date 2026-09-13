# 30 / 60 / 90-Day Remediation Roadmap

## Objective

Prioritize the simulated FRDC readiness gaps by security impact, control dependency, evidence value, and implementation effort.

The roadmap intentionally separates **immediate risk reduction** from **governance maturity**. A control is not considered closed until the remediation is implemented, tested, and supported by final evidence.

---

## First 30 days — close critical exposure and establish evidence discipline

### 1. Privileged access governance — R-001

- Export all privileged role assignments.
- Validate business and technical need.
- Remove stale or excessive privileged access.
- Establish quarterly certification with documented approvals.
- Retain review and exception evidence.

**Success measure:** 100% of privileged roles reviewed and approved; all exceptions time-bound.

### 2. Vulnerability scan coverage — R-010

- Reconcile vulnerability scanner inventory against the authoritative asset inventory.
- Deploy agent-based scanning or an enforced connectivity/check-in process for remote engineering laptops.
- Create tickets automatically for assets that miss the required scan window.

**Success measure:** 100% of in-scope assets represented in the completed authenticated scan cycle or formally documented as an approved exception.

### 3. Split tunneling — R-012

- Standardize CUI VPN profiles.
- Disable split tunneling for every approved CUI remote-access method.
- Test multiple representative users and endpoint profiles.

**Success measure:** controlled testing demonstrates no simultaneous untrusted path during CUI remote access.

### 4. Event-review governance — R-003

- Define review frequency by log source and risk.
- Assign SOC ownership.
- Retain review records and escalation tickets.

**Success measure:** every required review period produces a traceable analyst record.

### 5. Identifier handling — R-006

- Formalize disablement, retirement, and reuse rules.
- Integrate the requirement into the termination workflow.

**Success measure:** sampled terminated-user records show timely disablement and documented identifier disposition.

---

## Days 31–60 — strengthen monitoring, assessment, and incident readiness

### 6. Manufacturing-segment visibility — R-014

- Add missing network telemetry.
- Validate log ingestion into Sentinel.
- Develop detection / alert logic.
- Run controlled test traffic and verify investigation workflow.

**Success measure:** monitoring inventory shows complete expected coverage and test events produce actionable alerts.

### 7. Incident-response tabletop — R-007

Run a ransomware + CUI-exfiltration tabletop involving:

- Security Operations;
- IT;
- GRC;
- Legal / contracting role;
- executive management; and
- communications / customer-notification roles as appropriate.

Produce an after-action report and corrective-action tracker.

**Success measure:** exercise completed; lessons learned assigned to owners and target dates.

### 8. Annual security-control assessment — R-011

- Complete a formal current-cycle assessment.
- Document findings and evidence.
- Obtain management review.
- Feed gaps into risk and remediation tracking.

**Success measure:** final approved assessment report exists and open actions are assigned.

### 9. Remote-access monitoring — R-002

- Centralize VPN/session telemetry.
- Establish review criteria and alerting.
- Document recurring oversight.

**Success measure:** session activity can be traced from authentication through review / escalation.

### 10. Server baselines — R-004

- Create remaining hardened configuration baselines.
- Approve baseline owners and version control.
- Test deployed systems for drift.

**Success measure:** every in-scope server class has an approved baseline and validation evidence.

---

## Days 61–90 — mature preventive controls and operating cadence

### 11. Application allowlisting — R-005

- Complete staged rollout.
- Define exception / emergency-change workflow.
- Monitor blocked executions.

**Success measure:** all enclave engineering endpoints are covered by the approved application-control mechanism.

### 12. Media accountability — R-008

- Reconcile removable-media inventory.
- Implement checkout / return accountability.
- Perform quarterly inventory review.

### 13. Physical-access log consistency — R-009

- Standardize retention requirements.
- Validate both controlled areas follow the same approved process.

### 14. Threat-advisory workflow — R-013

- Create a ticketed intake and triage workflow.
- Document applicability, risk, owner, due date, and closure.

---

# Governance cadence after remediation

| Activity | Proposed cadence | Owner |
|---|---|---|
| Privileged-access review | Quarterly | IAM |
| Vulnerability scanning | At defined recurring frequency plus new-vulnerability triggers | Vulnerability Management |
| Security event review | Risk-based recurring cadence | SOC |
| Firewall / boundary rule review | Quarterly | Network Security |
| Removable-media inventory | Quarterly | IT Operations |
| Security-control assessment | At least annually in this portfolio scenario | GRC |
| Risk-register review | Monthly | GRC / Risk Owners |
| Incident-response exercise | At least annually and after material changes | Security Manager |
| SSP / scope review | At least annually and after significant changes | GRC / System Owner |

## Closure rule

No finding is closed solely because a policy was written or a ticket was opened. Closure requires:

1. implemented remediation;
2. evidence in final form;
3. validation through examine / interview / test as appropriate;
4. updated control documentation; and
5. reassessment of residual risk.

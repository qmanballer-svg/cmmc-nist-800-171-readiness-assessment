# Findings Report

## Assessment summary

This simulated readiness assessment evaluated the fictional FRDC CUI enclave against the 110 CMMC Level 2 requirements aligned to NIST SP 800-171 Rev. 2.

### Simulated results

- **94 MET**
- **14 NOT MET**
- **2 NOT APPLICABLE**

The results are intentionally imperfect. A realistic GRC portfolio should demonstrate the ability to identify, document, prioritize, and remediate deficiencies rather than present an implausibly perfect environment.

> These are synthetic portfolio findings, not an official CMMC score or certification result.

## Open findings

| Risk | Requirement | Finding | Risk rating |
|---|---|---|---|
| R-001 | AC.L2-3.1.5 — Least Privilege | Quarterly privileged-access review evidence is incomplete for all enclave admin roles. | Critical |
| R-002 | AC.L2-3.1.12 — Control Remote Access | Remote-access session monitoring and periodic review evidence is incomplete. | High |
| R-003 | AU.L2-3.3.3 — Event Review | Review cadence is not consistently evidenced across all security-log sources. | High |
| R-004 | CM.L2-3.4.1 — System Baselining | Approved baselines are incomplete for two enclave server classes. | High |
| R-005 | CM.L2-3.4.8 — Application Execution Policy | Application allowlisting is not enforced on all engineering workstations. | High |
| R-006 | IA.L2-3.5.6 — Identifier Handling | Account disablement / reuse procedure is inconsistently documented after separation. | Moderate |
| R-007 | IR.L2-3.6.3 — Incident Response Testing | No completed incident-response tabletop is available for the current period. | High |
| R-008 | MP.L2-3.8.5 — Media Accountability | Removable-media checkout / return records are incomplete. | Moderate |
| R-009 | PE.L2-3.10.4 — Physical Access Logs | Physical-access log retention differs between controlled areas. | Moderate |
| R-010 | RA.L2-3.11.2 — Vulnerability Scan | Authenticated scans do not consistently include intermittently connected engineering laptops. | Critical |
| R-011 | CA.L2-3.12.1 — Security Control Assessment | Current annual control assessment has not been formally completed and approved. | High |
| R-012 | SC.L2-3.13.7 — Split Tunneling | No-split-tunnel enforcement is not consistently demonstrated for every remote-access profile. | High |
| R-013 | SI.L2-3.14.3 — Security Alerts & Advisories | Threat/advisory triage occurs but disposition records are inconsistent. | Moderate |
| R-014 | SI.L2-3.14.6 — Monitor Communications for Attacks | Monitoring visibility is incomplete for one manufacturing-support segment. | Critical |

---

# Detailed finding examples

## Finding R-001 — Privileged access review gap

**Requirement:** AC.L2-3.1.5 — Least Privilege  
**Assessment status:** NOT MET  
**Risk rating:** Critical

### Condition

Privileged roles are technically restricted; however, evidence does not demonstrate that all privileged assignments receive a complete, documented quarterly review with owner approval and exception handling.

### Evidence considered

- Entra privileged-role assignment export.
- IAM access-control procedure.
- Prior access-review records.
- Interview with fictional IAM Lead.

### Risk

Excessive or stale administrative access may persist without timely detection, increasing the potential impact of compromised or inappropriate privileged credentials on systems processing CUI.

### Recommendation

Implement a quarterly privileged-access certification process that:

1. identifies all privileged accounts and role assignments;
2. requires business / system-owner approval;
3. documents exceptions and expiration dates;
4. removes unnecessary access promptly; and
5. retains evidence for future assessments.

### Closure evidence

- completed access-review export;
- approver record;
- exception log;
- removal ticket sample; and
- updated procedure.

---

## Finding R-010 — Vulnerability scan coverage gap

**Requirement:** RA.L2-3.11.2 — Vulnerability Scan  
**Assessment status:** NOT MET  
**Risk rating:** Critical

### Condition

Quarterly authenticated scans are performed, but a subset of intermittently connected engineering laptops does not reliably appear in completed scan results.

### Evidence considered

- vulnerability-scanning policy;
- quarterly scan reports;
- asset inventory;
- device-management inventory;
- interview with fictional Vulnerability Management owner.

### Risk

Unscanned endpoints may contain unknown vulnerabilities that could be exploited to gain access to CUI or provide a path into the enclave.

### Recommendation

Deploy an agent-based or enforced check-in scanning mechanism and reconcile each scan cycle against the authoritative asset inventory. Exceptions should generate a ticket and documented resolution.

### Closure evidence

- scan configuration;
- 100% in-scope asset reconciliation;
- representative authenticated results; and
- exception / remediation tickets.

---

## Finding R-007 — Incident response testing gap

**Requirement:** IR.L2-3.6.3 — Incident Response Testing  
**Assessment status:** NOT MET  
**Risk rating:** High

### Condition

An approved incident-response plan exists, but there is no completed test or tabletop exercise for the current assessment period.

### Risk

Roles, communications, escalation paths, evidence preservation, customer reporting, and containment procedures may not perform as expected during a real CUI incident.

### Recommendation

Conduct a tabletop exercise based on a realistic ransomware plus CUI-exfiltration scenario. Record participants, injects, decisions, gaps, lessons learned, assigned corrective actions, and target dates.

### Closure evidence

- exercise plan;
- attendee record;
- exercise timeline;
- after-action report; and
- corrective-action tracker.

---

## Finding R-012 — Split tunneling enforcement gap

**Requirement:** SC.L2-3.13.7 — Split Tunneling  
**Assessment status:** NOT MET  
**Risk rating:** High

### Condition

The standard VPN profile disables split tunneling, but configuration evidence does not demonstrate equivalent enforcement for every approved remote-access profile.

### Risk

A remote endpoint may simultaneously communicate with an untrusted network and the CUI enclave, increasing the risk of unauthorized network paths or data exposure.

### Recommendation

Standardize the remote-access configuration, block split tunneling for all CUI access paths, and test multiple representative profiles to verify enforcement.

---

## Finding R-014 — Network monitoring visibility gap

**Requirement:** SI.L2-3.14.6 — Monitor Communications for Attacks  
**Assessment status:** NOT MET  
**Risk rating:** Critical

### Condition

Sentinel and related tools provide broad monitoring coverage, but one manufacturing-support segment connected to the enclave boundary does not forward the same level of network telemetry as other in-scope segments.

### Risk

Malicious traffic could traverse or originate from the segment without equivalent detection coverage, delaying containment and investigation.

### Recommendation

Extend network telemetry to the segment, map the source into the monitoring inventory, implement alert logic, and perform a controlled test to verify that representative suspicious traffic is detected and investigated.

## NOT APPLICABLE examples

Two requirements are marked NOT APPLICABLE in this scenario:

- **SC.L2-3.13.5 — Public-Access System Separation:** no public-facing system is included in the CUI assessment boundary.
- **SC.L2-3.13.14 — Voice over Internet Protocol:** VoIP is not used in the fictional CUI enclave.

A real assessment would require sufficient evidence and assessor judgment to support any N/A determination.

# Executive Summary

## Purpose

This portfolio project simulates a CMMC Level 2 / NIST SP 800-171 Rev. 2 readiness assessment for the fictional **Falcon Ridge Defense Components (FRDC)** CUI enclave.

The assessment was structured to demonstrate how a cybersecurity GRC practitioner can translate security requirements into evidence, findings, risk, ownership, and remediation decisions.

## Scope

The simulated assessment covers a segmented Microsoft-centric CUI enclave supporting approximately 65 authorized users. In-scope technologies include Microsoft Entra ID, Microsoft 365 GCC High, Intune, Defender for Endpoint, Sentinel, Azure workloads, managed Windows endpoints, VPN access, security monitoring, backup services, network-security infrastructure, and supporting physical / administrative processes.

## Simulated assessment result

| Result | Count |
|---|---:|
| MET | 94 |
| NOT MET | 14 |
| NOT APPLICABLE | 2 |
| **Total** | **110** |

These results are synthetic and do not represent an official CMMC assessment, certification, SPRS score, or attestation.

## Overall posture

The fictional organization has established a substantial security baseline: identity management, MFA, endpoint security, network segmentation, centralized monitoring, incident-response procedures, encryption, training, and documented governance processes are present.

The primary readiness issue is **operational evidence and control consistency**, not the complete absence of security capabilities.

Three gaps are rated Critical in the portfolio risk methodology:

1. **Privileged-access review discipline** — incomplete evidence of recurring review for all enclave administrative roles.
2. **Vulnerability-scanning coverage** — intermittently connected engineering laptops are not consistently represented in authenticated scans.
3. **Monitoring coverage** — one manufacturing-support segment has reduced telemetry visibility compared with the rest of the enclave.

High-priority gaps also exist in incident-response testing, split-tunneling enforcement, security-event review, configuration baselines, application allowlisting, remote-access monitoring, and completion of the current annual security-control assessment.

## Management priorities

### Priority 1 — Reduce immediate technical exposure

- complete privileged-access certification;
- obtain full authenticated vulnerability-scan coverage;
- enforce no-split-tunnel remote access; and
- close the identified network-monitoring visibility gap.

### Priority 2 — Strengthen evidence and operating cadence

- formalize recurring log-review evidence;
- complete the annual security-control assessment;
- standardize remote-access review; and
- approve remaining configuration baselines.

### Priority 3 — Demonstrate resilience

- conduct and document an incident-response tabletop exercise;
- complete application allowlisting deployment;
- reconcile media accountability; and
- standardize threat-advisory / physical-log workflows.

## Recommended roadmap

A 30/60/90-day remediation plan is maintained in [`../06_remediation/remediation_roadmap.md`](../06_remediation/remediation_roadmap.md).

The first 30 days focus on critical access, scanning, remote-access, and review gaps. Days 31–60 focus on monitoring, incident response, assessment governance, and baselines. Days 61–90 mature preventive controls and recurring operating evidence.

## GRC conclusion

The scenario demonstrates a core GRC principle: **a control must be both implemented and demonstrable**.

A technically capable environment can still be unready for an assessment when:

- control ownership is unclear;
- evidence is incomplete;
- recurring reviews are not retained;
- scope and asset inventories are inconsistent;
- control operation is not tested; or
- remediation is not tracked to validated closure.

The project therefore treats governance, technical control implementation, evidence quality, and risk management as a single continuous process rather than separate compliance activities.

## Portfolio disclaimer

All information in this report is fictional. This project is not an official CMMC readiness opinion, certification, legal interpretation, or representation of any employer or customer environment.

# CMMC Level 2 / NIST SP 800-171 Readiness Assessment

A hands-on cybersecurity GRC portfolio project simulating a CMMC Level 2 / NIST SP 800-171 readiness assessment for a fictional defense-sector organization handling Controlled Unclassified Information (CUI).

> **Portfolio simulation:** All organizations, systems, users, findings, evidence, and risk data in this repository are fictional. No real customer, employer, government, CUI, confidential, or proprietary information is used.

## Project objective

Demonstrate an end-to-end GRC assessment workflow:

**scope → system boundary → control assessment → evidence → findings → risk → remediation → POA&M/readiness reporting**

The project is designed to show practical capability in:

- CMMC Level 2 readiness
- NIST SP 800-171 Rev. 2 control assessment
- CUI scoping and system-boundary analysis
- evidence collection and traceability
- control testing using examine / interview / test methods
- risk assessment and risk-register management
- security-control gap analysis
- remediation planning
- POA&M concepts and tracking
- System Security Plan (SSP) concepts
- executive risk communication
- Microsoft-centric security architecture (Entra ID, Microsoft 365, Defender, Sentinel, Intune, Azure)

## Framework version note

NIST published **SP 800-171 Rev. 3** in May 2024. However, the current CMMC Level 2 model continues to use the **110 security requirements in NIST SP 800-171 Rev. 2**. This repository therefore uses Rev. 2 for its CMMC Level 2 control matrix while treating Rev. 3 as an important future-transition consideration.

As of September 2026, CMMC Phase II implementation has been suspended while Phase I self-assessment requirements remain in effect. The portfolio therefore emphasizes readiness, self-assessment discipline, evidence quality, and remediation rather than representing a C3PAO certification exercise.

## Fictional organization

**Falcon Ridge Defense Components (FRDC)** is a fictional 250-person defense subcontractor that manufactures precision components and handles CUI for selected customer programs.

The simulated CUI enclave includes approximately 65 authorized users and uses:

- Microsoft 365 GCC High
- Microsoft Entra ID
- Microsoft Intune
- Microsoft Defender for Endpoint
- Microsoft Sentinel
- Azure-hosted workloads supporting the enclave
- managed Windows 11 endpoints
- VPN / controlled remote access
- segmented corporate, CUI, and manufacturing networks

See [`01_scope/organization_profile.md`](01_scope/organization_profile.md) and [`01_scope/system_boundary.md`](01_scope/system_boundary.md).

## Repository structure

```text
.
├── README.md
├── DISCLAIMER.md
├── 01_scope/
│   ├── organization_profile.md
│   ├── assessment_scope.md
│   └── system_boundary.md
├── 02_controls/
│   └── cmmc_level_2_control_matrix.csv
├── 03_risk/
│   ├── risk_methodology.md
│   └── risk_register.csv
├── 04_evidence/
│   └── evidence_request_list.csv
├── 05_findings/
│   └── findings_report.md
├── 06_remediation/
│   ├── poam_tracker.csv
│   └── remediation_roadmap.md
└── 07_reports/
    └── executive_summary.md
```

## Assessment approach

The simulated assessment follows the CMMC / NIST SP 800-171A model of using three assessment methods:

- **Examine** — review policies, procedures, configurations, logs, plans, inventories, tickets, diagrams, and other artifacts.
- **Interview** — validate how control owners and operators understand and perform the process.
- **Test** — exercise technical or procedural mechanisms to verify the expected behavior.

Official CMMC findings are recorded as **MET**, **NOT MET**, or **NOT APPLICABLE**. A requirement is only MET when all applicable assessment objectives are satisfied by adequate evidence.

## Important POA&M note

The included POA&M tracker is a **portfolio readiness artifact**, not an official CMMC POA&M determination. Formal POA&M eligibility is constrained by 32 CFR § 170.21, including restrictions on critical requirements and a 180-day closeout window for applicable Conditional Level 2 cases. Each real-world item must be checked against the current rule before being treated as POA&M-eligible.

## Key deliverables

The repository contains:

1. a full 110-requirement CMMC Level 2 control matrix;
2. a defined CUI environment and assessment boundary;
3. an evidence-request catalog;
4. a risk methodology and risk register;
5. documented example findings;
6. a remediation / POA&M-style tracker;
7. a prioritized 30/60/90-day remediation roadmap; and
8. an executive summary suitable for leadership review.

## Author

**Qasim Shirazi**  
Cybersecurity GRC | Security Governance | Risk & Compliance

## Primary references

- DoD CMMC Program: https://dodcio.defense.gov/CMMC/
- CMMC Level 2 Assessment Guide: https://dodcio.defense.gov/Portals/0/Documents/CMMC/AssessmentGuideL2v2.pdf
- NIST SP 800-171 Rev. 2: https://csrc.nist.gov/pubs/sp/800/171/r2/upd1/final
- NIST SP 800-171 Rev. 3: https://csrc.nist.gov/pubs/sp/800/171/r3/final
- 32 CFR Part 170: https://www.ecfr.gov/current/title-32/subtitle-A/chapter-I/subchapter-D/part-170

## Disclaimer

This project is educational and portfolio-oriented. It is not legal advice, a certification, an attestation, an official CMMC assessment, or a substitute for qualified CMMC, legal, contracting, or cybersecurity guidance.

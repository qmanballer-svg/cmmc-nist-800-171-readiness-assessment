# Risk Methodology

## Purpose

This portfolio uses a simple 5×5 qualitative risk model to convert control gaps into prioritized business/security risks. The goal is not to reproduce a specific organization’s enterprise-risk methodology; it is to demonstrate a repeatable GRC process for documenting, ranking, assigning, and tracking risk.

## Risk statement format

Each risk is written in the form:

> **Because of [condition / control gap], there is a possibility that [threat/event] could affect [asset / business process / CUI], resulting in [impact].**

## Likelihood scale

| Score | Rating | Definition |
|---:|---|---|
| 1 | Rare | Highly unlikely in the current environment |
| 2 | Unlikely | Possible but not expected under normal conditions |
| 3 | Possible | Credible and could occur during the assessment horizon |
| 4 | Likely | Expected to occur or recur without additional controls |
| 5 | Almost Certain | Repeated, persistent, or highly probable |

## Impact scale

| Score | Rating | Definition |
|---:|---|---|
| 1 | Insignificant | Minimal operational/security effect |
| 2 | Minor | Limited localized effect; low recovery cost |
| 3 | Moderate | Material operational disruption or limited CUI/security exposure |
| 4 | Major | Significant security, contractual, operational, or CUI impact |
| 5 | Severe | Major CUI compromise, mission impact, contractual loss, or severe business consequence |

## Inherent risk score

`Likelihood × Impact = Risk Score`

| Score | Rating |
|---:|---|
| 1–4 | Low |
| 5–9 | Moderate |
| 10–16 | High |
| 17–25 | Critical |

## Treatment options

- **Mitigate** — implement or improve controls to reduce likelihood and/or impact.
- **Accept** — formally accept risk within defined authority and tolerance.
- **Avoid** — stop the activity or change the process so the risk no longer exists.
- **Transfer** — shift part of the risk through contractual, insurance, or service-provider arrangements while retaining accountability for residual risk.

## Residual risk

Residual risk is reassessed after planned remediation. A control is not considered effective merely because remediation is planned; implementation and evidence must be validated.

## Ownership

Every open risk has:

- an accountable risk owner;
- a control / remediation owner;
- a target date;
- a treatment decision; and
- evidence required for closure.

## Relationship to CMMC findings

A CMMC requirement finding and a business-risk rating are related but are not the same thing.

- CMMC findings in this project use `MET`, `NOT MET`, or `NOT APPLICABLE`.
- The risk register prioritizes the business/security consequence associated with a gap.
- Remediation priority considers both compliance significance and practical security risk.

## Portfolio note

Scores in this project are synthetic and are intended to demonstrate methodology rather than represent an official CMMC scoring calculation or an actual contractor’s risk posture.

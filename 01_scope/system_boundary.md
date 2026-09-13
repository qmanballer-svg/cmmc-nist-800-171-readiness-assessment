# System Boundary

## Boundary overview

The simulated CUI enclave is logically separated from the general corporate environment and is intended to restrict CUI processing, storage, and transmission to approved users, devices, services, and network paths.

```text
                           Internet / External Services
                                      |
                               Managed Firewall
                                      |
                    +-----------------+-----------------+
                    |                                   |
             Corporate Network                    CUI Enclave
             (no CUI allowed)                         |
                                                      |
                         +----------------------------+---------------------------+
                         |                            |                           |
                    Entra ID / IAM              Managed Endpoints           Azure Workloads
                         |                            |                           |
                         +----------------------------+---------------------------+
                                                      |
                                             Microsoft 365 GCC High
                                                      |
                                      Security / Monitoring Services
                                   Defender + Sentinel + Vulnerability Mgmt
                                                      |
                                             Managed Backup Services
```

## Primary trust boundaries

### 1. Corporate-to-CUI boundary

Corporate systems are not authorized to process CUI. Traffic into the CUI enclave is restricted through firewall policy, identity-based access, managed endpoints, and approved application paths.

### 2. Remote-access boundary

Remote users enter through an approved VPN / remote-access path. Access is limited to authorized personnel using managed endpoints and multifactor authentication. Remote-access configuration and monitoring are in scope for assessment.

### 3. Cloud-service boundary

Microsoft cloud services supporting the enclave are treated as external/cloud service dependencies. The organization remains responsible for configuration, identity, data handling, customer-side controls, and evidence necessary to demonstrate applicable security requirements.

### 4. Manufacturing-support boundary

A limited manufacturing-support segment interfaces with selected enclave workflows. This path is tightly restricted and monitored. The simulated assessment identifies a visibility gap in one portion of this segment as a risk requiring remediation.

## CUI flow

1. CUI is received through an approved secure collaboration or file-transfer workflow.
2. Authorized users authenticate through Entra ID using MFA.
3. CUI is accessed only from managed enclave endpoints or approved enclave workloads.
4. Data is stored in approved repositories and protected by encryption and access controls.
5. CUI leaving the enclave uses approved encrypted channels and authorized recipients.
6. Printing, removable media, and physical handling are restricted by policy and operational controls.
7. Security events and telemetry are forwarded to monitoring services for review.

## Boundary security objectives

- restrict CUI to authorized identities, systems, and workflows;
- prevent uncontrolled movement of CUI to general corporate systems;
- preserve auditability of user and administrative activity;
- protect CUI in transit and at rest;
- centralize monitoring and detection;
- enforce controlled remote access;
- ensure security-protection assets are included where they affect the enclave;
- maintain evidence sufficient to demonstrate how each applicable requirement is implemented.

## Assumptions and limitations

This is a conceptual portfolio architecture. It is not a production network design, authorization boundary, FedRAMP determination, or claim that any named product automatically satisfies CMMC or NIST requirements.

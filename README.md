# IAM Homelab

A documented, hands-on journey into **Identity & Access Management** — the foundation of modern defensive and cloud security.

> Work in progress. Each phase is documented under `docs/` as it is built. Nothing here is theoretical — every step is executed in the lab first.

## Objective

Build practical IAM skills end to end: directory services, authentication, access governance, and identity threat detection — mapped to the **SC-300** exam domains.

## Lab paths

Two ways to build this lab. Pick the one your hardware allows — concepts transfer between them.

### Option A — On-premises (Windows Server AD)

- **Hypervisor:** VirtualBox or VMware Workstation
- **VMs:** 1× Windows Server 2022 (evaluation trial), 2× Windows 10/11 clients
- **Network:** Host-only / NAT, isolated from the home LAN

### Option B — Cloud-native (Microsoft Entra ID)

- **Tenant:** Microsoft Entra ID Free tier (free Microsoft 365 developer tenant works too)
- **Extras:** Azure free account for Conditional Access and Identity Protection trials

## Phases

- [ ] **Phase 1 — Core directory:** Install AD DS, create OUs, users, groups; join clients to the domain; Group Policy basics
- [ ] **Phase 2 — Harden authentication:** Enforce MFA, password policies, account lockout; Conditional Access policies (Entra)
- [ ] **Phase 3 — Lifecycle & governance:** Joiner/mover/leaver process, privileged access (separate admin accounts), periodic access reviews
- [ ] **Phase 4 — Detect identity attacks:** Forward sign-in/audit logs; write detections for password spray, impossible travel, dormant-account reactivation

## Tools

Active Directory · Microsoft Entra ID · Group Policy · Conditional Access · PowerShell · Sysmon · Wazuh

## Why IAM first?

In cloud environments, identity *is* the perimeter. Every AWS IAM policy and Entra ID role assignment traces back to the concepts practiced here.

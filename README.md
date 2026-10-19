# IAM Homelab

Teaching myself identity and access management by building a lab and working through it.

I am a CEH working in public-safety ops, moving toward defensive security with IAM as my specialty. This is where I get hands-on with the concepts -- directories, authentication, access reviews, and identity attack detection -- instead of just reading about them.

## Topology

```
DC01 (Win Srv 2022: AD DS, DNS) <--LAN--> CLIENT01 (Windows 11, domain-joined)
        |
        | Entra Connect (planned)
        v
Microsoft Entra ID (MFA + Conditional Access, free tier)
```

## Setup

- **On-prem:** Windows Server 2022 (trial) as domain controller + a Windows 10/11 client, on VirtualBox
- **Cloud:** Microsoft Entra ID free tier for the cloud side (MFA, Conditional Access)

## Build log

- **2026-10-12** -- Repo created. Starting with the on-prem build: DC promo, OU structure, users and groups.

## Roadmap

1. On-prem domain controller up: AD DS, DNS, OU structure, test users/groups
2. Join client, verify GPO basics
3. Entra ID tenant: MFA + Conditional Access policies
4. Identity attack scenarios: password spray, token theft, anomalous sign-ins -- detected with my own Sigma rules

# Active Directory Homelab
Windows Server 2019 Active Directory lab documenting OU design, Group Policy, privilege management, and attack/defense exercises including Kerberoasting, BloodHound and Pass-the-Hash.


## Overview
This homelab simulates a real-world Active Directory environment built from scratch on VirtualBox. The goal is to develop and demonstrate hands-on skills in AD administration, security hardening, and offensive/defensive security techniques used in enterprise environments.

This project is structured in three phases - administration, hardening, and attack/defense. Each phase will consist of full documentation, screenshots and write-ups.

## Lab Environment

| Component | Details |
| :--- | :--- |
| **Hypervisor** | Oracle VirtualBox |
| **Domain Controller** | Windows Server 2019 |
| **Workstations** | 2x Windows 10 Enterprise (domain joined) |
| **Attack Machine** | Kali Linux |
| **Domain** | 'ad.local' |
| **Users** | Simulated AD users via [vulnadplus.ps1](https://raw.githubusercontent.com/WaterExecution/vulnerable-AD-plus/master/vulnadplus.ps1) |

## Network Topology
![Lab Network Topology Diagram](assets/network-topology.png)

## Project Structure

```text
active-directory-homelab/
├── Phase1-Administration/
│   ├── ou-structure.md
│   ├── gpo-configurations.md
│   ├── user-group-management.md
│   ├── shared-folders-permissions.md
│   └── screenshots/
├── Phase2-Hardening/
│   ├── hardening-checklist.md
│   ├── audit-policy-config.md
│   ├── event-log-analysis.md
│   └── screenshots/
├── Phase3-Attack-Defend/
│   ├── kerberoasting.md
│   ├── asrep-roasting.md
│   ├── bloodhound-analysis.md
│   ├── pass-the-hash.md
│   ├── dcsync.md
│   └── screenshots/
├── Reports/
│   └── AD-Security-Assessment.pdf
└── README.md
└── assets
    └── network-topology.png
```

# Phase 1 - AD Administration

**Goal:** Build and manage a functional Active Directory environment from the ground up.

**Completed Tasks:**
- [ ] Designed and created OU structure (IT, HR, Finance)
- [ ] Created domain users and security groups
- [ ] Applied Group Policy Objects (password policy, lockout policy, drive mapping)
- [x] Joined Windows 10 VMs to the domain
- [ ] Configured shared folders with NTFS and share permissions
- [ ] Tested permission-based access across user accounts

**Writeups**:
[OU Structure]() | [GPO Configurations]() | [User & Group Management]()

# Phase 2 - Security Hardening

**Goal:** Identify and reduce the attack surface of the AD environment.

**Completed Tasks:**
- [ ] Audited privileged accounts and Domain Admins group
- [ ] Disabled legacy protocols (NTLM, SMBv1) via GPO
- [ ] Configured Fine-Grained Password Policies for admin accounts
- [ ] Enabled and configured audit policies (logon, account management, privilege use)
- [ ] Deployed Sysmon for enhanced event logging
- [ ] Reviewed key Event IDs: 4624, 4625, 4648, 4720, 4732

**Writeups**: [Hardening Checklist]() | [Audit Policy Config]()

# Phase 3 - Attack & Defend

**Goal:** Simulate common AD attacks, detect them via logs, and remediate the underlying vulnerabilities

| Attack | Tool | Status |
| :--- | :--- | :--- |
| Password Spraying | CrackMapExec | [ ] Pending |
| Kerberoasting | Impacket/Rubeus | [ ] Pending |
| AS-REP Roasting | Impacket | [ ] Pending |
| BloodHound Enumeration | BloodHound + SharpHound | [ ] Pending |
| Pass-the-Hash | Mimikatz | [ ] Pending |
| DCSync | Mimikatz | [ ] Pending |

**Writeups:** (*Note*: Each writeup follows the format: **Attack->Evidence in Logs->Detection->Remediation**
[Kerberoasting]() | [BloodHound Analysis]() | [Pass-the-Hash]()

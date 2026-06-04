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

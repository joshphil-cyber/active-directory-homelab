## Overview

Created a custom OU (Organizational Unit) structure in Active Directory Users and Computers (ADUC) to organize users, computers and groups by department.

## Why this matters?

OUs allow Group Policy to be applied in a granular fashion to specific departments rather than the entire domain. Without OUs, you lose the ability to precisely delegate control or target policies.

## OU Structure
ad.lab
├── _Computers
│   ├── Workstations
│   └── Servers
├── _Groups
│   ├── Security
│   └── Distribution
└── _Users
    ├── IT
    ├── HR
    └── Finance


## Screenshots
![Expanded tree of the ad.lab domain OUs](screenshots/ou_expanded.png)

![Members of the GRP_HR_USERS OU](screenshots/members_tab_expanded.png)

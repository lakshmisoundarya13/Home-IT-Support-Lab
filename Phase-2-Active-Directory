# Phase 2 — Active Directory Domain Services (AD DS) Installation & Domain Controller Promotion

## Objective
Install the Active Directory Domain Services role on Windows Server 2019 and promote the server to a Domain Controller (DC01), establishing the foundation for domain management.

## Steps Completed

1. **Installed AD DS Role**
   - Opened Server Manager on the Windows Server 2019 VM
   - Navigated to *Add Roles and Features Wizard*
   - Selected **Active Directory Domain Services** role and installed required features

2. **Promoted Server to Domain Controller**
   - Launched the post-deployment configuration from Server Manager notifications
   - Selected **Add a new forest** (since this was a fresh domain build)
   - Set the root domain name to **lab.local**

3. **Configured Domain Controller Options**
   - Set Forest and Domain functional level to **Windows Server 2019**
   - Enabled **DNS Server** role as part of the promotion (required for AD)
   - Set a Directory Services Restore Mode (DSRM) password

4. **Completed Promotion and Restart**
   - Reviewed the prerequisites check
   - Completed the installation wizard
   - Server automatically restarted as a fully functioning Domain Controller

5. **Verified Domain Controller Status**
   - Confirmed the server hostname changed to **DC01**
   - Verified DNS role was installed and running alongside AD DS
   - Confirmed **lab.local** appeared as the active domain in Server Manager

## Network Configuration at this Stage

| Machine | Adapter | IP Address |
|---|---|---|
| DC01 | Ethernet 2 (Internal) | 192.168.1.1 |

## Outcome
DC01 is now a fully promoted Domain Controller for the **lab.local** domain, with DNS integrated and ready for Organizational Unit (OU), user, and group configuration in Phase 3.

## Screenshots
See `/screenshots` folder in this phase directory:
- `01-add-roles-wizard.png` — AD DS role selection
- `02-promote-to-dc.png` — Domain Controller promotion wizard
- `03-domain-verification.png` — lab.local confirmed active in Server Manager

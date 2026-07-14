# Phase 6 — Client Domain Join & Verification

## Objective
Join CLIENT01 to the **lab.local** domain and verify successful domain connectivity, authentication, and policy application.

## Steps Completed

1. **Configured Network Connectivity**
   - Set CLIENT01's network adapter to the same internal network as DC01

   | Machine | Adapter | IP Address |
   |---|---|---|
   | DC01 | Ethernet 2 (Internal) | 192.168.1.1 |
   | CLIENT01 | Ethernet 2 (Internal) | 192.168.1.2 |

   - Set CLIENT01's preferred DNS server to **192.168.1.1** (DC01) so it could resolve the domain

2. **Tested Network Connectivity**
   - Ran `ping 192.168.1.1` from CLIENT01
   - Confirmed **0% packet loss**, verifying network connectivity to DC01

3. **Joined CLIENT01 to the Domain**
   - Opened *System Properties > Change Settings > Change* on CLIENT01
   - Selected **Domain** and entered **lab.local**
   - Entered domain administrator credentials when prompted
   - Received the **"Welcome to the lab.local domain"** confirmation message
   - Restarted CLIENT01 to apply domain membership

4. **Logged in as a Domain User**
   - At the login screen, logged in as **lab\jsmith**
   - Successful authentication against the Domain Controller confirmed

5. **Verified Domain Join and Login**
   - Ran `hostname` — confirmed the machine name as **CLIENT01**
   - Ran `whoami` — confirmed the logged-in identity as **lab\jsmith**
   - Checked **Event Viewer > Windows Logs > Security** — confirmed **Event ID 4624** (successful logon) recorded for the jsmith authentication

## Outcome
CLIENT01 is successfully joined to the **lab.local** domain, with confirmed authentication of a department-scoped user account (**jsmith**) and audit-trail verification via Event Viewer. This completes the core Active Directory home lab build: domain controller, OU structure, users/groups, GPO enforcement, and client integration are all functioning together end-to-end.

## Screenshots
See `/screenshots` folder in this phase directory:
- `01-network-config.png` — IP configuration on CLIENT01
- `02-ping-test.png` — Successful ping to DC01
- `03-domain-join-wizard.png` — Welcome to lab.local domain message
- `04-domain-login.png` — Logged in as lab\jsmith
- `05-event-viewer-4624.png` — Event ID 4624 successful logon record

## Lab Summary
This concludes the Home IT Support Lab build:
1. Windows Server 2019 installation and setup
2. AD DS installation and Domain Controller promotion
3. Organizational Unit structure (IT Department, HR Department)
4. User accounts and security groups (jsmith/IT-Staff, sjones/HR-Staff)
5. Group Policy configuration (password & account lockout policy)
6. Client domain join and verification (CLIENT01)

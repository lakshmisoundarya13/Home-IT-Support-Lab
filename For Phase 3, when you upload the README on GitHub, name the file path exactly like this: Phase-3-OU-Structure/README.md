# Phase 3 — Organizational Unit (OU) Structure

## Objective
Design and implement an Organizational Unit structure within the **lab.local** domain to logically separate departments, simulating a real-world business environment for user and policy management.

## Steps Completed

1. **Opened Active Directory Users and Computers (ADUC)**
   - Accessed via Server Manager > Tools > Active Directory Users and Computers on DC01

2. **Created Organizational Units**
   - Right-clicked on the **lab.local** domain root
   - Selected **New > Organizational Unit**
   - Created the following OUs directly under lab.local:

   | OU Name | Purpose |
   |---|---|
   | **IT Department** | Container for IT staff users and IT-related security groups |
   | **HR Department** | Container for HR staff users and HR-related security groups |

3. **Structured for Departmental Separation**
   - Each OU was created to hold department-specific users and groups
   - This structure allows for targeted Group Policy application per department (implemented in Phase 5)

4. **Verified OU Creation**
   - Confirmed both OUs appeared correctly under the lab.local domain in ADUC
   - Confirmed OUs were empty and ready for user/group population (Phase 4)

## Outcome
The domain now has a clean two-department OU structure (**IT Department**, **HR Department**), providing the organizational foundation needed to scope user accounts, security groups, and Group Policy Objects by department.

## Screenshots
See `/screenshots` folder in this phase directory:
- `01-aduc-console.png` — Active Directory Users and Computers open
- `02-ou-structure.png` — IT Department and HR Department OUs visible under lab.local

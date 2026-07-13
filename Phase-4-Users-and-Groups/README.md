# Phase 4 — User Accounts & Security Groups

## Objective
Create test user accounts and security groups within the appropriate Organizational Units, and assign users to their respective department groups.

## Steps Completed

1. **Created User Accounts in ADUC**
   - Right-clicked the relevant OU > **New > User**
   - Set logon names, temporary passwords, and enforced password change at next logon

   | User | Username | Department | OU Location |
   |---|---|---|---|
   | John Smith | jsmith | IT Department | IT Department OU |
   | Sarah Jones | sjones | HR Department | HR Department OU |

2. **Created Security Groups**
   - Right-clicked the relevant OU > **New > Group**
   - Set Group scope to **Global** and Group type to **Security**

   | Group | Type | Department | OU Location |
   |---|---|---|---|
   | IT-Staff | Security Group — Global | IT Department | IT Department OU |
   | HR-Staff | Security Group — Global | HR Department | HR Department OU |

3. **Assigned Users to Groups**
   - Added **jsmith** as a member of **IT-Staff**
   - Added **sjones** as a member of **HR-Staff**
   - Verified group membership via the *Member Of* tab on each user account

4. **Verified Account Configuration**
   - Confirmed both accounts were enabled and correctly placed in their department OUs
   - Confirmed group memberships were correctly reflected in ADUC

## Outcome
Two department-based user accounts and matching security groups are fully configured, correctly scoped to their OUs. This structure enables department-specific Group Policy targeting in Phase 5.

## Screenshots
See `/screenshots` folder in this phase directory:
- `01-new-user-wizard.png` — Creating jsmith / sjones
- `02-security-groups.png` — IT-Staff and HR-Staff group properties
- `03-group-membership.png` — Member Of tab showing correct group assignment

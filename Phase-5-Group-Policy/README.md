# Phase 5 — Group Policy Object (GPO) Configuration

## Objective
Configure domain-wide security policies using Group Policy to enforce password complexity and account lockout rules, simulating enterprise-level security hardening.

## Steps Completed

1. **Opened Group Policy Management Console (GPMC)**
   - Accessed via Server Manager > Tools > Group Policy Management

2. **Created a New GPO**
   - Right-clicked **lab.local** > **Create a GPO in this domain, and Link it here**
   - Named the policy to reflect its security purpose (domain-wide password/lockout policy)

3. **Configured Password Policy Settings**
   - Navigated to: *Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy*

   | Setting | Value |
   |---|---|
   | Minimum password length | 8 characters |
   | Password must meet complexity requirements | Enabled |
   | Maximum password age | 90 days |
   | Enforce password history | 5 passwords remembered |

4. **Configured Account Lockout Policy Settings**
   - Navigated to: *Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy*

   | Setting | Value |
   |---|---|
   | Account lockout threshold | 5 invalid logon attempts |
   | Account lockout duration | 30 minutes |
   | Reset account lockout counter after | 30 minutes |

5. **Linked and Applied the GPO**
   - Confirmed the GPO was linked at the domain level (lab.local), applying to all users and computers within the domain
   - Ran `gpupdate /force` on DC01 to apply changes immediately

6. **Verified Policy Application**
   - Confirmed settings via **Group Policy Management** console under the linked GPO's settings report
   - Confirmed policy would apply domain-wide, including to CLIENT01 once joined (Phase 6)

## Outcome
A domain-wide password and account lockout policy is enforced across lab.local, aligning the lab environment with standard enterprise security baseline practices.

## Screenshots
See `/screenshots` folder in this phase directory:
- `01-gpmc-console.png` — Group Policy Management Console
- `02-password-policy-settings.png` — Password Policy configuration
- `03-lockout-policy-settings.png` — Account Lockout Policy configuration

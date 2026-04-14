# Module Three: Group Policy Hardening
**CYB-220 | Network Security**

## Objective
Identify the correct Group Policy Object (GPO) paths for a set of security settings needed to harden a virtual Windows PC, using the Windows 10 / Windows Server 2016 Policy Settings reference.

---

## How GPO Paths Work
Every Group Policy setting has a specific path in the GPO hierarchy:
- **User Configuration** — applies to user accounts/sessions
- **Computer Configuration** — applies to the machine regardless of who logs in
- Both flow through: `Configuration → Administrative Templates → [Category] → [Setting]`

---

## GPO Settings Configured

| Policy Name | Scope | Full GPO Path |
|---|---|---|
| Hide specified Control Panel items (hide user accounts) | User | `User Configuration\Administrative Templates\Control Panel` |
| Remove Task Manager | User | `User Configuration\Administrative Templates\System\Ctrl+Alt+Del Options\Remove Task Manager` |
| Remove Recycle Bin icon from desktop | User | `User Configuration\Administrative Templates\Desktop\Remove Recycle Bin icon from desktop` |
| Disable delete notifications on all volumes | Machine | `Computer Configuration\Administrative Templates\System\Filesystem\Disable Delete Notifications on all Volumes` |

---

## Security Rationale for Each Setting

**Hide user accounts in Control Panel:** Prevents users from viewing, modifying, or enumerating other accounts on the system — reducing the information available to an attacker who gains user-level access.

**Remove Task Manager:** Prevents users from killing security monitoring processes or viewing running processes that might reveal system configuration.

**Remove Recycle Bin from desktop:** Reduces accidental or intentional data recovery from deleted files by removing easy access to the Recycle Bin.

**Disable delete notifications:** Prevents the system from broadcasting file deletion events to all volumes — reducing information leakage in shared environments.

---

## Skills Demonstrated
`Windows Group Policy (GPO)` `System Hardening` `GPO Path Navigation` `User vs. Computer Configuration` `Windows 10 Security` `Windows Server 2016` `GNS3`

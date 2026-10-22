# NTFS Permissions and Access Control

## Objective

Configure and verify department-based access control on a Windows 11 virtual machine using local user accounts, security groups, NTFS permissions, and PowerShell.

## Environment

- OS: Windows 11
- Environment: VMware Workstation virtual machine
- Lab directory: `C:\Admin_Lab`
- Departments: HR, Finance, and IT
- Tools: PowerShell and `icacls`

## User and Group Configuration

The lab contains separate local user accounts and security groups for each department.

| Department | User account | Security group |
|---|---|---|
| HR | `HR_User` | `HR` |
| Finance | `Finance_User` | `Finance` |
| IT | `IT_User` | `IT` |

## NTFS Permission Configuration

The department folders have Modify (`M`) permissions assigned to their corresponding groups. The built-in Administrators group and SYSTEM have Full Control (`F`) in the observed ACL output.

The permissions were inspected using:

```powershell
icacls C:\Admin_Lab\HR
icacls C:\Admin_Lab\Finance
icacls C:\Admin_Lab\IT
```

## Access Verification

The HR account was used to test access to the department folders.

| Test | Observed result |
|---|---|
| List `C:\Admin_Lab\HR` | Access granted; `employe.txt` was listed |
| List `C:\Admin_Lab\Finance` | Access denied |
| List `C:\Admin_Lab\IT` | Access denied |

The denied operations returned `UnauthorizedAccessException` in PowerShell.

These tests demonstrate that the HR account could access its own department folder but was denied access to the Finance and IT folders during the recorded session.

## Evidence

- [NTFS permission configuration](../screenshots/03-ntfs-permissions.png)
- [HR access verification](../screenshots/04-ntfs-access-verification.png)

## Security Relevance

Department-based NTFS permissions help enforce least privilege by limiting access to files and folders according to job responsibilities.

Testing with a standard user account is important because an administrator's elevated privileges can produce different access results.

## Limitations

Only the HR account's access behavior was tested and recorded in this exercise. Finance and IT access behavior has not been independently verified in the documented tests.

Windows file-access auditing is a separate activity and requires appropriate audit policies and folder auditing settings before corresponding events can be expected in the Security log.

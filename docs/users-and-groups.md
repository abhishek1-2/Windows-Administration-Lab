# Windows Local Users and Groups Management

## Objective

Create and inspect local Windows user accounts and security groups to understand identity management and access control.

## Environment

- Operating System: Windows 11
- Environment: VMware Workstation virtual machine
- Tools: PowerShell and Windows local account management utilities

## User Accounts

The lab includes separate local accounts for three departments.

| Department | Account | Purpose |
|---|---|---|
| HR | `HR_User` | HR department access testing |
| Finance | `Finance_User` | Finance department access testing |
| IT | `IT_User` | IT department access testing |

Additional built-in and administrative accounts were inspected during the exercise.

## Security Groups

The following local security groups were created and inspected:

- `HR`
- `Finance`
- `IT`

Each department's corresponding user account was verified as a member of its intended group using PowerShell.

## Commands Used

### List local users

```powershell
Get-LocalUser |
    Format-Table Name, Enabled, LastLogon
```

### List local groups

```powershell
Get-LocalGroup |
    Format-Table Name, Description -AutoSize
```

### Inspect department-group membership

```powershell
Get-LocalGroupMember -Group "HR"
Get-LocalGroupMember -Group "Finance"
Get-LocalGroupMember -Group "IT"
```

### Inspect the Administrators group

```powershell
Get-LocalGroupMember -Group "Administrators"
```

### Inspect the current user's group memberships

```powershell
whoami /groups
```

## Results

The recorded PowerShell output showed:

- The HR account belonged to the HR group.
- The Finance account belonged to the Finance group.
- The IT account belonged to the IT group.
- Local user accounts, local groups, and Administrators group membership could be inspected through PowerShell.

## Security Relevance

Separate accounts and groups make permissions easier to manage and help enforce least privilege. Assigning permissions to groups rather than individual users also makes administration more scalable.

Membership in the Administrators group grants extensive privileges, so administrative access should be limited to accounts that require it.

## Evidence

See the screenshots in the repository's `screenshots/` folder:

- `02-local-users-groups.png`
- `02b-group-membership.png`

## Scope

This exercise documents account and group inspection. It does not demonstrate domain-based Active Directory administration or prove that every department's folder permissions have been independently tested.

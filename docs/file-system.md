# Windows File System Exploration

## Objective

Explore the Windows directory structure, system folders, user profiles, and environment variables using PowerShell.

## Environment

- Operating System: Windows 11
- Environment: VMware Workstation virtual machine
- Tool: Windows PowerShell

## Areas Explored

The exercise examined:

- The Windows system directory
- `System32`
- `Program Files`
- The `Users` directory
- The current user's profile folders
- Windows environment variables

## Commands Used

### Inspect Windows directories

```powershell
Get-ChildItem C:\Windows -Directory |
    Select-Object -First 10 Name
```

### Inspect important system paths

```powershell
Get-Item C:\Windows\System32, "C:\Program Files", C:\Users |
    Select-Object FullName, Attributes
```

### Inspect environment variables

```powershell
$env:SystemRoot
$env:USERPROFILE
$env:APPDATA
```

### List directories in the current user profile

```powershell
Get-ChildItem $env:USERPROFILE -Directory |
    Select-Object Name, FullName
```

## Results

The commands displayed Windows system directories, directory attributes, environment variable values, and folders belonging to the current user profile.

The exercise also revealed the `Windows_admin_data` directory within the profile, which was used during the administration lab.

## Security Relevance

Understanding the Windows filesystem helps administrators and security analysts locate application files, user data, system components, and configuration locations.

User profile directories and application-data folders can also be relevant when investigating suspicious scripts, unexpected executables, or persistence mechanisms.

## Evidence

See the filesystem screenshot in the repository's `screenshots/` folder:

- `01-file-system.png`

## Scope

This exercise focused on read-only filesystem inspection. It did not involve modifying protected system directories or changing filesystem permissions.

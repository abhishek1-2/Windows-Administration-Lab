# Windows Administration Lab

A hands-on Windows administration lab built to develop a practical understanding of the Windows operating system using the command line.

This project is part of my cybersecurity/SOC learning path. The goal is not simply to memorize Windows commands, but to understand how Windows manages files, users, permissions, processes, services, networking, logs, and system configuration.

## Objectives

* Understand the Windows file system
* Work with Windows users and groups
* Understand NTFS permissions and ACLs
* Manage processes and services
* Use PowerShell for system administration
## Environment

* Operating System: Windows 11
* Environment: Virtual Machine
* Primary Interface: Command Line / PowerShell
* Tools: CMD, PowerShell, Windows built-in utilities

## Topics Covered

### 1. Windows File System

Topics include:

* Windows directory structure
* System directories
* Program Files
* Users and user profiles
* AppData
* System32
* Environment variables
* File and directory management from the command line

### 2. Users and Groups

Topics include:

* Creating and managing local users
* Creating and managing groups
* User membership
* Administrative privileges
* Checking the current user and group membership

### 3. NTFS Permissions and ACLs

Topics include:

* NTFS permissions
* Access Control Lists (ACLs)
* Permission inheritance
* Explicit vs inherited permissions
* Permission types
* `icacls`
* Testing access between different users

### 4. Processes

Topics include:

* Running processes
* Process IDs (PID)
* Parent and child processes
* Process monitoring
* Starting and terminating processes
* Investigating processes from the command line

### 5. Windows Services

Topics include:

* Listing services
* Starting and stopping services
* Service states
* Service configuration
* Understanding how Windows services operate

### 6. Windows Networking

Topics include:

* IP configuration
* Network interfaces
* Active connections
* Listening ports
* TCP/UDP
* DNS configuration
* Network troubleshooting from the command line

### 7. PowerShell

Topics include:

* PowerShell fundamentals
* System administration commands
* Process management
* Service management
* User and group management
* File system operations
* Networking commands

### 8. Windows Event Logs

Topics include:

* Event Viewer
* Security logs
* System logs
* Application logs
* PowerShell logs
* Understanding how system activity generates events

These concepts will later be connected to my SOC lab and SIEM investigations.

## SOC RELEVANCE 
##  Project Documentation

Explore the practical exercises documented in this repository:

- [Windows File System Exploration](docs/file-system.md)
- [Local Users and Groups Management](docs/users-and-groups.md)
- [NTFS Permissions and Access Control](docs/ntfs-permissions.md)

##  Practical Evidence

Screenshots of the lab exercises are available in the [`screenshots/`](screenshots/) directory.

The evidence includes:

- Windows directory structure and environment variables
- Local user accounts and department-group membership
- NTFS permissions and ACL entries
- Access granted and denied during HR account testing

##  Key Learning Outcomes

- Inspecting Windows system directories using PowerShell
- Managing local accounts and security groups
- Applying the principle of least privilege through NTFS permissions
- Verifying access behavior using standard user accounts
- Documenting administrative actions and observed security results


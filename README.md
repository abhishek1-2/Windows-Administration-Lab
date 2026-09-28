# Windows Administration Lab

A hands-on Windows administration lab built to develop a practical understanding of the Windows operating system using the command line.

This project is part of my cybersecurity/SOC learning path. The goal is not simply to memorize Windows commands, but to understand how Windows manages files, users, permissions, processes, services, networking, logs, and system configuration.

## Objectives

* Understand the Windows file system
* Work with Windows users and groups
* Understand NTFS permissions and ACLs
* Manage processes and services
* Learn Windows networking from the command line
* Use PowerShell for system administration
* Understand Windows Event Logs
* Explore the Windows Registry
* Work with scheduled tasks
* Understand Windows security concepts relevant to SOC analysis

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

### 9. Windows Registry

Topics include:

* Registry structure
* Registry keys and values
* Common registry locations
* Using the command line to inspect registry information
* Security relevance of registry modifications

### 10. Scheduled Tasks

Topics include:

* Viewing scheduled tasks
* Creating scheduled tasks
* Managing scheduled tasks
* Understanding why scheduled tasks are important for system administration and security monitoring

## SOC Relevance

Understanding the operating system is essential for security operations.

When investigating a security alert, an analyst may need to determine:

```text
Who performed the action?
        ↓
What process executed?
        ↓
What user was involved?
        ↓
What file or system resource was accessed?
        ↓
What network connection was created?
        ↓
What Windows event recorded the activity?
        ↓
Can the activity be detected in a SIEM?
```

This lab is designed to build that operating-system knowledge before moving deeper into SOC detection and incident investigation.

## What I Am Learning

This repository documents my hands-on work, commands, experiments, observations, and troubleshooting rather than simply listing topics that I have studied.

More sections will be added as the lab develops.

## Future Integration

This Windows lab will eventually be connected to my SOC environment using:

* Sysmon
* Splunk
* Windows Event Logs
* SIEM-based detection
* Security investigation scenarios

The objective is to move from **Windows administration → Windows security visibility → SOC investigation**.


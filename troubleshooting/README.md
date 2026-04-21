# Troubleshooting

## Purpose

Documents recurring problems, root causes, and fixes encountered during Active Directory lab deployment and validation.

## Current Focus Areas

- domain join failures
- DNS misconfiguration
- domain logon failures
- workstation trust relationship issues
- Group Policy refresh and validation issues

## Phase 3 Troubleshooting Topics

### Domain Join

Common causes of failed domain join:

- client DNS points to the wrong server
- the workstation cannot resolve `corp.local`
- the join account lacks sufficient privileges
- the computer account is stale or duplicated

### Authentication

Common causes of failed domain logon:

- wrong username format
- invalid credentials
- broken trust relationship
- incomplete domain join
- name resolution problems

### Trust Relationship

If the workstation shows:

`The trust relationship between this workstation and the primary domain failed`

validate and repair with:

```powershell
Test-ComputerSecureChannel
Test-ComputerSecureChannel -Repair -Credential (Get-Credential)

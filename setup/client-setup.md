# Phase 3 — Domain-Joined Windows Client Deployment (`CLIENT01`)

## Purpose

This runbook documents the deployment of the first domain-joined workstation in the `corp.local` lab domain.

Phase 3 extends the environment beyond the domain controller and validates real client-side Active Directory functionality, including:

- DNS-based domain discovery
- Domain join
- Domain user logon
- Workstation trust validation
- Initial Group Policy processing readiness

## Lab Context

- Domain: `corp.local`
- Domain Controller: `DC01`
- DC01 IP: `10.0.0.10`
- Client Name: `CLIENT01`
- Client IP: `10.0.0.101`
- Client OU: `OU=_WORKSTATIONS,DC=corp,DC=local`

## VirtualBox Configuration

### Recommended VM Specs

- Guest OS: Windows 10 Pro or Windows 11 Pro (I used Windows 10 Enterprise & it worked fine)
- vCPU: 2
- RAM: 4 GB minimum, 6 GB preferred
- Disk: 64 GB dynamically allocated

### Network Adapter Design

#### Adapter 1
- Mode: `Internal Network`
- Network Name: `AD-LAB`

#### Adapter 2
- Not required for domain join
- May be temporarily enabled later as `NAT` for updates if needed

## Windows Client Configuration

### Host Naming

Set the workstation name to:

`CLIENT01`

### Static IPv4 Configuration

- IP address: `10.0.0.101`
- Subnet mask: `255.255.255.0`
- Default gateway: _blank for this phase_
- Preferred DNS server: `10.0.0.10`

## Prestage the Computer Account (Recommended)

### GUI

On `DC01`:

1. Open **Active Directory Users and Computers**
2. Browse to **_WORKSTATIONS**
3. Right-click → **New** → **Computer**
4. Name the object `CLIENT01`

### PowerShell

```powershell
New-ADComputer -Name "CLIENT01" -Path "OU=_WORKSTATIONS,DC=corp,DC=local" -Enabled $true

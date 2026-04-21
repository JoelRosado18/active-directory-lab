# Architecture

## Purpose

Defines the network and system design of the Active Directory lab environment.

## Current Design

### Domain Controller

- `DC01`
- Windows Server 2022
- Roles:
  - AD DS
  - DNS
- Internal IP:
  - `10.0.0.10`

### Domain Client

- `CLIENT01`
- Windows client VM
- Internal IP:
  - `10.0.0.101`
- Domain membership:
  - `corp.local`

### AI Node

- `AI01`
- Raspberry Pi running Ollama + Gemma
- Present in the environment but not yet integrated into AD workflows

## Network Design

### VirtualBox Networks

- `NAT`
  - Used on `DC01` for internet access
- `Internal Network: AD-LAB`
  - Used for isolated domain communication between lab systems

## Phase 3 Architecture Value

Phase 3 introduces the first managed workstation into the environment. This enables:

- domain user logon testing
- workstation trust validation
- future workstation GPO targeting
- endpoint-focused troubleshooting
- more realistic enterprise-style architecture

## Notes

The lab remains segmented and intentionally controlled to keep domain communication isolated from the host and from unnecessary external exposure.

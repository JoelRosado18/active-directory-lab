# Active Directory Home Lab

## Overview

This project is an enterprise-style Active Directory lab built in VirtualBox to simulate real-world system administration and security environments.

The lab is designed to demonstrate hands-on experience with:

* Active Directory Domain Services (AD DS)
* DNS configuration
* Group Policy (GPO)
* User and group management (RBAC)
* Domain-joined systems
* Security hardening and auditing
* AI-assisted log analysis (Raspberry Pi)

---

## Architecture

* Domain Controller: DC01 (Windows Server 2022)
* Network Design:

  * NAT (internet access)
  * Internal Network: AD-LAB
* AI Node:

  * Raspberry Pi running local LLM (Ollama + Gemma)

---

## Lab Goals

* Simulate enterprise Active Directory environments
* Practice system administration and troubleshooting
* Implement security best practices
* Integrate modern tooling (AI for log analysis)

---

## Project Phases

### Phase 1 — Domain Controller Deployment ✅

* Installed Windows Server 2022
* Configured AD DS and DNS
* Implemented static IP and network segmentation
* Applied initial security hardening

### Phase 2 — Active Directory Structure (In Progress)

* Organizational Units (OUs)
* Users and Groups (RBAC)
* Naming conventions

### Phase 3 — Client Integration (Planned)

* Domain-joined Windows clients
* Authentication validation

### Phase 4 — Group Policy & Security (Planned)

* GPO baseline implementation
* Security configurations

### Phase 5 — File Services (Planned)

* Shared folders
* NTFS permissions

### Phase 6 — Monitoring & Logging (Planned)

* Event log analysis
* AI-assisted insights

---

## Repository Structure

```
setup/
infrastructure/
```

---

## Documentation

Detailed runbooks are available in each section of the repository.

---

## Status

🚧 In Progress — Continuously expanding and refining the environment

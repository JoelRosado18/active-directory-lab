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
- Installed Windows Server 2022 on DC01
- Configured NAT + Internal Network (AD-LAB)
- Assigned static IP addressing
- Installed AD DS and DNS
- Promoted `corp.local`
- Applied initial hardening and validation

### Phase 2 — Active Directory Structure ✅
- Designed enterprise-style OU hierarchy
- Created departmental and administrative OUs
- Implemented user naming standards
- Implemented group naming standards
- Built RBAC group model using Global and Domain Local groups
- Created test users and separated privileged admin identity
- Applied initial domain password and account lockout policy

### Phase 3 — Client Integration (Planned)
- Deploy Windows client VM
- Join client to `corp.local`
- Validate authentication, DNS, and policy application

### Phase 4 — Group Policy & Security Hardening (Planned)
- Expand workstation and server GPO baselines
- Apply administrative templates and security settings
- Harden client and member-server configuration

### Phase 5 — File Services (Planned)
- Deploy shared folders and mapped access model
- Apply NTFS and share permissions
- Validate access through RBAC groups

### Phase 6 — Monitoring & Logging (Planned)
- Review Windows event logs
- Build investigation workflows
- Prepare AI-assisted log analysis integration

---

## Repository Structure

``
active-directory-lab/
├── ad-structure/
├── architecture/
├── file-services/
├── group-policy/
├── infastructure/
├── security/
├── setup/
└── troubleshooting/ 
``

---

## Documentation

Detailed runbooks are available in each section of the repository.

---

## Status

🚧 In Progress — Continuously expanding and refining the environment

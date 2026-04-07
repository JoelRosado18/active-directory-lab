# Active Directory Home Lab

## Overview
This project simulates a secure enterprise Active Directory environment using virtualization. The lab is designed to develop hands-on system administration and security skills relevant to real-world IT roles.

## Development Approach

This lab follows a structured, documentation-driven approach similar to enterprise environments. AI-assisted tools were used to enhance workflow efficiency and maintain consistent, professional documentation standards.

All configurations and scenarios were implemented manually and tested within the environment.

## Objectives
- Deploy and manage a Windows Server Domain Controller
- Implement Active Directory (AD DS) and DNS
- Configure Group Policy for security enforcement
- Manage users, groups, and organizational units
- Implement file sharing with proper access controls
- Simulate real-world troubleshooting scenarios
- Apply system hardening and security best practices

## Environment
- Hypervisor: VirtualBox
- Host System: 32GB RAM, Ryzen 7 3700X
- Domain: corp.local

## Architecture
The lab uses a segmented virtual network:
- NAT Adapter: Internet access
- Internal Network (AD-LAB): Isolated domain environment

### AI Utility Node (AI01)
- Raspberry Pi 4 running local AI (Gemma via Ollama)
- Designed for future log analysis and security automation
- Currently isolated from AD environment to maintain clean deployment baseline

## Key Technologies
- Windows Server 2022
- Active Directory Domain Services (AD DS)
- DNS
- Group Policy (GPO)
- NTFS Permissions
- Virtual Networking

## Project Structure
- `architecture/` → Network design and diagrams
- `setup/` → Initial system deployment (DC, clients)
- `ad-structure/` → Organizational Units, users, groups
- `group-policy/` → Security and configuration policies
- `file-services/` → Shared resources and permissions
- `security/` → Hardening and best practices
- `troubleshooting/` → Issues and resolutions
- `infastructure/` → Ai-node configuration

## Skills Demonstrated
- Active Directory administration
- Windows Server configuration
- Network segmentation
- Access control and identity management
- Security hardening
- Troubleshooting and root cause analysis

## Status
🚧 In Progress – Building foundational infrastructure

## Author
Joel Rosado

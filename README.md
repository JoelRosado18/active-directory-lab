# Active Directory Home Lab

## Overview
This project simulates a secure enterprise Active Directory environment using virtualization. The lab is designed to develop hands-on system administration and security skills relevant to real-world IT roles.

## Development Notes

This project was developed using a combination of hands-on configuration, independent research, and AI-assisted guidance for structuring documentation and workflows.

All system configurations, troubleshooting, and implementation steps were performed and validated within the lab environment.

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
- Host System: 16GB RAM, Ryzen 7 3700X
- Domain: corp.local

## Architecture
The lab uses a segmented virtual network:
- NAT Adapter: Internet access
- Internal Network (AD-LAB): Isolated domain environment

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

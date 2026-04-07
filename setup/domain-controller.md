---

## Phase 1 Completion — Domain Controller (DC01)

### Validation

* Verified domain login (corp\administrator)
* Confirmed AD DS (NTDS) and DNS services are running
* Executed `dcdiag` to validate domain controller health
* Verified DNS resolution for `corp.local`

### Security Hardening

* Installed Windows updates using `sconfig`
* Verified Windows Firewall enabled across all profiles
* Disabled Print Spooler service to reduce attack surface
* Enabled system-wide auditing (success and failure)

### Network Configuration

* Configured dual-NIC setup:

  * NAT adapter for internet access
  * Internal network (`AD-LAB`) for domain traffic
* Assigned static IP `10.0.0.10` to internal interface
* Configured DNS to point to self (10.0.0.10)

### Outcome

Successfully deployed and hardened a Windows Server 2022 Domain Controller with:

* Active Directory Domain Services (AD DS)
* DNS
* Secure baseline configuration

### Snapshot

Created VirtualBox snapshot:
`DC01-POST-AD-BASELINE`

This snapshot serves as a rollback point before introducing additional infrastructure (clients, GPOs, etc.).

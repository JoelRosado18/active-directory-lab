# Group Policy Configurations

## Phase 2 Scope
Phase 2 applies the initial **domain account policy baseline** for `corp.local`.

## Policy Area
Configured in:
- `Default Domain Policy`

## Password Policy
Path:
`Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Password Policy`

Configured values:
- Enforce password history: `24`
- Maximum password age: `90 days`
- Minimum password age: `1 day`
- Minimum password length: `12`
- Password must meet complexity requirements: `Enabled`

## Account Lockout Policy
Path:
`Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy`

Configured values:
- Account lockout threshold: `5 invalid logon attempts`
- Account lockout duration: `15 minutes`
- Reset account lockout counter after: `15 minutes`

## Purpose
These settings establish an initial domain security baseline and prepare the lab for future client testing and authentication validation.

## Notes
Broader workstation and server hardening GPOs are planned for a later phase.

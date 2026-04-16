# Active Directory Structure

## Purpose
This section documents the identity and object organization model used in the `corp.local` lab domain.

## Scope
Phase 2 introduces:
- Organizational Unit (OU) design
- User naming conventions
- Group naming conventions
- RBAC using Global and Domain Local groups
- Administrative account separation

## Design Goals
- Organize objects in a way that scales cleanly
- Support future Group Policy targeting
- Support future file service permissions
- Reflect real-world system administration practices

## Included Documentation
- `ous.md` — OU hierarchy and placement logic
- `users-groups.md` — users, groups, naming, and RBAC model

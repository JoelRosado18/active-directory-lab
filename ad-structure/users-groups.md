# Users and Groups

## Objective
Implement a repeatable user and group strategy aligned with enterprise Active Directory administration.

## User Naming Convention
Standard user accounts:
- `firstname.lastname`

Administrative user accounts:
- `adm-firstname.lastname`

## Example Users
- `john.doe` — IT standard account
- `lisa.garcia` — HR standard account
- `noah.bennett` — Finance standard account
- `adm-john.doe` — separate privileged admin account

## Group Naming Convention

### Global Security Groups
Used to collect users by role or department.

Format:
- `GG_<Department>_<Role>`

Examples:
- `GG_IT_Admins`
- `GG_IT_Users`
- `GG_HR_Users`
- `GG_FIN_Users`

### Domain Local Security Groups
Used to represent resource permissions.

Format:
- `DL_<Resource>_<Permission>`

Examples:
- `DL_FS_IT_Full`
- `DL_FS_HR_Modify`
- `DL_FS_FIN_Modify`

### Distribution Groups
Used for communication-style grouping, not security permissions.

Format:
- `DG_<Purpose>`

Example:
- `DG_All_Staff`

## RBAC Model
This lab uses an AGDLP-style model:

``
User → Global Group → Domain Local Group → Permission
``

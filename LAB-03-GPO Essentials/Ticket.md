# IT Service Request - TICKET-2024-003

## Ticket Information
| Field | Value |
|-------|-------|
| **Ticket ID** | TICKET-2025-003 |
| **Request Type** | Service Request |
| **Priority** | Medium |
| **Category** | Group Policy / Configuration Management |
| **Status** | Completed |
| **Created Date** | 2025-12-11 |
| **Completed Date** | 2025-12-11 |
| **Requested By** | IT Manager |
| **Assigned To** | Systems Administrator |

## Request Summary
**Title:** Implement Group Policy for Desktop Standardization and Access Restrictions

## Description
The organization requires standardized desktop configurations across all workstations and role-based access restrictions. Standard users should have limited system access to prevent unauthorized changes, while IT staff require full administrative capabilities for troubleshooting.

## Work Performed
Created Group Policy Objects using the Group Policy Management Console to enforce desktop standards and departmental restrictions. A domain-level GPO was implemented for universal settings including corporate wallpaper and screensaver policies.

Department-specific GPOs were created and linked to Sales and Marketing OUs to restrict Control Panel access and prevent unauthorized system modifications. A separate GPO was linked to the IT Department OU ensuring full system access for technical staff.

Configured logon scripts to execute at user sign-in for consistent environment setup. Verified all policies using gpresult command-line tool and generated HTML reports for documentation.

## Configuration Details
| GPO Name | Target | Key Settings |
|----------|--------|--------------|
| Desktop Standards | Domain | Wallpaper, screensaver timeout 5 min |
| Sales-Restrictions | Sales OU | Control Panel disabled |
| Marketing-Restrictions | Marketing OU | Control Panel disabled |
| IT-FullAccess | IT OU | No restrictions applied |

## Testing & Validation
- Verified GPO links in Group Policy Management Console
- Tested restrictions by logging in as Sales department user
- Confirmed IT users retain full system access
- Generated gpresult reports on client machine
- Documented GPO processing order and inheritance

## Resolution
Group Policy infrastructure successfully implemented. Desktop standardization applied domain-wide. Department-specific restrictions in place and verified. IT staff retain necessary access for support functions.

## Status
✅ **Completed**

## Attachments
- Screenshot: GPMC with GPO structure
- Screenshot: GPO Editor settings
- Screenshot: Control Panel blocked for restricted user
- Screenshot: gpresult /H report

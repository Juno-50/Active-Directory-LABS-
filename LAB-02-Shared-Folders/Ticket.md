# IT Service Request - TICKET-2024-002

## Ticket Information
| Field | Value |
|-------|-------|
| **Ticket ID** | TICKET-2025-002 |
| **Request Type** | Service Request |
| **Priority** | Medium |
| **Category** | File Services / Infrastructure |
| **Status** | Completed |
| **Created Date** | 2025-12-10 |
| **Completed Date** | 2025-12-10 |
| **Requested By** | IT Manager |
| **Assigned To** | Systems Administrator |

## Request Summary
**Title:** Configure Departmental Shared Folders with Appropriate Access Controls

## Description
Following the creation of departmental organizational units and security groups, the organization requires dedicated shared storage for each department. This enables secure file collaboration within departments while preventing unauthorized cross-departmental access. Automatic drive mappings are also required to streamline user experience.

## Work Performed
Created centralized folder structure at `C:\Shares` on DC01 with dedicated subfolders for IT, Sales, and Marketing departments. Disabled NTFS inheritance on each folder and applied explicit permissions granting Modify access to respective department groups only. Domain Admins retain Full Control across all shares.

Network shares were created via Server Manager with share-level permissions aligned to NTFS settings. A company-wide share was also configured with read access for all domain users.

Group Policy Preferences were used to deploy automatic drive mappings. Three GPOs were created and linked to their respective OUs, assigning drive letters S: for IT, Sales, and Marketing departments.

## Configuration Details
| Share Name | Path | Drive Letter | Access Group |
|------------|------|--------------|--------------|
| IT Share | `\\corp.juno.com\IT Share` | S: | IT Department |
| Sales Share | `\\corp.juno.com\Sales Share` | S: | Sales Department |
| Marketing Share | `\\corp.juno.com\Marketing Share` | S: | Marketing Department |

## Testing & Validation
- Verified NTFS and share permissions on all departmental folders
- Confirmed drive mappings apply correctly on Windows 11 client
- Tested cross-department access restrictions—users denied access to other departments
- Validated GPO application using `gpresult /R`

## Resolution
All departmental shared folders configured and secured. Drive mappings deployed successfully via Group Policy. Users now have automatic access to their department's shared storage upon login.

## Status
✅ **Completed**

## Attachments
- Screenshot: Folder structure and NTFS permissions
- Screenshot: Share configuration in Server Manager
- Screenshot: GPO drive mapping settings
- Screenshot: Mapped drives on client machine

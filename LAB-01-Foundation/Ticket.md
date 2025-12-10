# IT Service Request - TICKET-2024-001

## Ticket Information
| Field | Value |
|-------|-------|
| **Ticket ID** | TICKET-2025-001 |
| **Request Type** | Service Request |
| **Priority** | High |
| **Category** | Infrastructure / Identity |
| **Status** | Completed |
| **Created Date** | 2025-12-09 |
| **Completed Date** | 2025-12-09 |
| **Requested By** | IT Director |
| **Assigned To** | Systems Administrator |

## Request Summary
**Title:** Deploy Active Directory Infrastructure and Create Departmental Structure

## Description
The organization requires a centralized identity management solution to manage user authentication, authorization, and resource access. An Active Directory domain must be established with a logical structure that separates users by department for simplified administration and policy management.

## Work Performed
Installed Active Directory Domain Services role on Windows Server 2025 and promoted the server to a Domain Controller, establishing the corp.juno.com domain. DNS was configured automatically during promotion to support AD name resolution.

Created three Organizational Units representing the company's departmental structure: IT Department, Sales Department, and Marketing Department. User accounts were provisioned for staff members and placed in their respective OUs based on department.

Security groups were created within each OU following the naming convention [Department]_Department. All users were added to their corresponding departmental group to enable group-based permission management.

A Windows 11 workstation was joined to the domain to validate user authentication and domain functionality.

## Configuration Details
| Organizational Unit | Security Group | Users Created |
|---------------------|----------------|---------------|
| IT Department | IT_Department | [count] |
| Sales Department | Sales_Department | [count] |
| Marketing Department | Marketing_Department | [count] |

## Domain Information
| Property | Value |
|----------|-------|
| Domain Name | corp.juno.com |
| Domain Controller | DC01 |
| Forest Functional Level | Windows Server 2025 |
| Domain Functional Level | Windows Server 2025 |

## Testing & Validation
- Verified all OUs created and visible in ADUC
- Confirmed user accounts exist in correct OUs
- Validated group memberships using PowerShell `Get-ADGroupMember`
- Tested domain authentication from Windows 11 client
- Verified DNS resolution for domain resources

## Resolution
Active Directory domain successfully deployed. Departmental OU structure implemented with corresponding user accounts and security groups. Domain client joined and authenticated without issue. Environment ready for Group Policy and shared resource configuration.

## Status
✅ **Completed**

## Attachments
- Screenshot: Server Manager showing AD DS role installed
- Screenshot: OU structure in ADUC
- Screenshot: User accounts in departmental OUs
- Screenshot: Security group memberships
- Screenshot: Successful domain login on client

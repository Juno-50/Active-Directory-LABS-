# Lab 1: Active Directory Foundation Setup

## Environment
- **Hypervisor:** VMware Workstation
- **Server OS:** Windows Server 2025
- **Domain:** corp.juno.com
- **Domain Controller:** DC01

## Objective
Establish the foundational Active Directory structure by creating organizational units, user accounts, and security groups to support a multi-department organization.

## Summary
This lab established the core Active Directory infrastructure for the organization. A logical OU structure was designed and implemented to separate users by department, enabling targeted Group Policy application and simplified administration.

User accounts were created for each department and placed in their respective OUs. Security groups were created within each OU to facilitate permission management—allowing access to be granted to groups rather than individual users. Users were added as members of their departmental security groups.

This foundation supports future configurations including shared folder permissions, Group Policy deployment, and delegated administration.

## Tasks Completed
- Installed and configured Active Directory Domain Services
- Promoted server to Domain Controller for corp.juno.com
- Created departmental Organizational Units:
  - IT Department
  - Sales Department
  - Marketing Department
- Created user accounts for each department
- Moved users to their respective OUs
- Created security groups within each OU:
  - IT Support Team
  - Sales Team
  - Marketing Department
- Added users to their corresponding departmental groups
- Joined Windows 11 client to the domain

## Technologies Used
- Windows Server 2025 Active Directory Domain Services
- Active Directory Users and Computers (ADUC)
- DNS Server Role
- Domain Join

## Verification
- Confirmed OU structure in Active Directory Users and Computers
- Verified user accounts are in correct OUs
- Confirmed group memberships for all users
- Successfully authenticated domain users on Windows 11 client

## Status
✅ **Lab Completed Successfully**

## Screenshots
See `/screenshots` folder for evidence of:
- OU structure in ADUC
- User accounts in departmental OUs
- Security group properties showing members
- Domain-joined client authentication

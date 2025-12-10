# Lab 2: Shared Folders & NTFS Permissions

## Environment
- **Hypervisor:** VMware Workstation
- **Server OS:** Windows Server 2025
- **Domain:** corp.juno.com
- **Domain Controller:** DC01

## Objective
Configure departmental shared folders with appropriate NTFS and share permissions, and implement automatic drive mappings via Group Policy for each organizational unit.

## Summary
This lab focused on creating a secure file sharing infrastructure for the organization. A centralized folder structure was created on the domain controller to host departmental shares for IT, Sales, and Marketing departments, along with a company-wide shared folder accessible to all domain users.

NTFS permissions were configured using the principle of least privilege—inheritance was disabled on each departmental folder and explicit permissions were assigned to ensure users can only access their own department's resources. Share permissions were layered on top to provide an additional level of access control.

Group Policy was used to automate network drive mappings. Separate GPOs were created and linked to each departmental OU, ensuring users automatically receive their mapped drive upon login without manual configuration.

## Tasks Completed
- Created folder structure at `C:\Shares` with departmental subfolders
- Disabled inheritance and configured explicit NTFS permissions per department
- Created network shares with appropriate share-level permissions
- Configured company-wide shared folder with read access for all domain users
- Created and linked drive mapping GPOs to each departmental OU
  - IT Department → S: drive
  - Sales Department → S: drive
  - Marketing Department → S: drive
- Verified drive mappings on domain-joined Windows 11 client

## Technologies Used
- Windows Server 2025 File and Storage Services
- NTFS Permissions
- SMB File Sharing
- Group Policy Preferences (Drive Maps)

## Verification
- Logged in as users from each department and confirmed correct drive mapping
- Verified access restrictions—users cannot access other departments' shares
- Confirmed GPO application using `gpresult /R`

## Status
✅ **Lab Completed Successfully**

## Screenshots
See `/screenshots` folder for evidence of:
- Folder structure and NTFS permissions
- Share configuration in Server Manager
- GPO drive mapping settings
- Mapped drives on client machine

# Lab 3: Group Policy Essentials

## Environment
- **Hypervisor:** VMware Workstation
- **Server OS:** Windows Server 2025
- **Domain:** corp.juno.com
- **Domain Controller:** DC01

## Objective
Understand Group Policy fundamentals and implement common GPO configurations used in enterprise environments to standardize user experience and enforce basic restrictions.

## Summary
This lab introduced Group Policy as a centralized management tool for controlling user and computer settings across the domain. GPOs were created to standardize desktop configurations, apply department-specific restrictions, and automate common administrative tasks.

The lab covered GPO creation, linking to OUs, and understanding how policies are inherited and applied. Department-specific policies were implemented to restrict Control Panel access for standard users while allowing IT staff full access. Logon scripts were configured to provide a consistent user experience.

Group Policy Results (gpresult) and the Resultant Set of Policy (RSoP) were used to verify policy application and troubleshoot issues—essential skills for any tech support role.

## Tasks Completed
- Created and linked GPOs to departmental OUs
- Configured desktop standardization settings (wallpaper, screensaver)
- Restricted Control Panel access for Sales and Marketing users
- Allowed full system access for IT Department users
- Configured logon scripts via GPO
- Verified GPO application using `gpresult /R` and `gpresult /H`
- Documented GPO inheritance and precedence
- Backed up GPOs for disaster recovery

## Key GPOs Created
| GPO Name | Linked To | Purpose |
|----------|-----------|---------|
| Desktop Standards | Domain | Wallpaper, screensaver timeout |
| IT-FullAccess | IT Department OU | Unrestricted access |
| Users-Restrictions | Sales & Marketing Department OU | Control Panel disabled |

## Technologies Used
- Group Policy Management Console (GPMC)
- Group Policy Editor
- gpresult / RSoP
- SYSVOL and NETLOGON shares

## Verification
- Confirmed GPOs appear in GPMC linked to correct OUs
- Logged in as Sales user—Control Panel access blocked
- Logged in as IT user—full access retained
- Generated policy report using `gpresult /R`
- Backed up GPO

## Status
✅ **Lab Completed Successfully**

## Screenshots
See `/Screenshots` folder for evidence of:
- GPMC showing GPO structure
- GPO settings in editor
- Blocked Control Panel on restricted user
- gpresult output confirming applied policies

# Lab 4: Password Policies & Account Management

## Environment
- **Hypervisor:** VMware Workstation
- **Server OS:** Windows Server 2025
- **Domain:** corp.juno.com
- **Domain Controller:** DC01

## Objective
Configure domain password policies and account lockout settings, and master common account management tasks performed daily by tech support staff.

## Summary
This lab focused on password and account security—one of the most common areas tech support handles daily. The Default Domain Policy was modified to enforce organizational password requirements including complexity, length, and expiration settings.

Account lockout policies were configured to protect against brute force attacks while balancing user experience. The lockout threshold, duration, and reset counter were set to organizational standards.

Practical account management tasks were performed including unlocking locked accounts, resetting passwords, enabling/disabling accounts, and troubleshooting authentication issues. PowerShell commands were used alongside ADUC to efficiently manage user accounts at scale.

## Tasks Completed
- Configured domain password policy in Default Domain Policy
  - Minimum length: 8 characters
  - Complexity requirements: Enabled
  - Password history: 24 passwords
  - Maximum age: 90 days
- Configured account lockout policy
  - Lockout threshold: 5 invalid attempts
  - Lockout duration: 10 minutes
  - Reset counter: 10 minutes
- Performed account unlock operations via ADUC 
- Reset user passwords using multiple methods
- Enabled/disabled user accounts


## Technologies Used
- Active Directory Users and Computers
- Group Policy Management (Default Domain Policy)
- Event Viewer (Security Log)

## Verification
- Tested password policy by attempting weak password—rejected
- Triggered account lockout with failed attempts
- Successfully unlocked account via ADUC


## Status
✅ **Lab Completed Successfully**

## Screenshots
See `/screenshots` folder for evidence of:
- Password policy settings in GPO
- Account lockout policy settings
- Locked account in ADUC

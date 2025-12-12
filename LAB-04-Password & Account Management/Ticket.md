# IT Service Request - TICKET-2024-004

## Ticket Information
| Field | Value |
|-------|-------|
| **Ticket ID** | TICKET-2025-004 |
| **Request Type** | Service Request |
| **Priority** | High |
| **Category** | Security / Identity Management |
| **Status** | Completed |
| **Created Date** | 2025-12-12 |
| **Completed Date** | 2025-12-12 |
| **Requested By** | Security Team |
| **Assigned To** | Systems Administrator |

## Request Summary
**Title:** Configure Domain Password and Account Lockout Policies

## Description
The organization requires enforcement of password security standards across all domain accounts. Password complexity, length, and expiration policies must meet compliance requirements. Account lockout policies are needed to protect against brute force attacks while minimizing user disruption.

## Work Performed
Modified the Default Domain Policy to enforce password requirements. Configured minimum password length of 8 characters with complexity requirements enabled. Set password history to remember 24 previous passwords preventing reuse. Maximum password age set to 90 days requiring regular password changes.

Implemented account lockout policy with threshold of 5 invalid attempts resulting in 10-minute lockout. Reset counter configured to clear failed attempts after 10 minutes of no activity.

Documented and practiced account management procedures for help desk operations including unlocking accounts, resetting passwords, and troubleshooting authentication issues using both ADUC and PowerShell.

## Configuration Details
| Setting | Value |
|---------|-------|
| Minimum Password Length | 8 characters |
| Password Complexity | Enabled |
| Password History | 24 passwords |
| Maximum Password Age | 90 days |
| Minimum Password Age | 1 day |
| Lockout Threshold | 5 attempts |
| Lockout Duration | 10 minutes |
| Reset Lockout Counter | 10 minutes |

## Testing & Validation
- Attempted to set password below 8 characters—rejected
- Attempted password without complexity—rejected
- Triggered lockout with 5 failed attempts—account locked
- Unlocked account via ADUC—successful
- Verified events logged in Security event log 

## Resolution
Password and account lockout policies successfully implemented. Policies verified functional through testing. Help desk procedures documented for daily account management tasks. Environment meets security compliance requirements.

## Status
✅ **Completed**


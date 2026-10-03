# Windows Endpoint Security Hardening Report

## 1. Project Overview

This project demonstrates a basic Windows endpoint security assessment and hardening exercise performed in a controlled lab environment.

The assessment focused on local user accounts, password policies, account lockout settings, Windows Firewall, Microsoft Defender, Windows services, and Windows Update.

## 2. Objectives

- Review existing Windows security settings.
- Identify areas that could be strengthened.
- Apply selected security hardening measures.
- Verify the changes after implementation.
- Document the results.

## 3. Environment

- Operating System: Windows
- Computer Role: Workstation
- Tools: Command Prompt, PowerShell, Local Security Policy, Windows Defender, Windows Firewall

## 4. Initial Findings

### User Accounts

The system contained several local accounts, including Administrator, Guest, User, DefaultAccount, and WDAGUtilityAccount.

The current account was `desktop-pbonb7e\user`.

The account was associated with the local Administrators group.

### Password Policy

The initial password policy showed:

- Minimum password length: 0
- Password history: None
- Maximum password age: 42 days
- Lockout threshold: 10 attempts
- Lockout duration: 10 minutes

The account itself also showed that a password was not required.

### Windows Firewall

Windows Firewall was enabled on the Domain, Private, and Public profiles.

Inbound connections were configured to be blocked while outbound connections were allowed.

Dropped connection logging was initially disabled.

### Microsoft Defender

The Microsoft Defender protections checked during the assessment were enabled.

### Windows Services

Running Windows services were reviewed to identify the services currently active on the endpoint. No services were disabled solely based on the review because their purpose and system dependencies should be confirmed before making changes.

### Windows Update

The Windows Update service was running with a Manual startup type.

## 5. Security Hardening Implemented

### Password Length

The minimum password length was changed from 0 to 12 characters.

### Password History

Password history was configured to remember the previous 24 passwords.

### Account Lockout

The account lockout policy was strengthened to:

- Lockout threshold: 5 invalid attempts
- Lockout duration: 15 minutes
- Lockout observation window: 15 minutes

### Firewall Logging

Dropped connection logging was enabled for all Windows Firewall profiles.

The firewall remained configured to block inbound connections and allow outbound connections.

## 6. Verification

The changes were verified using Windows command-line tools.

The updated password policy confirmed:

- Minimum password length: 12
- Password history: 24
- Lockout threshold: 5
- Lockout duration: 15 minutes
- Lockout observation window: 15 minutes

Windows Firewall verification confirmed that dropped connection logging was enabled across the available profiles.

## 7. Security Recommendations

- Use strong, unique passwords for user accounts.
- Avoid unnecessary administrator privileges.
- Review local user accounts regularly.
- Keep Microsoft Defender enabled and updated.
- Keep Windows and installed applications updated.
- Monitor Windows security and firewall logs.
- Review unnecessary services before disabling them.
- Apply the principle of least privilege.
- Maintain secure backups of important data.

## 8. Conclusion

The assessment established a baseline for the Windows endpoint and applied several security hardening measures.

The main improvements included stronger password requirements, password history, stricter account lockout settings, and firewall dropped-connection logging.

This project demonstrates practical experience with Windows security configuration, endpoint hardening, system administration, and security monitoring.

## Disclaimer

This project was performed on a controlled personal lab environment for educational and portfolio purposes. No unauthorized systems were accessed or modified.
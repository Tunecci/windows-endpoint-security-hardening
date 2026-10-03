# Windows Endpoint Security Hardening

## Overview

A controlled Windows security lab focused on assessing and hardening common endpoint security settings.

## Objectives

- Review local Windows user accounts and privileges
- Assess password and account lockout policies
- Review Windows Firewall configuration
- Verify Microsoft Defender protections
- Review running Windows services
- Check Windows Update status
- Apply selected endpoint security hardening measures
- Document and verify the changes

## Tools Used

- Windows Command Prompt
- PowerShell
- Local Security Policy
- Windows Defender
- Windows Firewall

## Security Assessment

The initial assessment identified several settings that could be strengthened, including:

- No minimum password length
- No password history
- A 10-attempt account lockout threshold
- Firewall dropped-connection logging disabled

Microsoft Defender protections were enabled, and Windows Firewall was active.

## Hardening Performed

The following changes were implemented:

- Minimum password length increased to 12 characters
- Password history configured to remember 24 passwords
- Account lockout threshold reduced to 5 invalid attempts
- Account lockout duration increased to 15 minutes
- Lockout observation window set to 15 minutes
- Windows Firewall dropped-connection logging enabled

## Verification

The updated security settings were verified using Windows command-line tools and Local Security Policy.

## Project Structure

```text
windows-endpoint-security-hardening/
├── README.md
├── evidence/
├── reports/
│   └── security-hardening-report.md
└── screenshots/
```

## Skills Demonstrated

- Windows endpoint security
- System administration
- Access control
- Password policy management
- Account lockout configuration
- Firewall configuration
- Security monitoring
- Security documentation

## Disclaimer

This project was performed in a controlled personal lab environment for educational and portfolio purposes. No unauthorized systems were accessed or modified.
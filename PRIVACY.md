# Privacy Policy

**Effective Date**: February 2025  
**Last Updated**: February 2025

## Overview

CoT Sentinel is a self-hosted administration tool. All data remains on your infrastructure under your control. We do not operate any cloud services, collect telemetry, or receive any data from your installation.

## Data Handled by CoT Sentinel

The following data is processed and stored locally on your server:

### User Account Data
- Usernames and email addresses
- Password hashes (bcrypt)
- Role assignments and permissions
- Session tokens

### Certificates and Keys
- TLS/SSL certificates
- Certificate signing requests
- Private keys (encrypted at rest)
- Trust store entries

### Connection Profiles
- Server endpoints and ports
- Authentication configurations
- Client device associations

### Audit Logs
- User login/logout events
- Administrative actions
- Configuration changes
- Certificate operations
- Timestamps and source IP addresses

### System Configuration
- Server settings
- Network configurations
- Backup schedules

## Data Storage

All data is stored locally on your server in:

| Data Type | Storage Location | Encryption |
|-----------|------------------|------------|
| User credentials | PostgreSQL database | Passwords hashed with bcrypt |
| Certificates/keys | `/opt/tak/certs/` | Private keys encrypted |
| Audit logs | PostgreSQL database | Not encrypted at rest |
| Configuration | Local filesystem | Not encrypted at rest |
| Backups | User-specified location | Optional encryption available |

## Data Transmission

CoT Sentinel communicates over the network in the following scenarios:

| Communication | Purpose | Encryption |
|---------------|---------|------------|
| Web interface | Admin access | TLS (when HTTPS enabled) |
| TAK Server | Management operations | TLS |
| Database | Local data storage | Local socket or TLS |

**CoT Sentinel does not transmit any data to BlackDot Technology LLC, third parties, or external services.**

## No Telemetry

CoT Sentinel does not include:
- Usage analytics
- Crash reporting
- Update checks
- License verification
- Any form of "phone home" functionality

## Data Retention

Data retention is entirely under your control:

- **Audit logs**: Retained until manually purged
- **User accounts**: Retained until deleted by administrator
- **Certificates**: Retained until expiration or manual deletion
- **Backups**: Retained per your backup schedule and retention policy

## Your Responsibilities

As the system administrator, you are responsible for:

1. **Access control** — Limiting who can access the CoT Sentinel interface
2. **Network security** — Deploying behind firewalls, VPNs, or other access controls
3. **Encryption in transit** — Enabling HTTPS for the web interface
4. **Encryption at rest** — Encrypting the underlying storage if required by your policies
5. **Backup security** — Protecting backup files containing sensitive data
6. **Log management** — Implementing log retention and disposal policies
7. **Compliance** — Ensuring deployment meets your organizational and regulatory requirements

## Compliance Considerations

Depending on your use case, the following regulations may apply:

- **ITAR** — If used with defense-related data
- **NIST 800-171** — For controlled unclassified information
- **GDPR** — If user data includes EU persons
- **HIPAA** — If integrated with healthcare systems

CoT Sentinel provides tools to support compliance (audit logging, access controls, encryption) but compliance is the responsibility of the deploying organization.

## Third-Party Components

CoT Sentinel uses open-source dependencies listed in [NOTICE](NOTICE). These components do not collect or transmit user data. Review each component's privacy practices if required by your compliance framework.

## Changes to This Policy

Updates to this policy will be documented in the repository changelog. Material changes will be noted in release notes.

## Contact

For privacy-related inquiries: **privacy@blackdottech.com**

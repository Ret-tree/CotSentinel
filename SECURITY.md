# Security Policy

## Reporting a Vulnerability

The CoT Sentinel team takes security vulnerabilities seriously. We appreciate your efforts to responsibly disclose your findings.

**Please do not report security vulnerabilities through public GitHub issues.**

### How to Report

Send vulnerability reports to: **security@blackdottech.com**

Include the following information:

- Description of the vulnerability
- Steps to reproduce the issue
- Affected versions
- Potential impact assessment
- Any suggested fixes (optional)

### What to Expect

| Timeframe | Action |
|-----------|--------|
| 24 hours | Acknowledgment of your report |
| 72 hours | Initial assessment and severity determination |
| 7 days | Status update on remediation progress |
| 90 days | Target resolution for most issues |

We will keep you informed throughout the process and credit you in the release notes (unless you prefer anonymity).

### Scope

The following are in scope for security reports:

- Authentication and authorization bypasses
- SQL injection, command injection, or code execution
- Cross-site scripting (XSS) or cross-site request forgery (CSRF)
- Sensitive data exposure (credentials, certificates, audit logs)
- Cryptographic weaknesses
- Privilege escalation
- Path traversal or file access vulnerabilities

The following are out of scope:

- Vulnerabilities in dependencies (report these upstream, but notify us)
- Issues requiring physical access to the server
- Social engineering attacks
- Denial of service attacks
- Issues in third-party TAK Server software

## Supported Versions

| Version | Supported |
|---------|-----------|
| 1.5.x | ✅ Yes |
| 1.4.x | ⚠️ Security fixes only |
| < 1.4 | ❌ No |

## Security Best Practices

When deploying CoT Sentinel:

1. **Always use HTTPS** — Run `setup_https.sh` before production deployment
2. **Change default credentials** — Never use default passwords in production
3. **Restrict network access** — Limit access to trusted networks or VPN
4. **Enable audit logging** — Monitor the audit log for suspicious activity
5. **Regular updates** — Keep CoT Sentinel and all dependencies current
6. **Backup encryption keys** — Store certificate backups securely offline

## Security Audit History

See [SECURITY_AUDIT_REPORT.md](SECURITY_AUDIT_REPORT.md) for details on past security reviews and remediation.

## PGP Key

For encrypted communications, use our PGP key:

```
[PGP key to be added]
```

Key fingerprint: `[Fingerprint to be added]`

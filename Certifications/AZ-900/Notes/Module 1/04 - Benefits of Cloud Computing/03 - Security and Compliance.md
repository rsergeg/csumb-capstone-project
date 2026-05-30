
## Why Security Matters

- Businesses store sensitive data in the cloud.
- Cybercriminals may steal information through:
    - Large security breaches
    - Small amounts of data stolen over time
- Security is one of the biggest concerns when moving to the cloud.

---

# Core Cloud Security Principles

## Encryption

### What is Encryption?

- Converts data into an unreadable format.
- Protects information from unauthorized access.
- Data can only be read with the correct decryption key.

### AES-256

- Common encryption standard used by cloud providers.
- Considered extremely secure.
- Frequently mentioned in cloud security discussions.

### Data at Rest

- Data stored on servers.
- Protected through encryption.

### Data in Transit

- Data moving between devices and the cloud.
- Protected through encryption while traveling across networks.

---

# Access Controls

## What Are Access Controls?

- Determine who can:
    - View data
    - Edit data
    - Delete data
- Permissions can be assigned based on job roles.

### Benefits

- Limits access to authorized users only.
- Reduces risk of unauthorized data exposure.
- Supports the principle of least privilege.

---

# Multi-Factor Authentication (MFA)

## What is MFA?

- Requires more than a username and password.
- Adds an extra layer of security.

### Examples

- One-time passcode sent to phone
- Fingerprint scan
- Security token
- Authentication app approval

### Why MFA Matters

- Even if a password is stolen, attackers still need the second factor.
- Significantly reduces unauthorized access.

---

# Compliance and Regulations

## GDPR

**General Data Protection Regulation**

- European Union privacy regulation.
- Governs how personal data is collected, stored, and protected.

## HIPAA

**Health Insurance Portability and Accountability Act**

- U.S. healthcare privacy regulation.
- Protects sensitive patient information.

## Why Compliance Matters

- Organizations must follow industry regulations.
- Cloud providers invest heavily to meet compliance standards.
- Businesses should select providers that support their compliance requirements.

---

# Cloud Provider Security Measures

## Physical Security

Cloud providers secure data centers using:

- 24/7 surveillance
- Access control systems
- Physical security protections

## Disaster Recovery

- Protects data during outages and disasters.
- Helps maintain availability and business continuity.

## Intrusion Detection Systems

- Monitor for suspicious activity.
- Help identify potential attacks.

## Vulnerability Assessments

- Regularly check systems for security weaknesses.
- Help prevent future attacks.

---

# Shared Responsibility Model

## Key Concept for AZ-900

### Cloud Provider Responsibilities

- Security of the cloud.
- Physical data centers.
- Infrastructure.
- Networking.
- Hardware.

### Customer Responsibilities

- User accounts.
- Passwords.
- Data protection.
- Access permissions.
- Security settings.

### Remember

**Security is a shared responsibility between the cloud provider and the customer.**

---

# Cloud Security Best Practices

## Strong Password Policies

- Require strong passwords.
- Avoid reused passwords.
- Enforce password standards.

## Enable MFA

- Use MFA on all cloud accounts whenever possible.

## Monitor Activity Logs

- Review logs for:
    - Suspicious behavior
    - Failed login attempts
    - Unauthorized access attempts

## Encrypt Sensitive Data

- Encrypt data at rest.
- Encrypt data in transit.

## Maintain Backups

- Regularly back up important data.
- Have a disaster recovery plan.

## Security Awareness Training

- Teach employees to recognize:
    - Phishing attacks
    - Suspicious emails
    - Malicious links

---

# Additional Cloud Considerations

## Vendor Lock-In

- Risk of becoming dependent on one cloud provider.
- Makes migration to another provider difficult.

## Performance and Scalability

- Ensure provider can support future growth.
- Infrastructure should meet long-term needs.

## Cost Effectiveness

- Compare pricing models carefully.
- Consider:
    - Storage costs
    - Bandwidth costs
    - Security feature costs

## Customer Support

- Reliable support is important during outages or issues.
- Evaluate support options before choosing a provider.

---

# AZ-900 Exam Takeaways

### Security Concepts

- Encryption
- Data at Rest
- Data in Transit
- Access Controls
- Multi-Factor Authentication (MFA)

### Compliance

- GDPR
- HIPAA

### Security Features

- Intrusion Detection
- Vulnerability Assessments
- Disaster Recovery

### Important Exam Concept

**Shared Responsibility Model**

- Cloud Provider = Security _of_ the cloud
- Customer = Security _in_ the cloud

### Quick Memory Trick

**E-A-M-C-S**

- **E**ncryption
- **A**ccess Controls
- **M**FA
- **C**ompliance
- **S**hared Responsibility

These five concepts are the foundation of cloud security and frequently appear in AZ-900 content.
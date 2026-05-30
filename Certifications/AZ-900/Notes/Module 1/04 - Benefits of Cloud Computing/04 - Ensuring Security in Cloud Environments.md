
# Ensuring Security in Cloud Environments

## Introduction

- Cloud computing provides:
    - Scalability
    - Agility
    - Cost savings
- However, moving to the cloud introduces new security challenges.
- Organizations must actively protect their data, applications, and users.

---

# Shared Responsibility Model

## What is the Shared Responsibility Model?

- Defines security responsibilities between:
    - Cloud Service Provider (CSP)
    - Customer
- One of the most important cloud security concepts.

### Cloud Provider Responsibilities

**Security OF the Cloud**

- Physical security
- Data centers
- Network infrastructure
- Hardware
- Core cloud services

### Customer Responsibilities

**Security IN the Cloud**

- Data
- Applications
- User accounts
- Access permissions
- Security configurations

### AZ-900 Exam Tip

**Provider secures the infrastructure.**  
**Customer secures their data and access.**

---

# Pillars of Cloud Security

## Encryption

### Purpose

- Protects data from unauthorized access.
- Converts data into unreadable text without the proper key.

### Data in Transit

- Protects data while moving across networks.

### Data at Rest

- Protects data stored in cloud systems.

### Remember

Encryption = Foundation of cloud security.

---

## Access Controls

### Purpose

- Determines who can access resources.
- Defines what actions users can perform.

### Identity and Access Management (IAM)

- Creates user identities.
- Assigns roles and permissions.
- Controls access to cloud resources.

### Multi-Factor Authentication (MFA)

- Requires more than a password.
- Examples:
    - Phone code
    - Fingerprint
    - Authenticator app

### Principle of Least Privilege (POLP)

- Give users only the access needed for their job.
- No extra permissions.
- Reduces security risks.

---

# Vulnerability Management

## Why It Matters

- New security weaknesses are discovered constantly.
- Organizations must proactively find and fix vulnerabilities.

### Best Practices

- Regular vulnerability scans
- Prioritize critical issues
- Apply security patches quickly
- Stay informed about new threats

### Key Term

**Patching = Installing updates that fix security holes.**

---

# Incident Response

## What is Incident Response?

- A plan for handling security incidents.
- Helps minimize damage and restore operations quickly.

### Incident Response Steps

#### Detection

- Identify suspicious activity.

#### Containment

- Prevent the attack from spreading.

#### Investigation

- Determine what happened and why.

#### Remediation

- Fix vulnerabilities and prevent recurrence.

#### Recovery

- Restore systems and services.

---

# Monitoring and Logging

## Continuous Monitoring

- Watch cloud resources for suspicious activity.
- Helps detect threats early.

### Monitoring Tracks

- Resource usage
- User activity
- System logs
- Security events

### SIEM

**Security Information and Event Management**

- Centralized security monitoring platform.
- Collects and analyzes logs from multiple systems.

---

# Compliance Considerations

## GDPR

**General Data Protection Regulation**

- Protects personal data of EU residents.
- Requires strict controls on data collection and storage.

## HIPAA

**Health Insurance Portability and Accountability Act**

- Protects healthcare information in the U.S.

## PCI DSS

**Payment Card Industry Data Security Standard**

- Protects credit card information.
- Required for businesses handling payment card data.

---

# Advanced Cloud Security Strategies

## Data Loss Prevention (DLP)

- Prevents sensitive information from leaving the cloud environment.
- Detects possible data theft attempts.

## Cloud Workload Protection Platform (CWPP)

- Protects cloud workloads and applications.
- Features:
    - Vulnerability scanning
    - Intrusion detection
    - Threat intelligence

## Cloud Security Posture Management (CSPM)

- Continuously evaluates cloud security settings.
- Finds:
    - Misconfigurations
    - Compliance issues
    - Security risks

## Zero Trust Security Model

### Core Idea

**Trust nothing. Verify everything.**

- No user or device is automatically trusted.
- Every access request is verified.
- Reduces risk from compromised accounts.

## Key Management Service (KMS)

- Protects encryption keys.
- Controls key storage, access, and rotation.

---

# Emerging Cloud Security Trends

## Cloud-Native Security

- Designed for:
    - Containers
    - Microservices
    - Modern cloud applications
- Provides automated security monitoring.

## Security as Code (SaC)

- Security settings managed through code.
- Benefits:
    - Consistency
    - Automation
    - Reduced human error

## AI and Machine Learning for Security

### Uses

- Detect unusual behavior
- Identify threats faster
- Automate security responses
- Improve threat detection accuracy

---

# AZ-900 Exam Takeaways

## Most Important Concepts

### Shared Responsibility Model

- Provider = Security OF the cloud
- Customer = Security IN the cloud

### Access Security

- IAM
- MFA
- Least Privilege (POLP)

### Data Protection

- Encryption at Rest
- Encryption in Transit

### Security Operations

- Monitoring
- Logging
- Vulnerability Management
- Incident Response

### Compliance

- GDPR
- HIPAA
- PCI DSS

### Advanced Security Terms

- DLP
- CWPP
- CSPM
- Zero Trust
- KMS

## Quick Memory List

**E-A-I-M-P-Z**

- **E**ncryption
- **A**ccess Control
- **I**AM
- **M**FA
- **P**OLP (Least Privilege)
- **Z**ero Trust

These are some of the most commonly tested cloud security concepts and form the foundation of cloud security knowledge.

# Identity and Access + Azure Service Ecosystem

## Important Azure Terms

### Tenant

- Represents an organization in Azure
- Multiple users share the same Azure environment
- Usually a company, school, or organization

Think:

- Tenant = Organization

---

### Account

- Your personal sign-in to Azure
- Can be:
    - Work account
    - School account
    - Microsoft personal account

Think:

- Account = You

---

### Subscription

- Billing and service agreement with Microsoft
- Resources are created inside subscriptions

Exam Note:

- Subscription controls billing and resource usage

---

### Region

- Physical Azure datacenter location

Examples:

- East US
- West US
- Central US

Benefits:

- Lower latency
- Data locality

Think:

- Region = Datacenter location

---

### Geography

- Collection of Azure regions
- Helps meet data residency requirements

Think:

- Geography > Region

---

### Resource

- Individual Azure service

Examples:

- VM
- Storage Account
- SQL Database

Think:

- Resource = Thing you create

---

### Resource Group

- Container for related resources

Example:

Resource Group:

- Web App
- SQL Database
- Storage Account

Benefits:

- Easier management
- Easier deployment
- Easier deletion

Exam Note:

- Resource Groups organize resources

---

### Azure Resource Manager (ARM)

- Azure management layer
- Deploys and manages resources
- Controls access to resources

Think:

- ARM = Azure control plane

---

### Storage Account

Provides access to:

- Blob Storage
- File Storage
- Queue Storage
- Table Storage

Exam Note:

- Storage Account is the parent container for storage services

---

### Image

- Template used to create virtual machines
- Contains:
    - Operating system
    - Configuration
    - Installed software

Think:

- VM blueprint

---

### Offer

- Azure pricing plan
- Credits and subscription terms

Examples:

- Free Account
- Student Account
- Pay-As-You-Go

---

### Azure Portal

- Web-based Azure management interface
- Used to create and manage resources

Think:

- Azure website for administration

---

### Service Level Agreement (SLA)

- Microsoft's uptime guarantee

Examples:

- 99.9%
- 99.95%
- 99.99%

Exam Note:

- SLA = uptime commitment

---

# Identity and Access Services

## Microsoft Entra ID

Formerly:

- Azure Active Directory (Azure AD)

Purpose:

- Identity and access management

Provides:

- Authentication
- Authorization
- Single Sign-On (SSO)

Examples:

- Logging into Azure
- Logging into Microsoft 365
- Accessing company applications

Exam Note:

- Azure AD was renamed to Microsoft Entra ID

⚠️ This is one of the most important AZ-900 services.

---

## Azure Key Vault

Purpose:

- Secure storage for secrets

Stores:

- Passwords
- API keys
- Certificates
- Connection strings

Benefits:

- Centralized security
- Reduced credential exposure

Think:

- Secure vault for sensitive information

---

# Compute Services Review

## Azure Functions

- Serverless computing
- Runs code on demand
- No server management

---

## Azure Virtual Machines

- Traditional virtual servers
- Full operating system control

---

# Containers

## Azure Kubernetes Service (AKS)

- Managed Kubernetes platform
- Runs containerized applications

Benefits:

- Easier container management
- Automatic scaling

---

## Azure Container Instances (ACI)

- Run containers quickly
- No Kubernetes cluster required

Good for:

- Small workloads
- Simple container deployments

---

# Database Services

## Azure SQL Database

- Managed relational database
- Uses SQL tables and relationships

Examples:

- Customer records
- Orders
- Inventory systems

---

## Azure Cosmos DB

- NoSQL database service

Benefits:

- Global distribution
- Massive scalability
- Low latency

Exam Note:

- SQL Database = Relational
- Cosmos DB = NoSQL

---

# DevOps Services

## Azure DevOps

Supports:

- Source control
- Agile planning
- CI/CD pipelines
- Automated deployments

Benefits:

- Faster software delivery
- Team collaboration

---

## Azure Monitor

Purpose:

- Application monitoring
- Performance tracking
- Resource health monitoring

Used for:

- Troubleshooting
- Performance analysis
- Alerting

---

# Hybrid and Multi-Cloud

## Azure Arc

Purpose:

- Manage resources outside Azure

Can manage:

- On-prem servers
- Other cloud environments

Think:

- Azure management everywhere

---

## Azure Stack

Purpose:

- Bring Azure services into your datacenter

Benefits:

- Hybrid cloud solutions

---

# Integration Services

## Azure API Management

Purpose:

- Create and manage APIs

Benefits:

- Security
- Monitoring
- Developer access control

Think:

- Front door for APIs

---

## Azure Logic Apps

Purpose:

- Workflow automation

Examples:

- Email notifications
- Approval processes
- System integrations

Think:

- If This → Then That for business processes

---

# Internet of Things (IoT)

## Azure IoT Hub

Purpose:

- Connect devices to Azure

Examples:

- Sensors
- Smart devices
- Industrial equipment

Provides:

- Device communication
- Device management

---

## Azure Time Series Insights

Purpose:

- Analyze IoT data over time

Used for:

- Monitoring trends
- Device analytics

---

# Governance and Security

## Azure Policy

Purpose:

- Enforce organizational rules

Examples:

- Allowed regions
- Allowed VM sizes
- Security requirements

Think:

- Rules engine for Azure

---

## Microsoft Defender for Cloud

Purpose:

- Security monitoring
- Threat detection
- Security recommendations

Benefits:

- Improves security posture
- Identifies vulnerabilities

Exam Note:

- Defender for Cloud = Cloud security management

---

# Networking Security

## Azure Virtual Network (VNet)

- Private Azure network
- Secure communication

---

## Web Application Firewall (WAF)

Purpose:

- Protect web applications

Protects against:

- Common web attacks
- Malicious traffic

Think:

- Firewall specifically for websites

---

## Azure DDoS Protection

Purpose:

- Protect against Distributed Denial of Service attacks

Benefits:

- Improved availability
- Reduced attack impact

---

# Storage Services Review

## Azure Blob Storage

Stores:

- Images
- Videos
- Documents
- Backups

Think:

- Unstructured data storage

---

## Azure Files

Provides:

- Shared cloud file storage

Benefits:

- Multiple systems can access files

---

# Virtual Desktop Infrastructure (VDI)

## Azure Virtual Desktop

Purpose:

- Cloud-hosted desktops

Benefits:

- Remote work
- Centralized management
- Secure access

Think:

- Windows desktop delivered from Azure

---

# Web Services

## Azure Static Web Apps

Best for:

- Static websites

Examples:

- Portfolio sites
- Documentation sites

---

## Azure App Service

Best for:

- Dynamic web applications
- APIs

Benefits:

- Managed hosting
- Automatic scaling

---

# Exam Notes

⚠️ Tenant = Organization

⚠️ Account = User login

⚠️ Subscription = Billing container

⚠️ Resource = Azure service instance

⚠️ Resource Group = Container for resources

⚠️ Region = Datacenter location

⚠️ Geography = Collection of regions

⚠️ Microsoft Entra ID = Identity management

⚠️ Azure Key Vault = Secrets management

⚠️ Azure Policy = Governance rules

⚠️ Defender for Cloud = Security monitoring

⚠️ Azure Arc = Manage resources outside Azure

⚠️ Azure Virtual Desktop = Cloud-hosted desktops

⚠️ Azure SQL Database = Relational

⚠️ Azure Cosmos DB = NoSQL

---

### Quick Memory Aids

**Identity**

- Entra ID = Users
- Key Vault = Secrets

**Governance**

- Policy = Rules
- Defender = Security

**Hybrid**

- Arc = Manage Anywhere
- Stack = Azure in Your Datacenter

**Databases**

- SQL = Relational
- Cosmos = NoSQL
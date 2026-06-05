
## What is Azure API Management?

- Azure API Management (APIM) is a service for publishing, securing, monitoring, and managing APIs.
- Acts as a central management layer between applications and backend services.
- Helps organizations control their entire API ecosystem.

Think:

- API = The service
- API Management = The control center

---

# Core Purpose

Azure API Management helps organizations:

- Publish APIs
- Secure APIs
- Monitor API usage
- Control access
- Improve performance

Benefits:

- Better governance
- Better security
- Easier API management

---

# Products

## What are Products?

- Products are collections of APIs exposed to developers.
- Developers subscribe to products to gain API access.

Features:

- Public or restricted access
- Subscription key support
- Publish when ready

Think:

- Product = Package of APIs

---

# Groups

## Purpose

Groups control who can see and use APIs.

### Built-In Groups

#### Administrators

- Manage API Management service.
- Create APIs and products.
- Configure settings.

---

#### Developers

- Build applications using APIs.
- Access developer portal.
- Subscribe to products.

---

#### Guests

- Unauthenticated users.
- Limited read-only access.

Example:

- View documentation
- Cannot call APIs

---

## Custom Groups

Organizations can create:

- Partner groups
- Department groups
- Project groups

Benefits:

- Granular access control

Exam Note:

Groups control API visibility and access.

---

# Developers

## What Are They?

- User accounts in API Management.
- Can belong to multiple groups.
- Can subscribe to products.

Uses:

- API consumers
- Internal developers
- External partners

---

# Workspaces

## Purpose

- Support decentralized development teams.
- Allow teams to manage APIs independently.

Benefits:

- Isolation
- Collaboration
- Access control

Think:

- Separate work areas for API teams.

---

# Policies

## Purpose

Policies change API behavior.

Can:

- Transform requests
- Transform responses
- Apply restrictions
- Enforce rules

Benefits:

- Flexible API control

Exam Note:

Policies modify API behavior without changing backend code.

---

# API Management Components

Azure API Management has three main components:

1. API Gateway
2. Management Plane
3. Developer Portal

This shows up often in Microsoft documentation.

---

# API Gateway

## What It Does

- Front door for API requests.
- Receives client requests.
- Sends requests to backend services.

Think:

Client  
↓  
API Gateway  
↓  
Backend Service

---

## Gateway Responsibilities

### Authentication

Verifies:

- API keys
- JWT tokens
- Certificates

---

### Rate Limiting

Controls:

- API usage
- Request volume

Benefits:

- Prevent abuse
- Protect resources

---

### Caching

Stores responses.

Benefits:

- Faster responses
- Reduced backend load

---

### Monitoring

Generates:

- Logs
- Metrics
- Traces

Benefits:

- Easier troubleshooting

Exam Note:

Gateway handles security, routing, caching, and monitoring.

---

# Self-Hosted Gateway

## Purpose

Run API Gateway outside Azure.

Locations:

- On-premises
- Other clouds
- Hybrid environments

Benefits:

- Compliance
- Reduced latency
- Local control

---

# Management Plane

## Purpose

Administrative control center.

Used to:

- Configure API Management
- Import APIs
- Manage users
- View analytics

---

## Supported Tools

- Azure Portal
- Azure CLI
- PowerShell
- REST API
- VS Code Extension
- SDKs

---

## Functions

### Import APIs

Supports:

- OpenAPI
- WSDL
- OData
- GraphQL
- gRPC

---

### Manage Products

- Package APIs
- Publish APIs

---

### Analytics

- Usage insights
- Performance data

Exam Note:

Management Plane = Administration layer.

---

# Developer Portal

## Purpose

Public-facing API portal.

Used by developers to:

- Discover APIs
- Read documentation
- Test APIs
- Obtain API keys

Think:

- API storefront

---

## Developer Capabilities

### Read Documentation

Learn API usage.

---

### Interactive Testing

Call APIs directly from the portal.

---

### API Keys

- Register
- Subscribe
- Manage keys

---

### Usage Analytics

View API consumption data.

Exam Note:

Developer Portal helps developers consume APIs.

---

# API Management Tiers

## Developer Tier

- Low-cost
- Non-production
- Testing and learning

---

## Basic Tier

- Production workloads
- Small deployments

---

## Standard Tier

- Production workloads
- Greater capacity

---

## Premium Tier

Enterprise features:

- Multi-region deployment
- Availability Zones
- Private networking
- High scalability

Exam Note:

Premium = Enterprise-level tier.

---

## Consumption Tier

Serverless API Management

Benefits:

- Pay per execution
- Auto-scaling

Good for:

- Microservices
- Variable workloads

Exam Note:

Consumption Tier = Serverless

---

# Azure Service Integrations

## Azure Key Vault

Stores:

- Secrets
- Certificates
- Keys

Benefits:

- Secure credential management

---

## Azure Monitor

Provides:

- Logging
- Alerts
- Monitoring

---

## Application Insights

Provides:

- Performance monitoring
- Tracing
- Diagnostics

---

## Virtual Networks & Private Endpoints

Provides:

- Network isolation
- Additional security

---

## Microsoft Entra ID

Provides:

- Authentication
- Authorization

Exam Note:

Formerly Azure Active Directory.

---

## Azure Defender for APIs

Provides:

- API threat protection
- Runtime security

---

## Azure DDoS Protection

Provides:

- Protection from denial-of-service attacks

---

## Event Hubs

Provides:

- Event streaming

---

# APIs Commonly Hosted on Azure

Azure API Management commonly works with:

- Azure Functions
- Logic Apps
- Web Apps
- Service Fabric
- Azure OpenAI Service

---

# AZ-900 Exam Notes

⚠️ API Management = Publish, secure, monitor, and manage APIs

⚠️ Three core components:

- API Gateway
- Management Plane
- Developer Portal

⚠️ Products expose APIs to developers

⚠️ Groups control visibility and access

⚠️ Policies modify API behavior

⚠️ Gateway handles:

- Authentication
- Routing
- Caching
- Rate limiting

⚠️ Developer Portal is used by API consumers

⚠️ Consumption Tier = Serverless

⚠️ Premium Tier supports:

- Multi-region deployment
- Availability Zones
- Enterprise workloads

---

### Quick Memory Trick

**Gateway = Traffic Control**

Receives and secures requests

**Management Plane = Administration**

Configure and manage APIs

**Developer Portal = Storefront**

Developers discover and use APIs

For AZ-900, remember:

**Azure API Management is the central platform for governing, securing, publishing, and monitoring APIs throughout their lifecycle.**

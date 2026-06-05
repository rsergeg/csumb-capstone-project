## Azure Core Service Categories

Azure services are divided into three main categories:

### Compute

Provides processing power for applications.

Services:

- Azure Virtual Machines (VMs)
- Azure App Service
- Azure Functions
- Azure Kubernetes Service (AKS)

Purpose:

- Run applications
- Host websites
- Execute workloads

---

### Storage

Stores data in the cloud.

Services:

- Azure Blob Storage
- Azure Files
- Azure SQL Database
- Azure Data Lake Storage

Purpose:

- Store files
- Store databases
- Store analytics data

---

### Networking

Connects resources and users.

Services:

- Azure Virtual Network (VNet)
- Azure Load Balancer
- Azure CDN
- Azure ExpressRoute

Purpose:

- Communication
- Connectivity
- Security

---

# Compute Services

## Azure Virtual Machines

- Infrastructure as a Service (IaaS)
- Full control of operating system
- Supports Windows and Linux

Good for:

- Legacy applications
- Custom environments

---

## Azure App Service

- Platform as a Service (PaaS)
- Host web applications and APIs
- Azure manages infrastructure

Good for:

- Websites
- Web APIs

---

## Azure Functions

- Serverless compute
- Event-driven execution
- Pay only when code runs

Good for:

- Automation
- Background processing

---

## Azure Kubernetes Service (AKS)

- Managed Kubernetes platform
- Runs containerized applications
- Supports scaling and orchestration

Good for:

- Microservices
- Containers

---

# Azure Pricing Calculator

Purpose:

- Estimate Azure costs before deployment.

Features:

- Real-time pricing estimates
- Service customization
- Export reports
- Compare configurations

Exam Note:

Used for cost planning and budgeting.

---

# High Availability (HA)

## Definition

Ability of a system to continue operating despite failures.

Goals:

- Reduce downtime
- Remove single points of failure
- Improve reliability

---

## Availability Zones

- Separate physical data centers within a region.
- Independent:
    - Power
    - Cooling
    - Networking

Benefits:

- Fault isolation
- 99.99% SLA

Exam Note:

Availability Zones = Highest availability option.

---

## Availability Sets

- Distribute VMs across fault domains.
- Protect against hardware failures.

SLA:

- 99.95%

---

## Fault Domains

- Groups of hardware resources.
- Isolate failures within a data center.

Think:

- Neighborhoods inside a data center.

---

# Azure Load Balancer

Purpose:

- Distributes traffic across multiple servers.

Benefits:

- Scalability
- High availability
- Health monitoring

Types:

### Public Load Balancer

- Internet-facing traffic

### Internal Load Balancer

- Private network traffic

Exam Note:

Load Balancer works at Layer 4 (TCP/UDP).

---

# Health Probes

Purpose:

- Monitor backend VM health.
- Route traffic only to healthy resources.

Protocols:

- TCP
- HTTP
- HTTPS

Exam Note:

Health probes help Load Balancer maintain availability.

---

# Azure Traffic Manager

Purpose:

- DNS-based traffic distribution.

Benefits:

- Global load balancing
- Failover
- Performance routing

Routing Methods:

- Priority
- Weighted
- Geographic
- Performance

Exam Note:

Traffic Manager operates at the DNS level.

---

# Azure Service Bus

Purpose:

- Reliable messaging between applications.

Communication Methods:

### Queue

- One sender → One receiver

### Topic

- One sender → Multiple subscribers

Features:

- Decoupled applications
- Guaranteed delivery
- Dead Letter Queue (DLQ)

Exam Note:

Service Bus = Messaging platform.

---

# APIs and Azure API Management

## API

Application Programming Interface

Purpose:

- Allow applications to communicate.

Common Types:

- REST
- SOAP
- GraphQL
- RPC

---

## Azure API Management

Purpose:

- Publish APIs
- Secure APIs
- Monitor APIs
- Manage APIs

Components:

### API Gateway

- Receives requests
- Applies security and policies

### Management Plane

- Administration and configuration

### Developer Portal

- Documentation and API access

Exam Note:

API Management = API governance platform.

---

# Azure Logic Apps

Purpose:

- Workflow automation.

Core Components:

### Trigger

Starts workflow.

Examples:

- Schedule
- Email received
- File uploaded

### Action

Task performed by workflow.

Examples:

- Send email
- Start VM
- Update database

### Connector

Links services together.

Examples:

- Office 365
- Blob Storage
- SQL Database

Exam Note:

Logic Apps = Low-code workflow automation.

---

# Azure Event Grid

Purpose:

- Event routing service.

Uses Publish/Subscribe model.

Components:

### Publisher

Creates events.

### Event Grid

Routes events.

### Subscriber

Receives events.

Supports:

- HTTP
- MQTT

Exam Note:

Event Grid = Event notifications.

---

# Important Service Comparisons

|Service|Purpose|
|---|---|
|Azure Service Bus|Reliable messaging|
|Azure Event Grid|Event routing and notifications|
|Azure Logic Apps|Workflow automation|
|Azure API Management|API publishing and management|

---

# AZ-900 Exam Review

Know the difference between:

- Availability Sets vs Availability Zones
- Load Balancer vs Traffic Manager
- Service Bus vs Event Grid
- Logic Apps vs Functions
- API vs API Management
- VM vs App Service vs Functions vs AKS

---

### Quick Memory Sheet

**VM** = Full server

**App Service** = Web apps

**Functions** = Serverless code

**AKS** = Containers

**Load Balancer** = Traffic inside a region

**Traffic Manager** = Traffic across regions

**Service Bus** = Messaging

**Event Grid** = Events

**Logic Apps** = Workflows

**API Management** = API control center

**Availability Zones** = High availability

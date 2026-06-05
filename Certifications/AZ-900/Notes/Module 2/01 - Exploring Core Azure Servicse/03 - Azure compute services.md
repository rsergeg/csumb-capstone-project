
## Compute Overview

- Compute services provide processing power in Azure
- Used to run applications, websites, containers, and workloads
- Azure offers many compute options depending on your needs

Think:

**Compute = Running Stuff**

---

# Azure Virtual Machines (VMs)

### What They Are

- Virtual computers in Azure
- Can run Windows or Linux
- Full control over operating system and software

Benefits:

- Flexible
- Familiar
- Scalable

Think:

- A computer in Microsoft's datacenter

### Common Uses

- Legacy applications
- Development and testing environments
- Mission-critical applications
- Custom server workloads

Exam Note:

- VM = Infrastructure as a Service (IaaS)

---

# Azure App Service

### What It Is

- Managed platform for web apps and APIs
- Azure handles infrastructure

Benefits:

- No server management
- Easy deployment
- Automatic scaling

Think:

- Upload your web app and Azure handles the rest

### Common Uses

- Company websites
- E-commerce sites
- APIs
- Mobile app backends

Exam Note:

- App Service = Platform as a Service (PaaS)

---

# Azure Functions

### What It Is

- Serverless compute service
- Runs code when triggered by an event

Benefits:

- No server management
- Auto scaling
- Pay only when code runs

Think:

- Tiny programs that run automatically

### Common Uses

- Processing uploaded files
- Responding to database changes
- IoT events
- Automation tasks

Exam Note:

- Functions = Serverless computing

---

# Azure Kubernetes Service (AKS)

### What It Is

- Managed Kubernetes platform
- Runs containerized applications

Benefits:

- Container orchestration
- Automatic scaling
- Azure manages Kubernetes infrastructure

Think:

- Large-scale container management

### Common Uses

- Microservices
- Modern cloud applications
- Containerized enterprise apps

Exam Note:

- AKS = Kubernetes in Azure

---

# Azure Container Apps

### What It Is

- Fully managed container platform
- Serverless container hosting

Benefits:

- Easy deployment
- No infrastructure management
- Cost efficient

Think:

- App Service for containers

### Common Uses

- Web applications
- APIs
- Event-driven workloads

---

# Azure Container Instances (ACI)

### What It Is

- Fast container deployment service
- No VM or Kubernetes cluster needed

Benefits:

- Quick setup
- Simple container execution
- Pay for usage only

Think:

- Run a container instantly

### Common Uses

- Short-lived workloads
- Testing containers
- One-time jobs

Exam Note:

- Simplest way to run containers in Azure

---

# Azure Red Hat OpenShift

### What It Is

- Managed Red Hat OpenShift platform
- Built on Kubernetes

Benefits:

- Enterprise container platform
- Familiar OpenShift experience
- Azure-managed infrastructure

### Common Uses

- Organizations already using OpenShift
- Enterprise container environments
- Kubernetes workloads

Exam Note:

- OpenShift = Enterprise Kubernetes solution

---

# Azure Spring Apps

### What It Is

- Managed platform for Spring Boot applications

Benefits:

- Optimized for Java developers
- Easy deployment
- Automatic scaling

Think:

- Azure for Spring Boot applications

### Common Uses

- Java web applications
- Enterprise Spring Boot projects
- Cloud-native Java services

---

# Azure Service Fabric

### What It Is

- Distributed application platform
- Supports microservices and stateful applications

Benefits:

- High scalability
- High reliability
- Supports complex architectures

### Common Uses

- Large enterprise applications
- Stateful services
- Distributed systems

Think:

- Platform for building complex cloud apps

---

# Azure Batch

### What It Is

- High-performance computing service
- Runs large parallel jobs

Benefits:

- Massive scalability
- Efficient resource usage
- Handles heavy compute workloads

Think:

- Thousands of computers working on one problem

### Common Uses

- Scientific simulations
- AI and Machine Learning
- Data analysis
- Rendering jobs

Exam Note:

- Batch = High Performance Computing (HPC)

---

# Container Services Quick Comparison

### Azure Container Instances (ACI)

- Simplest option
- Fast deployment
- No orchestration

### Azure Container Apps

- Managed containers
- Serverless containers
- Easy scaling

### Azure Kubernetes Service (AKS)

- Full Kubernetes platform
- Enterprise workloads
- Advanced container management

### Azure Red Hat OpenShift

- Enterprise Kubernetes with OpenShift tools
- Best for existing OpenShift organizations

---

# Compute Service Selection Guide

### Need a full server?

→ Azure Virtual Machines

### Need a website or API?

→ Azure App Service

### Need event-driven code?

→ Azure Functions

### Need containers?

→ Azure Container Apps or ACI

### Need large-scale container orchestration?

→ AKS

### Need enterprise OpenShift?

→ Azure Red Hat OpenShift

### Need Spring Boot hosting?

→ Azure Spring Apps

### Need complex distributed applications?

→ Service Fabric

### Need HPC or massive batch processing?

→ Azure Batch

---

# Exam Notes

⚠️ VM = Full control, virtual server

⚠️ App Service = Managed web applications

⚠️ Functions = Serverless

⚠️ AKS = Kubernetes

⚠️ Container Apps = Simplified serverless containers

⚠️ ACI = Quick container execution

⚠️ OpenShift = Enterprise Kubernetes

⚠️ Spring Apps = Spring Boot hosting

⚠️ Service Fabric = Distributed applications

⚠️ Batch = High-performance computing

---

### Quick Memory Trick

**VM → App → Function**

- VM = Most control
- App Service = Less management
- Functions = No server management

As you move right, Azure manages more of the infrastructure for you.
## What is High Availability?

- High Availability (HA) means applications continue working even when failures occur.
- Goal is to minimize downtime and keep services available.
- Important for:
    - Online stores
    - Banking systems
    - Business applications
    - Cloud services

### Key Idea

- Remove **Single Points of Failure (SPOFs)**.
- A SPOF is one component whose failure could bring down the entire system.

---

# Core HA Concepts

## Redundancy

- Duplicate important resources.
- If one resource fails, another takes over.
- Examples:
    - Multiple VMs
    - Data replication
    - Multiple regions

Think:

- Backup systems ready to take over.

---

## Failover

- Automatically switches to a healthy resource when failure occurs.
- Reduces downtime.
- Improves user experience.

Think:

- Automatic backup plan.

---

## Scalability

- Ability to increase or decrease resources based on demand.
- Helps maintain availability during traffic spikes.

Examples:

- Holiday shopping traffic
- Special promotions
- Unexpected growth

---

# Azure Regions

## Region

- Geographic location containing Azure datacenters.

Examples:

- East US
- West US
- Central US

Benefits:

- Lower latency
- Data residency options

---

# Availability Zones (AZs)

## What They Are

- Separate datacenters within the same Azure region.
- Each has independent:
    - Power
    - Cooling
    - Networking

### Benefits

- Fault isolation
- Improved resiliency
- Better availability

Example:

- Zone 1 fails
- Zones 2 and 3 continue running

Exam Note:

- Availability Zones protect against datacenter failures.

---

# Azure Load Balancer

## Purpose

- Distributes traffic across multiple virtual machines.

### Benefits

- Prevents overload on a single VM.
- Improves scalability.
- Improves availability.

### Health Monitoring

- Monitors VM health.
- Removes failed VMs from service automatically.

Think:

- Traffic cop for your servers.

Exam Note:

- Load Balancer helps maintain availability during failures.

---

# Azure App Service Environment (ASE)

## Purpose

- Highly available hosting environment for web applications.

### Features

- Dedicated infrastructure
- Automatic scaling
- Built-in load balancing

### Benefits

- Handles traffic spikes
- Improved isolation
- Better availability

---

# High Availability Across Regions

## Why?

- Availability Zones protect within a region.
- Entire regions can still experience outages.

Solution:

- Deploy applications in multiple regions.

---

# Azure Traffic Manager

## Purpose

- Routes users to application instances in different regions.

### Features

- DNS-based traffic routing
- Monitors endpoint health
- Automatic failover

### Benefits

- Regional outage protection
- Better performance
- Reduced downtime

Think:

- Global traffic director.

Exam Note:

- Traffic Manager works across multiple Azure regions.

---

# Azure Site Recovery (ASR)

## Purpose

- Disaster recovery service.

### Features

- Replicates VMs to another region.
- Continuously synchronizes data.
- Supports recovery after major failures.

### Benefits

- Business continuity
- Disaster recovery
- Reduced downtime

Think:

- Backup datacenter in another region.

---

# Azure Front Door

## Purpose

- Global application delivery service.

### Features

- Global CDN
- Intelligent routing
- Global load balancing

### Benefits

- Faster content delivery
- Improved performance
- Automatic failover

Think:

- Front entrance for global users.

Exam Note:

- Front Door improves both performance and availability.

---

# High Availability Best Practices

## Design for Fault Tolerance

- Build redundant systems.
- Avoid single points of failure.

---

## Monitoring and Alerts

- Continuously monitor resources.
- Configure automated alerts.

Benefits:

- Detect issues quickly.
- Faster response times.

---

## Test Failover Procedures

- Regularly test disaster recovery plans.
- Verify backups and recovery processes.

Benefits:

- Confirms recovery plans actually work.

---

## Use Availability Sets

### Purpose

- Spread VMs across fault domains and update domains.

Benefits:

- Protects against hardware failures.
- Protects during maintenance events.

Exam Note:

- Availability Sets improve VM uptime.

---

## Use Azure Managed Services

Examples:

- Azure SQL Database
- Azure Cosmos DB
- Azure Functions

Benefits:

- Azure manages infrastructure.
- Higher availability built in.
- Reduced administrative effort.

---

# Exam Notes

⚠️ HA = High Availability

⚠️ Goal = Reduce downtime and eliminate single points of failure

⚠️ Availability Zones = Multiple datacenters within a region

⚠️ Load Balancer = Distributes traffic across VMs

⚠️ Traffic Manager = Routes traffic between regions

⚠️ Azure Site Recovery = Disaster recovery solution

⚠️ Azure Front Door = Global traffic routing and CDN

⚠️ Availability Sets = Protect VMs from hardware and maintenance failures

⚠️ Managed services often provide built-in high availability

---

### Quick Memory Trick

**Zone → Region → Global**

- Availability Zones = Datacenter protection
- Traffic Manager = Region protection
- Front Door = Global availability and performance
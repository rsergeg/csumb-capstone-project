
## What is Azure Traffic Manager?

- Azure Traffic Manager is a **DNS-based traffic load balancer**.
- Routes users to the best application endpoint.
- Works across multiple Azure regions.
- Improves performance and availability.

Think:

- Traffic Manager = Global traffic director.

Unlike Azure Load Balancer:

- Load Balancer works within a region.
- Traffic Manager works between regions.

Exam Note:

- Traffic Manager operates at the **DNS level**.

---

# Why Use Traffic Manager?

## Better User Experience

- Sends users to the closest endpoint.
- Reduces latency.
- Faster page loading.

Example:

- User in Europe → Europe region
- User in US → US region

---

## High Availability

- Monitors endpoint health.
- Automatically redirects traffic if a region fails.

Benefits:

- Reduced downtime
- Improved reliability

---

## Global Reach

- Applications can serve users worldwide.
- Routes users to the nearest deployment.

---

## Scalability

- Handles growing traffic volumes.
- Supports multiple Azure regions.

---

## Cost Optimization

- Can route traffic to lower-cost regions.
- Helps manage cloud expenses.

---

# Traffic Routing Methods

## Priority Routing

### How It Works

- Sends all traffic to the primary endpoint.
- Uses backup endpoint only if primary fails.

Think:

- Primary server + backup server

Best for:

- Disaster recovery

---

## Weighted Routing

### How It Works

- Traffic is distributed based on assigned weights.

Example:

- Region A = 80%
- Region B = 20%

Uses:

- Gradual deployments
- Traffic testing

---

## Geographic Routing

### How It Works

- Sends users to the closest geographic region.

Example:

- Europe users → Europe endpoint
- US users → US endpoint

Benefits:

- Lower latency
- Better performance

---

## Performance Routing

### How It Works

- Sends traffic to the fastest responding endpoint.

Benefits:

- Best user experience
- Reduced response times

Exam Note:

- Geographic = Closest location
- Performance = Fastest response

---

# Health Monitoring

## Purpose

- Continuously checks endpoint health.

Methods:

- HTTP
- TCP
- Ping

Benefits:

- Detects failures quickly.
- Sends traffic only to healthy endpoints.

---

# Automatic Failover

## What Happens During Failure?

1. Endpoint becomes unavailable.
2. Traffic Manager detects failure.
3. Traffic automatically moves to a healthy endpoint.

Benefits:

- High availability
- Reduced downtime

Think:

- Automatic backup route.

---

# Metrics and Analytics

Traffic Manager provides:

- Traffic statistics
- Endpoint health data
- Performance metrics

Benefits:

- Easier troubleshooting
- Better planning

---

# Traffic Manager vs Load Balancer

## Azure Traffic Manager

- DNS-based
- Routes between regions
- Global traffic management

Example:

US Region ↔ Europe Region

---

## Azure Load Balancer

- Layer 4 load balancer
- Routes between servers
- Regional traffic management

Example:

VM1 ↔ VM2 ↔ VM3

Exam Note:

Traffic Manager = Global

Load Balancer = Regional

---

# How Traffic Manager Works

### Step 1

User requests website.

Example:

partners.contoso.com

---

### Step 2

DNS query begins.

---

### Step 3

Traffic Manager receives DNS request.

---

### Step 4

Traffic Manager checks:

- Endpoint health
- Routing rules

---

### Step 5

Best endpoint selected.

Example:

- US endpoint
- Europe endpoint
- Asia endpoint

---

### Step 6

Traffic Manager returns endpoint IP.

---

### Step 7

User connects directly to that endpoint.

Important:

Traffic Manager only handles DNS resolution.

It does NOT sit in the traffic path afterward.

Exam Note:

- Traffic Manager routes DNS requests, not application traffic itself.

---

# Real World Example

## Contoso Partner Portal

Application deployed in:

- US Region
- Europe Region
- Asia Region

Traffic Manager:

- Checks health of all regions.
- Chooses best endpoint.
- Sends user to closest healthy region.

Result:

- Better performance
- Better availability

---

# Important Considerations

## Public DNS Required

Traffic Manager requires:

- Public-facing DNS name

Cannot be used with:

- Internal-only applications

---

## Pricing

Pricing depends on:

- Number of DNS queries processed

---

## Regional Load Balancing

If you need load balancing inside a region:

Use:

- Azure Load Balancer
- Azure Application Gateway

Not Traffic Manager.

---

# Exam Notes

⚠️ Azure Traffic Manager = DNS-based traffic routing

⚠️ Routes traffic between regions

⚠️ Supports:

- Priority
- Weighted
- Geographic
- Performance routing

⚠️ Automatically performs failover

⚠️ Monitors endpoint health

⚠️ Traffic Manager = Global traffic management

⚠️ Azure Load Balancer = Regional traffic management

⚠️ Traffic Manager does NOT directly handle application traffic

---

### Quick Memory Trick

**Traffic Manager = Which Region?**

**Load Balancer = Which Server?**

User  
↓  
Traffic Manager chooses region  
↓  
Load Balancer chooses server  
↓  
Application responds

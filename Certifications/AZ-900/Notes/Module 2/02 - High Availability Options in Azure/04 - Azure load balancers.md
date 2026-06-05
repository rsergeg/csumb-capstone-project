## What is Azure Load Balancer?

- Azure Load Balancer distributes incoming network traffic across multiple servers.
- Prevents a single server from becoming overloaded.
- Improves:
    - Performance
    - Scalability
    - Availability

Think:

- One cashier = long line
- Multiple cashiers = faster service

Azure Load Balancer sends traffic to multiple VMs instead of one.

---

# How It Works

### Basic Process

1. User sends request.
2. Load Balancer receives request.
3. Load Balancer checks available VMs.
4. Traffic is sent to a healthy VM.
5. User receives response.

Benefits:

- Better performance
- Reduced downtime
- Improved user experience

---

# Layer 4 Load Balancer

Azure Load Balancer operates at:

### OSI Layer 4

Transport Layer

Works with:

- TCP
- UDP

Exam Note:

- Azure Load Balancer = Layer 4 service

---

# Health Probes

## What They Do

- Continuously monitor backend VMs.
- Check if a VM is healthy.

If a VM fails:

- Load Balancer stops sending traffic.
- Traffic is redirected to healthy VMs.

Think:

- Automatic health check system.

---

# Types of Load Balancer

## Public Load Balancer

### Purpose

- Internet-facing applications.
- Accepts traffic from the public internet.

Examples:

- Websites
- Web applications
- APIs

Uses:

- Public IP address

---

## Internal Load Balancer

### Purpose

- Internal company applications.
- Traffic stays inside the Azure network.

Examples:

- Internal databases
- Business applications
- Backend services

Uses:

- Private IP address

Exam Note:

Public = Internet

Internal = Private network

---

# Benefits of Azure Load Balancer

## Scalability

- Add or remove VMs as needed.
- Automatically distributes traffic.

---

## High Availability

- Redirects traffic away from failed VMs.
- Minimizes downtime.

---

## Performance

- Low latency
- High throughput

Benefits:

- Faster response times
- Better customer experience

---

## Protocol Support

Supports:

- TCP
- UDP
- HTTP
- HTTPS

---

## Security

Works with:

### Network Security Groups (NSGs)

Benefits:

- Controls traffic flow
- Improves security

---

# Key Components

## Frontend IP

- Entry point for client requests.
- Can be:
    - Public IP
    - Private IP

Think:

- Front door of the application

---

## Backend Pool

- Group of servers handling requests.

Usually contains:

- Virtual Machines
- VM Scale Sets

Think:

- Workers doing the actual work

---

## Health Probes

- Monitor VM health.
- Remove unhealthy servers from rotation.

---

## Load Balancing Rules

- Define how traffic is distributed.
- Based on:
    - Ports
    - Protocols

Examples:

- Port 80 (HTTP)
- Port 443 (HTTPS)

---

# HA Ports

## Purpose

- Load balance all TCP and UDP traffic.
- Supports multiple ports simultaneously.

Benefits:

- Simpler configuration
- High availability

---

# Inbound NAT Rules

## Purpose

- Send traffic to a specific VM.

Example:

Admin wants RDP access to a specific server.

Load Balancer forwards:

Public Port  
↓  
Specific VM

Think:

- Port forwarding

---

# Outbound Rules

## Purpose

- Allow backend VMs to access the internet.

Uses:

- Software updates
- External APIs
- Downloads

---

# Distribution Modes

## Hash-Based

Uses:

- Source IP
- Source Port
- Destination IP
- Destination Port
- Protocol

Benefits:

- Even traffic distribution

Limitation:

- No session persistence

---

## Session Persistence (Client IP)

- Same user always goes to the same server.

Benefits:

- Consistent user experience

Examples:

- Shopping carts
- User sessions

---

## Session Persistence (Client IP + Protocol)

- More specific session tracking.
- Same client and protocol stay together.

---

# Global Load Balancer

## Purpose

- Load balance across Azure regions.

Benefits:

- Global availability
- Disaster recovery
- Reduced latency

Features:

- Cross-region failover
- Global traffic distribution
- Client IP preservation

Exam Note:

- Global Load Balancer supports multiple regions.

---

# Regional Redundancy

## What It Means

- Multiple regional load balancers.
- Connected through a cross-region load balancer.

If one region fails:

- Traffic automatically redirects.
- Service remains available.

Benefits:

- Disaster recovery
- High availability

---

# Ultra-Low Latency

## Geo-Proximity Routing

Traffic goes to:

- Closest Azure region
- Best-performing deployment

Benefits:

- Faster response times
- Better customer experience

Think:

- Nearest store serves the customer.

---

# Exam Notes

⚠️ Azure Load Balancer = Layer 4 Load Balancer

⚠️ Public Load Balancer = Internet-facing

⚠️ Internal Load Balancer = Private network traffic

⚠️ Health Probes check VM health

⚠️ Backend Pool = Group of servers receiving traffic

⚠️ Load Balancer improves:

- Scalability
- Availability
- Performance

⚠️ Global Load Balancer supports cross-region traffic

⚠️ Regional redundancy protects against regional outages

---

### Quick Memory Trick

**Frontend → Health Probe → Backend Pool**

Client  
↓  
Frontend IP  
↓  
Load Balancer  
↓  
Health Probe checks servers  
↓  
Backend Pool receives traffic
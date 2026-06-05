
## High Availability Review

- Virtual Machines have some availability by default.
- Businesses often need higher availability.
- Azure provides:
    - Availability Sets
    - Availability Zones
    - Fault Domains

Purpose:

- Reduce downtime
- Improve reliability
- Protect against failures

---

# Availability Sets

## What They Do

- Spread VMs across different hardware within a datacenter.
- Protect against server and rack failures.
- Help prevent a single hardware issue from taking down all VMs.

Think:

- Don't put all your eggs in one basket.

---

## Benefits

- Higher availability than a single VM.
- Protection from hardware failures.
- Protection during maintenance events.

Exam Note:

- Availability Sets work within a single datacenter.

---

# Fault Domains

## What is a Fault Domain?

- A group of hardware resources within a datacenter.
- Includes:
    - Servers
    - Power supplies
    - Network equipment
    - Storage

Think:

- Neighborhoods inside a datacenter.

---

## Why They Matter

- If one fault domain fails, others continue operating.
- Reduces impact of hardware failures.
- Improves application uptime.

Exam Note:

- Fault Domains are used by Availability Sets.

---

# Availability Zones

## What Are They?

- Separate physical datacenters within the same Azure region.
- Each zone has independent:
    - Power
    - Cooling
    - Networking

Think:

- Multiple datacenters in the same city.

---

## Benefits

- Stronger protection than Availability Sets.
- Survives an entire datacenter outage.
- Improves resiliency for critical applications.

Example:

- Zone 1 fails
- Zone 2 and Zone 3 continue running

---

## SLA

Availability Zones provide:

✅ **99.99% SLA**

Very little downtime per month.

Exam Note:

- Availability Zones provide the highest availability option discussed in AZ-900.

---

# Azure Regions

## What is a Region?

- Geographic area containing multiple Azure datacenters.

Examples:

- East US
- West US
- Central US

---

## Relationship

Region  
↓  
Availability Zones  
↓  
Fault Domains

Think:

- Region = City
- Availability Zone = Datacenter
- Fault Domain = Neighborhood inside datacenter

---

# Availability Sets vs Availability Zones

## Availability Sets

- Protect against server failures.
- Operate within one datacenter.
- Use fault domains and update domains.

Availability:

- Approximately 99.95% SLA

---

## Availability Zones

- Protect against entire datacenter failures.
- Multiple datacenters within a region.
- Independent power, cooling, and networking.

Availability:

- Approximately 99.99% SLA

---

# SLA Comparison

### Single VM

- Premium SSD or Ultra Disk
- Around 99.9% SLA

### Availability Set

- Multiple VMs
- Around 99.95% SLA

### Availability Zone

- Multiple zones
- Around 99.99% SLA

Exam Note:

Microsoft loves questions comparing these three availability levels.

---

# Choosing Between Sets and Zones

## Use Availability Sets When

- Application is in one datacenter.
- Moderate availability is acceptable.
- Lower complexity is desired.

---

## Use Availability Zones When

- Mission-critical applications.
- Maximum uptime required.
- Protection from datacenter outages needed.

Examples:

- Banking applications
- E-commerce platforms
- Healthcare systems

---

# Design Considerations

Before using Availability Zones ask:

### Does the Region Support Availability Zones?

- Not every Azure region supports them.

---

### Does the Service Support Availability Zones?

- Some Azure services support zones.
- Others do not.

---

### What Availability Does the Business Need?

- 99.9%
- 99.95%
- 99.99%

Choose based on business requirements.

---

# Exam Notes

⚠️ Availability Set = Protects against server/rack failures

⚠️ Availability Zone = Protects against datacenter failures

⚠️ Fault Domain = Group of hardware resources

⚠️ Region = Geographic area with multiple datacenters

⚠️ Availability Sets use Fault Domains

⚠️ Availability Zones have independent power, cooling, and networking

⚠️ Single VM ≈ 99.9% SLA

⚠️ Availability Set ≈ 99.95% SLA

⚠️ Availability Zone ≈ 99.99% SLA

---

### Quick Memory Trick

**Server → Datacenter → Region**

- Fault Domain = Server-level protection
- Availability Set = Datacenter protection
- Availability Zone = Multi-datacenter protection
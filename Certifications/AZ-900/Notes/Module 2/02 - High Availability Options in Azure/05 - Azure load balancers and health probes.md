
## What is a Health Probe?

- Health probes monitor backend Virtual Machines (VMs).
- They check if a VM is healthy and responding.
- Azure Load Balancer uses probe results to decide where traffic should go.

Think:

- Health probe = heartbeat monitor for servers.

---

# Why Health Probes Matter

Without health probes:

- Load Balancer might send traffic to a failed VM.
- Users could experience errors or downtime.

With health probes:

- Unhealthy VMs are removed automatically.
- Traffic is sent only to healthy servers.

Benefits:

- Better uptime
- Better performance
- Better user experience

---

# E-Commerce Example

### Normal Operation

- Load Balancer sits in front of multiple web servers.
- Customer requests are spread across servers.
- Website remains responsive.

### During Failure

- One VM crashes.
- Health probe detects failure.
- Load Balancer stops sending traffic to that VM.
- Remaining VMs continue serving customers.

Result:

- Website stays online.

---

# Supported Probe Protocols

## Standard Load Balancer

Supports:

- TCP
- HTTP
- HTTPS

---

## Basic Load Balancer

Supports:

- TCP
- HTTP

Exam Note:

Standard SKU supports HTTPS probes.

---

# TCP Probes

## How They Work

- Attempt a TCP connection to the VM.
- If connection succeeds:
    - VM is healthy.
- If connection fails:
    - VM is unhealthy.

Good for:

- Basic service availability checks.

---

# HTTP Probes

## How They Work

- Send HTTP GET request to a specific path.
- Example:

```
/health
```

Healthy response:

- HTTP 200

Unhealthy responses:

- 403
- 404
- 500

Exam Note:

HTTP 200 = Healthy

---

# HTTPS Probes

## How They Work

- Same as HTTP probes.
- Uses encrypted HTTPS connection.

Additional Requirement:

- Certificates must use SHA256 or stronger.

Benefits:

- Secure health monitoring.

---

# Probe Failure

A VM becomes unhealthy when:

### TCP

- No response
- Connection timeout
- TCP reset received

---

### HTTP/HTTPS

- No response
- Timeout occurs
- HTTP response other than 200

Examples:

- 404
- 500
- 403

---

# Probe Success

A VM becomes healthy when:

### TCP

- Connection succeeds

### HTTP/HTTPS

- HTTP 200 returned

Once healthy:

- Load Balancer resumes routing traffic.

---

# Probe Intervals

## Default Behavior

- Probe runs every 5 seconds.

Purpose:

- Quickly detect failures.

---

## Timeouts

### HTTP/HTTPS

- 30-second timeout

If no response:

- Probe fails

---

# Probe Port

## Best Practice

Use a port that reflects application health.

Example:

Application:

- Port 443

Probe:

- Port 443

Benefits:

- More accurate monitoring

---

# Custom Health Responses

Applications can return custom responses.

Uses:

- Maintenance mode
- Connection draining
- Traffic throttling

Benefits:

- More control over traffic flow

---

# HA Ports

## Special Configuration

- One probe determines health of the entire VM.

Used when:

- Load balancing all ports

Exam Note:

HA Ports = all TCP and UDP traffic.

---

# Important Best Practices

## Keep VMs Running

- Health probes only monitor active VMs.

---

## Don't Block Probe Traffic

Probe source IP:

**168.63.129.16**

If blocked:

- Probe fails
- VM marked unhealthy

Exam Note:

Microsoft loves asking about this IP.

---

## Monitor Probe Status

Use:

### Azure Monitor

Benefits:

- View VM health
- Track failures
- Troubleshoot issues

---

## Test Failures

Use:

### Network Security Groups (NSGs)

Can simulate:

- Probe failures
- VM outages

Useful for testing failover.

---

# Probe Fluctuation Protection

Azure delays returning a VM to service after failure.

Purpose:

- Prevents constant switching.
- Avoids disruptions from temporary glitches.

Think:

- Wait and verify before trusting the VM again.

---

# Limitations

## HTTPS Probes

Do NOT support:

- Client certificate authentication

---

## HTTP Restrictions

Cannot use these ports:

- 19
- 21
- 25
- 70
- 110
- 119
- 143
- 220
- 993

---

# Exam Notes

⚠️ Health Probes monitor VM health

⚠️ Healthy VMs receive traffic

⚠️ Unhealthy VMs are removed from rotation

⚠️ Standard Load Balancer supports:

- TCP
- HTTP
- HTTPS

⚠️ HTTP 200 = Healthy

⚠️ Default probe interval = 5 seconds

⚠️ Probe source IP = 168.63.129.16

⚠️ Azure Monitor can track probe health

⚠️ Health probes help achieve High Availability (HA)

---

### Quick Memory Trick

**Probe → Check → Route**

Health Probe  
↓  
Checks VM  
↓  
Healthy = Send Traffic  
↓  
Unhealthy = Remove Traffic


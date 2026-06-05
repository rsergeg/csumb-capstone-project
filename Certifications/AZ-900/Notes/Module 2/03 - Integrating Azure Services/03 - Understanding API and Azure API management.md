## What is an API?

API = **Application Programming Interface**

- A set of rules that allows software applications to communicate.
- Defines how data is requested and exchanged.
- Acts like a contract between applications.

Think:

- API = Waiter in a restaurant.
- You place a request.
- The waiter delivers it to the kitchen.
- The waiter brings back the result.

---

# Why APIs Matter

## Enable Communication

- Applications exchange data.
- Systems work together.
- Services can integrate easily.

Examples:

- Mobile apps talking to servers.
- Websites retrieving weather data.
- Login systems validating users.

---

## Support Automation

- Developers can retrieve and manage data automatically.
- Eliminates manual processes.

Benefits:

- Faster development
- Better efficiency
- Reduced complexity

---

## Business Value

- Makes platforms easier to integrate.
- Encourages innovation.
- Supports third-party applications.

Think:

- More APIs = More integration possibilities.

---

# Types of APIs

## REST API

Representational State Transfer

Most common API type.

Uses:

- HTTP methods
    - GET
    - POST
    - PUT
    - DELETE

Benefits:

- Simple
- Flexible
- Widely used

Exam Note:

REST is the most commonly referenced API style.

---

## SOAP API

Simple Object Access Protocol

Characteristics:

- XML-based
- Strict standards
- Enterprise-focused

Benefits:

- Reliability
- Standardization
- Security

Common in:

- Large enterprise systems

---

## GraphQL

Graph Query Language

Benefits:

- Clients request exactly the data they need.
- Reduces unnecessary data transfer.

Good for:

- Efficient data retrieval

---

## RPC

Remote Procedure Call

Purpose:

- Execute functions on remote systems.

Think:

- Calling a function on another computer.

---

# Synchronous vs Asynchronous APIs

## Synchronous

- Request sent.
- Wait for response.
- Immediate result.

Example:

- Login request

---

## Asynchronous

- Request sent.
- Processing happens later.
- Application continues working.

Benefits:

- Better scalability
- Better resource usage

Exam Note:

Azure Service Bus is an example of asynchronous communication.

---

# What is Azure API Management?

Azure API Management (APIM)

- Azure service for managing APIs.
- Platform as a Service (PaaS).
- Central location for API governance.

Think:

- API Management = Control center for APIs.

---

# Why Use Azure API Management?

Organizations often have:

- Many APIs
- Different applications
- Multiple environments

Azure API Management helps organize and manage them all.

---

# Core Capabilities

## API Lifecycle Management

Manages APIs from:

- Creation
- Publishing
- Updating
- Retirement

Benefits:

- Better control
- Easier maintenance

---

## Backend Abstraction

Hides backend complexity.

API consumers:

- Do not need to know how backend systems work.

Benefits:

- Consistent developer experience

---

## Security and Access Control

Protects APIs.

Can secure:

- Cloud services
- On-premises services

Benefits:

- Controlled access
- Reduced risk

---

## Performance Optimization

Improves:

- Speed
- Scalability
- Responsiveness

Benefits:

- Better user experience

---

## Monitoring and Observability

Tracks:

- API usage
- Performance
- Errors
- Bottlenecks

Benefits:

- Easier troubleshooting
- Better planning

---

# Common Organizational Uses

## Legacy Modernization

Older systems can be exposed as APIs.

Benefits:

- Reuse existing systems
- Modernize gradually

---

## Application Integration

Makes applications easier to connect.

Benefits:

- Lower integration costs
- Faster deployment

---

## Multi-Channel Experiences

Same API can support:

- Websites
- Mobile apps
- Partner portals

Benefits:

- Reuse
- Consistency

---

## B2B Integration

Business-to-business communication.

Examples:

- Vendors
- Partners
- Customers

Benefits:

- Easier data exchange
- Better collaboration

---

# API Management vs Service Bus

### Azure API Management

Used for:

- Managing APIs
- Securing APIs
- Publishing APIs

Think:

- Front door to services

---

### Azure Service Bus

Used for:

- Messaging between applications
- Queues
- Topics
- Asynchronous communication

Think:

- Mail delivery system

Exam Note:

Microsoft loves asking the difference between these two.

---

# AZ-900 Exam Notes

⚠️ API = Application Programming Interface

⚠️ APIs allow applications to communicate

⚠️ REST uses:

- GET
- POST
- PUT
- DELETE

⚠️ SOAP uses XML and strict standards

⚠️ Azure API Management = API governance platform

⚠️ Azure API Management is a PaaS service

⚠️ API Management provides:

- Security
- Monitoring
- Lifecycle management
- Performance optimization

⚠️ API Management helps expose cloud and on-premises services as APIs

---

### Quick Memory Trick

**API = Communication**

Software ↔ Software

**API Management = Control**

Manage, Secure, Monitor APIs

**Service Bus = Messaging**

Application ↔ Queue ↔ Application

For AZ-900, the most important takeaway is:

**Azure API Management is used to publish, secure, monitor, and manage APIs throughout their lifecycle.**
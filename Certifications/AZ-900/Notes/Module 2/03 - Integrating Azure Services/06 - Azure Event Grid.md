## What is Azure Event Grid?

- Azure Event Grid is a fully managed event routing service.
- Uses a Publish/Subscribe (Pub/Sub) model.
- Helps applications communicate through events.
- Supports event-driven architectures.

Think:

- Event Grid = Event traffic controller.

Example:

- File uploaded
- Event Grid detects event
- Notifies interested services

---

# How Event Grid Works

## Publishers

- Generate events.
- Send event notifications to Event Grid.

Examples:

- Azure Blob Storage
- Applications
- IoT devices

---

## Event Grid

- Receives events.
- Routes events to subscribers.
- Ensures reliable delivery.

Think:

- Post office for events.

---

## Subscribers

- Receive events they care about.
- Perform actions when events occur.

Examples:

- Azure Functions
- Logic Apps
- Webhooks

---

# Publish / Subscribe Model

## Publish

A service creates an event.

Example:

- New product image uploaded.

---

## Subscribe

A service listens for events.

Example:

- Website update service waits for new product uploads.

---

## Event Routing

Event Grid automatically connects publishers and subscribers.

Benefits:

- Loose coupling
- Scalability
- Simpler architecture

Exam Note:

Event Grid uses the Publish/Subscribe model.

---

# Key Features

## Fully Managed Service

Azure handles:

- Infrastructure
- Scaling
- Availability
- Maintenance

---

## Multiple Protocol Support

Supports:

- HTTP
- MQTT

Exam Note:

MQTT is commonly used for IoT devices.

---

## Push and Pull Delivery

### Push Delivery

- Event Grid sends events automatically.

Think:

- Notification pushed to you.

---

### Pull Delivery

- Applications retrieve events when ready.

Think:

- Checking your mailbox when convenient.

Exam Note:

Event Grid supports both push and pull delivery.

---

## CloudEvents 1.0 Support

Benefits:

- Industry standard format
- Better interoperability
- Easier integration

---

# Common Use Cases

## IoT Solutions

Scenario:

- Sensors collect temperature data.

Process:

Sensor  
↓  
Event Grid  
↓  
Azure Function  
↓  
Database

Benefits:

- Real-time monitoring
- Scalable processing

---

## Blob Storage Events

Scenario:

- Product image uploaded.

Process:

Blob Storage  
↓  
Event Grid  
↓  
Logic App  
↓  
Update website

Benefits:

- Automatic updates
- No manual intervention

---

## Serverless Applications

Scenario:

- Social media platform experiences traffic spikes.

Process:

User Activity  
↓  
Event Grid  
↓  
Azure Functions  
↓  
Scale resources

Benefits:

- Cost savings
- Automatic scaling

---

## Analytics Processing

Scenario:

- Large amounts of event data.

Solution:

- Pull events gradually.
- Prevent resource overload.

Benefits:

- Controlled processing
- Better performance

---

# Event Grid and Microservices

## What are Microservices?

- Small independent applications.
- Work together to form larger systems.

Examples:

- Order service
- Payment service
- Shipping service

---

## Loose Coupling

Services:

- Do not communicate directly.
- Communicate through events.

Benefits:

- Easier development
- Easier deployment
- Easier maintenance

Exam Note:

Event Grid promotes loose coupling.

---

## Scalability

Each microservice:

- Can scale independently.

Benefits:

- Better performance
- More efficient resource usage

---

## Resilience

If one service fails:

- Other services continue working.

Benefits:

- Improved reliability
- Reduced downtime

---

# Event Grid vs Service Bus

This is a common AZ-900 comparison.

## Azure Event Grid

Used for:

- Event notifications
- Reactive systems
- Publish/Subscribe events

Examples:

- Blob uploaded
- User registered
- Sensor reading received

Think:

- "Something happened."

---

## Azure Service Bus

Used for:

- Reliable messaging
- Queues
- Business transactions

Examples:

- Orders
- Payments
- Inventory processing

Think:

- "Process this task."

---

# Event Grid vs Logic Apps

## Event Grid

- Routes events.
- Handles event notifications.

---

## Logic Apps

- Executes workflows.
- Performs business actions.

Example:

Blob uploaded  
↓  
Event Grid detects event  
↓  
Logic App runs workflow

---

# AZ-900 Exam Notes

⚠️ Event Grid = Event routing service

⚠️ Uses Publish/Subscribe model

⚠️ Publishers send events

⚠️ Subscribers receive events

⚠️ Supports:

- HTTP
- MQTT

⚠️ Supports:

- Push delivery
- Pull delivery

⚠️ Common integrations:

- Azure Functions
- Logic Apps
- Blob Storage

⚠️ Event Grid supports event-driven architectures

⚠️ Promotes:

- Loose coupling
- Scalability
- Resilience

⚠️ Event Grid = "Something happened"

⚠️ Service Bus = "Process this message"

---

### Quick Memory Trick

**Event Grid = Notifications**

"New file uploaded!"

"New user registered!"

"Sensor reported data!"

**Service Bus = Work Queue**

"Process this order."

"Generate this invoice."

"Ship this package."

For AZ-900, remember:

**Azure Event Grid is Microsoft's event routing service that connects publishers and subscribers in event-driven applications using the Publish/Subscribe model.**


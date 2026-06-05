
#### Azure Functions

- Serverless compute service that runs code in response to events.
- Triggered by actions such as:
    - HTTP requests
    - File uploads
    - Database changes
    - Timer schedules
- Azure manages the infrastructure automatically.
- Scales up and down based on demand.
- Pay only for execution time and resources used.
- Common uses:
    - API endpoints
    - Automation tasks
    - Event processing
    - Backend services for web and mobile apps

**Azure Functions vs Logic Apps**

- Azure Functions = write code to perform tasks.
- Azure Logic Apps = visual workflow automation with connectors.
- Often used together in larger solutions.

---

#### Azure Virtual Machines (VMs)

- Provides full control over operating system and software.
- Supports Windows and Linux.
- Suitable for:
    - Legacy applications
    - Custom software
    - Lift-and-shift migrations
- User is responsible for:
    - OS updates
    - Security patches
    - Application maintenance

**Benefits**

- Flexible sizing options.
- Can scale resources as needed.
- Supports many workloads.

---

#### Virtual Machine Scale Sets (VMSS)

- Group of identical VMs managed together.
- Automatically increases or decreases VM count.
- Responds to:
    - Traffic demand
    - CPU utilization
    - Scheduled events
- Often used with Azure Load Balancer.

**Benefits**

- Automatic scaling.
- High availability.
- Easier management of large VM deployments.

---

#### Monitoring Azure Virtual Machines

- Azure Monitor collects performance and health information.
- Tracks:
    - CPU usage
    - Memory usage
    - Disk performance
    - Network activity
- Helps identify bottlenecks and troubleshoot issues.
- Supports alerts and reporting.

---

#### Azure Service Bus

- Messaging service for communication between applications.
- Works as a message broker.
- Allows applications to communicate without being directly connected.

**Queues**

- Point-to-point messaging.
- One sender → one receiver.
- Messages processed in order.

**Topics and Subscriptions**

- Publish/subscribe model.
- One message can be delivered to multiple subscribers.
- Useful for events and notifications.

---

#### Advanced Service Bus Features

- Reliable message delivery.
- Message persistence prevents data loss.
- Dead Letter Queue (DLQ) stores failed messages for troubleshooting.
- Message filtering controls which subscribers receive messages.
- Supports complex enterprise integrations.

---

#### Key Takeaways

- Azure Functions = serverless code execution.
- Logic Apps = workflow automation.
- Virtual Machines = full control over operating systems and applications.
- VM Scale Sets = automatic VM scaling and high availability.
- Azure Monitor = tracks VM performance and health.
- Service Bus = reliable communication between applications.
- Topics and subscriptions support publish/subscribe messaging patterns.

### AZ-900 Exam Tips

- **Functions = code triggered by events**
- **Logic Apps = no-code/low-code workflows**
- **VM = maximum control**
- **VMSS = automatic scaling of VMs**
- **Service Bus = messaging between applications**
- **Queue = one receiver**
- **Topic = multiple receivers (publish/subscribe)**



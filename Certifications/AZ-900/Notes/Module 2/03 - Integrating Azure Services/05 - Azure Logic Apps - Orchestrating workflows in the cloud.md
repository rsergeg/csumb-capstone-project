
## What is Azure Logic Apps?

- Azure Logic Apps is a workflow automation service.
- Used to automate tasks and business processes.
- Connects different services together with little or no code.

Think:

- If This Happens → Then Do That

Example:

- New email arrives
- Save attachment to OneDrive
- Send Teams notification

---

# Why Use Logic Apps?

Benefits:

- Automates repetitive tasks
- Reduces manual work
- Connects cloud and on-premises services
- Improves efficiency
- Supports business workflows

Exam Note:

- Logic Apps = Workflow Automation

---

# Core Components

## Workflows

- The automation process you create.
- Made up of triggers and actions.

Think:

- Workflow = Recipe

---

## Triggers

- Event that starts the workflow.

Examples:

- New email received
- New file uploaded
- Scheduled time
- Database update

Exam Note:

- Trigger starts the workflow.

---

## Actions

- Tasks performed after the trigger.

Examples:

- Send email
- Start VM
- Update database
- Call API

Exam Note:

- Actions happen after the trigger.

---

## Connectors

- Connect Logic Apps to services.

Examples:

- Azure Blob Storage
- Office 365
- Dynamics 365
- SQL Database
- Twitter/X

Think:

- Connector = Bridge between services.

---

# VM Automation Example

## Goal

Automatically:

- Start VM at 8:00 AM
- Stop VM at 6:00 PM

Benefits:

- Saves money
- Reduces wasted resources

---

## Workflow Process

### Trigger

Recurrence Schedule

Runs:

- Daily
- 8:00 AM

---

### Action

Start Virtual Machine

Azure automatically:

- Starts VM
- Makes resources available

---

### Evening Workflow

Trigger:

- Daily
- 6:00 PM

Action:

- Stop Virtual Machine

Result:

- Lower Azure costs

---

# Logic App Workflow Types

## Stateful Workflow

- Saves workflow history.
- Supports long-running processes.
- More resilient.

Used for:

- Business processes
- Auditing
- Tracking workflow execution

Exam Note:

- Stateful stores execution history.

---

# Scheduling Workflows

Common trigger:

### Recurrence

Runs:

- Daily
- Weekly
- Monthly
- Custom schedules

Uses:

- VM automation
- Reports
- Maintenance tasks

---

# Advanced Capabilities

## Multiple Actions

One workflow can:

- Send email
- Update database
- Call API
- Create file

All in sequence.

---

## Conditional Logic

Supports:

IF condition is true  
→ Action A

ELSE  
→ Action B

Benefits:

- Smarter workflows

---

## Hundreds of Connectors

Can integrate with:

- Azure services
- Microsoft 365
- Databases
- Third-party applications

---

# Common Use Cases

### IT Operations

- Start/stop VMs
- Send alerts
- Create tickets

---

### Business Processes

- Approval workflows
- Employee onboarding
- Document processing

---

### Cloud Automation

- File movement
- Data synchronization
- Scheduled jobs

---

# Logic Apps vs Functions

## Azure Logic Apps

- Workflow automation
- Visual designer
- Low-code/no-code

Think:

- Business process automation

---

## Azure Functions

- Runs custom code
- Event-driven
- Serverless compute

Think:

- Code execution

Exam Note:

Logic Apps = Workflows

Functions = Code

---

# AZ-900 Exam Notes

⚠️ Azure Logic Apps = Workflow automation service

⚠️ Trigger starts a workflow

⚠️ Actions perform tasks

⚠️ Connectors link services together

⚠️ Recurrence trigger runs on a schedule

⚠️ Can automate VM startup and shutdown

⚠️ Supports low-code/no-code development

⚠️ Integrates with Azure and third-party services

---

### Quick Memory Trick

**Trigger → Action → Result**

8:00 AM  
↓  
Trigger fires  
↓  
Start VM action  
↓  
Server available

6:00 PM  
↓  
Trigger fires  
↓  
Stop VM action  
↓  
Save money

For AZ-900, remember:

**Azure Logic Apps is Microsoft's workflow automation service that connects applications and automates business processes with minimal coding.**


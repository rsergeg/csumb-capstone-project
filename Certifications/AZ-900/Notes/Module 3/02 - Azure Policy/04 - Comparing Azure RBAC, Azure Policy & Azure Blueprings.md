
# Comparing Azure RBAC, Azure Policy, and Azure Blueprints (Student Notes)

## Why Do We Need All Three?

Azure governance is built on three major services:

1. **Azure RBAC** → Controls who can do something.
2. **Azure Policy** → Controls what is allowed.
3. **Azure Blueprints** → Controls how environments are deployed.

Think of it this way:

- RBAC = Security Guard
- Policy = Rule Book
- Blueprint = Building Plan

Together they provide secure, compliant, and repeatable Azure deployments.

---

# Azure RBAC (Role-Based Access Control)

## What is RBAC?

RBAC controls access to Azure resources.

It determines:

- Who can access resources
- What actions they can perform
- Where those permissions apply

Similar to an Access Control List (ACL).

---

## Key Functions of RBAC

### Assign Roles

Built-in roles include:

### Owner

- Full control
- Can manage resources
- Can manage permissions

### Contributor

- Can create and manage resources
- Cannot grant permissions

### Reader

- Read-only access
- Cannot make changes

### Custom Roles

- Organization-created roles
- More granular permissions

---

## RBAC Principles

### Least Privilege

Users receive only the permissions needed.

Example:

- Help Desk should not have Owner access.

---

### Separation of Duties (SoD)

Critical tasks are divided among multiple people.

Example:

- One person creates resources.
- Another approves changes.

---

### Need-to-Know

Users only access resources necessary for their job.

Example:

- HR staff do not need access to production databases.

---

## RBAC Components

### Roles

Define permissions.

Examples:

- Owner
- Contributor
- Reader

---

### Identities

Roles can be assigned to:

#### Users

Individual people.

#### Groups

Collections of users.

#### Service Principals

Applications and services.

Example:

- Web application accessing Azure Storage.

---

### Permissions

Examples:

```
ReadWriteDeleteCreate
```

Permissions define allowed actions.

---

### Scope

Permissions can be assigned at:

- Subscription
- Resource Group
- Resource

Example:

```
Subscription └─ Resource Group      └─ Virtual Machine
```

Permissions inherit downward.

---

## RBAC Example

Developer needs VM access.

Assign:

```
Virtual Machine Contributor
```

Result:

- Can manage VMs
- Cannot manage storage accounts
- Cannot manage networking

---

# Azure Policy

## What is Azure Policy?

Azure Policy enforces compliance and governance standards.

It evaluates resources continuously.

Think of it as:

```
RBAC = Who can do itPolicy = Is it allowed?
```

---

## Key Functions

### Define Policies

Policies evaluate:

- Tags
- Locations
- Encryption
- Resource configurations

---

### Built-In Policies

Microsoft provides many ready-made policies.

Examples:

- Require resource tags
- Restrict locations
- Enforce encryption
- Enable monitoring

---

### Custom Policies

Organizations can create their own compliance rules.

Example:

```
All VMs must use approved images.
```

---

## Azure Policy Example

Requirement:

```
All VMs must have disk encryption.
```

Policy checks:

- Existing VMs
- New VMs during deployment

Possible actions:

- Audit
- Deny
- Modify
- Remediate

---

# Azure Blueprints

## What are Azure Blueprints?

Blueprints are reusable deployment packages.

Think:

```
ARM Template = One buildingBlueprint = Entire neighborhood
```

Blueprints package together:

- Resources
- Configurations
- RBAC assignments
- Azure Policies

---

## Components of a Blueprint

### Resources

Examples:

- Virtual Machines
- Storage Accounts
- Virtual Networks

---

### Configurations

Resource settings.

Example:

```
Storage replication typeVM size
```

---

### RBAC Assignments

Who gets access.

Example:

```
Developers = ContributorAdmins = Owner
```

---

### Azure Policies

Compliance requirements.

Example:

```
Require encryptionRequire tagsRestrict locations
```

---

# Azure Blueprint Process

## Step 1: Create Blueprint Definition

Define:

- Resources
- Policies
- RBAC assignments
- ARM templates

These are called artifacts.

---

## Step 2: Version the Blueprint

Blueprints support versioning.

Benefits:

- Track changes
- Roll back if necessary
- Maintain deployment history

---

## Step 3: Stamp Out Environments

Deploy blueprint repeatedly.

Example:

```
DevelopmentTestingProduction
```

All environments remain consistent.

---

# Blueprint Benefits

## Reusable Templates

Build once.

Deploy many times.

---

## Automated Deployment

Reduces manual work.

Ensures consistency.

---

## Version Control

Track modifications over time.

Similar to source control for infrastructure.

---

# Blueprints and Infrastructure as Code (IaC)

## Why Blueprints Matter

### Consistency

Every deployment follows the same standards.

---

### Repeatability

Same environment can be recreated anytime.

---

### Governance

Policies and RBAC are built into deployments.

---

### Compliance

Standards are enforced automatically.

---

## Blueprint Example

Company needs a standard web application environment.

Blueprint includes:

### Resources

- VM
- Storage Account
- Web App

### RBAC

- Developers = Contributor
- Operations = Reader

### Policies

- Encryption required
- Approved regions only

Result:

- Every deployment follows the same standards.

---

# Comparing the Three Services

|Feature|Azure RBAC|Azure Policy|Azure Blueprints|
|---|---|---|---|
|Primary Function|Access Control|Compliance Enforcement|Standardized Deployment|
|Focus|User Permissions|Resource Properties|Entire Environment|
|Mechanism|Roles|Policy Definitions|Blueprints|
|Controls|Who can do it|What is allowed|How resources are deployed|
|Scope|Subscription, RG, Resource|Subscription, RG, Resource|Subscription, RG|
|Goal|Security Access|Governance & Compliance|Consistency & Automation|

---

# Easy Exam Trick

### Azure RBAC

**Who can do it?**

Example:

```
Can Sergio manage VMs?
```

---

### Azure Policy

**Is it allowed?**

Example:

```
Can this VM be created in West Europe?
```

---

### Azure Blueprints

**How should the environment be built?**

Example:

```
Deploy a standard company web environment.
```

---

# How They Work Together

Example:

### RBAC

Developer receives:

```
Contributor
```

access.

---

### Policy

Organization requires:

```
EncryptionRequired TagsEast US 2 only
```

---

### Blueprint

Deploys:

```
VMStorageRBAC assignmentsPolicies
```

all at once.

---

# Key Takeaways

- Azure RBAC manages access permissions.
- Azure Policy enforces governance and compliance rules.
- Azure Blueprints provide repeatable, standardized deployments.
- RBAC focuses on users.
- Policy focuses on resources.
- Blueprints focus on entire environments.
- All three services work together to create a secure, compliant Azure environment.

---

## Flashcard Quick Review

**What does Azure RBAC control?**  
Who can access and manage resources.

**What does Azure Policy control?**  
Resource compliance and governance.

**What does Azure Blueprint provide?**  
Reusable deployment templates that include resources, policies, and RBAC.

**What principle gives users only the permissions they need?**  
Least Privilege.

**What RBAC role has full control?**  
Owner.

**What Azure service enforces encryption requirements?**  
Azure Policy.

**What Azure service supports versioned infrastructure deployments?**  
Azure Blueprints.

**RBAC = ?**  
Who can do it.

**Policy = ?**  
What is allowed.

**Blueprint = ?**  
How the environment is deployed.


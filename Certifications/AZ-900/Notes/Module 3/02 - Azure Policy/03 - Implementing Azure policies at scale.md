
## Purpose of Azure Policy at Scale

- Azure Policy helps enforce compliance across large Azure environments.
- Policies ensure resources follow organizational standards automatically.
- Can use:
    - Built-in policies
    - Custom policies
    - Initiative definitions (groups of policies)

Goal:

- Consistent governance
- Improved security
- Easier compliance management

---

# Assigning a Built-In Policy

## Example Policy

**Inherit a tag from the resource group if missing**

Purpose:

- Automatically applies a resource group tag to resources that do not already have it.

Example:  
Resource Group Tag:

```
ENV = Production
```

New VM without tag:

```
ENV = Production
```

Policy automatically applies the tag.

---

## Steps to Assign a Policy

### 1. Open Azure Policy

Azure Portal → Search:

```
Policy
```

Select:

```
Policy
```

---

### 2. Open Assignments

Navigate to:

```
Policy └─ Authoring      └─ Assignments
```

Select:

```
Assign Policy
```

---

### 3. Choose Scope

Policy can apply to:

- Management Group
- Subscription
- Resource Group
- Individual Resource

Example:

```
Subscription └─ Policy-RG
```

The scope determines where enforcement occurs.

---

### 4. Select Policy Definition

Search for:

```
Inherit a tag from the resource group if missing
```

Use Built-In policy filter.

Select:

```
Add
```

---

### 5. Configure Assignment

Optional:

- Rename assignment
- Add description

Keep:

```
Policy Enforcement = Enabled
```

Enabled means Azure actively enforces the policy.

---

### 6. Configure Parameters

Example:

Tag Name:

```
ENV
```

Policy will look for and apply the ENV tag.

---

### 7. Configure Non-Compliance Message

Custom message:

```
This resource doesn't have the required tag.
```

Users see this message when violations occur.

---

### 8. Review and Create

Select:

```
Review + Create
```

Then:

```
Create
```

Policy is now active.

---

# Why Use Built-In Policies?

Benefits:

- Ready to use
- Microsoft maintained
- Easy implementation
- Covers common governance requirements

Examples:

- Required tags
- Approved regions
- Encryption requirements
- Diagnostic logging

---

# Custom Policies and Initiatives

## Why Create Custom Policies?

Built-in policies may not cover every business requirement.

Custom policies allow:

- More specific rules
- Organization-specific standards
- Greater control over governance

---

# Initiative Definitions

## What is an Initiative?

An Initiative is a collection of related policies grouped under a common goal.

Think of it like:

```
Folder ├─ Policy 1 ├─ Policy 2 ├─ Policy 3
```

Benefits:

- Easier management
- Single assignment
- Consistent governance

---

## Example Initiative

Initiative Name:

```
Get Secure
```

Purpose:

- Security compliance

Category:

```
SecOps
```

---

# Creating an Initiative

Navigate to:

```
Policy └─ Authoring      └─ Definitions
```

Select:

```
+ Initiative Definition
```

---

## Configure Initiative

Provide:

### Name

```
Get Secure
```

### Description

```
Security-related policies
```

### Category

```
SecOps
```

### Version

```
1.0
```

Versioning helps track changes.

---

# Add Policies to Initiative

Example policies:

### Allowed Locations

Restricts resource deployment regions.

Example:

```
East US 2
```

---

### Endpoint Protection for Machines

Ensures machines have security protection.

---

### Add or Replace Tags

Tag 1:

```
ENV = Test
```

Tag 2:

```
CostCenter = Lab
```

Multiple tagging policies can be included.

---

# Initiative Parameters

Parameters allow customization.

Example:

Allowed Location:

```
East US 2
```

Tags:

```
ENV = TestCostCenter = Lab
```

This makes initiatives reusable.

---

# Assigning an Initiative

After creation:

Navigate to:

```
Definitions
```

Find:

```
Get Secure
```

Select:

```
Assign Initiative
```

---

## Choose Scope

Apply to:

- Subscription
- Resource Group
- Management Group

Example:

```
Subscription
```

---

## Configure Assignment

Typically:

```
Policy Enforcement = Enabled
```

Leave exclusions blank unless necessary.

Review settings.

Select:

```
Create
```

---

# Checking Compliance

Navigate to:

```
Policy └─ Compliance
```

Find:

```
Get Secure
```

---

## Compliance Status

Possible states:

### Not Started

Evaluation still running.

### Compliant

Resources meet policy requirements.

### Non-Compliant

Resources violate one or more policies.

---

## Drill Down

You can view:

- Individual policies
- Resource-level details
- Specific compliance failures

Useful for troubleshooting.

---

# Real-World Example

Organization Requirements:

✔ Resources only in East US 2

✔ Every resource must have:

```
ENVCostCenter
```

✔ Endpoint protection enabled

Create one initiative:

```
Get Secure
```

Assign it once.

Azure automatically enforces all three requirements.

---

# Best Practices

### Start with Built-In Policies

Use Microsoft's built-in policies before creating custom ones.

### Group Related Policies

Use initiatives for easier management.

### Use Meaningful Names

Examples:

```
Get SecureProduction GovernanceResource Tagging Standards
```

### Use Parameters

Makes policies reusable across environments.

### Monitor Compliance Regularly

Check the Compliance dashboard frequently.

### Test Before Production

Validate policies in development environments first.

---

# Key Takeaways

- Azure Policy assignments enforce compliance rules.
- Policies can be assigned at management group, subscription, resource group, or resource level.
- Built-in policies provide quick governance solutions.
- Custom policies support organization-specific requirements.
- Initiatives group multiple policies into a single compliance objective.
- Parameters make policies reusable and flexible.
- Compliance reports help identify violations and track enforcement.
- Azure Policy is a critical governance tool for managing Azure environments at scale.

---

## Flashcard Quick Review

**What does a policy assignment do?**  
Applies a policy to a specific scope.

**What is the purpose of the "Inherit a tag from the resource group if missing" policy?**  
Automatically applies missing tags from the resource group.

**What is an Initiative?**  
A collection of related policies managed as one unit.

**Why use initiatives?**  
Simplify policy management and assignments.

**What are common policy scopes?**  
Management Group, Subscription, Resource Group, Resource.

**What dashboard shows policy compliance?**  
Compliance Dashboard.

**What is the purpose of policy parameters?**  
Allow policies and initiatives to be reused with different values.

**What compliance state indicates Azure has not evaluated the policy yet?**  
Not Started.


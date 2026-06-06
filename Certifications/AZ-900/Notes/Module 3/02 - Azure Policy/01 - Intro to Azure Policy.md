
#### What is Azure Policy?

- Azure Policy helps organizations enforce rules and standards across Azure resources.
- Used for **governance, compliance, and security**.
- Provides a **centralized dashboard** to view compliance status across the environment.
- Helps ensure all departments follow company policies when deploying resources.

---

### How Azure Policy Works

1. Create a **Policy Definition** (the rule).
2. Assign the policy to a **scope**.
3. Azure evaluates resources against the rule.
4. If resources do not comply, Azure can audit, deny, modify, or remediate them.

---

### Policy Definitions

- Written in **JSON format**.
- Contain:
    - Conditions (what to check)
    - Effects (what action to take)

Examples:

- Only allow resource deployment in approved regions.
- Require resource tags (Department, Owner, Cost Center).
- Force diagnostic logs to be sent to Log Analytics.

---

### Policy Scopes

Policies can be assigned at different levels:

- **Management Group**
- **Subscription**
- **Resource Group**
- **Individual Resource**

Policies are inherited by child resources below the assigned scope.

Example:

- Assign a policy at the subscription level.
- Every resource group and resource inside that subscription inherits the policy.

---

### Compliance Dashboard

Azure Policy provides:

- Overall compliance view
- Compliance by policy
- Compliance by resource
- Ability to drill down into violations

Useful for audits and governance reviews.

---

### Remediation

Azure Policy can help fix non-compliant resources.

Examples:

- Add missing tags
- Apply required settings
- Bring resources back into compliance

This reduces manual work for administrators.

---

### Azure Arc Integration

Azure Policy is not limited to Azure resources.

With **Azure Arc**, policies can also be applied to:

- Other cloud providers
- On-premises servers
- Local data centers

This provides a single governance model across hybrid environments.

---

### Azure Policy vs Azure RBAC

|Azure Policy|Azure RBAC|
|---|---|
|Controls resource compliance|Controls user permissions|
|Focuses on resource state|Focuses on user actions|
|Enforces business rules|Grants or restricts access|
|Doesn't care who made the change|Determines who can make changes|

**Easy way to remember:**

- **RBAC = Who can do it**
- **Policy = What is allowed**

---

### Policy Parameters

Parameters make policies reusable.

Instead of creating multiple policies:

- Create one generic policy.
- Supply different values during assignment.

Example:

- Allowed Region Policy
    - Production = East US
    - Testing = West US

Same policy, different parameters.

---

### Initiative Definitions

An **Initiative** is a collection of related policies.

Benefits:

- Easier management
- Single assignment
- Consistent governance goals

Example:  
Security Initiative:

- Require encryption
- Require diagnostic logging
- Require approved regions

All assigned together as one initiative.

---

### Policy Assignments

Assignments determine where a policy is enforced.

Can be assigned to:

- Management Groups
- Subscriptions
- Resource Groups
- Resources

The assignment connects the policy to the target environment.

---

### Components of a Policy Definition

#### Display Name

- Human-readable policy name.

#### Description

- Explains the policy purpose.

#### Policy Type

- Built-in policies provided by Microsoft.
- Custom policies created by organizations.

#### Mode

- Determines which resource types are evaluated.

#### Metadata

- Optional information for organization and management.

#### Parameters

- Allow customization and reuse.

#### Conditions

- Rules that determine compliance.

#### Effect

Action taken when conditions are met.

Common effects:

- **Audit** → Record violation.
- **Deny** → Block deployment.
- **Modify** → Change configuration.
- **DeployIfNotExists** → Automatically deploy required resources.
- **AuditIfNotExists** → Report missing requirements.

---

### Policy Functions

Used to create advanced policy logic.

Functions can:

- Retrieve resource properties
- Compare values
- Manipulate data
- Perform conditional checks

Allows more sophisticated governance rules.

---

### Key Takeaways

- Azure Policy enforces organizational standards and compliance.
- Policies are written as JSON definitions and assigned to scopes.
- Policies can audit, deny, modify, or remediate resources.
- Azure Arc extends policy enforcement beyond Azure.
- RBAC controls **who can act**; Policy controls **what is compliant**.
- Parameters make policies reusable.
- Initiatives group multiple policies together.
- Policy assignments determine where rules are enforced.
- Azure Policy is a core governance tool for maintaining secure, compliant Azure environments.

---

### Flashcard Quick Review

**What does Azure Policy do?**  
Enforces compliance, governance, and organizational standards.

**What format are policy definitions written in?**  
JSON.

**What are the four common scopes for policy assignments?**  
Management Group, Subscription, Resource Group, Resource.

**What is the difference between Azure Policy and RBAC?**  
Policy controls compliance; RBAC controls permissions.

**What is an Initiative?**  
A collection of related policies managed as a single unit.

**What feature allows governance outside Azure?**  
Azure Arc.

**What does the Deny effect do?**  
Blocks non-compliant deployments.

**What do policy parameters provide?**  
Reusable and customizable policy definitions.


## Why It Matters

- Cloud costs can grow quickly
- Easy to accidentally overspend
- Need a way to estimate costs before deploying resources

Azure provides a free tool called the:

### Azure Pricing Calculator

Purpose:

- Estimate Azure costs before deployment
- Compare different configurations
- Help with budgeting and planning

Think:

- Shopping cart for Azure services

---

# What is the Azure Pricing Calculator?

- Free Microsoft tool
- Provides cost estimates for Azure services
- Uses real-time Azure pricing
- Allows custom configurations

Benefits:

- Predict cloud expenses
- Compare options
- Avoid budget surprises

---

# Key Features

## Comprehensive Product Catalog

- Includes nearly all Azure services
- Provides descriptions for each service
- Links to detailed product information

Examples:

- Virtual Machines
- Storage
- Databases
- Networking

---

## Customization

You can customize:

- Region
- VM size
- Storage amount
- Performance tier
- Billing option

Benefits:

- More accurate estimates
- Matches real-world deployments

---

## Cost Breakdown

Calculator shows:

- Individual service costs
- Monthly estimates
- Resource-specific pricing

Benefits:

- Easy to identify expensive services
- Better budgeting

---

## Flexible Editing

Can:

- Change settings
- Remove services
- Add services
- Adjust quantities

Benefits:

- Quickly compare scenarios

---

## Export and Share

Options include:

- Save estimates
- Export to Excel
- Share estimates
- Reopen estimates later

Useful for:

- Project proposals
- Budget meetings
- Client planning

---

# Azure Pricing Components

## Virtual Machines

VM pricing depends on:

- VM size
- Region
- Operating system
- Performance level

---

### VM Categories

#### General Purpose

Balanced resources

Good for:

- Web servers
- Development
- Small databases

---

#### Memory Optimized

More RAM

Good for:

- Large databases
- Memory-intensive applications

---

#### Compute Optimized

More CPU power

Good for:

- Processing workloads
- Analytics
- High-performance applications

---

# VM Billing Models

## Pay-As-You-Go

- Pay only for what you use
- No long-term commitment

Benefits:

- Flexible
- Easy to start

Downside:

- Higher cost over time

Exam Note:

- Most common billing model

---

## Reserved Instances

- Commit to long-term usage
- Receive discounted pricing

Benefits:

- Lower costs

Downside:

- Less flexibility

Exam Note:

- Reserved = cheaper if usage is predictable

---

# Storage Pricing

Azure storage costs vary based on:

## Storage Type

Examples:

- Blob Storage
- Azure Files
- NetApp Files
- Table Storage

---

## Redundancy

More copies of data = higher cost

Examples:

- LRS
- ZRS
- GRS

Remember:

- More protection = more expensive

---

## Access Frequency

Storage tiers:

### Hot

- Frequently accessed data

Higher storage cost  
Lower access cost

---

### Cool

- Less frequently accessed

Lower storage cost  
Higher access cost

---

### Archive

- Rarely accessed data

Lowest storage cost  
Highest retrieval time

Exam Note:

- Hot = Fast access
- Archive = Cheapest storage

---

# How to Use the Pricing Calculator

## Step 1

Open the calculator

---

## Step 2

Select products

Examples:

- Virtual Machine
- SQL Database
- Blob Storage

---

## Step 3

Configure resources

Choose:

- Region
- Size
- Tier
- Quantity

---

## Step 4

Review estimate

View:

- Monthly costs
- Hourly costs
- Service breakdown

---

## Step 5

Optimize costs

Questions to ask:

- Is the VM too large?
- Can storage be reduced?
- Can reserved pricing save money?

---

## Step 6

Save or Export

Options:

- Excel export
- Save estimate
- Share estimate

---

# Cost Optimization Tips

### Use the Right VM Size

Avoid:

- Oversized VMs

Choose:

- Resources that match workload needs

---

### Use Reserved Instances

Best for:

- Long-term workloads
- Predictable usage

Can significantly reduce costs

---

### Review Storage Tiers

Hot storage is not always necessary.

Older files may fit:

- Cool tier
- Archive tier

---

### Remove Unused Resources

Common cost mistakes:

- Unused VMs
- Forgotten storage accounts
- Old databases

---

# Why AZ-900 Cares About This

Microsoft wants administrators to:

- Estimate costs before deployment
- Understand pricing factors
- Optimize cloud spending
- Make informed business decisions

---

# Exam Notes

⚠️ Azure Pricing Calculator = Cost estimation tool

⚠️ Uses real Azure pricing

⚠️ Can estimate monthly costs

⚠️ Pay-As-You-Go = Flexible pricing

⚠️ Reserved Instances = Discounted long-term pricing

⚠️ VM cost depends on:

- Size
- Region
- Usage

⚠️ Storage cost depends on:

- Storage type
- Redundancy
- Access tier

⚠️ Estimates can be exported and shared

---

### Quick Memory Aid

**Calculator = Estimate Before You Deploy**

If a question asks:

_"How can an organization estimate Azure costs before creating resources?"_

Answer:

**Azure Pricing Calculator**.

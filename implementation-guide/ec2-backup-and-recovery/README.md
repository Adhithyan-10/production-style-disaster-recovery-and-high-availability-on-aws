# EC2 AMI Backup & Recovery – Compute Layer Disaster Recovery

## Overview

This implementation demonstrates how Amazon Machine Images (AMIs) can be used to:

- create EC2 server backups
- recover failed EC2 instances
- quickly restore application environments
- improve disaster recovery readiness

The workflow simulates a production-style disaster recovery scenario where an EC2 instance is backed up using an AMI and later restored after instance failure.

---

# AWS Services Used

| Service | Purpose |
|---|---|
| Amazon EC2 | Compute server |
| Amazon AMI | Instance backup image |
| Amazon EBS | Root storage volume |
| AWS Region | Infrastructure hosting |

---

# Architecture Workflow

1. Launch EC2 instance
2. Create AMI backup
3. Verify AMI availability
4. Simulate disaster by terminating instance
5. Launch recovered EC2 instance from AMI
6. Validate successful recovery

---

# Step-by-Step Implementation

---

## Step 1 – EC2 Instance Running

An EC2 instance was launched to host the application server before backup operations.

![EC2 Instance Running](./1-EC2-Instance-Running.png)

---

## Step 2 – Create AMI Backup

An Amazon Machine Image (AMI) backup was created from the running EC2 instance.

![AMI Create Popup](./2-AMI-Create-Popup.png)

---

## Step 3 – Verify AMI Availability

The AMI backup became available and ready for disaster recovery usage.

![AMI Available](./3-AMI-Available.png)

---

## Step 4 – Simulate Disaster Recovery Scenario

The original EC2 instance was terminated to simulate infrastructure failure.

![EC2 Instance Terminated](./4-EC2-Instance-Terminated.png)

---

## Step 5 – Recover EC2 Instance from AMI

A new EC2 instance was launched using the previously created AMI backup.

![Recovered EC2 Instance Running](./5-Recovered-EC2-Instance-Running.png)

---

# Recovery Validation

The disaster recovery process was successfully validated by:

- restoring the EC2 server from AMI
- recovering compute infrastructure rapidly
- validating server availability
- demonstrating production-style recovery workflow

---

# Key Learning Outcomes

- Understanding Amazon AMI backups
- EC2 disaster recovery workflow
- Infrastructure restoration process
- Compute layer backup strategy
- Fast recovery using AMIs
- Production-ready DR concepts

---

# Disaster Recovery Benefits

| Benefit | Description |
|---|---|
| Fast Recovery | Quickly launch replacement servers |
| Infrastructure Backup | Full EC2 server image backup |
| Reduced Downtime | Faster disaster recovery |
| Operational Continuity | Restore workloads rapidly |
| Production Readiness | Real-world DR implementation |

---

# Conclusion

This project demonstrates a real-world EC2 disaster recovery workflow using Amazon Machine Images (AMIs). By creating reusable server images and restoring instances from backups, organizations can minimize downtime and improve infrastructure resilience during failures.

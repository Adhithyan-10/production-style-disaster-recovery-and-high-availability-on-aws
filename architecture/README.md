# Production-Style Disaster Recovery & High Availability Architecture on AWS

## Architecture Overview

This architecture demonstrates a production-style implementation of:

- Disaster Recovery (DR)
- High Availability (HA)
- Backup & Restore Strategy
- Infrastructure Recovery
- Database Resilience

using native AWS services.

The project focuses on protecting three critical infrastructure layers:

- Compute Layer (EC2 + AMI)
- Storage Layer (EBS + Snapshots)
- Database Layer (RDS + Multi-AZ + Snapshots)

---

# Architecture Diagram

![Architecture Diagram](./arc.png)

---

# Core AWS Services Used

| Service | Purpose |
|---|---|
| Amazon EC2 | Application/Server hosting |
| Amazon Machine Image (AMI) | EC2 backup and recovery |
| Amazon EBS | Persistent block storage |
| EBS Snapshots | Point-in-time storage backup |
| Amazon RDS MySQL | Managed relational database |
| RDS Multi-AZ | High availability for database |
| RDS Snapshots | Database backup and recovery |
| AWS VPC | Network isolation |
| Security Groups | Access control and security |

---

# What This Architecture Demonstrates

## 1. Compute Layer Recovery

- Created EC2 instance for application hosting
- Created AMI backup of EC2 instance
- Terminated original EC2 instance
- Successfully launched recovered EC2 instance from AMI

### Key Learning
AMI-based recovery enables rapid infrastructure restoration during failures.

---

## 2. Storage Layer Recovery

- Attached EBS volume to EC2 instance
- Created EBS snapshots
- Demonstrated volume restoration from snapshot

### Key Learning
Snapshots provide point-in-time recovery capability for persistent storage.

---

## 3. Database High Availability & Recovery

- Configured Amazon RDS MySQL
- Enabled Multi-AZ deployment
- Created manual database snapshots
- Restored database from snapshot

### Key Learning
Multi-AZ improves database availability while snapshots provide recovery capability.

---

# Disaster Recovery Workflow

## Step 1 — Failure Occurs
Infrastructure failure, corruption, accidental deletion, or outage occurs.

## Step 2 — Identify Recovery Point
Latest stable AMI, EBS snapshot, or RDS snapshot is selected.

## Step 3 — Restore Infrastructure
- Launch EC2 from AMI
- Restore EBS volume from snapshot
- Restore RDS database from snapshot

## Step 4 — Validate Services
Verify application availability, connectivity, and data integrity.

## Step 5 — Resume Operations
Application environment becomes operational again.

---

# High Availability Features

## RDS Multi-AZ Deployment

- Automatic standby instance
- Improved fault tolerance
- Increased database availability

---

# Backup Strategy

| Resource | Backup Method |
|---|---|
| EC2 | AMI Backup |
| EBS Volume | EBS Snapshot |
| RDS Database | RDS Snapshot |

---

# Recovery Objectives

## RTO (Recovery Time Objective)

The target time required to restore services after failure.

This architecture focuses on low recovery time using:
- AMI-based EC2 recovery
- Snapshot-based restoration

---

## RPO (Recovery Point Objective)

The acceptable amount of data loss during recovery.

This architecture minimizes data loss using:
- Point-in-time snapshots
- Automated database backups
- Multi-AZ database deployment

---

# Security & Networking

- VPC-based network isolation
- Controlled access using Security Groups
- Private database architecture concepts
- Managed AWS infrastructure services

---

# Real-World Use Cases

This architecture pattern is commonly used in:

- Production cloud environments
- Business continuity planning
- Backup and recovery systems
- Mission-critical workloads
- Disaster recovery strategies

---

# Key Outcomes

- Implemented production-style backup strategy
- Demonstrated EC2 disaster recovery using AMIs
- Implemented storage recovery using EBS snapshots
- Configured database high availability using RDS Multi-AZ
- Demonstrated database restoration using snapshots
- Built a scalable and resilient AWS infrastructure foundation

---

# Architecture Summary

This project demonstrates how AWS native services can be combined to build a resilient, highly available, and disaster recovery-ready cloud environment capable of handling infrastructure failures while minimizing downtime and data loss.

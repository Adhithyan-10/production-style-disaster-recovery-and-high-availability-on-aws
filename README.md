# 🚨 AWS Disaster Recovery Architecture using EC2 AMI & RDS Snapshots

<p align="center">
  <img src="https://img.shields.io/badge/AWS-Disaster%20Recovery-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white"/>
  <img src="https://img.shields.io/badge/EC2-AMI%20Backup-orange?style=for-the-badge&logo=amazonec2"/>
  <img src="https://img.shields.io/badge/RDS-Snapshot%20Recovery-blue?style=for-the-badge&logo=amazonrds"/>
  <img src="https://img.shields.io/badge/Cloud-Business%20Continuity-success?style=for-the-badge"/>
</p>

<p align="center">
Production-style Disaster Recovery implementation using EC2 AMIs and RDS Snapshots to recover servers and databases after failures.
</p>

---

## 📖 Project Overview

What happens when your production server suddenly goes down?

What happens if your application database becomes unavailable?

In real-world environments, infrastructure failures are not a matter of **if**, but **when**.

Instances can fail. Databases can become unavailable. Human errors happen. Systems crash.

Without a proper Disaster Recovery strategy:

❌ Applications become unavailable  
❌ Data loss may occur  
❌ Downtime impacts users and business operations  
❌ Recovery becomes difficult and time consuming  

This project demonstrates a practical **AWS Disaster Recovery strategy** by implementing:

✅ EC2 server backup and recovery using **Amazon Machine Images (AMI)**  
✅ Database backup and restoration using **Amazon RDS Snapshots**  
✅ Failure simulation and recovery validation  
✅ Production-style infrastructure thinking for business continuity  

This project focuses not only on creating backups — but on ensuring systems can recover quickly with minimal downtime.

---

# 🎯 Problem Statement

Many applications rely on a single server and database.

Possible failure scenarios:

❌ EC2 instance accidentally terminated  
❌ Server corruption  
❌ Database outage  
❌ Human mistakes  
❌ Infrastructure failure  
❌ Data loss situations  

Without Disaster Recovery planning, restoring services becomes difficult.

This project demonstrates how cloud backup and recovery strategies help maintain availability and business continuity.

---

# 🏗️ Architecture Diagram

<p align="center">
<img src="./images/arc.png" width="900">
</p>

### Architecture Flow

```text
Users
   ↓
Application Server (EC2)
   ↓
Database (RDS)

Backup Strategy:

EC2 → Create AMI → Launch Recovery Instance

RDS → Create Snapshot → Restore Database
```

---

# ⚡ AWS Services Used

| Service | Purpose |
|---|---|
| Amazon EC2 | Application server |
| Amazon AMI | Server backup |
| Amazon RDS | Managed database |
| RDS Snapshots | Database recovery |
| VPC | Network isolation |
| Security Groups | Access management |

---

# 🔄 Disaster Recovery Workflow

## EC2 Recovery Process

### Step 1:
Created production EC2 instance

### Step 2:
Configured application server

### Step 3:
Created AMI backup

### Step 4:
Simulated server failure by terminating instance

### Step 5:
Recovered infrastructure using saved AMI

Result:

✅ EC2 server restored successfully

---

## RDS Recovery Process

### Step 1:
Created MySQL RDS database

### Step 2:
Configured networking and access settings

### Step 3:
Created manual database snapshot

### Step 4:
Simulated failure scenario

### Step 5:
Restored database using snapshot

Result:

✅ Database restored successfully

---

# 📸 Project Screenshots

## EC2 Instance Running

<img src="./images/ec2-running.png">

---

## Creating EC2 AMI Backup

<img src="./images/create-ami.png">

---

## AMI Successfully Created

<img src="./images/ami-created.png">

---

## Simulating EC2 Failure

<img src="./images/ec2-terminated.png">

---

## Recovered EC2 Instance

<img src="./images/ec2-recovered.png">

---

## Creating RDS Database

<img src="./images/rds-create.png">

---

## RDS Instance Running

<img src="./images/rds-running.png">

---

## Creating RDS Snapshot

<img src="./images/rds-snapshot.png">

---

## Restoring Database from Snapshot

<img src="./images/rds-restore.png">

---

# 📊 Key Learnings

Through this project I learned:

- Disaster Recovery planning in AWS
- Difference between backup and recovery
- EC2 restoration using AMIs
- RDS snapshot recovery process
- Infrastructure resilience strategies
- Recovery validation process
- Business continuity concepts

---

# ⚠️ Common Mistakes

❌ Creating backups but never testing restoration

❌ Ignoring database recovery plans

❌ Depending on a single server

❌ Missing security configurations during recovery

❌ Assuming backups alone guarantee availability

---

# 🚀 Future Improvements

- Cross-region disaster recovery
- Multi-AZ deployments
- Automated backup scheduling
- CloudWatch monitoring
- Route53 failover routing
- Infrastructure as Code using Terraform

---

# 📄 Documentation

Detailed implementation guide with screenshots and architecture explanation:

📘 **[View Documentation](./documentation/AWS_Disaster_Recovery.pdf)**

---

# 👨‍💻 About Me

I'm **Adhithyan Sivaraman T**, a Computer Science and Engineering student passionate about Cloud Computing, DevOps, and project-based learning.

Instead of only learning concepts theoretically, I focus on building real-world projects, documenting them, and consistently sharing my learning journey through GitHub and LinkedIn.

I strongly believe the best way to learn cloud is by building systems and understanding how real infrastructure works.

Currently building:

☁️ AWS Projects  
⚙️ DevOps Projects  
🚀 Production-style Architectures  
📘 Learning in Public

---

## 🌐 Connect With Me

🔗 LinkedIn: www.linkedin.com/in/adhithyan-sivaraman-t-399b5b362

💻 GitHub: https://github.com/Adhithyan-10

---

⭐ If you found this project useful, consider giving it a star.

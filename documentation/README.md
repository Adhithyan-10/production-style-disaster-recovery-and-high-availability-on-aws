# 📘 Project Documentation

This folder contains the complete project documentation for:

# Architecting Disaster Recovery & High Availability on AWS

The documentation provides a production-style walkthrough of implementing Disaster Recovery (DR) and High Availability (HA) strategies using AWS services including EC2, EBS, AMI, RDS Multi-AZ, Snapshots, and DR architecture patterns.

---

## 📄 Documentation Contents

The PDF includes:

✅ Real-world disaster scenarios and business impact

✅ Architecture overview (Compute, Storage, Database layers)

✅ Core concepts:
- Recovery Time Objective (RTO)
- Recovery Point Objective (RPO)
- High Availability
- Fault Tolerance

✅ Disaster Recovery strategies:
- Backup & Restore
- Pilot Light
- Warm Standby
- Active–Active

✅ Hands-on implementation:

### Project 1
EBS Backup & Restore

- Create EBS volume
- Attach and mount
- Create snapshots
- Restore and verify recovery

### Project 2
EC2 + RDS Disaster Recovery

EC2:
- Create AMI
- Simulate failure
- Recover instance

RDS:
- Multi-AZ deployment
- Snapshot creation
- Recovery workflow

---

## 🎯 Production Best Practices Covered

- Application Load Balancer across multiple AZs
- Auto Scaling Groups
- Route53 DNS failover
- Cross-region recovery concepts
- Backup automation
- Encryption and security considerations
- CloudWatch and CloudTrail monitoring

---

## 📊 Recovery Goals

| Metric | Value |
|----------|---------|
| RTO | Minutes |
| RPO | Minimal Data Loss |
| SLA Goal | 99.9% |

---

## 📚 View Full Documentation

👉 **Click here:** [Project Documentation PDF](./Disaster_Doc.pdf)

---

## 🧠 Interview Focus

This documentation also includes:

- Common mistakes
- Real-world doubts
- Production considerations
- Interview questions and answers
- Key learning outcomes

---

Production-grade • Portfolio-ready • Interview-focused 🚀

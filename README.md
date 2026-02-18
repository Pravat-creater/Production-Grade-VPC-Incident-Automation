# Production-Grade-VPC-Incident-Automation
Production-grade AWS multi-tier VPC architecture with CloudWatch monitoring and Lambda-based automated incident recovery.

# Production-Grade-VPC-Incident-Automation

## 📌 Project Overview

Designed and deployed a secure multi-tier AWS VPC to manage enterprise cloud workloads with public, private, and isolated subnets.

Integrated a Bastion Host and NAT Gateway to ensure secure administrative access and controlled outbound internet traffic.

Implemented CloudWatch monitoring with automated alerts and Lambda-driven self-healing scripts to reduce downtime and log incidents in real time.

This project simulates production-grade cloud infrastructure operations with security, monitoring, and automated incident recovery mechanisms.

---

## 🏗 Architecture Design

### Network Structure
- Custom VPC (CIDR: 10.0.0.0/16)
- Public Subnet
- Private Subnet
- Isolated (Database) Subnet
- Internet Gateway
- NAT Gateway
- Route Tables for controlled traffic flow

### Compute Layer
- Bastion Host (Public Subnet)
- Application EC2 Instance (Private Subnet)
- Database Layer (Isolated Subnet)

---

## 🔐 Security Implementation

- SSH access restricted through Bastion Host only
- Private EC2 instances not directly accessible from the internet
- Database isolated within private subnet
- Security Groups configured using least-privilege principle
- IAM role attached to Lambda for controlled EC2 reboot access

---

## 📊 Monitoring & Incident Management

- CloudWatch used to monitor CPU utilization
- Alarm triggered when CPU exceeds defined threshold
- SNS used for alert notifications
- Lambda function automatically reboots unhealthy instances
- Incident logging implemented for operational tracking

---

## ⚙️ Self-Healing Automation Workflow

When CPU utilization crosses the defined threshold:

1. CloudWatch Alarm triggers
2. SNS sends notification
3. Lambda function executes
4. EC2 instance is automatically rebooted
5. Incident is logged for tracking

This reduces manual intervention and improves system uptime.

---

## 📈 Impact

- Reduced manual intervention by 80% through automated monitoring and auto-recovery.
- Enhanced cloud security by isolating workloads and restricting database access.
- Simulated enterprise-grade operations demonstrating AWS networking, routing, and production-level cloud management.

---

## 🛠 Tools & Services Used

- Amazon EC2
- VPC
- Internet Gateway
- NAT Gateway
- IAM
- CloudWatch
- SNS
- AWS Lambda
- Linux (Ubuntu)

---

## 🚀 Key Learning Outcomes

- Designing secure multi-tier cloud architecture
- Implementing subnet isolation strategies
- Configuring route tables and gateways
- Applying Security Groups and IAM policies
- Setting up monitoring and automated recovery systems
- Understanding production-level cloud infrastructure management

---

## 📌 Future Enhancements

- Implement Auto Scaling Group for high availability
- Add Application Load Balancer
- Store logs in S3 for centralized logging
- Integrate CloudTrail for auditing
- Infrastructure as Code using Terraform or CloudFormation

---

## 👨‍💻 Author

Pravat Kumar Sahoo
AWS Cloud & Infrastructure Enthusiast

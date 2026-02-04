# aws-3tier-webapp
Secure and Highly Available 3-tier Web Application Architecture on AWS
# Secure & Highly Available 3-Tier Web Application on AWS

## Project Overview
This project demonstrates how to design and deploy a secure, highly available, and scalable 3-tier web application architecture using AWS services.

The architecture follows AWS best practices by isolating resources into public and private subnets and using managed services for scalability and monitoring.


Designed and deployed a secure 3-tier web application architecture on AWS using VPC, EC2, Auto Scaling, Application Load Balancer, and RDS.
The application is highly available, scalable, and follows AWS security best practices using private subnets, IAM roles, and security groups.
CloudWatch is used for monitoring and Auto Scaling ensures availability during traffic spikes.”
---

## Architecture Overview
User traffic is routed through an Application Load Balancer placed in public subnets.  
The load balancer forwards requests to EC2 instances running in private subnets managed by an Auto Scaling Group.  
The application connects securely to an RDS MySQL database hosted in private subnets.

---

## AWS Services Used

| Service | Purpose |
|------|--------|
| VPC | Network isolation |
| EC2 | Application servers |
| Auto Scaling | Automatic scaling |
| Application Load Balancer | Traffic distribution |
| RDS (MySQL) | Database |
| CloudWatch | Monitoring |
| IAM | Secure access |
| NAT Gateway | Private subnet internet access |
| Security Groups | Traffic control |

---

## Security Implementation
- EC2 instances are deployed in private subnets
- ALB is placed in public subnets
- Database is not publicly accessible
- IAM roles used instead of access keys
- Least privilege access followed

---

## Auto Scaling Configuration
- Minimum instances: 1  
- Desired instances: 2  
- Maximum instances: 3  
- Scaling metric: Average CPU utilization  

---

## Monitoring & Alerts
- CloudWatch monitors EC2 CPU usage
- Alarms trigger scaling actions
- System health is continuously monitored

---

## Outcome
This project provides hands-on experience with real-world AWS infrastructure design, networking, security, and scalability.

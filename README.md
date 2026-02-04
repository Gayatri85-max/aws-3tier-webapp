# aws-3tier-webapp
Secure and Highly Available 3-tier Web Application Architecture on AWS


# Secure & Highly Available 3-Tier Web Application on AWS

## Project Overview
This project demonstrates the design and deployment of a secure, highly available, and scalable 3-tier web application architecture using AWS services.

The architecture follows AWS best practices by isolating resources into public and private subnets and using managed services for scalability, security, and monitoring.

---

## Architecture and Implementation

### Architecture Overview
User traffic is routed through an Application Load Balancer (ALB) placed in public subnets.  
The ALB forwards incoming requests to EC2 instances running in private subnets, which are managed by an Auto Scaling Group to ensure high availability and scalability.  
The application layer securely connects to an Amazon RDS MySQL database deployed in private subnets, ensuring that the database is not exposed to the public internet.

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
| IAM | Secure access management |
| NAT Gateway | Internet access for private subnets |
| Security Groups | Traffic control and firewall rules |

---

## Security Implementation
- EC2 instances are deployed in private subnets
- Application Load Balancer is placed in public subnets
- RDS database is not publicly accessible
- IAM roles are used instead of long-term access keys
- Security groups enforce least-privilege access between tiers

---

## Auto Scaling Configuration
- Minimum instances: 1  
- Desired instances: 2  
- Maximum instances: 3  
- Scaling metric: Average CPU utilization  

---

## Monitoring & Alerts
- Amazon CloudWatch monitors EC2 CPU utilization
- CloudWatch alarms trigger Auto Scaling actions during traffic spikes
- Application and system health are continuously monitored

---

## Outcome
This project provides hands-on experience with real-world AWS infrastructure design, including networking, security, monitoring, and high availability.  
It demonstrates the implementation of a production-style 3-tier architecture following AWS best practices.

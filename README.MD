# AWS EC2 Web Servers with Load Balancer and Auto Scaling

## Project Overview
This project demonstrates a highly available web application deployed on AWS using EC2, Application Load Balancer (ALB), Launch Templates, AMI, and Auto Scaling Group (ASG).

The goal was to create a scalable, fault-tolerant web architecture that distributes traffic across multiple instances automatically.

---

## Architecture



Users
       |
       v
  Application Load Balancer
       |
       v
  Target Group
       |
---------------------
|                   |

EC2 Instance 1       EC2 Instance 2 (Managed by Auto Scaling Group)



---

## AWS Services Used
- EC2 Instances (Web Servers)
- Application Load Balancer
- Auto Scaling Group
- Launch Template
- Custom AMI
- Security Groups
- Target Groups and Health Checks

---

## Implementation Steps
1. Launched a working EC2 instance with Apache installed.
2. Created a custom AMI from the working instance.
3. Created a Launch Template using the custom AMI and proper Security Group.
4. Configured an Auto Scaling Group with minimum/desired capacity = 2.
5. Created an Application Load Balancer and connected it to a Target Group.
6. Verified traffic routing through the Load Balancer.
7. Ensured high availability and health checks were passing.

---

## Outcome
- Web traffic is automatically distributed across two EC2 instances.
- Auto Scaling ensures the number of running instances matches the desired capacity.
- System is fault-tolerant and ready for scaling.

---

## Notes
- All sensitive information (AWS keys, passwords) are excluded.
- Security Group allows HTTP (80), HTTPS (443), and SSH (22) for management.



# Introduction to Amazon EC2 – Hands-On Lab

## Overview
This lab provided a hands-on introduction to **Amazon Elastic Compute Cloud (EC2)**, covering how to launch, resize, secure, monitor, and terminate an instance.  

Amazon EC2 provides scalable compute capacity in the cloud, enabling faster deployment and cost-efficient scaling of applications.

## Lab Objectives
By the end of this lab, I successfully:
- Launched an EC2 instance with **termination protection** enabled.
- Installed and served a web page via **Apache HTTP Server** using User Data.
- Configured and modified **security groups** to allow HTTP traffic.
- Monitored the instance using **CloudWatch** metrics and status checks.
- Resized the instance type (**t3.micro → t3.small**) and expanded EBS volume (8 GiB → 10 GiB).
- Tested **termination protection** before safely terminating the instance.

## Architecture Diagram
![EC2 Lab Architecture](diagram.png)  
*EC2 instance running Apache Web Server, secured by Security Group, monitored with CloudWatch, attached to EBS storage.*

## Duration
⏱️ ~45 minutes

## Skills Practiced
- AWS Management Console
- Amazon EC2 provisioning
- Security groups & firewall rules
- CloudWatch monitoring
- EBS storage management
- Termination protection best practices

## Next Steps
- Automate EC2 provisioning with **Terraform/CloudFormation**.
- Explore **IAM roles** and EC2 instance profiles for security.
- Configure **detailed CloudWatch monitoring**.

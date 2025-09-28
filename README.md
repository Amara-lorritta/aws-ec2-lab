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


## Steps I Completed

•	I launched an Amazon Linux EC2 instance (t3.micro) and chose Proceed without a key pair (no SSH key created).

•	In Advanced Details → User Data, I provided a bash script to install and start Apache and create a simple HTML page.

•	I enabled Termination Protection for the instance.

•	I verified instance Status Checks (2/2) and basic CloudWatch metrics.

•	I attempted to access the public IP and discovered the Security Group had no inbound rules, preventing web access.

•	I updated the Security Group inbound rules to allow HTTP (port 80) from Anywhere (0.0.0.0/0).

•	I accessed the web page at the instance’s public IPv4 address and confirmed the message:
“Hello From Your Web Server!”

•	I stopped the instance, changed the instance type from t3.micro → t3.small, and modified the EBS volume size from 8 GiB → 10 GiB, then started the instance again.

•	I tested termination protection by attempting to terminate the instance (it failed while protection was enabled), then disabled termination protection and terminated the instance successfully


## Architecture Diagram

![EC2 Lab Architecture]
(<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/5447b70f-2dd0-4083-85b2-627842769089" />


![EC2 Instance Running](screenshot<img width="1905" height="853" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/aee7eb4b-563f-4f35-9511-b55031eb1ad0" />
s/ec2-dashboard.png)

![Web Server Output](screenshots/webpage.png)<img width="1646" height="696" alt="Screenshot (44)" src="https://github.com/user-attachments/assets/c0a7b7e1-c350-4bb9-ab87-3a25d77083c2" />


*EC2 instance running Apache Web Server, secured by Security Group, monitored with CloudWatch, attached to EBS storage.*


## Skills Practiced
- AWS Management Console
- Amazon EC2 provisioning
- Security groups & firewall rules
- CloudWatch monitoring
- EBS storage management
- Termination protection best practices


#aws, #ec2, #cloud, #cloud-security, #portfolio.

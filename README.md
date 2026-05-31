## AWS Highly Available Web Application

Project Overview

This project demonstrates the deployment of a highly available web application on AWS using EC2, Application Load Balancer (ALB), Auto Scaling Group (ASG), Target Group, Launch Template, and a custom Amazon Machine Image (AMI).

AWS Services Used

•	Amazon EC2
•	Security Groups
•	Apache Web Server
•	 Amazon Machine Image (AMI)  
•	Target Group
•	 Application Load Balancer (ALB)  
•	Launch Template
•	 Auto Scaling Group (ASG)  
•	CloudWatch

Architecture

User → Application Load Balancer → Target Group → Auto Scaling Group → EC2 Instances

Project Implementation

1. EC2 Instance Creation
•	Launched an Amazon Linux EC2 instance.
•	Configured Security Groups for HTTP, HTTPS and SSH access.
2. Web Server Deployment
•	Installed Apache HTTP Server using EC2 User Data.
•	Deployed a sample website.
3. Custom AMI Creation
•	Created a custom AMI from the configured EC2 instance.
4. Launch Template Creation
•	Created a Launch Template using the custom AMI.
5. Target Group Configuration
•	Created a Target Group and configured health checks.
6. Application Load Balancer
•	Created an internet-facing Application Load Balancer.
•	Added Availability Zones in the Load Balancer.
7. Auto Scaling Group
•	 Attached the Target Group to the Load Balancer.  
•	 Created an Auto Scaling Group across multiple Availability Zones using selected Availability Zones from the Load Balancer.  
•	Configured:
o	Minimum Capacity: 2
o	Desired Capacity: 2
o	Maximum Capacity: 4
8. Auto Scaling Demonstration
•	Verified automatic scaling from 2 EC2 instances to 4 EC2 instances.
•	Confirmed all instances passed health checks successfully.

Project Results
•	Successfully deployed a highly available web application.
•	Load Balancer distributed incoming traffic.
•	Auto Scaling automatically launched additional EC2 instances when traffic increased.
•	Target Group registered all instances and reported healthy status.

Screenshots
The screenshots folder contains:
•	EC2 Instance
•	Security Group
•	User Data Script
•	Website Deployment
•	Custom AMI
•	Launch Template
•	Target Group
•	Application Load Balancer
•	Auto Scaling Group
•	Scale-out Event (2 to 4 Instances)
•	Healthy Targets
•	Website Access through ALB DNS
Author
Anshika Arya

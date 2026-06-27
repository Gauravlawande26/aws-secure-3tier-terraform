# Deploy Scalable VPC Architecture on AWS

## Overview

This project demonstrates the deployment of a scalable and highly available network architecture on AWS using Amazon VPC. The infrastructure is designed following AWS best practices and includes public and private subnets, Auto Scaling, Application Load Balancer, NAT Gateway, Transit Gateway, Bastion Host, CloudWatch monitoring, and Route 53.

The objective of this project was to gain hands-on experience in designing production-style AWS networking infrastructure and deploying a highly available web application.

---

## Architecture

> **Add your own architecture diagram here**
>
> Example:
>
> ```
> images/aws-vpc-architecture.png
> ```

---

## Project Objectives

* Design a secure and scalable AWS network.
* Deploy web servers inside private subnets.
* Provide secure administrative access using a Bastion Host.
* Configure Auto Scaling for high availability.
* Distribute traffic using an Application Load Balancer.
* Enable monitoring using CloudWatch and VPC Flow Logs.
* Configure private communication between VPCs using Transit Gateway.
* Manage DNS using Route 53.

---

## AWS Services Used

* Amazon VPC
* EC2
* Auto Scaling Group
* Launch Template
* Application Load Balancer (ALB)
* NAT Gateway
* Internet Gateway
* Transit Gateway
* Route 53
* CloudWatch
* IAM
* Systems Manager (SSM)
* S3
* Elastic IP

---

## Network Design

### VPC 1

* CIDR: `192.168.0.0/16`
* Public Subnet
* Bastion Host

### VPC 2

* CIDR: `172.32.0.0/16`
* Public Subnets
* Private Subnets
* Application Servers

Both VPCs are connected using a Transit Gateway for secure internal communication.

---

## Deployment Steps

### Step 1

Create two VPCs with different CIDR blocks.

### Step 2

Create public and private subnets across multiple Availability Zones.

### Step 3

Attach Internet Gateways to both VPCs.

### Step 4

Create a NAT Gateway for outbound internet access from private subnets.

### Step 5

Configure route tables for public and private subnets.

### Step 6

Deploy a Bastion Host in the public subnet.

### Step 7

Create an S3 bucket for application configuration.

### Step 8

Create a Launch Template with:

* Amazon Linux AMI
* t3.micro instance
* IAM Role
* User Data Script
* Security Group
* Key Pair

### Step 9

Create an Auto Scaling Group.

* Minimum Instances: 2
* Maximum Instances: 4

### Step 10

Create an Application Load Balancer.

### Step 11

Create a Target Group and register EC2 instances.

### Step 12

Configure Route 53 to point the domain to the ALB.

### Step 13

Enable CloudWatch Logs and VPC Flow Logs.

### Step 14

Validate the deployment by accessing the application through the Load Balancer DNS.

---

## Security Features

* Bastion Host for SSH access
* Private EC2 instances
* Security Groups
* IAM Roles
* Session Manager (SSM)
* Private routing using Transit Gateway

---

## Project Structure

```
Project/
│
├── README.md
├── architecture/
│   └── architecture.png
├── scripts/
├── userdata/
└── screenshots/
```

---

## Learning Outcomes

Through this project I learned:

* AWS VPC networking
* CIDR planning
* Public and Private Subnets
* Route Tables
* Internet Gateway
* NAT Gateway
* Transit Gateway
* Launch Templates
* Auto Scaling Groups
* Application Load Balancer
* Route 53
* CloudWatch Monitoring
* IAM Best Practices

---

## Future Improvements

* Infrastructure as Code using Terraform
* CI/CD with Jenkins
* Kubernetes deployment using EKS
* AWS WAF integration
* HTTPS using ACM

---

## Author

**Gaurav Lawande**

Aspiring DevOps & Cloud Engineer

### Connect With Me

* GitHub: https://github.com/YourGitHubUsername
* LinkedIn: https://linkedin.com/in/YourLinkedIn
* Email: [your-email@example.com](mailto:your-email@example.com)

---

## License

This project is created for educational and portfolio purposes.

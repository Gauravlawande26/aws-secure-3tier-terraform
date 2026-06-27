# 🚀 Deploy Scalable VPC Architecture on AWS

## 📌 Project Overview

This project demonstrates the deployment of a secure, scalable, and highly available network architecture on Amazon Web Services (AWS). The infrastructure is built using AWS best practices, featuring public and private subnets, Auto Scaling Groups, an Application Load Balancer (ALB), NAT Gateway, Transit Gateway, CloudWatch monitoring, and Route 53 for DNS management.

The primary objective of this project is to gain hands-on experience in designing production-ready cloud infrastructure capable of hosting web applications with high availability, security, and fault tolerance.

---

## 🏗️ Architecture

> **Replace this section with your own architecture diagram.**

```text
images/aws-vpc-architecture.png
```

---

## 🎯 Project Objectives

* Design a scalable and secure AWS VPC architecture.
* Deploy highly available EC2 instances across multiple Availability Zones.
* Secure application servers using private subnets.
* Configure internet access using NAT Gateway.
* Implement secure administrative access through a Bastion Host.
* Configure Auto Scaling for automatic capacity management.
* Distribute traffic using an Application Load Balancer (ALB).
* Monitor infrastructure with Amazon CloudWatch.
* Connect multiple VPCs using AWS Transit Gateway.
* Configure DNS routing using Amazon Route 53.

---

# 🛠️ AWS Services Used

| AWS Service               | Purpose                                 |
| ------------------------- | --------------------------------------- |
| Amazon VPC                | Create isolated virtual networks        |
| Amazon EC2                | Host the web application                |
| Auto Scaling Group        | Automatically scale application servers |
| Launch Template           | Standardize EC2 deployments             |
| Application Load Balancer | Distribute incoming traffic             |
| NAT Gateway               | Internet access for private instances   |
| Internet Gateway          | Public internet connectivity            |
| Transit Gateway           | Connect multiple VPCs                   |
| Route 53                  | DNS management                          |
| CloudWatch                | Monitoring and logging                  |
| IAM                       | Identity and access management          |
| AWS Systems Manager (SSM) | Secure EC2 management                   |
| Amazon S3                 | Store application configuration         |

---

# 🌐 Network Architecture

## VPC 1

* CIDR Block: `192.168.0.0/16`
* Public Subnet
* Bastion Host
* Internet Gateway

## VPC 2

* CIDR Block: `172.32.0.0/16`
* Public and Private Subnets
* Auto Scaling Group
* Application Load Balancer
* Web Application Servers

Both VPCs are connected securely using an AWS Transit Gateway.

---

# 📋 Deployment Steps

### Step 1 – Create VPCs

Create two VPCs with separate CIDR blocks.

### Step 2 – Configure Networking

* Create Public Subnets
* Create Private Subnets
* Create Route Tables
* Associate Route Tables
* Attach Internet Gateways

### Step 3 – Configure NAT Gateway

Deploy a NAT Gateway to provide outbound internet connectivity for private instances.

### Step 4 – Configure Transit Gateway

Attach both VPCs to a Transit Gateway to enable private communication.

### Step 5 – Configure Security Groups

Create Security Groups for:

* Bastion Host
* Load Balancer
* Application Servers

Allow only required inbound and outbound traffic.

### Step 6 – Launch Bastion Host

Deploy an EC2 Bastion Host in the public subnet and associate an Elastic IP.

### Step 7 – Create Launch Template

Configure:

* Amazon Linux AMI
* t3.micro Instance Type
* IAM Role
* User Data Script
* Security Group
* Key Pair

### Step 8 – Create Auto Scaling Group

Configure:

* Minimum Capacity: 2
* Desired Capacity: 2
* Maximum Capacity: 4

Deploy instances across multiple Availability Zones.

### Step 9 – Configure Application Load Balancer

Create an ALB and register the Auto Scaling Group using a Target Group.

### Step 10 – Enable Monitoring

Configure:

* Amazon CloudWatch Logs
* VPC Flow Logs
* EC2 Monitoring

### Step 11 – Configure Route 53

Create a DNS record pointing your domain name to the ALB.

---

# ✅ Validation

Verify the deployment by:

* Accessing the application using the ALB DNS name.
* Confirming EC2 instances are healthy.
* Testing Auto Scaling functionality.
* Verifying SSH access through the Bastion Host.
* Checking communication between VPCs.
* Reviewing CloudWatch Logs and VPC Flow Logs.

---

# 🔒 Security Features

* Bastion Host for secure SSH access
* Private EC2 instances
* Security Groups with least-privilege rules
* IAM Roles
* AWS Systems Manager (SSM)
* NAT Gateway
* Transit Gateway
* CloudWatch Monitoring
* VPC Flow Logs

---

# 📁 Project Structure

```text
AWS-Scalable-VPC/
│
├── README.md
├── architecture/
│   └── aws-vpc-architecture.png
├── screenshots/
│   ├── vpc.png
│   ├── subnets.png
│   ├── ec2.png
│   ├── alb.png
│   ├── autoscaling.png
│   └── cloudwatch.png
├── userdata/
└── scripts/
```

---

# 📚 Learning Outcomes

By completing this project, I gained practical experience in:

* AWS VPC Networking
* CIDR Planning
* Public and Private Subnets
* Internet Gateway
* NAT Gateway
* Transit Gateway
* Route Tables
* Security Groups
* IAM
* Amazon EC2
* Launch Templates
* Auto Scaling Groups
* Application Load Balancer
* Amazon Route 53
* Amazon CloudWatch
* AWS Systems Manager (SSM)

---

# 🚀 Future Improvements

* Provision infrastructure using Terraform
* Automate deployments with Jenkins or GitHub Actions
* Containerize the application using Docker
* Deploy workloads on Amazon EKS
* Configure HTTPS using AWS Certificate Manager (ACM)
* Integrate AWS WAF for enhanced security
* Add Prometheus and Grafana for monitoring

---

# 👨‍💻 Author

**Gaurav Lawande**

Aspiring DevOps & Cloud Engineer passionate about building scalable, secure, and highly available cloud infrastructure. I enjoy working with AWS, Docker, Kubernetes, Jenkins, and Linux while continuously improving my DevOps skills through hands-on projects.

## 📬 Connect With Me

* **GitHub:** https://github.com/Gauravlawande26
* **LinkedIn:** https://www.linkedin.com/in/gaurav-lawande-40ab01289/
* **Email:** [gauravlawande26@gmail.com](mailto:gauravlawande26@gmail.com)

---

# ⭐ Support

If you found this project helpful, please consider giving it a **⭐ Star** on GitHub. Your support motivates me to build and share more DevOps and Cloud projects.

Feel free to fork this repository, open issues, or submit pull requests with improvements.

---

# 📄 License

This project is created for educational purposes and to demonstrate practical AWS cloud architecture and DevOps skills. Feel free to explore, learn from, and adapt it for your own learning.

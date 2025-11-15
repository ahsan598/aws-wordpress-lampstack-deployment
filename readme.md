# 🚀 Deploying a Dynamic WordPress Website on AWS Using a LAMP Stack Architecture

This project demonstrates how to deploy a dynamic WordPress website on AWS using a production-grade LAMP stack reference architecture. WordPress is a PHP-based Content Management System (CMS) that stores its data in a MySQL database, making it an ideal fit for LAMP environments.

**What is LAMP Stack?**
The LAMP Stack is a traditional and widely-used web application architecture consisting of **Linux** (operating system), **Apache** (web server), **MySQL** (database), and **PHP** (server-side language).
It provides a stable, secure, and scalable platform for hosting dynamic websites — including WordPress, which is built entirely using PHP and MySQL.


### 🚀 Prerequisites
1. AWS account
2. Basic understanding of EC2 and security groups
3. WordPress files or plan to install fresh
4. Domain name (optional)


### 📌 Architecture Overview
The deployment is based on AWS best practices and includes the following components:

**1. 🌐 Networking**
- **VPC** — Custom virtual network for resource isolation
- **Public & Private Subnets** — Web tier + Database tier separation
- **Internet Gateway (IGW)** — Allows public internet access for ALB & public subnets
- **NAT Gateway** — Enables secure outbound traffic for private EC2 instances
- **Route Tables** — Control traffic routing between subnets and gateways

**2. 🖥 Compute & Application**
- **EC2 Instances** — Running Apache + PHP + WordPress application
- **Auto Scaling Group (ASG)** — Automatically scales EC2 instances
- **Application Load Balancer (ALB)** — Distributes incoming user traffic

**3. 🗄 Storage & Database**
- **Amazon RDS (MySQL)** — Managed MySQL database for WordPress backend
- **Amazon S3** — Used for storing static website assets (media, backups, logs)
- **IAM Roles & Policies** — Grant EC2 access to S3 securely

**4. 🌐 DNS, Security & HTTPS**
- **Route 53** — Domain and DNS management
- **AWS Certificate Manager (ACM)** — SSL/TLS for HTTPS
- **Security Groups** — Firewall rules for EC2, ALB, and RDS

**5. 📊 Monitoring**
- **CloudWatch** — Logs, metrics, and alarms

This architecture ensures high availability, fault tolerance, scalability, and security.


### Architect Diagram
![Architect-Diagram](/imgs/architect-overview.jpg)


### ⚙️ How to Deploy
This repository includes a [deployment file](/wordpress/deploy-wordpress-on-aws.md). Follow the instructions to deploy via console.


### 📚 Key Learnings
This project demonstrates how different AWS services integrate to create a scalable, secure, and production-ready WordPress deployment.

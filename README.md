# 🚀 Cloud Mini Project - Deploying an Enterprise Web on Huawei Cloud (CentOS + LAMP)

## 📌 Overview

This project demonstrates how to deploy a LAMP-based enterprise web application on **Huawei Cloud** using **CentOS** ECS instances. The architecture includes Elastic Load Balancing (ELB), RDS for database services, EIP for public access, and CES for resource monitoring.

---

## 🧰 Technologies Used

- **Huawei Elastic Cloud Server (ECS) – CentOS 7**
- **Relational Database Service (RDS) – MySQL**
- **Elastic IP (EIP)**
- **Elastic Load Balance (ELB)**
- **Cloud Eye (CES)**
- **Linux, Apache, MySQL, PHP (LAMP Stack)**

---

## 🎯 Tasks Completed

1. Logged into Huawei Cloud Developer Lab  
2. Set up **LAMP environment on CentOS ECS**  
3. Connected RDS MySQL database to the web server  
4. Achieved **High Availability** using ELB and multiple ECS instances  
5. Configured **EIP for public access**  
6. Visited and tested the deployed website  
7. Monitored infrastructure using Cloud Eye (CES)

---

## 🔧 Step-by-Step Guide

### ✅ Step 1: Setup LAMP on CentOS ECS

```bash
# Update system
sudo yum update -y

# Install Apache
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd

# Install PHP
sudo yum install php php-mysql -y

# Install MySQL client
sudo yum install mysql -y

# Allow firewall (if needed)
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --reload

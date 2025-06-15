# AWS Infrastructure Setup – EC2 + VPC + IAM + Apache Hosting

This project demonstrates a basic AWS infrastructure deployment using a custom VPC, subnets, EC2 instance, IAM roles, and a web server hosted on Apache.

## 🔧 Technologies Used

- AWS EC2
- AWS VPC, Subnets, Route Tables
- AWS IAM
- Amazon Linux/Ubuntu
- Apache2 Web Server
- AWS CLI (v2)
- Git Bash (for SSH on Windows)

---

## 📁 Project Structure
---

## 🚀 What I Built

### ✅ 1. Custom VPC & Subnet Setup
- Created a VPC with CIDR 10.0.0.0/16
- Added a *Public Subnet* (10.0.1.0/24)
- Attached an *Internet Gateway* to allow outbound internet access
- Created a *Route Table* with 0.0.0.0/0 → IGW

### ✅ 2. EC2 Instance Deployment
- Launched a *t2.micro Ubuntu instance*
- Enabled *auto-assign Public IP*
- Added *security group* to allow:
  - SSH (port 22) from 0.0.0.0/0
  - HTTP (port 80) from 0.0.0.0/0

### ✅ 3. Apache Web Server Hosting
- SSH'd into EC2 via Git Bash
- Installed Apache2 and hosted a basic HTML page:
- <h1>Hello from Chandan's EC2 server</h1>
  ```
- Verified page was public using the EC2
  
IAM Role Integration

- Created IAM Role: EC2-S3-ReadOnly-Role

- Attached AmazonS3ReadOnlyAccess policy

- Assigned role to EC2 instance

- Verified access from EC2 using aws s3 ls (via AWS CLI)

---

🧪 IAM Role Test (from EC2)
aws s3 ls        # No AccessDenied = Success
---

## 🧪 Tools Used
- AWS Console
- Git Bash (SSH)
- Ubuntu EC2 instance
- Apache2 web server
- AWS CLI v2

---

## ✅ Clean-Up
- Terminated EC2 instance
- Verified volumes were deleted
- Checked billing (no extra charges)

---

## 👨‍💻 Author
*Chandan Upadhyay*  
[LinkedIn](https://www.linkedin.com/in/chandan-upadhyay-813077141)

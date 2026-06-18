# 🚀 DevOps Static Website Deployment on AWS

![AWS](https://img.shields.io/badge/AWS-EC2-orange?logo=amazonaws)
![Terraform](https://img.shields.io/badge/Terraform-IaC-purple?logo=terraform)
![Docker](https://img.shields.io/badge/Docker-Containerization-blue?logo=docker)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-CI%2FCD-black?logo=githubactions)
![S3 Backend](https://img.shields.io/badge/S3-Remote_State-green?logo=amazon-s3)
![License](https://img.shields.io/badge/License-MIT-yellow)

---

## 🌟 Project Overview

This project demonstrates a complete **DevOps CI/CD pipeline** for deploying a Dockerized static website on **AWS EC2** using:

- 🐳 Docker
- ⚡ GitHub Actions
- ☁️ AWS EC2
- 🏗️ Terraform
- 📦 Docker Hub
- 🗄️ Amazon S3 Remote Backend

Every code push automatically builds a Docker image, pushes it to Docker Hub, and deploys the latest version to AWS EC2.

---

# 🏛️ Architecture

```text
Developer
    │
    ▼
Git Push
    │
    ▼
GitHub Repository
    │
    ▼
GitHub Actions
    │
    ├── Build Docker Image
    ├── Tag Image with Commit SHA
    └── Push to Docker Hub
    │
    ▼
AWS EC2
    │
    ├── Pull Latest Docker Image
    ├── Stop Old Container
    └── Start New Container
    │
    ▼
Static Website
```

---

# 📸 Live Demo

### Website

🌐 Live demo available on request (EC2 instance started before interview)

---

# ✨ Features

✅ Infrastructure as Code using Terraform

✅ Automated CI/CD Pipeline

✅ Dockerized Application

✅ GitHub Actions Automation

✅ Docker Hub Integration

✅ AWS EC2 Deployment

✅ Automatic Container Restart

✅ Commit SHA Image Versioning

✅ Terraform Remote State in Amazon S3

✅ Infrastructure Import into Terraform

---

# 🛠️ Tech Stack

| Category | Technology |
|-----------|------------|
| Cloud | AWS EC2 |
| IaC | Terraform |
| Containerization | Docker |
| Registry | Docker Hub |
| CI/CD | GitHub Actions |
| State Management | Amazon S3 |
| OS | Ubuntu Linux |
| Version Control | Git & GitHub |

---

# ⚙️ CI/CD Workflow

```text
Code Push
    ↓
GitHub Actions Triggered
    ↓
Docker Image Build
    ↓
Image Tagged with Commit SHA
    ↓
Push to Docker Hub
    ↓
SSH into EC2
    ↓
Pull Latest Image
    ↓
Replace Existing Container
    ↓
Deploy Updated Website
```

---

# 🏗️ Terraform Infrastructure

Managed Resources:

- EC2 Instance
- Security Group
- S3 Backend

Terraform State:

```text
Amazon S3
└── terraform.tfstate
```

Benefits:

- Centralized state storage
- Backup & recovery
- Team collaboration support
- Version history enabled

---

# 📂 Project Structure

```text
devops-static-site/
│
├── .github/
│   └── workflows/
│       └── docker.yml
│
├── terraform-deploy/
│   ├── backend.tf
│   ├── main.tf
│   ├── variables.tf
│   └── outputs.tf
│
├── Dockerfile
├── index.html
├── style.css
└── README.md
```

---

# 🚀 Deployment Commands

### Build Docker Image

```bash
docker build -t devops-static-site .
```

### Run Container

```bash
docker run -d -p 80:80 devops-static-site
```

### Terraform Plan

```bash
terraform plan
```

### Terraform Apply

```bash
terraform apply
```

---

# 📊 Current Infrastructure Status

```bash
terraform plan
```

Output:

```text
No changes. Your infrastructure matches the configuration.
```

---

# 🧠 What I Learned

- Infrastructure as Code (Terraform)
- Docker Containerization
- AWS EC2 Management
- GitHub Actions CI/CD
- Docker Hub Integration
- Terraform State Management
- AWS S3 Backend Configuration
- Infrastructure Importing into Terraform

---

# 🔒 Security Considerations

Current Implementation:

- GitHub Secrets
- AWS CLI Authentication
- SSH Key Authentication

Production Improvement:

- GitHub OIDC
- IAM Roles
- Temporary Credentials

---

# 📈 Future Enhancements

- [ ] GitHub OIDC Authentication
- [ ] IAM Roles
- [ ] CloudWatch Monitoring
- [ ] SNS Notifications
- [ ] HTTPS using Nginx
- [ ] Custom Domain
- [ ] Blue-Green Deployment
- [ ] Multi-Environment Terraform

---

# 🎯 Resume Highlights

This project demonstrates:

- DevOps Practices
- CI/CD Automation
- Infrastructure as Code
- AWS Cloud Deployment
- Docker Containerization
- Terraform Remote State Management

---

## 👨‍💻 Author

### Sahil Pawar

GitHub: https://github.com/Sahil4912

---

⭐ If you found this project useful, give it a star!

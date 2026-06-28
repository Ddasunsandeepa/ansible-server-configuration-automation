<div align="center">

# 🚀 Ansible Server Configuration Automation

![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)
![Infrastructure](https://img.shields.io/badge/Infrastructure-Automation-blue?style=for-the-badge)
![IaC](https://img.shields.io/badge/Infrastructure%20as%20Code-Ansible-red?style=for-the-badge)

---

![GitHub repo size](https://img.shields.io/github/repo-size/Ddasunsandeepa/ansible-server-configuration-automation?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/Ddasunsandeepa/ansible-server-configuration-automation?style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/Ddasunsandeepa/ansible-server-configuration-automation?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/Ddasunsandeepa/ansible-server-configuration-automation?style=for-the-badge)
![GitHub license](https://img.shields.io/github/license/Ddasunsandeepa/ansible-server-configuration-automation?style=for-the-badge)

---

![Ansible](https://img.shields.io/badge/Ansible-Automation-EE0000?style=for-the-badge&logo=ansible&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-EC2-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-22.04-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Installed-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-Bash-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NGINX](https://img.shields.io/badge/Nginx-Web_Server-009639?style=for-the-badge&logo=nginx&logoColor=white)

**Enterprise Infrastructure Automation using Ansible Roles, Playbooks and AWS EC2**

*Automating Linux server provisioning, configuration and service deployment with reusable Infrastructure as Code (IaC).*

</div>

---

<p align="center">
  <img src="screenshots/dashboard.png" width="1000"/>
</p>

---

## 📑 Table of Contents

- [Project Overview](#-project-overview)
- [Features](#-features)
- [Architecture](#-architecture)
- [Project Statistics](#-project-statistics)
- [Technologies](#-technologies-used)
- [Project Structure](#-project-structure)
- [Installation](#-how-to-run)
- [Verification](#-verification)
- [Screenshots](#-screenshots)
- [Roadmap](#-roadmap)
- [Skills Demonstrated](#-skills-demonstrated)
- [Author](#-connect-with-me)

---

## 📖 Project Overview

Managing Linux servers manually becomes time-consuming and error-prone as infrastructure grows.

This project demonstrates how **Ansible** can automate the complete configuration of AWS EC2 instances using reusable playbooks and modular roles.

The automation provisions and configures an Ubuntu server by installing essential software, creating users, deploying a web server, and verifying services automatically.

The entire infrastructure can be configured using a **single Ansible command**.

---

## 🎯 Project Objectives

- Automate Linux server configuration
- Eliminate repetitive manual administration
- Deploy production-ready infrastructure
- Demonstrate Infrastructure as Code (IaC)
- Apply Ansible best practices using Roles
- Improve consistency and scalability

---

## 🏗 Architecture

```
                    Developer

                        │
                        ▼

               Ansible Control Node
                 (Ubuntu EC2)

                        │
                SSH Authentication

                        │
                        ▼

                Inventory (hosts)

                        │

                  site.yml Playbook

                        │

        ┌───────────────┼────────────────┐

        ▼               ▼                ▼

   Common Role      Docker Role     Users Role

                        │

                        ▼

                  Nginx Role

                        │

                        ▼

             Target Ubuntu EC2 Instance

                        │

         Docker + Nginx + DevOps User

                        │

                        ▼

         Automated Infrastructure Ready
```

---

## 🚀 Features

✅ Passwordless SSH Authentication  
✅ Inventory-based Server Management  
✅ Modular Ansible Roles  
✅ Reusable Playbooks  
✅ Docker Installation  
✅ Nginx Deployment  
✅ DevOps User Provisioning  
✅ Ubuntu System Update  
✅ Jinja2 Template Deployment  
✅ Automatic Service Management  
✅ Handler-based Service Restart  
✅ Infrastructure Verification  

---

## 📊 Project Statistics

| Category | Details |
|---|---|
| Platform | AWS EC2 |
| Operating System | Ubuntu 22.04 LTS |
| Automation Tool | Ansible |
| Configuration Language | YAML |
| Template Engine | Jinja2 |
| Services Installed | Docker, Nginx |
| Users Created | DevOps User |
| SSH Authentication | Passwordless |
| Infrastructure Type | Infrastructure as Code (IaC) |

---

## ⭐ Repository Highlights

- Infrastructure as Code (IaC)
- Modular Role-Based Architecture
- Reusable Playbooks
- Passwordless SSH Authentication
- Automated Package Management
- Docker Deployment
- Nginx Configuration
- Jinja2 Template Rendering
- Service Verification
- Production-Oriented Automation

---

## ⚙ Technologies Used

| Technology | Purpose |
|---|---|
| Ansible | Infrastructure Automation |
| AWS EC2 | Cloud Infrastructure |
| Ubuntu 22.04 LTS | Operating System |
| Docker | Container Runtime |
| Nginx | Web Server |
| SSH | Secure Remote Access |
| YAML | Playbook Configuration |
| Jinja2 | Dynamic HTML Templates |

---

## 📂 Project Structure

```
ansible-server-configuration-automation/

├── ansible.cfg
├── inventory/
│   ├── hosts
│   └── group_vars/
│
├── playbooks/
│   ├── docker.yml
│   ├── install-nginx.yml
│   ├── update-system.yml
│   └── users.yml
│
├── roles/
│   ├── common/
│   ├── docker/
│   ├── nginx/
│   └── users/
│
├── templates/
│   └── index.html.j2
│
├── screenshots/
│
├── docs/
│
├── site.yml
│
└── README.md
```

---

## ▶ How to Run

### Clone Repository

```bash
git clone https://github.com/Ddasunsandeepa/ansible-server-configuration-automation.git
cd ansible-server-configuration-automation
```

### Verify Inventory

```bash
ansible all -m ping
```

### Run Complete Automation

```bash
ansible-playbook site.yml
```

### Run Individual Playbooks

**Update Servers**
```bash
ansible-playbook playbooks/update-system.yml
```

**Install Docker**
```bash
ansible-playbook playbooks/docker.yml
```

**Install Nginx**
```bash
ansible-playbook playbooks/install-nginx.yml
```

**Create DevOps User**
```bash
ansible-playbook playbooks/users.yml
```

---

## 🧪 Verification

**Verify Docker**
```bash
docker --version
```

**Verify Nginx**
```bash
systemctl status nginx
```

**Verify User**
```bash
id devops
```

**Open Browser**
```
http://<EC2-Public-IP>
```

---

## 📊 Deployment Results

✔ Infrastructure provisioned successfully  
✔ Ubuntu packages updated  
✔ Docker installed and running  
✔ Nginx installed and enabled  
✔ DevOps user created  
✔ Custom HTML dashboard deployed  
✔ Services verified  
✔ Public web access enabled  

---

## 📸 Screenshots

### Infrastructure Architecture
![Architecture](screenshots/architecture.png)

---

### Successful Playbook Execution
![Playbook](screenshots/playbook.png)

---

### Project Structure
![Structure](screenshots/project-structure.png)

---

### AWS Infrastructure
![AWS](screenshots/aws-console.png)

---

### Nginx Dashboard
![Dashboard](screenshots/dashboard.png)

---

### Service Verification
![Verification](screenshots/verification.png)

---

## 🚀 Roadmap

- [x] Passwordless SSH
- [x] Inventory Management
- [x] Playbook Automation
- [x] Role-Based Architecture
- [x] Docker Installation
- [x] Nginx Deployment
- [x] Jinja2 Templates
- [x] Custom Dashboard

### Upcoming Features

- [ ] Dynamic Inventory
- [ ] Terraform Integration
- [ ] Jenkins CI/CD
- [ ] Kubernetes Deployment
- [ ] Prometheus Monitoring
- [ ] Grafana Dashboard
- [ ] Ansible Vault
- [ ] Multi-Region Deployment

---

## 🎓 Skills Demonstrated

- Linux Administration
- Configuration Management
- Infrastructure Automation
- Cloud Computing
- AWS EC2
- SSH Authentication
- Docker Installation
- Web Server Deployment
- Ansible Playbooks
- Ansible Roles
- Jinja2 Templates
- YAML

---

## 🤝 Connect With Me

👨‍💻 **Dasun Sandeepa**

🎓 BSc (Hons) Software Engineering Undergraduate

💻 Passionate about DevOps, Cloud Computing and Infrastructure Automation

🔗 **GitHub:** https://github.com/Ddasunsandeepa

🔗 **LinkedIn:** https://linkedin.com/in/YOUR-LINKEDIN

---

## ⭐ Support

If you found this project helpful, consider giving it a ⭐ on GitHub.

It motivates me to continue building and sharing more DevOps automation projects. 💙
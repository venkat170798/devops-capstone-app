# 🚀 DevOps Capstone Project

## 📌 Overview

This project demonstrates an end-to-end DevOps pipeline for deploying a Node.js application using modern DevOps tools and practices.

The pipeline automates the complete software delivery lifecycle — from code commit to build, containerization, deployment, monitoring, and maintenance.

---

## 🧱 Architecture

Developer → GitHub → Jenkins → Docker → Docker Hub → AWS EC2 → Monitoring (Prometheus + Grafana)

---

## 🛠️ Tech Stack

* Version Control: Git, GitHub
* CI/CD: Jenkins
* Application: Node.js (Express)
* Containerization: Docker, Docker Hub
* Cloud: AWS EC2 (Ubuntu)
* Monitoring: Prometheus, Grafana, Node Exporter
* Automation: Bash scripting, Cron jobs

---

## 🔁 Workflow

1. Developer pushes code to GitHub
2. Jenkins pipeline is triggered automatically
3. Jenkins:

   * Clones repository
   * Installs dependencies
   * Builds Docker image
   * Deploys container
   * Pushes image to Docker Hub
4. Application is deployed on EC2 (port 80)
5. Prometheus collects system metrics via Node Exporter
6. Grafana visualizes metrics via dashboards
7. Cron jobs automate backup and cleanup

---

## ⚙️ Setup Instructions

### 1. Clone Repository

```bash
git clone https://github.com/<your-username>/devops-capstone-app.git
cd devops-capstone-app
```

---

### 2. Run Application Locally

```bash
npm install
node app.js
```

Access:

```
http://localhost:3000
```

---

### 3. Docker Setup

#### Build Image

```bash
docker build -t devops-app .
```

#### Run Container (Production Style)

```bash
docker run -d -p 80:3000 devops-app
```

Access:

```
http://<EC2-IP>
```

---

## 🔧 Jenkins Pipeline Stages

* Clone Code
* Install Dependencies
* Build Docker Image
* Deploy Container
* Push to Docker Hub

---

## 📊 Monitoring Setup

| Service       | Port |
| ------------- | ---- |
| Application   | 80   |
| Grafana       | 3000 |
| Prometheus    | 9090 |
| Node Exporter | 9100 |

### Grafana Dashboard

* Dashboard ID: **1860**
* Node Exporter Full Dashboard

---

## ⏱️ Automation (Bash + Cron)

### Backup Script

```
/home/ubuntu/backup.sh
```

### Cleanup Script

```
/home/ubuntu/cleanup.sh
```

### Cron Jobs

```bash
0 2 * * * /home/ubuntu/backup.sh
0 3 * * * /home/ubuntu/cleanup.sh
```

---

## 📈 Features

* Automated CI/CD pipeline
* Docker-based deployment
* AWS EC2 hosting
* Real-time monitoring
* Automated backup & cleanup
* Health endpoint (`/health`)

---

## 🧠 Key Learnings

* CI/CD using Jenkins
* Docker lifecycle management
* AWS EC2 deployment
* Monitoring with Prometheus & Grafana
* Automation using Bash & Cron
* Debugging real DevOps issues

---

## 🗣️ Interview Summary

"I built an end-to-end CI/CD pipeline using GitHub, Jenkins, Docker, and AWS EC2. The application is deployed on port 80, with monitoring implemented using Prometheus and Grafana, and automation handled via cron jobs."

---

## 🚀 Future Improvements

* Kubernetes deployment
* Terraform (IaC)
* Grafana alerts
* Multi-environment setup

---

## 👨‍💻 Author

Venkat

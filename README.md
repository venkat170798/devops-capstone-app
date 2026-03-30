# 🚀 DevOps Capstone Project

## 📌 Overview

This project demonstrates an end-to-end DevOps pipeline for deploying a Node.js application using modern DevOps tools and practices.

The pipeline automates the complete software delivery lifecycle — from code commit to build, containerization, deployment, monitoring, and maintenance.

---

## 🧱 Architecture

```
Developer → GitHub → Jenkins → Docker → Docker Hub → AWS EC2 → Monitoring (Prometheus + Grafana)
```

---

## 🛠️ Tech Stack

* **Version Control:** Git, GitHub
* **CI/CD:** Jenkins
* **Application:** Node.js (Express)
* **Containerization:** Docker, Docker Hub
* **Cloud:** AWS EC2 (Ubuntu)
* **Monitoring:** Prometheus, Grafana, Node Exporter
* **Automation:** Bash scripting, Cron jobs

---

## 🔁 Workflow

1. Developer pushes code to GitHub
2. Jenkins pipeline is triggered automatically
3. Jenkins performs:

   * Clones repository
   * Installs dependencies
   * Builds Docker image
   * Runs container for validation
   * Pushes image to Docker Hub
4. EC2 instance pulls the image and runs the container
5. Prometheus collects system metrics via Node Exporter
6. Grafana visualizes metrics through dashboards
7. Cron jobs automate backup and cleanup tasks

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

#### Run Container

```bash
docker run -d -p 3000:3000 devops-app
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

| Tool          | Port |
| ------------- | ---- |
| Node Exporter | 9100 |
| Prometheus    | 9090 |
| Grafana       | 3000 |

### Grafana Dashboard

* Dashboard ID: **1860**
* Name: Node Exporter Full

---

## ⏱️ Automation (Bash + Cron)

### Backup Script

```bash
/home/ubuntu/backup.sh
```

### Cleanup Script

```bash
/home/ubuntu/cleanup.sh
```

### Cron Jobs

```bash
0 2 * * * /home/ubuntu/backup.sh
0 3 * * * /home/ubuntu/cleanup.sh
```

---

## 📈 Features

* ✅ Automated CI/CD pipeline
* ✅ Docker-based container deployment
* ✅ Cloud hosting on AWS EC2
* ✅ Real-time monitoring with Prometheus & Grafana
* ✅ Automated backup and cleanup
* ✅ Health check endpoint (`/health`)

---

## 🧠 Key Learnings

* CI/CD pipeline implementation using Jenkins
* Docker image lifecycle (build → tag → push → deploy)
* AWS EC2 provisioning and configuration
* Monitoring with Prometheus and Grafana
* Automation using Bash scripting and Cron jobs
* Troubleshooting real-world DevOps issues

---

## 🗣️ Interview Summary

"I built an end-to-end CI/CD pipeline using GitHub, Jenkins, Docker, and AWS EC2. The pipeline automates build, containerization, deployment, and monitoring using Prometheus and Grafana, along with automation using cron jobs."

---

## 🚀 Future Improvements

* Kubernetes deployment
* Infrastructure as Code (Terraform)
* Grafana alerting setup
* Multi-environment setup (Dev/Prod)

---

## 👨‍💻 Author

**Venkat**

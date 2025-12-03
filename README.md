# Hey, I'm Akshan Khanna

Cloud and DevOps engineering student building practical projects around microservices, AWS, automation and CI/CD. I enjoy creating small but real deployments that reflect how things work in production.

🔧 Tools and Technologies

Cloud: AWS (ECS, ECR, S3, ALB, EC2)
DevOps: Docker, Git, GitHub Actions, Terraform, Ansible
Backend: Python, Flask
Frontend: React basics
Other: Linux, Shell scripting

🚀 Featured Projects


# TravelEase – Cloud-Native Microservices Platform

TravelEase is a microservices-based travel booking platform built with Flask and deployed on AWS using ECS Fargate, ALB path-based routing and Terraform IaC. The project demonstrates production-style containerization, cloud deployment and CI/CD integrations.

---

## 🚀 Architecture Overview

- Three microservices:
  - Booking Service (Port 5000)
  - Flight Service (Port 5002)
  - Payment Service (Port 5003)
- Containerized with Docker
- Deployed on AWS ECS Fargate
- ALB routes traffic based on URL paths
- Infrastructure created using Terraform
- Logs captured using CloudWatch
- Images stored in ECR

(ASCII architecture diagram you provided goes here)

---

## 🧩 Tech Stack

**Cloud:** AWS ECS, ECR, S3, ALB, EC2, IAM  
**Infrastructure:** Terraform  
**Containers:** Docker  
**Backend:** Python Flask  
**CI/CD:** GitHub Actions / AWS Pipeline (optional)

---

## 🏗 Project Structure


                   ┌──────────────────────────┐
                   │        Users / UI        │
                   │   (React Frontend)       │
                   └────────────┬─────────────┘
                                │
                                ▼
                     ┌──────────────────────┐
                     │  AWS Application     │
                     │    Load Balancer     │
                     └──────────┬───────────┘
                                │ Path-based routing
        ┌───────────────────────┼─────────────────────────┐
        │                       │                         │
        ▼                       ▼                         ▼
┌──────────────┐      ┌────────────────┐         ┌────────────────┐
│ Booking Svc  │      │ Flight Svc     │         │ Payment Svc    │
│ Flask API    │      │ Flask API      │         │ Flask API      │
│ Port 5000    │      │ Port 5002      │         │ Port 5003      │
└───────┬──────┘      └──────┬─────────┘         └──────┬─────────┘
        │                     │                           │
        ▼                     ▼                           ▼
┌───────────────────────────────────────────────────────────────────┐
│                     AWS ECS Fargate Cluster                       │
│        (Each service runs in its own Task Definition + ENI)       │
└───────────────────────────────────────────────────────────────────┘
        │                     │                           │
        ▼                     ▼                           ▼
┌───────────────────────────────────────────────────────────────────┐
│                             ECR Repos                              │
│   (booking-image, flight-image, payment-image pushed via CI/CD)    │
└───────────────────────────────────────────────────────────────────┘

                 ┌──────────────────────────────────────┐
                 │        CloudWatch Logs                │
                 │  (Service logs + ALB access logs)     │
                 └──────────────────────────────────────┘

                 ┌──────────────────────────────────────┐
                 │        Terraform IaC                  │
                 │ VPC, Subnets, ALB, ECS, IAM, ECR     │
                 └──────────────────────────────────────┘
                 
---

## ▶ How to Run Locally

```bash
docker-compose up --build
🌩 Deployment on AWS
terraform init
terraform plan
terraform apply


Terraform handles all cloud provisioning:

--- 
# **End To End DevOps Pipeline for Cloud Native Monitoring and Logging**

This project sets up centralized monitoring and logging for a Node.js application deployed on Minikube using the ELK stack, Fluentd and Prometheus/Grafana.

# **🧩 Tools Used**
Kubernetes (Minikube)
Fluentd
Elasticsearch
Kibana
Prometheus
Grafana
Node.js App
---
# **📊 What This Project Shows**
Metrics collection (Prometheus)
Dashboarding and visualization (Grafana)
Log collection via Fluentd
Log storage in Elasticsearch
Log analysis with Kibana
Kubernetes manifests for deployments
---
# **How to Run**
minikube start
kubectl apply -f k8s/

---
#**📈 Dashboards Included**
Application metrics (CPU, memory, latency)
Log explorer (Kibana)
Custom Grafana panels
---
# **CI/CD Pipeline Demo**
A simple containerized application with a GitHub Actions workflow that automatically builds, tests and verifies the application on every push.

# **⚙ Features**
Docker-based build
Automated testing
On-push GitHub Actions workflow
Easy extension for deployment pipelines
---
# **🚀 Tech Stack**
Docker
GitHub Actions
Node.js / Python (whichever your app uses)
---
## ▶ How to Run
docker build -t demo-app .
docker run -p 3000:3000 demo-app
---
#**💡 **GitHub Actions Workflow****
Triggers on push
Installs dependencies
Runs tests
Builds the container
https://github.com/AkshanKhanna06/End-to-End.git
---
#📌 What I’m focusing on
Improving cloud infrastructure skills
Building end-to-end deployments using Terraform
Creating cleaner documentation and diagrams for my projects
Strengthening CI/CD automation
---
📫 Connect
LinkedIn: https://www.linkedin.com/in/akshan-khanna-a94544247/
Email: akshank610@gmail.com
---
🧩 Fun fact
I break things on purpose just to see how fast I can fix them.

# 🚀 Node.js Todo Application – Jenkins CI/CD on AWS ECS Fargate

A containerized Node.js Todo application deployed on **AWS ECS Fargate** using **Docker** and **Jenkins CI/CD**, with application logs monitored through **Amazon CloudWatch**.

This project demonstrates a practical DevOps workflow covering application containerization, CI/CD automation, AWS ECS deployment, task definitions, networking, and centralized logging.

---

## 📌 Project Overview

The objective of this project is to deploy a Node.js Todo application as a Docker container on AWS ECS using the Fargate launch type.

The application was successfully deployed and accessed through the public endpoint of the running ECS task.

### Key Technologies Used

- **Node.js** – Application runtime
- **Docker** – Application containerization
- **Jenkins** – CI/CD automation
- **AWS ECS** – Container orchestration
- **AWS Fargate** – Serverless container execution
- **Amazon CloudWatch** – Application and container logging
- **Git/GitHub** – Source code management

---

# 🏗️ Architecture

```text
                 ┌─────────────────┐
                 │     Developer   │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │     GitHub      │
                 │ Source Control  │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │     Jenkins     │
                 │    CI / CD      │
                 └────────┬────────┘
                          │
                          ▼
                 ┌─────────────────┐
                 │      Docker     │
                 │    Container    │
                 └────────┬────────┘
                          │
                          ▼
              ┌─────────────────────────┐
              │      AWS ECS Cluster    │
              │                         │
              │    node-app-cluster     │
              │                         │
              │   ┌─────────────────┐   │
              │   │  Fargate Task   │   │
              │   │                 │   │
              │   │ Node.js Todo    │   │
              │   │ Application     │   │
              │   └─────────────────┘   │
              └────────────┬────────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │ Amazon CloudWatch│
                  │      Logs       │
                  └─────────────────┘

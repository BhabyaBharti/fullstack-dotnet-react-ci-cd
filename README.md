# Full-Stack .NET + React Application with Enterprise CI/CD


## 🚀 Overview

This repository demonstrates an **end-to-end CI/CD implementation** for a
**full-stack enterprise-style application** consisting of:

- ⚙️ Backend: .NET (ASP.NET Core)
- 🎨 Frontend: React
- 🗄️ Database: MySQL
- 🔄 CI/CD: GitHub Actions & Azure DevOps
- ☁️ Target Platforms: Azure VM, AWS EC2, Docker containers

> ⚠️ **Important:**  
> The primary focus of this project is **DevOps automation, CI/CD orchestration,
> and cloud readiness**, not application feature development.

---

## 🧩 Business Context

In real-world enterprise environments, applications are rarely single-stack.
Most systems consist of:
- Separate frontend and backend teams
- Shared databases or managed services
- Multiple deployment environments
- Strict CI/CD and release controls

This project simulates such a setup and focuses on **how DevOps pipelines
handle multi-technology applications reliably and repeatably**.

---

## 🏗️ Application Architecture

┌───────────────────┐ ┌────────────────────┐
│ React Frontend │ ---> │ .NET Backend API │
└───────────────────┘ └────────────────────┘
│
▼
┌──────────┐
│ MySQL │
└──────────┘


Each component is built, tested, and packaged independently
while being orchestrated through a **single CI/CD pipeline**.

---

## 📂 Repository Structure

.
├── elearn-backend
│ ├── Controllers
│ ├── Models
│ ├── Data
│ ├── Dockerfile
│ └── Program.cs
│
├── elearn-frontend
│ ├── public
│ ├── src
│ └── package.json
│
├── .github/workflows
│ ├── cicd_workflow.yml
│ └── workflow_net.yml
│
├── azure-pipelines.yml
└── README.md



---

## 🔄 CI/CD Design

### GitHub Actions (CI)

The GitHub Actions workflow performs:

- ✅ Source code checkout
- ✅ Frontend dependency installation, build & tests
- ✅ Backend dependency restore, build & tests
- ✅ MySQL service container for integration testing
- ✅ Manual and automated triggers

#### Key CI Features
- Uses **MySQL as a service container** to mimic real integration tests
- Builds **frontend and backend independently**
- Ensures failures are caught early before deployment

---

### Azure DevOps Pipelines (CD)

The Azure DevOps pipeline is designed for:
- Controlled deployments
- Environment-specific releases
- Artifact-based delivery

This mirrors how many enterprises separate:
- **CI (GitHub)** → **CD (Azure DevOps)**

---

## 🐳 Containerization Strategy

- Backend includes a **Dockerfile**
- Application is container-ready for:
  - Docker-based deployments
  - Future Kubernetes adoption
- Enables cloud-agnostic deployments

---

## ☁️ Deployment Targets

This application is designed to be deployed on:

- 🔵 **Azure Virtual Machines**
- 🟠 **AWS EC2 instances**
- 🐳 **Docker containers**

The CI/CD pipeline ensures that the same build artifacts
can be deployed across multiple platforms with minimal changes.

---

## 🔐 Security & Best Practices

- No hardcoded credentials in pipelines
- Environment variables used for sensitive configuration
- Database access controlled via CI service containers
- Separation of CI and CD responsibilities

---

## 🧠 Design Decisions & Trade-offs

- **Single repo, multi-component** setup for easier pipeline orchestration
- **Service containers** used instead of mocks for realistic testing
- **Pipeline-first approach**, app kept intentionally simple
- Designed for extensibility (Kubernetes, cloud-native services)

---

## 🔮 Future Enhancements

- Kubernetes deployment (AKS / EKS)
- Blue-Green or Canary deployments
- Monitoring & logging integration

---

## 📌 Author

**Bhabya Bharti**  
DevOps Engineer | Cloud | CI/CD | Terraform | Containers

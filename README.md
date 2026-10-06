# Hospital-Cloud-Infrastructure

## Enterprise Hospital Cloud Infrastructure

A lightweight enterprise-style hospital infrastructure project designed to demonstrate **cloud computing, containerization, Kubernetes orchestration, Infrastructure as Code, CI/CD, monitoring, high availability, backup, and disaster recovery**.

> **Project Type:** Educational / Portfolio Project  
> **Cloud Platform:** AWS  
> **Target:** Enterprise-style Hospital Infrastructure Simulation

---

## Project Overview

Hospitals depend on applications that must remain available, scalable, secure, and recoverable because downtime or data loss can affect critical healthcare operations.

This project demonstrates how a hospital application can be deployed and managed using modern cloud and DevOps technologies.

The infrastructure combines:

- Linux
- Docker
- Kubernetes
- PostgreSQL
- AWS
- Terraform
- GitHub Actions
- Prometheus
- Grafana
- Backup and Disaster Recovery

The project is designed as a **lightweight implementation suitable for a student development environment** while demonstrating enterprise-style infrastructure concepts.

---

## Project Objectives

The main objectives of this project are to demonstrate:

- High availability
- Containerized application deployment
- Kubernetes orchestration
- Application scaling
- Cloud infrastructure provisioning
- Infrastructure as Code
- CI/CD automation
- Monitoring and observability
- Database backup and restoration
- Disaster recovery
- Secure configuration management
- Hybrid cloud concepts

---

## Architecture

The project follows a hybrid architecture where local Linux infrastructure is used for development and Kubernetes-based infrastructure testing, while AWS is used to demonstrate cloud infrastructure and disaster recovery concepts.

```text
                    ┌─────────────────────┐
                    │      Developer      │
                    │     Windows 11      │
                    └──────────┬──────────┘
                               │
                               │ Git
                               ▼
                    ┌─────────────────────┐
                    │       GitHub        │
                    │   Source Control    │
                    └──────────┬──────────┘
                               │
                         Git Pull / Push
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Linux System     │
                    │                     │
                    │ Docker + Kubernetes│
                    │ PostgreSQL          │
                    │ Prometheus          │
                    │ Grafana             │
                    └──────────┬──────────┘
                               │
                               │ Cloud / DR
                               ▼
                    ┌─────────────────────┐
                    │        AWS          │
                    │                     │
                    │ VPC                 │
                    │ EC2                 │
                    │ Security Groups     │
                    │ Networking          │
                    └─────────────────────┘
```

---

## Application

The project will contain a simple hospital application consisting of:

### Frontend

A web-based hospital dashboard that provides a user interface for hospital-related information.

### Backend

REST APIs for:

- Patient management
- Doctor management
- Appointment management
- Application health checks

### Database

PostgreSQL will be used for storing application data.

---

## Technology Stack

| Category | Technology |
|---|---|
| Operating System | Linux |
| Frontend | HTML / JavaScript / React |
| Backend | REST API |
| Database | PostgreSQL |
| Containerization | Docker |
| Orchestration | Kubernetes |
| Cloud | AWS |
| Infrastructure as Code | Terraform |
| CI/CD | GitHub Actions |
| Monitoring | Prometheus |
| Visualization | Grafana |
| Version Control | Git / GitHub |

---

## Project Structure

```text
Hospital-Cloud-Infrastructure/
│
├── frontend/
│
├── backend/
│
├── database/
│
├── docker/
│
├── kubernetes/
│
├── terraform/
│
├── monitoring/
│
├── scripts/
│
├── docs/
│
├── .github/
│   └── workflows/
│
└── README.md
```

---

## Docker

Docker will be used to containerize the application components.

The project will contain containers for:

- Frontend
- Backend
- PostgreSQL

Docker networking and persistent volumes will be used to allow the application components to communicate while maintaining database data.

---

## Kubernetes

Kubernetes will be used to orchestrate the application containers.

The Kubernetes implementation will demonstrate:

- Pods
- Deployments
- Services
- ConfigMaps
- Secrets
- Persistent Storage
- Health Checks
- Multiple Replicas
- Application Scaling

---

## High Availability

High availability will be demonstrated using multiple backend replicas.

If a running backend Pod fails or is deleted, Kubernetes will automatically create a replacement Pod.

This demonstrates the self-healing capability of Kubernetes.

The project targets the **concept of 99.9% availability** as an architectural objective and does not claim production uptime.

---

## Scaling

The application will demonstrate horizontal scaling by increasing or decreasing the number of backend replicas.

Example:

```text
Backend Replica 1
Backend Replica 2
Backend Replica 3
```

Kubernetes Services will distribute traffic across available application Pods.

---

## AWS Infrastructure

AWS will be used to demonstrate cloud infrastructure concepts.

The planned AWS infrastructure includes:

- VPC
- Subnets
- Security Groups
- EC2
- IAM
- Networking
- Cloud-based infrastructure
- Disaster Recovery components where required

AWS resources will be kept lightweight to reduce unnecessary costs.

---

## Terraform

Terraform will be used as Infrastructure as Code to automate AWS infrastructure provisioning.

Planned Terraform resources include:

- VPC
- Subnets
- Security Groups
- EC2 infrastructure
- Required networking resources

Infrastructure will be defined using Terraform configuration files instead of manually creating every resource.

---

## CI/CD

GitHub Actions will be used to demonstrate automated application deployment workflows.

The planned pipeline includes:

```text
Git Push
   ↓
GitHub Actions
   ↓
Checkout Code
   ↓
Build
   ↓
Test
   ↓
Build Docker Image
   ↓
Deploy
```

---

## Monitoring

Prometheus and Grafana will be used for monitoring and visualization.

The monitoring system will demonstrate:

- Application availability
- Container status
- CPU usage
- Memory usage
- Kubernetes workload status

Monitoring components will be started when required to keep the development environment lightweight.

---

## Backup and Disaster Recovery

PostgreSQL database backup and restoration will be implemented.

The project will demonstrate:

```text
Database
   ↓
Backup
   ↓
Failure Simulation
   ↓
Database Restore
   ↓
Application Verification
```

Disaster recovery testing will include simulated failures and restoration of application or database components.

---

## Failure Testing

The project will include controlled failure simulations such as:

- Backend container failure
- Kubernetes Pod deletion
- Application instance failure
- Database failure
- Database restoration

The objective is to demonstrate how the infrastructure responds to failures.

---

## Security

Security practices included in the project:

- Linux permissions
- AWS IAM
- AWS Security Groups
- Kubernetes Secrets
- Environment variables
- GitHub repository security
- `.gitignore`
- No credentials committed to Git
- No AWS access keys stored in source code
- No private keys stored in the repository

---

## Development Workflow

Because the development environment uses separate Windows and Linux systems through dual boot, GitHub is used as the synchronization layer.

```text
Windows
   ↓
Git Commit
   ↓
Git Push
   ↓
GitHub
   ↓
Linux
   ↓
Git Pull
```

Changes made on Linux can be synchronized back to Windows using the same process.

---

## Cost Management

The project is designed to minimize cloud costs.

The implementation will prioritize:

- Free/open-source tools
- Local Linux resources
- Lightweight Kubernetes
- Small AWS resources
- AWS free-tier eligible resources where applicable
- Avoiding unnecessary paid AWS services
- Cleaning unused AWS resources after testing

No paid AWS service will be used without checking its potential cost first.

---

## Important Note

This is an **educational and portfolio project**.

It does not use real patient information and does not claim to provide production healthcare compliance or a production hospital system.

All demonstrations use sample or simulated data.

---

## Expected Learning Outcomes

By completing this project, the following practical skills will be demonstrated:

- Linux
- Git and GitHub
- Docker
- Kubernetes
- PostgreSQL
- AWS
- Terraform
- CI/CD
- Infrastructure as Code
- Monitoring
- High Availability
- Scaling
- Backup and Disaster Recovery
- Cloud Infrastructure Design

---

## Final Project Goal

The final goal is to demonstrate how a hospital application can be designed, deployed, monitored, scaled, secured, and recovered using modern cloud and DevOps technologies.

### Target Architecture

```text
Application
     ↓
Docker
     ↓
Kubernetes
     ↓
High Availability
     ↓
Monitoring
     ↓
Terraform
     ↓
AWS
     ↓
Backup & Disaster Recovery
     ↓
CI/CD Automation
```

---

## Project Status

🚧 **Project In Progress**

The infrastructure will be implemented step by step and tested at each stage.

---

## Author

**Hospital-Cloud-Infrastructure**

**Project Focus:** Cloud Engineering / DevOps / Infrastructure

**Cloud Platform:** AWS

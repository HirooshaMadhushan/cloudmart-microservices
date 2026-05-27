# CloudMart Microservices Platform

## Project Overview

CloudMart is a cloud-native microservices e-commerce platform deployed on Amazon EKS using Kubernetes. The system follows DevOps and cloud engineering best practices including containerization, CI/CD automation, autoscaling, monitoring, security policies, and infrastructure orchestration.

---

# Architecture

## Microservices

| Service | Description |
|---|---|
| frontend | User-facing web application |
| product-service | Product catalog management |
| order-service | Order processing |
| user-service | User account management |
| notification-service | Notification handling |

---

# Technologies Used

## Backend
- Node.js
- Express.js

## Frontend
- React.js

## DevOps & Cloud
- Docker
- Kubernetes
- Amazon EKS
- Amazon ECR
- GitHub Actions
- AWS IAM
- AWS ELB
- CloudWatch

---

# Kubernetes Features Implemented

- Deployments
- Services
- LoadBalancer
- Horizontal Pod Autoscaler (HPA)
- ConfigMap
- Secret
- Liveness Probes
- Readiness Probes
- Resource Limits
- Network Policies
- Rolling Updates

---

# CI/CD Pipeline

GitHub Actions pipeline automatically:

1. Builds Docker images
2. Pushes images to Amazon ECR
3. Deploys updated services to Amazon EKS

The pipeline automatically triggers when code is pushed to:
- master
- main
- develop

---

# AWS Services Used

| AWS Service | Usage |
|---|---|
| EKS | Kubernetes cluster |
| ECR | Docker image registry |
| EC2 | Kubernetes worker nodes |
| ELB | Public frontend access |
| IAM | Security and permissions |
| CloudWatch | Monitoring |

---
# Repository Structure

```text
cloude/
├── services/
├── k8s/
├── docs/
├── .github/workflows/
├── README.md
```

# Deployment Steps

## Clone Repository

```bash
git clone https://github.com/HirooshaMadhushan/cloudmart-microservices.git
cd cloude
```
---

# Frontend Access

The frontend application is exposed using AWS Elastic Load Balancer.

Example:

```text
http://a30574e2c8518460da87f72937169740-1183378597.us-east-1.elb.amazonaws.com
```
## Deploy Kubernetes Resources

```bash
kubectl apply -f k8s/cloudmart.yaml
```

## Check Running Pods

```bash
kubectl get pods -n cloudmart-prod
```

## Check Services

```bash
kubectl get svc -n cloudmart-prod
```

---

# Autoscaling

Horizontal Pod Autoscaler (HPA) is configured for:

- product-service
- order-service

The services automatically scale based on CPU usage.

---

# Security Features

- Kubernetes Secrets
- ConfigMaps
- Network Policies
- IAM Authentication
- Resource Isolation

---

# Monitoring

The platform uses:

- Kubernetes Metrics Server
- AWS CloudWatch
- HPA Metrics

---

# Disaster Recovery

The system supports:

- Kubernetes self-healing
- Multiple replicas
- Rolling deployments
- Docker image backup in ECR
- Source code backup in GitHub

---

# Screenshots

Add screenshots for:

- EKS Cluster
- Running Pods
- Kubernetes Services
- HPA
- GitHub Actions
- Amazon ECR repositories
- Frontend application

---

# Author

## Hiroosha Weerasuriya

Undergraduate | Full Stack Developer | DevOps & Cloud Engineering Enthusiast

### Technologies

- Node.js
- React.js
- Docker
- Kubernetes
- AWS
- GitHub Actions

---

# Conclusion

CloudMart demonstrates the implementation of a cloud-native microservices platform using Kubernetes, Docker, AWS, and CI/CD automation. The project applies DevOps engineering principles including scalability, monitoring, security, automation, and container orchestration.
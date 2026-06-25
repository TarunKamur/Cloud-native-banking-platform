# Cloud Native Banking Platform

A cloud-native full-stack banking application built with modern application development and Kubernetes deployment practices.

## Overview

This project demonstrates the design, containerization, and deployment of a banking platform using:

* React Frontend
* Node.js Backend
* MongoDB Database
* Redis Cache
* Ollama AI Service
* Docker & Docker Compose
* Kubernetes
* Helm Charts
* NGINX Ingress

The repository contains both application source code and Infrastructure-as-Code (IaC) assets required to deploy the platform on Kubernetes.

---

## Repository Structure

```text
Cloud-native-banking-platform/
│
├── Paisa-bank-app/
│   ├── frontend/
│   ├── backend/
│   ├── docker-compose.yaml
│   └── README.md
│
├── paisa-bank-k8s/
│   ├── frontend-chart/
│   ├── backend-chart/
│   ├── mongodb-chart/
│   ├── redis-chart/
│   ├── ollama-chart/
│   └── ingress-chart/
│
└── README.md
```

---

## Architecture

```text
                    ┌─────────────────┐
                    │     Users       │
                    └────────┬────────┘
                             │
                             ▼
                   ┌──────────────────┐
                   │ NGINX Ingress    │
                   └────────┬─────────┘
                            │
              ┌─────────────┴─────────────┐
              │                           │
              ▼                           ▼
      ┌──────────────┐           ┌──────────────┐
      │ React Frontend│           │ Node Backend │
      └──────┬───────┘           └──────┬───────┘
             │                          │
             └──────────┬───────────────┘
                        │
        ┌───────────────┼────────────────┐
        │               │                │
        ▼               ▼                ▼
 ┌────────────┐  ┌────────────┐  ┌────────────┐
 │ MongoDB    │  │ Redis      │  │ Ollama     │
 │ Database   │  │ Cache      │  │ AI Service │
 └────────────┘  └────────────┘  └────────────┘
```

---

## Technology Stack

### Frontend

* React
* Vite
* Tailwind CSS
* Nginx

### Backend

* Node.js
* Express.js
* REST APIs

### Data Layer

* MongoDB
* Redis

### Infrastructure

* Docker
* Docker Compose
* Kubernetes
* Helm
* NGINX Ingress Controller

---

## Local Development

### Clone Repository

```bash
git clone https://github.com/TarunKamur/Cloud-native-banking-platform.git
cd Cloud-native-banking-platform
```

### Run Application Using Docker Compose

```bash
cd Paisa-bank-app

docker compose up -d
```

Verify running containers:

```bash
docker ps
```

---

## Kubernetes Deployment

Navigate to Helm charts:

```bash
cd paisa-bank-k8s
```

Deploy services:

### MongoDB

```bash
helm install mongodb ./mongodb-chart
```

### Redis

```bash
helm install redis ./redis-chart
```

### Backend

```bash
helm install backend ./backend-chart
```

### Frontend

```bash
helm install frontend ./frontend-chart
```

### Ollama

```bash
helm install ollama ./ollama-chart
```

### Ingress

```bash
helm install ingress ./ingress-chart
```

---

## Verify Deployments

```bash
kubectl get pods
kubectl get svc
kubectl get ingress
```

---

## Features

* User account management
* Banking transaction APIs
* Containerized microservice deployment
* Kubernetes-native architecture
* Helm-based application packaging
* Redis caching support
* MongoDB persistent storage
* AI service integration using Ollama
* NGINX Ingress routing

---

## DevOps Highlights

* Dockerized application stack
* Infrastructure as Code (IaC)
* Kubernetes deployments
* Helm chart packaging
* Service discovery
* Ingress-based routing
* Scalable cloud-native architecture

---

## Future Enhancements

* CI/CD with GitHub Actions
* ArgoCD GitOps deployment
* Prometheus Monitoring
* Grafana Dashboards
* Loki Log Aggregation
* Horizontal Pod Autoscaling (HPA)
* TLS with Cert Manager
* Kubernetes Secrets Management

---

## Author

**Tarun Kumar**

Cloud Engineer | DevOps Engineer | Kubernetes Enthusiast

GitHub: https://github.com/TarunKamur


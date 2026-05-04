# 🚀 Kubernetes Infrastructure Platform

> Production-grade Kubernetes cluster with full observability stack, CI/CD pipeline, and auto-scaling.

![Kubernetes](https://img.shields.io/badge/Kubernetes-1.29-326CE5?logo=kubernetes&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-CD-FC6D26?logo=gitlab&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-3-0F1689?logo=helm&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-Grafana-E6522C?logo=prometheus&logoColor=white)

---

## 📋 Overview

Deployed a production-ready Kubernetes infrastructure for an e-commerce microservices platform. Migrated from Docker Compose on bare-metal to a fully orchestrated Kubernetes cluster with monitoring, logging, and auto-scaling.

---

## 🏗️ Architecture
---

## ⚙️ Stack

| Component | Technology |
|-----------|-----------|
| Container Orchestration | Kubernetes 1.29 |
| Cluster Topology | 3 control-plane + 1 worker |
| Ingress | NGINX Ingress Controller |
| CI/CD | GitLab CI/CD |
| Package Manager | Helm 3 |
| Monitoring | Prometheus + Grafana |
| Logging | Loki + Promtail |
| Auto-scaling | HorizontalPodAutoscaler |
| Container Registry | GitLab Container Registry |

---

## ✅ What Was Done

### 1. Kubernetes Cluster
- Deployed HA cluster: **3 control-plane nodes + 1 worker**
- Configured NGINX Ingress Controller
- All nodes in Ready state

### 2. Microservices & CI/CD
- Deployed **11 microservices** (Google Online Boutique)
- Written **Helm chart** for loadgenerator with ConfigMap
- GitLab CI/CD pipeline with 3 stages:
  - build — Docker image with git SHA tag
  - push — GitLab Container Registry
  - deploy — Helm deploy to Kubernetes

### 3. Monitoring
- Prometheus + Grafana dashboards
- CPU & Memory per pod/namespace

### 4. Logging
- Loki + Promtail for centralized log collection
- Logs visible in Grafana Explore

### 5. Auto-scaling
- HPA for frontend: scales 1→10 replicas at CPU > 50%

---

## 🔄 CI/CD Pipeline
---

## 👨‍💻 Author

**Ернар Нурмаш** — Junior DevOps Engineer

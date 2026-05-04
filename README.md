# 🚀 Kubernetes Infrastructure Platform

> Production-grade Kubernetes кластер с полным стеком наблюдаемости, CI/CD пайплайном и автомасштабированием.

![Kubernetes](https://img.shields.io/badge/Kubernetes-1.29-326CE5?logo=kubernetes&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-CD-FC6D26?logo=gitlab&logoColor=white)
![Helm](https://img.shields.io/badge/Helm-3-0F1689?logo=helm&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-Grafana-E6522C?logo=prometheus&logoColor=white)

---

## 📋 Описание

Развернул production-ready Kubernetes инфраструктуру для платформы электронной коммерции (аналог Ozon/AliExpress). Выполнил миграцию с Docker Compose на bare-metal серверах на полностью оркестрированный Kubernetes кластер с мониторингом, логированием и автомасштабированием.

---

## ⚙️ Стек технологий

| Компонент | Технология |
|-----------|-----------|
| Оркестрация контейнеров | Kubernetes 1.29 |
| Топология кластера | 3 control-plane + 1 worker |
| Ingress | NGINX Ingress Controller |
| CI/CD | GitLab CI/CD |
| Пакетный менеджер | Helm 3 |
| Мониторинг | Prometheus + Grafana |
| Логирование | Loki + Promtail |
| Автомасштабирование | HorizontalPodAutoscaler |
| Container Registry | GitLab Container Registry |

---

## ✅ Что было сделано

### 1. Kubernetes кластер
- Развернул HA кластер: **3 control-plane ноды + 1 worker**
- Настроил NGINX Ingress Controller
- Все ноды в статусе Ready

### 2. Микросервисы и CI/CD
- Развернул **11 микросервисов** (Google Online Boutique)
- Написал **Helm chart** для сервиса loadgenerator с ConfigMap для переменных окружения
- Настроил GitLab CI/CD пайплайн с 3 стадиями:
  - `build` — сборка Docker образа с тегом git SHA
  - `push` — загрузка в GitLab Container Registry
  - `deploy` — деплой через Helm в Kubernetes
- Kubeconfig хранится в GitLab Secrets (не в коде)

### 3. Мониторинг
- Развернул Prometheus + Grafana
- Настроил дашборды: CPU и Memory по каждому поду и namespace

### 4. Логирование
- Развернул Loki + Promtail для централизованного сбора логов
- Логи всех микросервисов доступны в Grafana Explore

### 5. Автомасштабирование
- Настроил HPA для сервиса frontend
- Масштабируется от 1 до 10 реплик при CPU > 50%

---

## 🔄 CI/CD пайплайн

git push → GitLab CI → docker build → push в Registry → helm deploy → Kubernetes

---

## 👨‍💻 Автор

**Ернар Нурмаш** — Junior DevOps Engineer

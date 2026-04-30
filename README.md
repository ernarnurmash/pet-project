# Pet Project — Kubernetes DevOps

## Стек
- Nginx, httpbin, PostgreSQL 15
- Kubernetes (Minikube)
- GitLab CI/CD
- Prometheus + Grafana
- Helm

## Архитектура
Пользователь → Ingress → Nginx / Backend → PostgreSQL

## CI/CD
git push → GitLab Runner → kubectl apply → K8s

## Мониторинг
Prometheus + Grafana через Helm

## Автор
Ернар Нурмаш — Junior DevOps Engineer

# Monitoring

Prometheus + Grafana установлены через Helm:

helm install monitoring prometheus-community/kube-prometheus-stack \
  --namespace monitoring \
  --set grafana.adminPassword=admin123

Grafana доступна через port-forward:
kubectl port-forward -n monitoring svc/monitoring-grafana 3000:80

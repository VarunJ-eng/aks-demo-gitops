# AKS Monitoring Stack

## Helm Repository

Name: prometheus-community

URL: https://prometheus-community.github.io/helm-charts

Chart: kube-prometheus-stack

## Installation

helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm repo update

helm upgrade --install monitoring \
  prometheus-community/kube-prometheus-stack \
  --namespace monitoring \
  --create-namespace \
  -f monitoring/prometheus/values.yaml \
  -f monitoring/grafana/values.yaml

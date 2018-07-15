# Kubernetes monitoring with Prometheus + Grafana
Monitoring solution for Kubernetes clusters based on Prometheus(metrics collector) and Grafana(metrics visualizator)
### Features:
- Node-exporter DaemonSet for Prometheus (https://github.com/prometheus/node_exporter)
- Grafana plugins  `grafana-kubernetes-app`,`grafana-worldmap-panel`
- Persistent storage with volume type `hostPath`
- Ingress support for NGINX Ingress Controller (https://github.com/kubernetes/ingress-nginx)
### Installation
##### Tested on Kubernetes v1.8.2
Make changes requred for your infrastructure (`deployment.yaml` files and `ingress.yaml`)
On master node (or other k8s node, providing additional key `--kubeconfig path_to_your_kubeconfig_file`) execute:
```sh
git clone https://github.com/antontinishov/kubernetes-monitoring.git
kubectl create -f prometheus/ -f grafana/
```
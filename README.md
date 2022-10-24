# Free5GC | 5G Core SA network & RAN on Kubernetes with Grafana KPI Monitoring
Deploy 5G Core SA on Kubernetes | minikube &amp; kubectl on AWS | Grafana KPI Monitoring

## 📚 Concepts
- 3GPP 5G SA Core Network
- Kubernetes
- Helm chart
- Prometheus
- Grafana
- AWS EC2
- Ansible
- Docker
- Linux

## 📚 Review
- minikube (minikube implements a local Kubernetes cluster)
- CNI Calico plugin (features for container network interface)
- kubectl (the Kubernetes command-line tool, kubectl, allows you to run commands against Kubernetes clusters)
- Helm (helps you manage Kubernetes applications )
- Multus-CNI (enables attaching multiple network interfaces to pods)
- Free5GC (open-source project for 5th generation mobile core networks)
- Prometheus (monitoring system with a dimensional data model)
- Grafana (multi-platform open source analytics and interactive visualization web application)

## 📚 Tutorial
1- Launch AWS EC2 Ubuntu (4GB RAM and 2vCPUs minimum)

```
sudo apt update -y
sudo apt upgrade -y
sudo apt install ansible -y
```
2- Run Ansible playbook.yml
```
#check docker
sudo systemctl status docker

#check minikube
minikube status

#check kubectl
kubectl version -o yaml

#check helm
helm list -A

#check pods
kubectl get pods --all-namespaces

#check free5gc pods
kubectl get pods -n free5gc

#check free5gc service
kubectl get svc -n free5gc

#check prometheus pods
kubectl get pods -n prometheus

#check grafana service
kubectl get svc -n prometheus | grep grafana

#access local SSH service port
ssh -i "yourkey" -L localhost:5000:localhost:5000 user@EC2-IP
```


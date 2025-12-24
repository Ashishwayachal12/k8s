
---

## 🚀 Django Notes Application Deployment

The `django-notes-app` is containerized and deployed on Kubernetes.  
It includes:

- Namespace configuration
- Deployment & Service manifests
- Ingress for external access
- KIND/Minikube compatible setup

---

## 🛠️ Tech Stack & Tools Used

| Category | Technologies |
|--------|-------------|
| Containerization | Docker |
| Orchestration | Kubernetes, KIND, Minikube |
| Web Servers | NGINX, Apache |
| Databases | MySQL (RDBMS), NoSQL exposure via AWS DynamoDB |
| Monitoring | Grafana, Prometheus dashboards |
| Package Management | Helm |
| Version Control | Git, GitHub |
| OS & Scripting | Linux, Bash Automation |

---

## 📌 Cluster Setup

Example commands used:

```bash
# Start Minikube cluster (Docker driver)
minikube start --driver=docker --memory=2000 --cpus=2 --kubernetes-version=v1.34.0 --force

# Create KIND cluster using config file
kind create cluster --config config.yml

# Apply manifests
kubectl apply -f django-notes-app/k8s/

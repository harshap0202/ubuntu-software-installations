# Commands to install Kubernetes on Ubuntu [With Minikube]

## Kubectl setup
```bash
curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
chmod +x ./kubectl
sudo mv ./kubectl /usr/local/bin/kubectl
kubectl version
```

## Minikube Setup

```bash
# Confirm virtualization is enabled
grep -E --color 'vmx | svm' /proc/cpuinfo

# Install Minikube
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

# Using Minikube with Docker 
minikube start --driver=docker
# OR
# Using Minikube with Virtual Box 
minikube start --driver=virtualbox

minikube status
kubectl get nodes
```

# 🌀 Kubernetes ReplicaSet (Minikube)

A minimal example demonstrating how to create and manage a **ReplicaSet** in Kubernetes using Minikube. This project helps you understand core scaling and availability concepts by deploying a simple **nginx** container with replica management.

---

## 📌 Project Overview

* **Name**: replicaset-minikube
* **Stack**: Kubernetes YAML, Minikube
* **Goal**: Showcase how a ReplicaSet maintains desired pod replica count
* **Use Case**: Educational tool for learning Kubernetes workload controllers

---

## 📁 Project Structure

```
├── rs.yaml        # Defines a ReplicaSet to maintain one running nginx pod
```

---

## 🚀 Getting Started

### Prerequisites

* [Minikube](https://minikube.sigs.k8s.io/docs/start/)
* [kubectl](https://kubernetes.io/docs/tasks/tools/)

### Installation Steps

```bash
# 1. Start your local cluster
minikube start

# 2. Apply the ReplicaSet configuration
kubectl apply -f rs.yaml

# 3. Verify that the ReplicaSet and pods are running
kubectl get rs
kubectl get pods
```

---

## 📦 Technologies Used

* **Kubernetes** – Orchestration platform for containers
* **Minikube** – Local Kubernetes cluster for testing
* **YAML** – Declarative configuration

---

## 🧪 Testing and Coverage

> Not applicable — this is a declarative infrastructure project.

### Manual Testing

* Delete the pod and watch it auto-recreate:

```bash
kubectl delete pod <pod-name>
kubectl get pods
```

---

## 🧠 Key Challenges & Learnings

* Gained experience writing a ReplicaSet spec from scratch
* Learned how label selectors (`matchLabels`) link ReplicaSets to pods
* Observed self-healing capabilities by testing pod deletion and recovery

---

## 📷 Screenshots or Live Demo

> Sample output:

```bash
kubectl get rs
NAME          DESIRED   CURRENT   READY   AGE
landingpage   1         1         1       10s
```

---

## 📜 License

[MIT](https://opensource.org/licenses/MIT)

---

> Created by [David Hernández](https://github.com/davidhernandez-adm) as part of Kubernetes learning modules.


## What is Kubernetes?
Kubernetes (K8s) is an open-source container orchestration platform for automating deployment, scaling, and management of containerized applications.

---

## Key Concepts

### 1. **Cluster**
- A set of machines (nodes) running Kubernetes.
- Consists of a **master node** (control plane) and **worker nodes**.

### 2. **Node**
- A physical or virtual machine in the cluster.
- **Master Node:** Manages the cluster.
- **Worker Node:** Runs application workloads.

### 3. **Pod**
- The smallest deployable unit.
- Encapsulates one or more containers, storage, and network resources.

### 4. **Service**
- Exposes a set of pods as a network service.
- Types: ClusterIP, NodePort, LoadBalancer, ExternalName.

### 5. **Deployment**
- Manages replica sets and pod updates.
- Ensures the desired number of pods are running.

### 6. **ReplicaSet**
- Ensures a specified number of pod replicas are running at any time.

### 7. **Namespace**
- Provides a mechanism for isolating groups of resources within a cluster.

---

## Kubernetes Architecture

- **Control Plane Components:**
    - `kube-apiserver`: API entry point.
    - `etcd`: Key-value store for cluster data.
    - `kube-scheduler`: Assigns pods to nodes.
    - `kube-controller-manager`: Runs controllers.
    - `cloud-controller-manager`: Integrates with cloud providers.

- **Node Components:**
    - `kubelet`: Ensures containers are running.
    - `kube-proxy`: Manages networking.
    - `Container runtime`: (e.g., Docker, containerd).

---

## Key Features

- **Self-healing:** Restarts failed containers, replaces and reschedules pods.
- **Horizontal scaling:** Scale applications up/down automatically.
- **Service discovery & load balancing:** Exposes services and balances traffic.
- **Automated rollouts & rollbacks:** Updates applications with zero downtime.
- **Secret & configuration management:** Manages sensitive data and configs.

---

## Basic Workflow

1. **Write a manifest** (YAML/JSON) describing the desired state.
2. **Apply the manifest** using `kubectl apply -f <file>`.
3. **Kubernetes reconciles** the actual state to match the desired state.

---

## Common Commands

```sh
kubectl get pods
kubectl get services
kubectl apply -f deployment.yaml
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl scale deployment <deployment-name> --replicas=3
```

---

## Useful Resources

- [Kubernetes Official Documentation](https://kubernetes.io/docs/)
- [Kubernetes GitHub](https://github.com/kubernetes/kubernetes)
- [Kubernetes Tutorials](https://kubernetes.io/docs/tutorials/)

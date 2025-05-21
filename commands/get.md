### kubectl get
The `kubectl get` command is used to list resources in a Kubernetes cluster. It can be used to retrieve information about various resources such as pods, services, deployments, and more.

---

##### List all nodes in the cluster:
```bash
kubectl get nodes
```

##### List all pods in the current namespace:
```bash
kubectl get pods
```

##### List all replication controllers in the current namespace:
```bash
kubectl get rc
```

##### List all replicasets in the current namespace:
```bash
kubectl get rs
```

##### List all deployments in the current namespace:
```bash
kubectl get deployments
```

##### List all services in the current namespace:
```bash
kubectl get services
```

##### List all deployments, services, replicasets, and pods in the current namespace:
```bash
kubectl get all
```
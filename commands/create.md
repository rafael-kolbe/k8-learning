### kubectl create
The `kubectl create` command is used to create a resource in Kubernetes. It allows you to specify the type of resource you want to create, such as a pod, service, or deployment, along with its configuration.

---

##### Create a new resource using a file configuration:
```bash
kubectl create -f <file>
```

##### Create a new resource in a different namespace:
```bash
kubectl create -f <file> -n <namespace>
```
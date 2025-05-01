### kubectl apply
The `kubectl apply` command is used to apply a configuration to a resource (pod, deployment, service, etc). It can be used to create or update resources in a Kubernetes cluster.

---

##### Apply a configuration to a resource:
```bash
kubectl apply -f <file>
```
_If the resource does not exist, it will be created, otherwise, it will be updated with the new configuration._
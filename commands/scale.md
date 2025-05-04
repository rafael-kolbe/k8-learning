### kubectl scale
The `kubectl scale` command is used to change the number of replicas of a resource in Kubernetes. It allows you to scale up or down the number of instances of a deployment, replica set, or replication controller without having to edit the definition file.
It's intended to be used for quick up or down scaling of resources, depending on the server demand.

---

##### Scale a deployment to 5 replicas:
```bash
kubectl scale deployment <deployment-name> --replicas=5
```

##### Scale by using a file configuration:
```bash
kubectl scale --replicas=5 -f <file>
```

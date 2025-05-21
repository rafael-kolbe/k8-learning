### `kubectl rollout`
The `kubectl rollout` command is used to manage the rollout of a resource in Kubernetes. It allows you to view the status of a rollout, pause or resume a rollout, and undo a rollout to a previous version.

---

##### View the rollout status of a deployment:
```bash
kubectl rollout status deployment/<deployment-name>
```

##### View the history of a deployment rollout:
```bash
kubectl rollout history deployment/<deployment-name>
```

##### Undo a rollout to a previous version:
```bash
kubectl rollout undo deployment/<deployment-name>
```

### kubectl replace
The `kubectl replace` command is used to update a resource in Kubernetes by replacing it with a new configuration. It allows you to specify the type of resource you want to update, such as a pod, service, or deployment, along with its new configuration.

---

##### Replace the configuration of a resource:
```bash
kubectl replace -f <file>
```
_If the resource was modified manually by a command, for example the `kubectl scale`, the replace command **will** undo the scale command, as the full written definition will be applied again._
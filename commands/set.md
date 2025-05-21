### `kubectl set`
The `kubectl set` command is used to modify the configuration of a resource in Kubernetes. It allows you to set specific fields or properties of a resource, such as environment variables, image versions, and more.
It is a more targeted approach compared to `kubectl apply` or `kubectl replace`, which can be used to update the entire resource configuration.
Keep in mind that any changes made with this command won't be in sync with the configuration file.

---

##### Set the image of a deployment:
```bash
kubectl set image deployment/<deployment-name> <container-name>=<new-image>
```

##### Set the environment variable of a deployment:
```bash
kubectl set env deployment/<deployment-name> <env-var-name>=<env-var-value>
```

##### Set the resource limits of a deployment:
```bash
kubectl set resources deployment/<deployment-name> --limits=<resource-limits>
```

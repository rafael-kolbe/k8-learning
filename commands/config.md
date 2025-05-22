### kubectl config
The `kubectl config` command is used to manage the Kubernetes configuration file, which contains information about clusters, users, and contexts. This command allows you to set up and modify your Kubernetes configuration, making it easier to switch between different clusters and namespaces.

---

##### View the current context:
```bash
kubectl config current-context
```

##### Switch to a different namespace:
```bash
kubectl config set-context --current -n <namespace>
kubectl config set-context $(kubectl config current-context) -n <namespace>
```
_Both commands set the current context to use the specified namespace. This is useful for managing resources in different namespaces without having to specify the namespace each time. The second command is how you can embed information (current-context in this case) through another command._
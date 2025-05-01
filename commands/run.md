### kubectl run
The `kubectl run` command is used to create a new deployment in Kubernetes. It allows you to specify the name of the deployment, the image to use, and the port to expose.

---

##### Start a new deployment with the specified name, image, and port:
```bash
kubectl run <name> --image=<image> --port=<port>
```
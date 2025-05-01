### `kubectl <command> -<flag>`
There are several flags that can be used with `kubectl` commands. These flags modify the behavior of the command and can be used to specify options such as output format, namespace, and more. 

---

##### Output Format Flags
- `-o` or `--output`: This flag is used to specify the output format of the command. Common formats include `json`, `yaml`, `wide`, and `name`.
```bash
kubectl get pods -o wide
```
_This will add information such as node name, IP address, and container status to the output._

##### File Flags
- `-f` or `--filename`: This flag is used to specify the file containing the resource definition. It can be used with commands like `kubectl apply`, `kubectl create`, and `kubectl delete`.
```bash
kubectl create -f 1_pod-definition.yaml
```
_This will create a pod using the configuration defined in the `1_pod-definition.yaml` file._

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

##### Target all resources
- `--all`: This flag is used to target all resources of a specific type. It can be used with commands like `kubectl get`, `kubectl delete`, and `kubectl describe`.
```bash
kubectl delete pods --all
```
_This will delete all pods in the current namespace._

##### Namespace Flags
- `-n` or `--namespace`: This flag is used to specify the namespace in which the command should be executed. It can be used with all commands.
```bash
kubectl get pods -n test
```
_This will list all pods in the `test` namespace._
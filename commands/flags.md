### `kubectl <command> -<flag>`
There are several flags that can be used with `kubectl` commands. These flags modify the behavior of the command and can be used to specify options such as output format, namespace, and more. 

---

##### Output Format Flags
- `-o` or `--output`: This flag is used to specify the output format of the command. Common formats include `json`, `yaml`, `wide`, and `name`.
```bash
kubectl get pods -o wide
```
_This will add information such as node name, IP address, and container status to the output._
`API Server` - The frontend of kubernetes. All user commands in the terminal use this API to manage the kubernetes environment.

`etcd` - Key-Value store, used by kubernetes to store all data responsible to manage the cluster.

`Scheduler` - Distributes work on containers across multiples nodes, it looks for newly created containers and assigns them to nodes.

`Controller` - The brain behind orchestration, responsible for noticing and responding when nodes, containers or endpoints does down. They make decisions to bring up new containers in such cases.

`Container Runtime` - The underlying software that is used to run containers. Usually Docker.

`kubelet` - An agent that runs on each node in the cluster. It's responsible to make sure the containers are running as expected.

---

The Master node contains the API server, etcd, scheduler and controller. 
The Worker nodes contain the kubelet and container runtime.
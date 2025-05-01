`Nodes` - A machine, physical or virtual on which kubernetes is installed. A node is a worker machine, and it's where containers will be launched by kubernetes.

`Cluster` - A set of nodes grouped together. This way, if your application (node) fails, it will still be accessible by the other nodes. Also, having multiples nodes helps in sharing load as well.

`Master` - Also a node with kubernetes installed in it. It's responsible for managing the other nodes in the cluster, for example when a node fails, it will deploy another in its place. Basically the orchestrator.
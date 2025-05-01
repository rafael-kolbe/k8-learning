Pods are single instance of an application. It contains one or more containers, a unique network IP, and storage resources.
They are the smallest deployable units in Kubernetes.
When user demand of your applications increases, the correct way to scale it is by creating more pods, instead of adding new containers to the same pod.
If the demand further increases and your node has no sufficient capacity, you can add more nodes to the cluster together with more pods.
Multi-container pods are used when you need to share resources between containers, for example, and API server that uses a database. In this case, the API server and the database will be in the same pod, so they can communicate with each other using the localhost address (Their POD network IP).
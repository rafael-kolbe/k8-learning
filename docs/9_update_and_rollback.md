Any update is done by a Rollout, which is a type of migration that allows for versioning control. This enables the possibility to roll back to a previous version if needed.

There are different ways to update a resource in Kubernetes:

Recreate: This method involves deleting the existing resource and creating a new one with the updated configuration. This is not the best way as the application will be unavailable between the time all resources are deleted, and the first new version is created.

Rolling Update: This method involves updating the resource in a way that ensures that the application remains available during the update process. This is done by gradually replacing the old version of the resource with the new version, ensuring that a minimum number of replicas are always available. This is also the default method for updating a deployment in Kubernetes.

---

When a command to update a deployment is issued as a Rolling Update, it creates a new ReplicaSet under the hood. The new ReplicaSet is then scaled up, and the old ReplicaSet is scaled down. This process continues until all replicas of the old ReplicaSet are terminated and replaced by the new ReplicaSet. This ensures that there is no downtime during the update process.

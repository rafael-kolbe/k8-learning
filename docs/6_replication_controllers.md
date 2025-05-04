Replication Controllers are made to achieve high availability, by ensuring a specified number of pods are running at any time, be that 1 or 100.
They also help with load balancing and scaling, by adding or removing pods automatically based on server demand.
They are the old way of doing this, and are now deprecated in favor of ReplicaSets, which will be discussed in docs/7_replicasets.md
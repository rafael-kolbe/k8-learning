# Voting App

### Description
This project is a simple voting app that uses different technologies to demonstrate how to deploy a multi-container application using Kubernetes.
The user will be able to vote for either cats or dogs, and the results will be displayed in real-time.

### Technologies
voting-app: Frontend made in Python
result-app: Frontend made in Node
redis: Redis database
db: PostgreSQL database
worker: Worker made in C#

### Architecture
The voting-app is the entry point for the voting process.
The vote will be sent to the Redis database.
The worker will then process the vote and store in the PostgreSQL database.
The result-app will retrieve the results from the PostgreSQL database and display them in real-time.

### Deployment
The deployment will be done using a single node from Minikube.

##### Create all resources using a file configuration:
```bash
kubectl create -f <file-name>
```

##### Deploy with Minikube:
```bash
minikube service voting-app-service --url
minikube service result-app-service --url
```
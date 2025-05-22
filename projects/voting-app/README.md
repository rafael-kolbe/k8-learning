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

---

### Notes
It appears that the voting app doesn't work as expected. The logs show that the postgres container is having trouble to insert new votes.
Since all containers are third-party images, I can't really fix the issue, unless I make my own versions of each image.
But since this is a kubernetes repository for learning, the most important part is the definition files, which are correctly configured.
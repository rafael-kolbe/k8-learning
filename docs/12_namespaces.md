Namespaces are separate environments in the Kubernetes cluster that allow you to organize and manage resources. They are useful for separating different environments such as development, testing, and production. By default, Kubernetes creates a "default" namespace for all resources. You are fine with only "default" if you are just testing or learning Kubernetes. But if you want to make a more complex application to ship to production, you should consider using namespaces to separate your resources.

Say you have a "dev" and a "test" namespace. From the "dev" namespace, you can call its resources just by their name. But if you want to call a resource from the "test" namespace, you need to specify the correct address like below:

##### Using a resource from the "dev" namespace, while being in it:
```bash
kubectl get pods
```

##### Using a resource from the "test" namespace, while being in the "dev" namespace:
```bash
kubectl get pods -n test
```
_Here the "-n" flag is used to specify the namespace._

##### Connecting a mysql database in the "dev" namespace, while being in it:
```python
import mysql.connector
import os

def connect_to_db():
    db = mysql.connector.connect(
        host="db-service",
        user=os.getenv("MYSQL_USER"),
        password=os.getenv("MYSQL_PASSWORD"),
        database=os.getenv("MYSQL_DATABASE")
    )
    return db
```
_Here, the "db-service" is the name of the service that connects to the database. Since we are in the "dev" namespace, we don't need to specify the namespace._

##### Connecting a mysql database from the "test" namespace, while being in the "dev" namespace:
```python
import mysql.connector
import os

def connect_to_db():
    db = mysql.connector.connect(
        host="db-service.test.svc.cluster.local",
        user=os.getenv("MYSQL_USER"),
        password=os.getenv("MYSQL_PASSWORD"),
        database=os.getenv("MYSQL_DATABASE")
    )
    return db
```
_Here, "db-service" is the name of the service in the "test" namespace. Since we are in the "dev" namespace, we need to specify the full DNS name to reach the service._
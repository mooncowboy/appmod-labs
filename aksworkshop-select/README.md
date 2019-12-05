Selected tasks from the [The Azure Kubernetes Workshop](https://aksworkshop.io/) for half-day hands-on workshops.

Lab Time: 4 hours

# Pre-requisites

* As defined in https://aksworkshop.io/#prereq

* Cloud Shell: Storage Account name must be globally unique 

# Lab Steps

* Deploy Helm (if using Helm 3, see command below): 

```
helm install orders-mongo stable/mongodb --set mongodbUsername=orders-user,mongodbPassword=orders-password,mongodbDatabase=akschallenge

```

* [Deploy Order Capture API](https://aksworkshop.io/#api)

* [Deploy Frontend with Ingress](https://aksworkshop.io/#frontend)

* [Mongo replication with StatefulSet](https://aksworkshop.io/#mongostateful)

* [Scaling](https://aksworkshop.io/#scaling)
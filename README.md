DESCRIPTION

For the deployment of the main application i localy used another image (wordpress) for testing purpose. 

The frontend application can be hit up by the backend application throughout a service. The one named postgresql-service which exposes the postgresql database.

Both are exposed throughout services. Otherwise it would not be possible to communcate with each other. Inside the cluster, the bottom line to establish the communication between them is to set up the backend application with a clusterIP service. 

An ingress resource has been set up to allow the main application being reachable outside the cluster. So that the frontend application has been exposed by a nodeport service. 

Notice that all the deployments have been done inside a unique namespace. The one front-back-app.



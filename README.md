DESCRIPTION

For the deployment of the main application i localy used another image (wordpress) for testing purpose. 

The frontend application can be hit up by the backend application throughout a service. The one named posgresql which exposes the posgresql database.

Both are exposed throughout services. Otherwise it would not be possible to communcate with each other. Inside the cluster, the bottom line to establish the communication between them is to set up the backend application with a clusterIP service. 

A ingress resource has been set up to allow the main application being reachable outside the cluster. So that the frontend application has been exposed by a nodeport service. 

Notice that all the deployment have been done inside a uniq namespace. The one front-back-app-namespace.



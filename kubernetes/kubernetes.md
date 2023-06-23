# Kubernetes
## What is Kubernetes
System for running many different containers over multiple different machine
## Why use Kubernetes
When you need to run many different containers with different images.

## Working with Kubernetes
![Kubernetes visualization](attachments/Kubernetes%20Visualization.jpg)

## Kubernetes Dev vs Prod
![KUBERNETES Dev vs Prod](attachments/Kubernetes%20Dev%20vs%20prod.jpg)

## Kubernetes Dev Setup
![Kubernetes](attachments/kubernetes%20dev%20setup.jpg)
![Kubernetes](attachments/kubernetes%20dev%20setup%202.jpg)

## Feed a config file to Kubectl

> Kubectl apply -f `<filename>`

- apply: change the current configuration of our cluster

>Kubectl get pods
>Kubectl get services

- get: we want to retrieve information about a running object


## Important Basic
- Nodes are individual machine vm run containers
-  Master r machine with a set of programs to manage Nodes
-  Kubernetes didnt build our image, it got them from somewhere else
-  Kubernetes decided where to run each container - each node can run a dissimilar set of containers
-  To deploy something, we update the desired state of the master with a config file
-  The master works constantly to meet your desired state


## Object Type
- Pods: runs one or more closely related container
- services: Sets up networking in a Kubernetes cluster
  - ClusterIP: Exposes a set of pods to other objects in the cluster
  - NodePort: Eposes a set of pods to the outside world (only good for dev purpose)
  - LoadBalancer
  - Ingress
![Kubernetes](attachments/kubernetes%20ingress.jpg)

## Volumes
- Volumes in generic container: some type of mechanism that allows a container to access a filesystem outside itself
- Volume in Kubernetes: An object that allows a container to store data at the pod level

## KUBECTL SECRET
- kubectl create secret generic pgpassword --from-literal PGPASSWORD=12345asdf
# ***Kubernetes***

To understand K8s

1. What is Kubernetes?
2. Why Kubernetes?
3. Kubernetes Architecture
4. KUbernetes Lifecycle
5. Instalation of Minikube
-------------------------------------------
### List of Objects
---
___`Pod`___ - Smallest entity managing by the k8s. Thin wrapper on container.

___`Service`___ - expose application in network
- ***ClusterIP*** - Expose application inside the cluster
- ***NodePort*** - Expose application outside the cluster with the help of Node Ports
- ***LoadBalancer*** - Expose application outside the cluster using cloud loadbalancers


___`Volume`___ - mount on pods

- ***persitent volume*** - will last after the pod dies
- ***ephemeral volume*** - will last till pod running


___`Namespaces`___ - segregate the objects/resources

___`Deployments`___ - manage multiple pods and provides scaling, strategy, and rollback features.

___`ReplicationController`___ - It ensure that the correct number of pod replicas are running on the cluster. Uses equility-based selector.

___`ReplicaSet`___ - It ensure that the correct number of pod replicas are running on the cluster. Uses in, notin, exists operator based selector.

___`DaemonSet`___ - To create pod on all nodes / specific node similar to daemon

___`StatefulSet`___ - Will provide unique indentities to pods even it restarts

___`ConfigMaps / Secrets`___ - Use to store the credential

-----------------

## ***Kubernetes Cheat Sheet***
--------
- `kubectl get nodes` - list all nodes present in the cluster

- `kubectl get pods` - list all pods running in the cluster

- `kubectl get pods` -o wide - to get ip of pods

- `kubectl run --image httpd web -

- `kubectl describe pod web` - detailed information of pods

- `kubectl get <objects>` - get list of objects

- `kubectl get all` - get list of all objects runnning in the container

- `kubectl get ns` - list namespaces

- `kubectl create namespace <name>` - create namespace

- `kubectl delete namespace <name>` - to delete namespace

- `kubectl get pods -n <namespace_name>` - to get pods in specific namespace. Use `-n` option to execute commond in perticular namespace

- `kubectl describe pod <pod_name>` - to get detailed info about pod

- `kubectl logs <pod_name> -c <container_name>` - to get logs of the container
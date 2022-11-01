# ***Kubernetes Architecture***
-----------------------------------------------
![kubernetes-archetecture](https://github.com/akshaypatil-3/Kubernetes/blob/main/images/WhatsApp%20Image%202022-10-16%20at%2011.31.13%20PM.jpeg)
-----------------------------------------------
>Kubernetes architecture contains clusters, each kubernetes cluster contains two types of node master node and worker node, master node also called as master plane or control plane, and worker node also called as slave node.
The responsibility of the control plane is to manage the deployment on the worker node, the control plane consists of four components: API server, Scheduler, Control manager and ETCD.

>***`API`*** server will handle all the communication or all the connection between user, control plane and worker node, It serves as front end to the cluster. This is the only component that communicates with the etcd cluster, making sure data is stored in etcd, It is the central management entity that receives all REST requests for modifications to pods, services, replication sets/controllers and others.

>***`scheduler`*** is responsible to send the command to the worker node. It is responsible for distributing (or schedule) the workload on the various worker nodes based on resource utilization.

>The ***`control manager`*** controls all the activity inside the worker node like how many replicas are to be created, how many containers are to be managed, how many pods should be there and what are the desired capacity, min capacity, maximum capacity of the pods all will be managed by the control manager. even in which worker node pod should be created also managed by the control manager

>***`ETCD`*** is responsible to store all the state related information of the worker nodes such as  how many pods are running in which worker node, how many worker nodes are there and which worker node is unavailable, all information stored in etcd. It is accessible only by Kubernetes API server for security reasons.

>Then lets toward the worker node actual deployment happen over the worker node like the actual application, containers and pods are going to deploy on the worker node, inside the worker node there are four components present among this two major component one are kublet and kubeproxy 

>`Kubelets` which is responsible to execute the command which is given by the scheduler. It regularly taking in new or modified specifications from etcd through the api server and ensuring that pods and their containers are healthy and running in the desired state

>`kube proxy` is responsible to communicate within the cluster. It is a proxy service that runs on each worker node helps in making services available to the external host.
  It performs request forwarding to the correct pods/containers across the various isolated networks in a cluster. It manages pods on node, volumes, secrets, creating new containers health checkup, etc.

>`container tool` it is the container engine just like docker which is going to execute or run the container inside the pods.

>`pods` are the smallest unit of the deployment in which one or more than one container can be created.
---

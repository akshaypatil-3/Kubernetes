# **Kubenetes**
---
## What is kubernetes ?
>kubernetes is an open-source container orchestration system for automating software deployment, scaling, and management.
---
### Why we should used kubernetes or Why you are using kubernetes insted of docker compose and docker swan ?
-  It makes it easier to create load balancer and implemet load balancer on docker container.
- kubernates is cloud native application.
- kubernates provide security in term of credential and network level security {attach proxy server, firewall, engress}.
- easy to mange docker container
-  it provide autoscaling of horizontal and vertical scaling possible
-  scheduling of the container
---
### Kubernetes Feature
1. Autoscaling 
    >Automatically scale containrized application and their resources up or down based on usage
2. Lifecycle Management 
    >Automate deployments and updates with the ability to:
    >- Rollback of previous version
    >- Pause and continue a deployment 
3. Declaratic Model
    >Declare the desired state, and k8s works in the background to maintain that stae and recover from any failure.

4. Resilience and Self-healing
    >Auto placment, auto restart, auro replication and auro scaling provide application self-healing.

5. Persitance Storege
    >Ability to mount and add storage dynamically.

6. Load Balancing
   >kubernetes supports a variety of internal and external load balancing options to address diverse needs.

7. DevSecOps
   >DevSec is an advance approarch to security that simpifies and automate container lifecycle, and enables teams deliver secure,
   high-qualiy software more quickly. Combining DevSecOps practices and Kubernetes improves developer productivity.
   ---
#### Kubernetes use
> In company senario we write docker image then kubernetes run container by using docker image.
  and manged container include how many container required and also we doing  scheduling of container 
  edit and modification of container , service expose on the network all the thing handle by using kubnernetes
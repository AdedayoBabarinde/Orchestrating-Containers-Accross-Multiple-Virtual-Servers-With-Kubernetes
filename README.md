# Orchestrating-Containers-Accross-Multiple-Virtual-Servers-With-Kubernetes


This project involves the following:

- Creating Public Key Infrastructure(PKI) for implementing TLS encryption for data on flight.
- Provisioning Ec2 instances for master(3) and worker nodes(3)
- provisioning of Network infrastructure to power the Ec2 instances
- Configuring the instances: Installing the required software needed by the instances to perform respective roles.



##  Kubernetes Cluster Architecture.

K8s cluster has 3 master nodes and 3 worker nodes.

The following services are active on each of the Master nodes:

  - ETCD - Key value distributed store. Used to persist the state of the cluster.
  - Kube-Api-Server - This acts as the cluster's brain and as a portal into the cluster.
  - Kube-Scheduler - Select the worker node to run containerized workload. 
  - kube-Controller-Manager - Ensures the desired state of the cluster is meet. 



The Worker nodes has the following services running on each of them:

  - Kubelet - Its servers the agent and is in constant communication with kube-api-server
  - Kube-Proxy - In charge of maintaining network rules within the node. This enables communication between pods both inside and outside of the cluster.
  - Container runtime - Is the Engine responsible for running container work loads. We used containers in this project.




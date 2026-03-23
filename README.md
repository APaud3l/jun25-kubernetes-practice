# jun25-kubernetes-practice
Practicing Kubernetes using minikube

## Core Kubernetes Concepts

### Cluster
- A cluster is the full Kubernetes environment
- eg. School System (cluster) managing students (apps)

### Node
- A machine that runs your workloads
- eg. A classroom or a building (node) where students learn (apps run)

### Pod
- The basic deployable unit in Kubernetes
- eg. A student/desk (pod) in a classroom (node)

### Deployment
- A deployment manages the pods declaratively
- eg. A teacher (deployment) keeps the right number of students (pod) in class (node)

### Service
- A service gives a stable network access to the pods.
- eg. The front desk/reception (service) where visitors/students ask for directions to buildings/classrooms (pod)

### Notable mentions
- ClusterIP: internal-only, is provided by default
- NodePort: exposes the app on a port of the node, is best for local work
- LoadBalancer: Distribute request loads across different pods
- ControlPlane: Keeps it all working

# Getting Started

- `minikube start --driver=docker`: Creates and starts a local kubernetes cluster with Docker as the runtime environment

- `kubectl cluster-info`: Shows where the K8s control plane is running 

- `kubectl get nodes`: List of nodes that exist in the cluster

- `kubectl create deployment demo-minikube --image=kicbase/echo-server:1.0`

# kubernetes-cluster

#minikube cluster master and 4 nodes for deployment
minikube start --driver docker --nodes 4

k get nodes

NAME           STATUS   ROLES           AGE   VERSION
minikube       Ready    control-plane   15h   v1.30.0
minikube-m02   Ready    <none>          15h   v1.30.0
minikube-m03   Ready    <none>          15h   v1.30.0
minikube-m04   Ready    <none>          15h   v1.30.0

#Tainting master nodes so that it will deploy in the worker nodes
k taint nodes minikube admin=true:NoSchedule


Kubernetes Clusters 

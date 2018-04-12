# Kebernetes

## Minikube start
minikube start
kubectl get ns

## Create pod
kubectl create -f pod.yml
kubectl get pod
kubectl delete pod ghost

## Create replicaset
kubectl create -f rs.yml
kubectl get service
minikube service ghost

## Create service
kubectl create -f svc.yml
kubectl get rs
kubectl scale rs ghost --replicas=2

## All together using generator
kubectl run ghost-new --image=ghost:1.7 --port 2368 --expose=true
kubectl edit svc ghost-new 
>type: NodePort

## Rolling update



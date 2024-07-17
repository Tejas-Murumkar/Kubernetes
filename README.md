# Kubernetes Commands
${\color{green}\textbf{Pod}}$
1. To Run the Pod
````
kubectl apply -f <filename>
````
2. To list Pods
````
kubectl get pods
````
3. To Delete the Pod
````
kubectl delete pod <pod-name>
````
4. To get brief details of pods
````
kubectl get pod -o wide
````
5. To Enter into pods
````
kubectl exec -it <Pod-name> /bin/bash
````
${\color{green}\textbf{Replication Controller}}$
7. To list replication controller
````
kubectl get rc
````
7. To Run RC
````
kubectl apply -f <rc-filename>
````
8. To delete rc
````
kubectl delete rc <rc-name>
````
${\color{green}\text{ReplicaSet}}$
9. To run ReplicaSet
````
kubectl apply -f <rs-filename>
````

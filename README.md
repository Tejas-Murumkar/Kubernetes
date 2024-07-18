# Kubernetes Commands
## ${\color{lightblue}\textbf{Pod}}$
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
## ${\color{lightblue}\textbf{Replication Controller}}$<br>

6. To list replication controller
````
kubectl get rc
````
7. To Run RC
````
kubectl apply -f <rc-filename>
````
8. To get brief details of rc
````
kubectl get rc -o wide
````
9. To delete rc
````
kubectl delete rc <rc-name>
````
## ${\color{lightblue}\textbf{ReplicaSet}}$<br>

9. To run ReplicaSet
````
kubectl apply -f <rs-filename>
````
10. To List RS
````
kubectl get rs
````
11. To delete RS
````
kubectl delete rc <rc-name>
````
12. To get brief details of RS
````
kubectl get rs -o wide
````

## ${\color{lightblue}\textbf{Deployment}}$<br>

13. To run Deployment
````
kubectl apply -f <deploy-filename>
````
14. To List Deployment
````
kubectl get deployment
````
15. To Delete deployment
````
kubectl delete deployment <deployment-name>
````
16. To get brief details of Deployment
````
kubectl get deployment -o wide
````
17. To Create Deployment without file
````
kubectl create deployment <deployment-name> --image=<imagename> --replicas=<no.of replicas>
````
18. To Create yaml file from Deployment
````
kubectl get deployment -o yaml > <filename.yaml>
````
19. To update or change the image in deployment
````
kubectl set image deployment <deployment-name> <container-name>=<image-name>:<version> --record
````
20. To Check the rollout status
````
kubectl rollout status deployment <deployment-name>
````
21. To Check the history of changes made in deployment
````
kubectl rollout history deployment <deployment-name>
````
22. To Rollback to previous version
````
kubectl rollout undo deployment <deployment-name>
````
23. To Rollback to particular version of deployment
````
kubectl rollout undo deployment <deployment-name> --to-revision=<no. of the revision>
````
## ${\color{lightblue}\textbf{Namespace}}$<br>

24. To Create Namespace
````
kubectl create namespace <namespace_name>
````
25. To List Namespaces
````
kubectl get namespaces
````
26. To list all pods with their namespaces
````
kubectl get pods --all-namespaces
````
27. To List pods in particular namespace
````
kubectl get pods -n <namespace_name>
````
28. To set default namespace
````
kubectl config set-context --current --namespace= <namespace_name>
````
29. To Create pod in particular namespace
````
kubectl apply -f <filename> --namespace=<namespace_name>
````
30. To display the current namespace
````
kubectl config view --minify | grep namespace:
````

    

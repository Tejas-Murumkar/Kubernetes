${\color{yellow}\textbf{Deployment}}$
````
apiVersion: apps/v1
kind: Deployment
metadata:
  name: appdeployment
  labels:
    app: ngix-deployment
spec:
  replicas: 3
  strategy:
    type: RollingUpdate
    rollingUpdate:
     maxSurge: 4
     maxUnavailable: 2
  selector:
     matchExpressions:
       - key: app
         operator: Exists
  template:
     metadata:
         name: nginx-temp
         labels:
            app: nginx-app
     spec:
        containers:
              - name: nginx-app
                image: nginx:latest
                ports:
                  - containerPort: 80
````

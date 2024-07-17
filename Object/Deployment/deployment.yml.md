${\color{red} \textbf{Deployment}}$

````
apiVersion: apps/v1
kind: Deployment
metadata:
  name: deployment-1
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template: 
    metadata:
      labels:
        app: my-app
    spec: 
      containers: 
      - name: cont1
        image: httpd:latest
        ports:
        - containerPort: 80
````

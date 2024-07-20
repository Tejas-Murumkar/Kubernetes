# $${\color{lightblue}\textbf{CLuster IP}}$$
## Deployment
```yml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: d1
  labels:
    type: trial
spec:
  replicas: 1
  selector:
    matchLabels:
            app: nginx
  template:
    metadata:
      name: nginx-temp
      labels:
        app: nginx
    spec:
      containers:
        - name: nginx
          image: nginx:latest
          ports:
            - containerPort: 80
```
## Service
```yml
apiVersion: v1
kind: Service
metadata:
   name: myservice
spec:
  selector:
    app: nginx
  ports:
   - name: mysvcports
     protocol: TCP
     port: 80
```
     targetPort: 80

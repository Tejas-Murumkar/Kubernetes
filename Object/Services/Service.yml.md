# $${\color{lightblue}\textbf{Service}}$$
## $${\color{lightlightblue}\textbf{Deployment}}$$
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
## $${\color{lightlightblue}\textbf{Cluster IP}}$$
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
     targetPort: 80
```
## $${\color{lightlightblue}\textbf{NodePort}}$$
```yml
apiVersion: v1
kind: Service
metadata:
   name: myservice
spec:
  type: NodePort
  selector:
    app: nginx
  ports:
   - name: mysvcports
     protocol: TCP
     port: 80
     targetPort: 80
     nodePort: 30009
```

## $${\color{lightlightblue}\textbf{LoadBalancer}}$$
```yml
apiVersion: v1
kind: Service
metadata:
   name: myservice
spec:
  type: LoadBalancer
  externalIPs:
   - 192.168.0.20
  selector:
    app: nginx
  ports:
   - name: mysvcports
     protocol: TCP
     port: 80
     targetPort: 80
```

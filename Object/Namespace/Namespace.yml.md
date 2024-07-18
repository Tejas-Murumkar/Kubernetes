# ${\color{lightgreen}\textbf{Namespace create}}$
```
apiVersion: v1
kind: Namespace
metadata:
  name: nginx-ns
```
# ${\color{lightgreen}\textbf{Pod with particular namespace}}$

```
apiVersion: v1
kind: Pod
metadata:
  name: nginx-pod
  namespace: nginx-ns
```

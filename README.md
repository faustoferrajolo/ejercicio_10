# Ejercicio 10
## Desplegar nicopaez/pingapp:2.1.0 en Kubernetes


### Secret creation
```sh
$ echo {"mypass":"password!"} | base64
$ e215cGFzczpwYXNzd29yZCF9Cg==
```
### Comandos
```sh
kubectl apply -f 01-namespace.yaml
kubectl apply -f 02-configmap.yaml
kubectl apply -f 03-configmap.yaml
kubectl apply -f 04-secret.yaml
kubectl apply -f 05-deployment.yaml
kubectl apply -f 06-sevices.yaml

kubectl port-forward svc/pingapp210 -n ej10 8080:8080 --address='0.0.0.0'
```

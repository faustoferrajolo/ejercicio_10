# Ejercicio 10
## Desplegar nicopaez/pingapp:2.1.0 en Kubernetes


### Secret creation
```sh
$ echo {"mypass":"password!"} | base64
$ e215cGFzczpwYXNzd29yZCF9Cg==
```
### Comandos
```sh
kubectl apply -f .

kubectl port-forward svc/pingapp210 -n ej10 8080:8080 --address='0.0.0.0'
```

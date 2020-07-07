# Kube Demo

[https://linuxacademy.com/blog/containers/kubernetes-cheat-sheet/](https://linuxacademy.com/blog/containers/kubernetes-cheat-sheet/)

## Namespace

```sh
kubectl create namespace demo
```

## Pods

```sh
kubectl apply -f .\pod.yaml -n demo
```

```sh
kubectl get pods -n demo
kubectl describe pods hello -n demo
kubectl get pods hello -n demo -o yaml
```

```sh
kubectl delete -f .\pod.yaml -n demo
kubectl delete pods hello -n demo
kubectl get pods -n demo
```

## Dempoyments

```sh
kubectl apply -f .\deployment.yaml -n demo
```

```sh
kubectl get deployments -n demo
kubectl describe deployments hello -n demo
kubectl get deployments hello -n demo -o yaml
```

## Services

```sh
kubectl apply -f .\service.yaml -n demo
```

```sh
kubectl get services -n demo
kubectl describe services hello -n demo
kubectl get services hello -n demo -o yaml
```

```sh
kubectl port-forward -n demo service/hello 5000:80
```

[http://127.0.0.1:5000/](http://127.0.0.1:5000)

## Ingress

```sh
kubectl get ingress -n demo
```

```sh
kubectl get ingress -n demo
```

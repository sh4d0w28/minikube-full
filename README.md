## Run minikube

```sh
minikube start --memory=7923 --cpus=4 
```

## Deploy k8s pods
```sh
kubectl apply -f namespaces.yaml -f elastic.yaml -f kafka-ui.yaml -f kafka.yaml -f mysql.yaml -f postgres.yaml -f redis.yaml
```

## Proxy pods to local

```sh
minikube tunnel
```

```sh
kubectl exec -it elasticsearch-0 -n elastic -- ./bin/elasticsearch-setup-passwords interactive
```
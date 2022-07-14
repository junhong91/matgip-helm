## matgip helm chart

### 1. Create matgip namespace

```
$ kubectl create ns matgip
```

### 2. Use matgip namespace

```
$ kubectl config set-context --current --namespace=matgip
```

### 3. Make `tgz` file to install helm chart

```
$ tar czvf matgip-helm.tgz matgip-helm/
```

### 4. Install matgip helm chart

```
$ helm install matgip-service matgip-helm.tgz -f matgip-helm/values.yaml
```

### 5. Check all services are running

```
$ kubectl get all -n matgip
```

## Reference

[ingress guide](https://kubernetes.io/ko/docs/tasks/access-application-cluster/ingress-minikube/)

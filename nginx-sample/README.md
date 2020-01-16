## nginx-sample

```
$ cat cluster-config.yaml
$ kind create cluster --name sample --config cluster-config.yaml
$ kubectl config get-clusters
$ kubectl get nodes
$ docker ps
$ cat deployment.yaml
$ kubectl apply -f deployment.yaml
$ kubectl get deployments
$ kubectl get pods
$ docker images
$ docker exec -it sample-worker /bin/bash
# which docker
# which containerd
# ctr -n k8s.io images ls -q
$ cat cluster-config.yaml
$ cat service.yaml
$ kubectl apply -f service.yaml
$ kubectl get svc
$ curl localhost:8080
$ kind delete cluster --name sample
$ kubectl config get-clusters
$ docker ps -a
```

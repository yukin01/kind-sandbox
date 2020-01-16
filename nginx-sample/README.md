## nginx-sample

```
$ make create-cluster
$ make apply
$ docker images
$ docker exec -it sample-worker /bin/bash
# ctr -n k8s.io images ls -q "name~=nginx"
# ctr -n k8s.io containers ls "image~=nginx"
```

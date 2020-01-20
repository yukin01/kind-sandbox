CLUSTER_NAME=argocd-ha

.PHONY: create-cluster delete-cluster

create-cluster:
	kind create cluster --name $(CLUSTER_NAME) --config cluster-config.yaml

delete-cluster:
	kind delete cluster --name $(CLUSTER_NAME)

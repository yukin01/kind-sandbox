CLUSTER_NAME=argocd-demo

.PHONY: create delete

create:
	kind create cluster --name $(CLUSTER_NAME) --config cluster-config.yaml

delete:
	kind delete cluster --name $(CLUSTER_NAME)

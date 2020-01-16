CLUSTER_NAME=sample

.PHONY: create delete

create-cluster:
	kind create cluster --name $(CLUSTER_NAME) --config cluster-config.yaml

delete-cluster:
	kind delete cluster --name $(CLUSTER_NAME)

apply:
	kubectl apply -f deployment.yaml
	kubectl apply -f service.yaml

delete:
	kubectl delete -f deployment.yaml
	kubectl delete -f service.yaml

port-forward:
	kubectl port-forward $$(kubectl get pods -l app=nginx -o name) 3000:80

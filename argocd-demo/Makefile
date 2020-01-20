CLUSTER_NAME=argocd-demo

.PHONY: create-cluster delete-cluster build clean apply delete get-pod-name

create-cluster:
	kind create cluster --name $(CLUSTER_NAME) --config cluster-config.yaml

delete-cluster:
	kind delete cluster --name $(CLUSTER_NAME)

build:
	touch .output.yaml
	mv -f .output.yaml .output.old.yaml
	kubectl kustomize . > .output.yaml

clean:
	rm -f .output.yaml .output.old.yaml

apply:
	kubectl apply -k .

delete:
	kubectl delete -k .

get-pod-name:
	kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2

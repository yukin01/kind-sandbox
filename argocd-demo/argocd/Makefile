.PHONY: build clean apply delete get-pod-name

build:
	touch .output.yaml
	mv -f .output.yaml .output.old.yaml
	kustomize build . > .output.yaml

clean:
	rm -f .output.yaml .output.old.yaml

apply:
	kubectl apply -k .

delete:
	kubectl delete -k .

get-pod-name:
	kubectl get pods -n argocd -l app.kubernetes.io/name=argocd-server -o name | cut -d'/' -f 2
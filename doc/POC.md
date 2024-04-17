# Proof of Concept. ArgoCD

Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.

![argocd_arch](https://github.com/mykolapryvalov/AsciiArtify/blob/main/doc/img/argocd_arch.png)

## How it works

Argo CD follows the GitOps pattern of using Git repositories as the source of truth for defining the desired application state. Kubernetes manifests can be specified in several ways:

  -  kustomize applications
  -  helm charts
  -  jsonnet files
  -  Plain directory of YAML/json manifests
  -  Any custom config management tool configured as a config management plugin

Argo CD is implemented as a Kubernetes controller which continuously monitors running applications and compares the current, live state against the desired target state (as specified in the Git repo).

#
## Installation

Instal k3d from the source:
	    
	curl -s https://raw.githubusercontent.com/rancher/k3d/main/install.sh | bash

Setup K3D cluster:

	k3d cluster create argo-cluster

Create namespace for ArgoCD:

	kubectl create namespace argocd

Install ArgoCD:

	kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

Forward ArgoCD Server port to the localhost:

	kubectl port-forward svc/argocd-server -n argocd 8080:443

Get ArgoCD UI Admin Password:

	kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d

Enter the received password and login **admin** in the ArgoCD Web interface:

![argoCDWebUI](https://github.com/mykolapryvalov/AsciiArtify/blob/main/doc/img/argoCDWebUI.png)
 
	

  




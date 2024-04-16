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



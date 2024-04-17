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

vim Container
    
	FROM busybox
	CMD while true; do { echo -e 'HTTP/1.1 200 OK\n\nVersion: v1.0.0'; }|nc -vlp 8080;done
	EXPOSE 8080
 #   
	img build -t denvasyliev/demo:v1.0.0 -f Container .
	img unpack denvasyliev/demo:v1.0.0
	runc spec
	runc run demo
	vim config.json:
		terminal false
		"sh", "-c", "while true; do { echo -e 'HTTP/1.1 200 OK\n\nVersion: v1.0.0'; }|nc -vlp 8080;done"
		rootfs false
		"path": "/var/run/netns/runc"


  




# Introduction

AsciiArtify, a startup focused on developing a new software product for transforming images into ASCII art using Machine Learning, faces the challenge of selecting the right tool for local Kubernetes cluster development. The team, comprised of two young programmers with expertise in software development but lacking DevOps experience, is considering three options: minikube, kind and k3d.

# Characteristics

# Minikube

- Supported OS and Architectures: Works on multiple operating systems, including Windows, macOS, and Linux. Supports various architectures.
- Automation Capability: Offers automation for cluster creation and management.
- Additional Features: Suitable for local development and testing. Concerns arise regarding scalability limitations.

# Kind (Kubernetes IN Docker)

- Supported OS and Architectures: Compatible with Windows, macOS, and Linux. Works within Docker containers.
- Automation Capability: Allows the creation of local Kubernetes clusters in Docker containers.
- Additional Features: Considered for local testing purposes.

# k3d

- Supported OS and Architectures: Works on multiple operating systems. Uses Rancher Kubernetes Engine (RKE) in Docker containers.
- Automation Capability: Facilitates quick creation and testing of Kubernetes clusters in Docker containers.
- Additional Features: Chosen for preparing Proof of Concept (PoC).

# Advantages and disadvantages

| Pros and Cons  |	Minikube   	   |     Kind           |     k3d        |    Podman      |
|:--------------:|:---------------:|:------------------:|:--------------:|:--------------:|
| Pros           |+ Easy to use    |+ Suitable for local|                |                |
|:--------------:|:---------------:|:------------------:|:--------------:|:--------------:|
|                | + Suitable for  |            |                |                |
   




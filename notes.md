# Notes

## Setup

Install the software and tools needed in the following order. These instructions are for Cubbli / Ubuntu.

1. install [Docker](https://docs.docker.com/get-docker)
2. install [kubectl](https://kubernetes.io/docs/tasks/tools)
   - run `snap install kubectl --classic`
   - installed version must be within one minor version of the cluster
   - latest compatible version is recommended
3. install [k3d](https://github.com/k3d-io/k3d#get)
   - run `wget -q -O - https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash`
   - requirements: `docker` and `kubectl`
   - in case of missing permissions, run `sudo chmod 755 /usr/local/bin/k3d`

## Part 1

### First Deploy

- _microservices_
  - small, autonomous services that work together
  - reasons to use
    - zero-downtime independent deployability
    - isolation of data and of processing around that data
    - use microservices to reflect the organizational structure
- Kubernetes
  - K8s for short
  - open-source
  - container orchestration system
  - used for automating deployment, scaling, and management of containerized applications
  - networking between containers and health monitoring
- K3s
  - a lightweight Kubernetes distribution
- _clusters_
  - a group of machines or _nodes_ working together form a cluster
  - can be of any size, anywhere from one machine up to 5000
  - the _control plane_ exposes interfaces to control other components
  - _server nodes_ are have control plane, _agent nodes_ do not

## Vocabulary

| term          | definition                                                                        |
| :------------ | :-------------------------------------------------------------------------------- |
| agent node    | a node without control plane                                                      |
| cluster       | a group of (1 to 5000) machines or nodes working together                         |
| container     | a standardized, repeatable unit of code and its dependencies                      |
| control plane | a layer exposing the API and interfaces for managing containers                   |
| K3s           | a lightweight Kubernetes distribution                                             |
| K8s           | short for Kubernetes                                                              |
| Kubernetes    | a system for automating deployment, scaling, and management of containerized apps |
| microservice  | a small, autonomous service that works together with other microservices          |
| monolith      | a self-contained and independent service, opposite of microservice                |
| node          | a machine or a server                                                             |
| server node   | a node with control plane                                                         |

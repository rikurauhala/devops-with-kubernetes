# Notes

## Setup

1. install [Docker](https://docs.docker.com/get-docker)
2. install [kubectl](https://kubernetes.io/docs/tasks/tools)
   - on Ubuntu: `snap install kubectl --classic`
   - installed version must be within one minor version of the cluster
   - latest compatible version is recommended
3. install [k3d](https://github.com/k3d-io/k3d#get)
   - on Ubuntu: `wget -q -O - https://raw.githubusercontent.com/k3d-io/k3d/main/install.sh | bash`
   - requirements: `docker` and `kubectl`

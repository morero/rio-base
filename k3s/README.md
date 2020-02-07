# K3S

Local K3S server for development. Will start a K3S server and a K3S agent running in docker, locally

Requirements: 
 - direnv, OR set the K3S_TOKEN environment variable
 - docker
 - docker-compose

Run:
docker-compose up -d

## Install RIO
rio install (uses direnv to read the KUBECONFIG env variable in this directory)

# Using K3D instead:
k3d create --api-port localhost:6444 --publish 8080:80 --server-arg --tls-san="127.0.0.1" 

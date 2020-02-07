# Glesys K3S Kluster

## requirements

Install server with df user and ssh key

Server needs to have docker and curl installed:
sudo apt-get update && sudo apt-get upgrade
sudo apt-get install -y docker.io
sudo usermod -aG docker df

K3SUP: 
curl -sLS https://get.k3sup.dev | sh
sudo install k3sup /usr/local/bin/

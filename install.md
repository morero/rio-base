# Installation

## Manual Steps

### Create a ssh key to use

### Install servers (2)
- Create a VPS (ex. Glesys)
- Add your public ssh key (from step above) to ~/.ssh/authorized_keys (or paste it in ssh key in Glesys)
- Install curl: (sudo apt-get install -y curl)
- SSH to the machine from and approve host key

### Install k3s on master node
k3sup install --user df --ip <your master node ip> --ssh-key ~/.ssh/<your private key name>_rsa --k3s-extra-args '--no-deploy traefik'

### Install k3s on worker node
k3sup join --user df --server-ip <your master node ip> --ip <your worker node ip> --ssh-key ~/.ssh/<your private key name>_rsa

### Install Rio
rio install --email <your email>

### Deploy your workloads
rio up

### Point your public domain towards your rio rdns
rio info (check the dns name with on-rio in it)
CNAME *rio.example.com -> <dns name above>

### Point a public domain to a route
rio domain register route/svelte-example


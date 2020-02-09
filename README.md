# DF

## Getting started

### Local Environment
cd k3s/ and follow the README.md

### Remote environment
TBD

### RIO
Install the rio cli client
curl -sfL https://get.rio.io | sh -

Assume that RIO agent is installed in the cluster you want to use

# rio-base
# rio-base


## Using a custom domain
Easiest is to use a CNAME to the cluster domain (see rio info)
Then you need to connect to public domain to a route:
$ rio domain register  df.forked.se router/svelte-example

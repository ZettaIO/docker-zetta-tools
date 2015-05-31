# Zetta Tools

Zetta.io is an Openstack based cloud provider. The images has a number of tools installed to interact with the 
Zetta.io cloud. 

## Authentication

You authenticate to Zetta.io with a domain, username, and password. You should define them in a .sh file
```
ZETTA_DOMAIN_NAME=<your domain name>
ZETTA_DOMAIN_ID=<your domain id>
ZETTA_USERNAME=<your username>
ZETTA_PASSWORD=<your password>
ZETTA_PROJECT=<your project>  # Optional, if not defined it defaults to 'Standard'
```

This file should be in a directory that is bound during container creation.

## Volume Bindings

The entrypoint of the image sources all *.sh files in /config. You should bind this directory to a directory with your customization files. At tlease the authentication parameter should be defined.

You might consider binding /root/.docker/machine where docker-machine stores its data

# Basic Shit #

## Dev v. Production ##
production runs on `3334`  
/dev/ty runs on `3333`  
/dev/alan runs on `3335`  
view logs: `docker-compose logs -f --tail=0`  

### Dev ###

## Updating Production Instance ##
Updating Docker instance  
`docker-compose exec proxy /bin/bash`
`nginx -s reload`  

Updating system-wide instance  
`sudo service nginx restart`

## See what services... ##
`service --status-all`

## What Kernel? ##
`uname -a`

## Preview a file ##
`cat filename`

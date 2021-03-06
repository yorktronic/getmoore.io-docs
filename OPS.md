# Basic Shit #

## Dev v. Production ##
production runs on `3334`  
/dev/ty runs on `3333`  
/dev/alan runs on `3335`  
view logs: `docker-compose logs -f --tail=0`  

### Dev ###
Setting it up. Start with following rapid-service-template [README](https://github.com/whilesoftware/rapid-service-template/blob/master/README.md)  
Pick your port (see above)  
Can probably skip step 6  
edit `node/static/index.html` and `node/static/js/main.js` to include updated development paths  


## Updating Production Instance ##
Updating Docker nginx instance (web1, web2, tydev, alandev)  
`docker-compose exec proxy /bin/bash`  
`nginx -s reload`  

Updating system-wide nginx instance  
`sudo service nginx reload`

## See what services... ##
`service --status-all`

## What Kernel? ##
`uname -a`

## Preview a file ##
`cat filename`
`docker-compose ps`

## Ports ##
ssh = 22  
http = 80  
https = 443  

## Cheapest ##
JSON-formatted data by "offers," timestamped and updated with some frequency  

## Logs ##
`tail -F` vs `tail -f` vs `tailf`  
docker-compose logs  
docker-compose logs -f  
docker-compose logs -f --tail=0

## token ##
`var data = JSON.parse(responseBody);`
`postman.setEnvironmentVariable("token", data.token);`

## curl ##
`-v` - verbose?
get poopy man's auth token: `curl -H "Content-Type: application/json" -X POST -d '{"username":"poopy","password":"man"}' https://getmoore.io/dev/alan/api/login`  
get poopy man's auth token (via http instead of https): `curl -H "Content-Type: application/json" -X POST -d '{"username":"poopy","password":"man"}' http://localhost:3335/api/login`  

## other ##
`nc` - netcat  

## mongo shell ##
ref: https://docs.mongodb.com/manual/reference/mongo-shell/  
`show dbs`  
`use x`  
`show collections`  


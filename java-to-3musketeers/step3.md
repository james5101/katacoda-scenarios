Now that we have a running application, lets try and add docker-compose it. This will help us consitently run our app across any infra.

## Task


## Task
Lets build it!
`docker-compose up -d`{{execute}}

## Task 
Test it!

`curl localhost:8080`{{execute "T2"}}

## Task
Kill everything and remove images

`docker-compose down`{{execute}}
`docker rmi -f $(docker images -a -q)`{{execute}}
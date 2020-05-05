Musketeer 3 - Docker-Compose
Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration.

## Task
Lets update our project to use docker-compose. First thing we need to do is to add a docker-compose.yml file. Lets create a docker-compose.yml file in the editor or by clicking the text below.
`touch docker-compose.yml`{{execute}}

## Task
The next thing we must do is to load up our docker-compose.yml file. Lets keep it simple and add 1 service. Lets add a service of 'alpine' that pulls down the alpine image. Add the following code to the docker-compose.yml file. 
```
version: '3'
services:
  alpine:
    image: alpine
```

## Task
Next up, we have to update our Makefile receipe to call docker-compose instead of docker. Open up the Makefile and update the receipe to the following:
```
echo:
	docker-compose run --rm alpine echo 'Hello, World!'
```

## Task
Finally, let's run our make target. Either type ```make echo``` in the terminal or click the following:
`make echo`{{execute}}
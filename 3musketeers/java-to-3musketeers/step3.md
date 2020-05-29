Compose is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services (and their dependencies) from your configuration. In 3 Musketeers, it also simplifies our Makefiles. For more in depth information on docker-compose, visit the website https://docs.docker.com/compose/

Our next task will be to add docker-compose. In order to do this we need a docker-compose.yml file. We will keep this file rather simple. If you open the `docker-compose.yml`{{open}}, you will see we have a service named ```javaspring```. Under ```javaspring``` we have a build section (which builds our dockerfile,an image section (which tags our image) and a ports section (which tells us what port to open on the host and container respectivley)

## Task
We can use compose to orchestrate the build and run of our container with the 1 command

`docker-compose up -d`{{execute}}

This command is a lot cleaner than using the regular docker build and docker run commands. Docker-Compose allows us to declartivley run our containers by setting their configurations in the docker-compose.yml file. 

## Task 
Let's try and hit our endpoint. 

`curl localhost:8080`{{execute T2}}

## Task
Docker-Compose will also do a bit of clean up for us with the ```down``` flag. It will stop and remove any items created by the ```up``` flag. 

`docker-compose down --rmi all`{{execute}}
`docker rmi -f $(docker images -a -q)`{{execute}}
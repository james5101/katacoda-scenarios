Now that we have a running application, lets try and dockerize it. This will help us consitently run our app across any infra.

## Task
Let's open the `Dockerfile`{{open}} and take a look at whats going on. It's a rather simple Dockerfile in that it simply:
1. Pulls down the openjdk base image
2. Copies our current directory into /app on the container
3. Sets a working dir to /app
4. Makes the gradle wrapper executable
5. Runs a few gradle tasks that generate a jar file.
6. Moves that jar file
7. Finally, execute the jar file. 

## Task
Lets build it!
`docker build -t javaspring-docker .`{{execute}}


## Task
Lets run it!
`docker run -p 8080:8080 javaspring-docker`{{execute}}

## Task 
Test it!

`curl localhost:8080`{{execute "T2"}}

## Task
Kill everything and remove images

`docker rm -f $(docker ps -a -q)`{{execute}}
`docker rmi -f $(docker images -a -q)`{{execute}}
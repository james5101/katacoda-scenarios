Containers offer a logical packaging mechanism in which applications can be abstracted from the environment in which they actually run. This decoupling allows container-based applications to be deployed easily and consistently, regardless of whether the target environment is a private data center, the public cloud, or even a developer’s personal laptop. This gives developers the ability to create predictable environments that are isolated from the rest of the applications and can be run anywhere. For more in depth information on docker,please visit their website at https://www.docker.com/

## Task
Let's open the `Dockerfile`{{open}} and take a look at whats going on. It's a rather simple Dockerfile in that it simply:
1. Pulls down the openjdk base image
2. Copies our current directory into /app on the container
3. Sets a working dir to /app
4. Makes the gradle wrapper executable
5. Runs a few gradle tasks that generate a jar file
6. Moves that jar file
7. Finally, execute the jar file

## Task
Lets build it!
`docker build -t javaspring-docker .`{{execute T1}}


## Task
Lets run it!
`docker run -p 8080:8080 javaspring-docker`{{execute T1}}

## Task 
Test it!

`curl localhost:8080`{{execute T3}}

## Task
Kill everything and remove images

`docker rm -f $(docker ps -a -q)`{{execute T1}}
`docker rmi -f $(docker images -a -q)`{{execute T1}}
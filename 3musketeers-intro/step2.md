Musketeer 2 - Docker
Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. We can stack up different docker commands into make targets and orchestrate those different steps to help us acheive our desired outcome. In this section we will cover running a docker container from a make target with a simple Hello World example.

## Task 
Lets update our Makefile target name and receipe to call docker run. We will pull and run a simple alpine image and pass it the command echo 'Hello World'

Musketeer 2 - Docker
Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. We can stack up different docker commands into make targets and orchestrate those different steps to help us acheive our desired outcome. In this section we will cover running a docker container from a make target with a simple Hello World example.

## Task 
Lets update our Makefile receipe to call docker run. We will pull and run a simple alpine image and pass it the command echo 'Hello World'
Our echo target should now look like the following snippet:
```
echo:
	docker run --rm alpine echo 'Hello, World!'
```

## Task
Finally, lets run make echo again and see our results. Either type ```make echo``` in the terminal or click the following:
`make echo`{{execute}}
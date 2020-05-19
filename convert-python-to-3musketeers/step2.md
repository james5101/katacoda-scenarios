Containers offer a logical packaging mechanism in which applications can be abstracted from the environment in which they actually run. This decoupling allows container-based applications to be deployed easily and consistently, regardless of whether the target environment is a private data center, the public cloud, or even a developer’s personal laptop. This gives developers the ability to create predictable environments that are isolated from the rest of the applications and can be run anywhere.

## Task
Lets open the Dockerfile `Dockerfile`{{open}} and take a look at whats going on. We have a pretty simple dockerfile that pulls down a base python image. 

## Task
For the next task let's add a few lines that will add our script to the root of the image and then execute that script. 
*TIP-If you are stuck with what to add to the Dockerfile there is a "Show Solution" button at the bottom the scenario.*

## Task
After we edit the Dockerfile, let's try to build our image.

`docker build -t printvar .`{{execute}}

Next let's see if our image was created sucesfully.

`docker images`{{execute}}

We should see an image with a tag of printvar:latest. Excellent

## Task
Lastly let's run our image and see our output.

`docker run printvar`{{execute}}

We should see some output, but we see `None` for the variable we want. When we use the docker run command we can pass a flag of -e to pass the container a variable, lets try that now. 

`docker run -e DOG=POODLE printvar`{{execute}}

As you can imagine, if we had multiple environment variables, volume mounts, args, etc. that we had to pass to our container, that docker run command could get long and ugly. Lucky for us, docker-compose exists!!
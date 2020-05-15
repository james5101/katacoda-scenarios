Containers offer a logical packaging mechanism in which applications can be abstracted from the environment in which they actually run. This decoupling allows container-based applications to be deployed easily and consistently, regardless of whether the target environment is a private data center, the public cloud, or even a developer’s personal laptop. This gives developers the ability to create predictable environments that are isolated from the rest of the applications and can be run anywhere.

## Task
Lets open the Dockerfile and take a look at whats going on. We have a pretty simple dockerfile that pulls down a python image, adds out script to it then runs that script. 

Lets try to build our image.
`docker build -t printvar .
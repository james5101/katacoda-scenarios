Make is a build automation tool that automatically builds programs and runs commands via the same interface. Make is installed on all distros of Unix/Linux operating systems. It is also available on Windows operating systems as well. Make obtains all its knowledge of how to build the program from a file called the ```Makefile```. This file contains ```targets``` that can be executed.

Makefiles can be as simple or complex as you like. The key to a good Makefile is a clean one. Lets open the Makefile and walk through whats going on. 

## Task
Our first target in our Makefile is a ```help``` target. This target will scan the Makefile and look for any text that comes after a ```##```. We can create self documenting Makefiles using this convention. Lets run the following command to see what our help looks like.
`make help`{{execute}}

## Task
Let's try and build our image via docker-compose and make. If you take a look at target named ```build```. You will see we have the same command as the previous scenario. We simply wrap that command into a make target and then call that target

`make build`{{execute}}
Make is a build automation tool that automatically builds programs and runs commands via the same interface. Make is installed on all distros of Unix/Linux operating systems. It is also available on Windows operating systems as well. Make obtains all its knowledge of how to build the program from a file called the ```Makefile```. This file contains ```targets``` that can be executed. For more in depth information on make go to the website https://www.gnu.org/software/make/manual/make.html

## Task
Let's open the `Makefile`{{open}} and take a look around. First let's go through the some of the basic layout of the Makefile. At the top you will see line 1 ```DOCKER_COMPOSE ?= docker-compose```. This line is simply setting a variable of DOCKER_COMPOSE to the docker-compose binary. 
*Note: if you are interested in why we use ?= visit https://www.gnu.org/software/make/manual/html_node/Flavors.html#Flavors to see the different ways of setting a variable*


Let's move down the file until we get to our help target. We start off our first target with a ```.PHONY```. What does this mean? Pretty much make works on a file based system. PHONY means run this target even if there is a file named ```help``` in the directory. 
*Note: For more information visit https://www.gnu.org/software/make/manual/html_node/Phony-Targets.html. Note: this ```.PHONY``` could also be put at the top of the file, I put it here to make the file look cleaner.*

Next, we we declare our first target. We named this first target ```help```. This is the name that we will call when we want to run this target. You will also see a line that seems to be commented out with ```##```. This will make more sense in a minute. 

Ok, after we define the name of our target. We want to create our ```recipe```. Recipe is just a fancy name for the commands we would like our target to perform. In the case of the ```help``` target, its a grep and sed of our Makefile. This line simply scans our Makefile and parses it for anything that comes after a ```##``` and displays that to the screen. 
*Note: Each recipe in a target is performed in a separate shell*

Ok, now that we have a better understanding of how the Makefile is laid out, let's try and run our ```help target```. In order to run our target we just need to execute the following:

`make help`{{execute T1}}

## Task 
Run it!
`make up-compose`{{execute T1}}


## Task
Test it
`curl localhost:8080`{{execute T3}}

## Task
Kill everything and remove images

`make down-compose`{{execute T1}}
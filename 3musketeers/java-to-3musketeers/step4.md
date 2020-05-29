Make is a build automation tool that automatically builds programs and runs commands via the same interface. Make is installed on all distros of Unix/Linux operating systems. It is also available on Windows operating systems as well. Make obtains all its knowledge of how to build the program from a file called the ```Makefile```. This file contains ```targets``` that can be executed. For more in depth information on make go to the website https://www.gnu.org/software/make/manual/make.html

## Task
Lets build it!
`make build`{{execute T1}}

## Task 
Run it!
`make up-compose`{{execute T1}}


## Task
Test it
`curl localhost:8080`{{execute T3}}

## Task
Kill everything and remove images

`make down-compose`{{execute T1}}
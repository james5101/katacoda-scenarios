Often there are many environment variables and having them in a .env file becomes handy. Docker and Compose do use environment variables file to pass the variables to the containers. A env.template file will provide some help when managing env variables in a project. This file is meant to be the template for our environment variables, we should not update env variables in this file, rather if we excepect new env vars we can add them to this list. 

## Task
Let's add some variable that we would like to later define inside the the env.template file. 

`echo hello`{{execute}}

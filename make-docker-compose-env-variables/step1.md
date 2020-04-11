Often there are many environment variables and having them in a .env file becomes handy. An env.template file will provide some help when managing env variables that are expected inside a container. This file is meant to be the template for our environment variables, we should not update env variables in this file, rather if we excpect new env vars we can add them to this list. 

## Task
Let's take a look at the env.template file. Suppose we have a container that accepts 3 env variables in order to run correctly. We simply add those keys into the env.template file. 

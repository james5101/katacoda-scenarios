Lets review the python script. It is a simple python script that prints some text to stdout. 
In line 1, we import the os package. Next, we create a variable called 'text' and set it to the value of the environment variable TEXT, and then lastly print that to the scren.

## Task
Lets try and run this application. The first thing we need to do is set the environment variable TEXT.
`export TEXT=DOG`{{execute}}

After we set the environment variable lets run that script. 
`python3 helloworld.py`{{execute}}
Lets review the python script  `printvar.py`{{open}}. It is a simple python script that prints some text to stdout. 
In line 1, we import the os package. Next, we create a variable called 'dog' and set it to the value of the environment variable DOG, and then lastly print a line to the scren.

## Task
Lets try and run this application. The first thing we need to do is set the environment variable DOG.

`export DOG=POODLE`{{execute}}

After we set the environment variable lets run that script.

`python printvar.py`{{execute}}

If everything went well we should see some output on the screen. CONGRATS!

So now that we have a working script, how do we distribute the script so that everyone can run it the same way everytime without having to install all of the dependencies? DOCKER!!!
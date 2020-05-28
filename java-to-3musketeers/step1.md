Lets review the java project. It is a simple java springboot application that displays ```Greetings from Spring Boot!``` when ran. At the top level we have all our supporting files from our gradle configuration down to the source code which is housed inside the ```src``` folder. Let's try and run this the old fashioned way with gradle directly from the terminal. 

## Task
We will be building the jars today with gradle. The first step we need to perform is to build the jar. We will run the following command to genreate a jar.

`chmod u+x ./gradlew`{{execute}}

`./gradlew bootJar`{{execute}}


After this gradle task completes we should have a jar file locatated under build/libs.

`ls build/libs/`{{execute}}

After its built and you see the jar, lets try and run it. 

`java -jar build/libs/demo-0.0.1-SNAPSHOT.jar`{{execute}}

After we run this lets open another terminal inside Katacoda and try and hit the endpoint:

`curl localhost:8080`{{exceute}}

And just like that we have a running sprint boot app! Now onto the fun stuff, Docker!
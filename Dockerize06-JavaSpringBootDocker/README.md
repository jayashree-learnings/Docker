### Dockerize java-springboot application

In this exercise, the community edition of 'intellij IDEA' ide is used to build a basic web page. Since the community edition does not support the spring boot application, a basic sample project structure of a spring boot application is created from the website "https://start.spring.io/". In the first step, the application is tested on the local host successfully. In the second step, it is dockerized and run and the web pages are accessed. 

1)Running java-springboot application on localhost  

1) A basic structure of the project was created from the above website and the same was imported to the intellij idea IDE.

2) The default template consisted of the  class with the annotation "@SpringBootApplication" containing the main method.Another "@RestController" annotated class with a method annotated with "@GetMapping" was created . This method prints the required message.
##### ![00](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/00_basicTemplate.PNG)
##### ![01](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/01_folderStructure.PNG) 

3) The main class was run and by default the embedded apache tomcat runs on a default port number:8080. In the browser, give the url as 'localhost:8080/welcome' and it displays the message. Here "/welcome" is the url given to the "@GetMapping" annotation.
##### ![02](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/02_WelcomeMessage.PNG)  

2)Running java-springboot application  using docker

1) To dockerize a SpringBoot application, a .jar file is required. For the same purpose, run the "maven install" and it creates a .jar file in the target directory.
##### ![03](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/03_mavenbuild.PNG)  

2) In the project folder , create the Dockerfile.
##### ![04](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/04_Dockerfile.PNG)  

3) Install the docker desktop in the local machine.  

4) In the command prompt of the local machine(Windows OS), run the commands to build the image and run it to create a container.While running the image, map an appropriate localhost-portnumber(eg-8002) to the default container prt number of 8080.
##### ![05](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/05_buildAndListImage.PNG)
##### ![06](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/06_runImageAndPortMapping.PNG)  

5) In the  browser, give the url as localhost:8002/welcome because that is the port number which is now mapped to our local system.
##### ![07](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d06/07_portmapping.PNG)
















### Dockerize java script 

In this exercise, the alpine distro version of 'play with docker' is used as the linux flavour.In the first step, java is installed and a simple script is executed in the 'play with docker' host and tested successfully. In the second step, it is dockerized and tested.

part1 - Testing in localhost  

1) update and upgrade apk packages. Install openjdk8 and check the version
##### ![01](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/01_addjdk.PNG)
##### ![02](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/02_checkVersion.PNG)  

2) make a project directory 
   mkdir HelloTestProj  

3) navigate to it and create HelloWorld.java file using vim command.  

4) verify the contents using 
    cat HelloWorld.java 
##### ![03](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/03_catHelloWorldjava-version1.PNG) 

5) compile using 'javac HelloWorld.java'  

6) Execute the program using 'java HelloWorld'. The statements will be printed to the console
##### ![04](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/04_executionin%20LocalHost.PNG)  

Part2 - Running HelloWorld using docker  

1) In the same folder create Dockerfile
##### ![00](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/00_fileStucture.PNG)  

2) verify the contents using cat command
##### ![05](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/05_Dockerfile.PNG)  

3) build image using 
     docker build -t test-helloworld:01 .  

4) verify using the command 'docker images'.
we can see that an image of the given name is created with an id.  

5) run the image using the command
      docker run <imagename or first 3 characters of id>  

6) The output is printed
##### ![06](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/06_buildAndRunImage.PNG)  

7) check the containers using 
    docker ps -a 
    docker ps -q
We can see that container  has exited immediately after the execution of the program  

8) Now modify the file HelloWorld.java
##### ![07](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/07_appendedJavaFile.PNG)  

9) build a new image with the tag 02 meaning its the second version.  

10) run the image and we can see the modified output of the java program.
##### ![08](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d05/08_modifiedContainer.PNG)




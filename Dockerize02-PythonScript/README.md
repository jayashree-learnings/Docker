### Dockerize python script 

In this exercise, the alpine distro version of 'play with docker' is used as the linux flavour.In the first step, python is installed and a simple script is executed in the 'play with doker' host and tested successfully. In the second step, it is dockerized and tested.

1)part1- Testing in localhost  

1) update and upgrade apk packages. Install python3 and check the version.
##### ![01a](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/01a_addPythonAndVerify.PNG)
##### ![01b](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/01b_pythonVersion.PNG)  

2) create a working directory for the project using 'mkdir testProj'  

3) navigate to it and create helloWorld.py file using vim command.  

4) Execute the program using 'python3 helloWorld.py'. It displays the print statements
##### ![02](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/02_localHostProjExecution.PNG)

2)part2- dockerizing python script

1) In the same folder create Dockerfile  

2) verify the contents using cat command
##### ![03](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/03_Dockerfile.PNG)  

3) build image using 'docker build -t dockerhellotest:01 .'
##### ![04](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/04_buildImage.PNG)  

4) verify using the command 'docker images'.we can see that an image of the given name is created with an id.  

5) run the image using the command
      docker run <imagename or first 3 characters of id>  

6) The output of the two print statements is displayed  

7) check the containers using 
    'docker ps -a or 
    docker ps -q'
We can see that container  has exited immediately after the execution of the program
##### ![05](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/05_runImage.PNG)  

8) Now modify the file helloWorld.py
##### ![06](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/06_editedPythonfile.PNG)  

9) build a new image with the tag 02 meaning its the second version.  

10) run the image and we can see the modified ouput of the python parogram.
##### ![07](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d02/07_newContainer.PNG)





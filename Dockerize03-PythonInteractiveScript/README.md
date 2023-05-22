### Dockerize an interactive python script  

In this exercise, the alpine distro version of 'play with docker' is used as the linux flavour.In the first step, python is installed and an interactive python script which takes two numbers and returning the result after performing four arithmetic operation is executed and tested successfully. In the second step, it is dockerized and tested.

1)part1- Testing in localhost  

1) update and upgrade apk packages. Install python3 
##### ![01](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d03/01_pyVersion.PNG) 

2) create a working directory for the project using 'mkdir testProj'  

3) navigate to it and create numbers.py file using vim command.  
##### ![02](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d03/02_catnumbersFile.PNG)

4) Execute the program using 'python3 numbers.py' just to ensure that it works properly 

2)part2- dockerizing python script

1) In the same folder create Dockerfile 
##### ![00](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d03/00.PNG) 

2) verify the contents using cat command
##### ![03](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d03/03_dockerFile.PNG)  

3) build image using 
     docker build -t img2 .
4) verify using the command
     docker images
we can see that an image of the given name is created with an id.
##### ![04](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d03/04_dockerBuild.PNG)  

5) run the image in interative mode using the command
      docker run -it <imagename or first 3 characters of id>  
  
6) The program will take the inputs from the user and display appropriate results
##### ![05](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d03/05_dockerRunInteractivemode.PNG)









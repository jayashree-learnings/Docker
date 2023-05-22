### Dockerize apache2 php image  

In this exercise, the alpine distro version of 'play with docker' is used as the linux flavour.In the first step, apache2 and php are installed in the local host and tested successfully. In the second step, it is dockerized and tested.

1)part1- Testing in localhost
1) update and upgrade apk packages
2) install php8-apache2 and apache2 on alpine linux (play with docker) and verify that its up and running.
3) create info.php and index3.html in /var/www/localhost/htdocs and verify that the webpages can be accessed. 
##### ![02](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/02-index3html-infophp.PNG)
4) start the apache2 service and verify that index.html,info.php and index3.html are displayed properly

2)part2- dockerizing

5) copy the info.php and index3.html to the current location and use ls command to see them 
##### ![03](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/03_Index3htmlInfoPhpDockerInPWD.PNG)  

6) create the docker file in the current directory  

7) in the Dockerfile give the copy command to copy these two files from the current location to /var/www/localhost/htdocs in the container
##### ![04](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/04_Dockerfile.PNG)  

8) build the image
##### ![05](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/05_buildimage.PNG)  

9) run the image by configuring the appropriate ports(here the port 80 in the container is mapped to port 85 of play with docker)
##### ![06](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/06_runImageatPort85.PNG)  

10) verify that all the 3 pages are displayed properly by opening port 85 at play with docker.
##### ![07](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/07_ItWorks.PNG)
##### ![08](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/08_phpinfo.PNG)
##### ![09](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d01/09_index3html.PNG)







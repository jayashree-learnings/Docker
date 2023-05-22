### Dockerize python-flask application

using pycharm as the IDE, a basic python flask application is created in the local host and the web page successfully accessed. In the second step, the flask application is dockerized.

1)Running PythonFlaskApplication on localhost

1) Create a new conda/virtual environment for the project in the Pycharm IDE.Specify the python version

2) Use 'pip install flask' in the pycharm terminal and in the main.py, specify basic flask methods and routes appropriately.
##### ![01](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/01_main-py.PNG)  

3) Run the main.py  

4) In the browser, specify the url as localhost:5000 (5000 is the default port number for flask). Access both the web pages
##### ![02a](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/02a-helloworld.PNG)
##### ![02b](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/02b_loginpage.PNG)  

2)Running PythonFlaskApplication using docker

1) In the main.py give localhost = '0.0.0.0'  
##### ![03a](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/03a_SpecifyLocalHost.PNG)

2) Create a requirements.txt file using the command(in the pycharm terminal) 'pip freeze > requirements.txt'. It will have all the dependencies in it.
##### ![03b](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/03b_requirement.PNG)    

3) Create the Dockerfile in the same project folder.
##### ![03c](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/03c_Dockerfile.PNG)  
 

4) Build and run the image .While running the image map, the localhost port number to the container port number address.
##### ![04a](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/04a_buildImage.PNG)
##### ![04b](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/04b_runImage.PNG)

5) Access the webpages by giving ip address and port number of the local host correctly.
##### ![05a](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/05a_hellomsg.PNG)
##### ![05b](https://github.com/jayashree-learnings/Docker/blob/main/00_includes/d04/05b_loginPage.PNG)















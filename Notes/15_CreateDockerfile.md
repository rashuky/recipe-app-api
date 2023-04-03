# Creating a dockerfile

## Construction of dockerfile
Steps that docker need to build our image:

1. Define the name of the image that we are going to base our image on. We will build on top of that image. Different version of the images are listed on hub.docker.com
2. Next we define maintainer. It can be your name
3. `ENV PYTHONUNBUFFERED 1` we want to see the logs immediatly. Without any delay
4. Next we copy python requirements and the app from our local environemnt to the docker image.
5. Define working directory. Default directory where our commands will be run
6. We expose port to allow the port on the contianer and via this connect to the server
7. Next we run a couple of command. In one run block to not create a separate image layer for each command. This will keep our image more lightweight. It is possible by ussing `&& \` syntax. 
    - One of the command removes `/tmp` directory. This is to keep the image lightweight this folder is no longer needed as all the req. were installed.
    - The last command adds new user in the docker image. It is the best practice to not use root user. Cause it is dengarous.
8. `ENV` updates the environment variable. We add new path to the PATH
9. `USER` we specify user to switch to. 

## Creating .dockerignore

The file listing files that wont be included in the docker context.

### python file
If we wouldn't exclude the python files containing the cache they might confilict with docker apline environment
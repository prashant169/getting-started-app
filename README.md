# Getting started
Get the app
This repository is a sample application for users following the getting started guide at https://docs.docker.com/get-started/.
Get Started with Docker .Docker Playground - Play with Docker DockerPlayground :  

Before you can run the application, you need to get the application source code onto your machine.
Use following command.
1) Clone ➖https://github.com/prashant169/getting-started-app.git
   
Make sure you're in the getting-started-app directory.
2) cd /path/to/getting-started-app

3) cd /path/to/getting-started-app

3)Create an empty file named Dockerfile.

    touch Dockerfile
    
5) Using a text editor or code editor, add the following contents to the Dockerfile:
   
    vim Dockerfile
7)
   #syntax=docker/dockerfile:1
   FROM node:18-alpine
   WORKDIR /app
   COPY . .
   RUN yarn install --production
   CMD ["node", "src/index.js"]
   EXPOSE 3000
  
9) wq!     (exit frome vi editor)
    
11) Build the image using the following commands:
    docker build -t getting-started .
    
8)Run the application in a container using the docker run command.
    docker run -dp  3000:3000 getting-started
    
9)Run the following docker ps command in a terminal to list your containers.
   docker ps

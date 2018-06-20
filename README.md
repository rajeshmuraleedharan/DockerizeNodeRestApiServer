# DockerizeNodeRestApiServer
running fake rest api server in docker using node

The goal of this example is to show you how to create a REST api server using Express.Js framework into a Docker container.

Note: I have used Visual Studio Code to build this

# Step 1
Create a package.json file that describes your app and its dependencies
![alt text](https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/images/package.png)

https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/package.json

# Step 2
create a server.js file that defines a web app using the Express.js framework
![alt text](https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/images/serverjs.PNG)

https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/server.js

now you can test your fake rest api server from CMD. Open CMD window from sorce folder. 

. Run command "npm install"

. Run "node server.js"

browse http://localhost:8080 url from your browser or "curl -i localhost:49160" from command line.

# Step 3
Create a Dockerfile

![alt text](https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/images/dockerfile.PNG)

https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/Dockerfile

Create a .dockerignore file
https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/.dockerignore

# Step 4
Building docker image
docker build -t <your docker hub username>/<image name and tag>
docker build -f Dockerfile --no-cache . -t rajeshmuraleedharan/dockerizenoderestapiserver:v1
  
# Step 5
Run the image
docker run -p 49160:8080 -d rajeshmuraleedharan/dockerizenoderestapiserver:v1

Open a web browser and navigate to http://localhost:49160

# Step 6 (optional)
Push docker image to docker hub
docker push rajeshmuraleedharan/dockerizenoderestapiserver:v1

https://hub.docker.com/r/rajeshmuraleedharan/dockerizenoderestapiserver/


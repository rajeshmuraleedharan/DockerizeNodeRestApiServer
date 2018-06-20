# DockerizeNodeRestApiServer
running fake rest api server in docker using node

The goal of this example is to show you how to create a REST api server using Node.js into a Docker container.

Note: I have used Visual Studio Code to build this

Step 1
Create a package.json file that describes your app and its dependencies

{
  "name": "dockerize-node-restapi-server",
  "version": "1.0.0",
  "description": "Node.js on Docker",
  "author": "Rajesh Muraleedharan",
  "main": "server.js",
  "scripts": {
    "start": "node server.js"
  },
  "dependencies": {
    "express": "^4.16.3"
  }
}

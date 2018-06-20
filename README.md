# DockerizeNodeRestApiServer
running fake rest api server in docker using node

The goal of this example is to show you how to create a REST api server using Express.Js framework into a Docker container.

Note: I have used Visual Studio Code to build this

# Step 1
Create a package.json file that describes your app and its dependencies
![alt text](https://github.com/rajeshmuraleedharan/DockerizeNodeRestApiServer/blob/master/images/package.png)
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

# Step 2
create a server.js file that defines a web app using the Express.js framework

'use strict';

const express = require('express');

// Constants

const PORT = 8080;
const HOST = '0.0.0.0';

// App

const app = express();
app.get('/', (req, res) => {
  res.send('Hello world\n');
});

app.listen(PORT, HOST);
console.log(`Running on http://${HOST}:${PORT}`);

Step 2

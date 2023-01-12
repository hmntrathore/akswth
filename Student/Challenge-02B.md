# Challenge 02 - Path B: Dockerfiles

[< Previous Challenge](./Challenge-01.md) - **[Home](../README.md)** - [Next Challenge >](./Challenge-03.md)

## Introduction

The first step in our journey will be to take our application and package it as a container image, which will be stored in a container registry.

## Create Dockerfiles to Containerize the FabMedical Application
- You will find two sample Dockerfiles which will be used to build the container images for your application in the `/Challenge-02` folder of the `Resources.zip` files provided by your coach.
- You will find the source code for `content-web` and `content-api` in the `/Challenge-01/` folder of the `Resources.zip` file provided by your coach. Review how the provided Dockerfiles correspond to each of these applications.
- Create a Dockerfile for the content-api app that will:
	- Create a container based on the **node:8** container image
	- Build the Node application like you did above (Hint: npm install)
	- Exposes the needed port
	- Starts the node application

- Create a Dockerfile for the content-web app that will:
	- Do the same as the Dockerfile for the content-api
	- Also sets the environment variable value as above

- Build Docker images for both content-api and content-web

### Run the Containerized FabMedical Application with Docker

- Run both containers you just built and verify that it is working. 
	- **Hint:** Run the containers in 'detached' mode so that they run in the background.
	- **NOTE:** The containers need to run in the same network to talk to each other. 
		- Create a Docker network named "fabmedical"
		- Run each container using the "fabmedical" network
		- **Hint:** Each container you run needs to have a "name" on the fabmedical network and this is how you access it from other containers on that network.
		- **Hint:** You can run your containers in "detached" mode so that the running container does NOT block your command prompt.



## Success Criteria

1. Verify that you have created 2 Dockerfiles files and created a container image for both web and api.
1. Verify that you have built and deployed your container images to the registry.
1. Verify that you can run the application using containers


## Learning Resources

- [Dockerizing a Node.js web app](https://nodejs.org/en/docs/guides/nodejs-docker-webapp/)
- [How to Dockerize a Node.js application](https://buddy.works/guides/how-dockerize-node-application)
- [Why and How To Containerize Modern Node.js Applications](https://www.cuelogic.com/blog/why-and-how-to-containerize-modern-nodejs-applications)
- [Push your first image to your Azure container registry using the Docker CLI](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-get-started-docker-cli?tabs=azure-cli)
- [Import container images to a container registry](https://learn.microsoft.com/en-us/azure/container-registry/container-registry-import-images?tabs=azure-cli)

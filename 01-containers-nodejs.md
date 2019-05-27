# Containers Lab

In this lab, you'll get familiar with:
- Building Docker images
- Creating a Dockerfile
- Pushing to a registry 
- Understanding how to optimize a Dockerfile

## Build a docker image

**Pre-requisites:** Make sure you've gone thru the steps in [README.md](README.md) before proceeding

As a 1st step, let's build a Docker image that runs our NodeJS app. Notice that we don't need to have NodeJS installed on the VM.

1. Go to the src/nodejs folder
2. Create a dockerfile (tip: use VS Code with Docker extension)
3. Type `docker build -t mynodeapp .`
4. Type `docker run --rm -p 80:80 mynodeapp`
5. In the Azure Portal, find the IP address of the VM and browse to it. You should see your application running

## Pushing to a registry

In the Azure Portal, go to the Azure Container Registry that was created by the DevOps Project, then Settings -> Admin User. Make sure it's enabled and take note of the username and password (one of them).

Your login server below should be replaced with <something>.azurecr.io.

1. Authenticate with Docker by typing `docker login <login_server> -u <username> -p <password>`
2. Tag the image so it includes the container registry: `docker tag mvc1 <login_server>/mvc1`
3. Push it `docker push <login_server>/mvc1`

## Run your image

Repeat the ACI command, but this time use your custom image

`az container create -n myimage -g <your_rg_here> --ip-address public --image <login_server>/mvc1`

## Using Web App

Container Instances are just one way of running containers. Another way is using Web Apps. 

1. In the Azure Portal, create a new Web App
2. Specify OS = Linux
3. Specify Publish = Docker Image
4. Choose Azure Container Registry and select your uploaded docker image

## Optimize Dockerfile

Compare the `Dockerfile` and `Dockerfile.optimized` files. Can you understand the differences? 
Add Docker with Windows containers to an existing app, then deploy to Azure Container Instances and App Service.

Lab Time: 1 hour max

# Pre-requisites

* Azure Subscription
* Parts Unlimited build virtual machine ([deployment instructions here](http://microsoft.github.io/PartsUnlimited/configmgmt/200.4x-ConfigMgmt-CDwithWindowsContainersandVSTS.html) - see Task 1)

# Lab Steps

## Provision a container registry 
1. Create an Azure Container Registry instance by [following this tutorial](https://docs.microsoft.com/en-us/azure/container-registry/container-registry-get-started-portal). This is where we'll store the Docker images we create.

## Build and run a container locally

1. Open the [src/aspnetcore](./src/aspnetcore) application in Visual Studio

2. Add Docker Support and choose Windows Containers. You can do this by right-clicking the project file. More info available in [our docs site](https://docs.microsoft.com/en-us/aspnet/core/host-and-deploy/docker/visual-studio-tools-for-docker?view=aspnetcore-2.2#existing-app).

3. Build the project

4. Run the project locally. You should see the app running in http://localhost:3000

## Push the image to Azure Container Registry

1. 

## Deploy the application to Azure Container Instances

## Deploy the application to Azure App Service

## Updating the application

## Optional exercices

## Further Reading
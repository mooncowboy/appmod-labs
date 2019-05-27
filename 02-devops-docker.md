# Automate with Azure DevOps

Start by forking this repo in GitHub or clone it to Azure DevOps.

## Build

**IMPORTANT**: When creating a build pipeline, you may use YAML or the Visual Designer. For this workshop, we'll use the **Visual Designer**. 

Create a build pipeline that:

1. Builds the Docker image using the `Dockerfile` file
2. Pushes the result to Azure Container Registry
3. Make sure the build is triggered automatically (enable continuous integration)
4. Change the [src/nodejs/views/index.pug](src/nodejs/views/index.pug) file by adding a div with your name
5. Git add, commit and push to the master branch
6. Check if the build was triggered and the image was pushed to ACR

## Release

Create a release pipeline that:

1. Runs automatically when a build finishes
2. Updates the container image in Azure App Service
3. Restarts the App Service

## Help

[Azure DevOps Labs - Deploying a Docker based web application to Azure App Service](https://azuredevopslabs.com/labs/vstsextend/docker/)

[Build, test, and push Docker container apps](https://docs.microsoft.com/en-us/azure/devops/pipelines/languages/docker?view=azure-devops)







## Optional

1. Add IaC (Infrastructure as Code) ARM Templates that create the App Service. 
2. Use those templates in the release pipeline to automate infrastructure provisioning.
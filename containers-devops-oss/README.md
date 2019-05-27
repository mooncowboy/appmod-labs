# Containers and DevOps OSS 
Content for the Containers and DevOps workshop delivered for Microsoft partners in Lisbon. May 28, 2019.

# Goals

- Create Docker containers for OSS technologies like node.js, aspnet core, ruby, python, ...
- Understand the options for running containers and choose the right one (Kubernetes, Serverless, PaaS, ...)
- Use Kubernetes as a container orchestrator
- Create continuous integration and deployment pipelines for Docker and Kubernetes
- Influence and transform teams into good DevOps practices

# Main Topics
- Containers
- DevOps
- Kubernetes


# Presentations and go-to materials
    - [Docker and Containers - Tech Primer (Azure Citadel)](https://azurecitadel.com/cloud-native/tech-primer-containers/)
    - [The Azure Container platform ](https://azure.microsoft.com/en-us/product-categories/containers/)
    - [Azure Container Strategy and Orchestration with Kubernetes](https://onedrive.live.com/?cid=86b2652bd1f71711&id=86B2652BD1F71711%21473&authkey=%21APzBA4%2D%2DC1ChiyU)

# Pre-requisites

## Azure Subscription

You need access to a subscription where you can create resources including service principals. You can use your own or a voucher (if given to you).

To activate the voucher:

1. Do **NOT** use your work account or an account that has previously activated a voucher
2. In an **In-Private / Incognito** browser window, go to <https://www.microsoftazurepass.com/>  
3. Sign in (or [create a Microsoft Account](https://account.microsoft.com/account?lang=en-us) if you need to)
4. Follow the steps to activate the voucher

## Azure DevOps Organization 

Using the same account as above, login to [Azure DevOps Services](https://azure.microsoft.com/en-us/services/devops/) (or [create an account](https://azure.microsoft.com/en-us/services/devops/))

## Tooling

* Docker (to run Linux containers)
* Azure CLI or Azure Cloud Shell
* kubectl 
* Visual Studio Code with Docker and Kubernetes extensions (recommended)

If you don't have the tools above in your local computer, you can launch an available on GitHub by following the steps below.

## Using the Ubuntu VM with Docker

https://github.com/Azure/azure-quickstart-templates/tree/master/docker-simple-on-ubuntu

1. Click the **Deploy To Azure** Button
2. Specify parameters:
    - **Resource Group:** create a new one
    - **Location**: North or West Europe
    - **Admin Username and Password:** (choose your own)
    - **Dns Name:** must be globally unique (eg: rifiel-ubuntudockervm)
3. Once started, connect to the VM via SSH
4. Make sure docker is running by typing `docker run hello-world`
5. Install git `sudo apt-get install git`
6. Clone this repo `git clone https://github.com/theplastictoy/appmod-labs`

# Lab Steps

## Run Docker containers locally

Available in [01-containers-run.md](01-containers-run.md)

## Create your own container

Available in [01-containers-nodejs.md](01-containers-nodejs.md)

## CI/CD in Azure DevOps

Available in [02-devops-docker.md](02-devops-docker.md)

## Kubernetes

Available in [03-kubernetes.md](03-kubernetes.md)

# Slide contents

[Containers & Docker Tech Primer](https://azurecitadel.com/cloud-native/tech-primer-containers/)

[Designing Microservices, Masashi Narumoto](https://www.slideshare.net/masashin/designing-microservices)

[Kubernetes: Hands on With Microservices](https://azurecitadel.com/cloud-native/kubernetes/)

[Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/)

# Learn More

[Microsoft Cloud Workshops](https://github.com/Microsoft/MCW)

[Microsoft Learn](https://docs.microsoft.com/en-us/learn/)

[Azure DevOps Labs](https://www.azuredevopslabs.com/)

# E-Books

[Kubernetes Objects on Microsoft Azure](https://azure.microsoft.com/en-us/resources/kubernetes-objects-on-microsoft-azure/en-us/)


# Microsoft Exam

Cluster details
1.      Use Azure and AKS

2.      Set up K8S cluster , with RBAC enabled

3.      Cluster should have 2 services – A and B

4.      Cluster should have Ingress controller, redirecting traffic by URL: xxx/service-A or xxx/service-B

5.      Service-A should not be able to “talk” with Service-B (policy disabled)

6.      For Service A:write a script\application which retrieves the bitcoin value in dollar from an API on the web (you should find one) every minute and prints it, And also every 10 minutes it should print the average value of the last 10 minutes.

## Before You Begin
You need an Azure account with an active subscription. If you don't have one, create an account for free [HERE](https://azure.microsoft.com/en-us/pricing/purchase-options/azure-account?icid=azurefreeaccount&WT.mc_id=A261C142F).

## Installation - If you are using Azure DevOps Self-Hostet Agent Pool
Ensure that you have:

Install Azure CLI [here](https://learn.microsoft.com/en-us/cli/azure/get-started-with-azure-cli?view=azure-cli-latest).

Install Terraform [here](https://learn.microsoft.com/en-us/azure/developer/terraform/get-started-windows-powershell).

Create account and install docker [here](https://www.docker.com/).

Install kubectl [here](https://kubernetes.io/releases/download/).

Install helm [here](https://helm.sh/docs/intro/install/).

## Installation - If you arre using Azure DevOps Agent Pool

install Terraform plugin for Azure DevOps [here](https://marketplace.visualstudio.com/items?itemName=ms-devlabs.custom-terraform-tasks).

## Set Up K8s Cluster With Service A and Service B

Get all the files in this repository and upload to your Githab.

Create new project in  [Azure DevOps Organization](https://aex.dev.azure.com/me?mkt=he-IL) -> Go to you project -> Project Settings -> GitHub Connections -> New Connection, connect you Github to your DevOps project.

Go to your project -> pipelines -> new pipeline -> Github -> choose you repository where the files at -> Existing Azure Pipelines YAML file -> choose pipeline.yaml/WindowShellPipeline.yaml/LinuxPipeline.yaml (according to the pool agent you define, if you not define/ you want the default one, choose pipeline.yaml).

Run the pipeline and wait until it finish the job.

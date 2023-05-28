---
page_type: sample
languages:
- nodejs
- javascript
products:
- azure
- azure-app-service
description: "This sample demonstrates a tiny Hello World Node.js app for Azure App Service."
---

# Node.js Hello World

This sample demonstrates a tiny Hello World node.js app for [App Service Web App](https://docs.microsoft.com/azure/app-service-web).

## Contributing

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Deploy to Azure via GitHub Actions

see .github/workflows/azure-webapps-node.yml

## Manage Azure Web App via Terraform

Go to terraform folder

```bash
# login
az login

terraform init

terraform validate

terraform plan

terraform apply

terraform destroy
```

## Manage Azure Web App via Azure CLI

app name: webapp-node-app-5344
resource group: dev-gomoon-node-app

```bash
# login
az login

# list webapp
az webapp list --query "[].{hostName: defaultHostName, state: state}"

# show webapp
az webapp show --name webapp-node-app --resource-group dev-gomoon-node-app

# browse webapp
az webapp browse --name webapp-node-app --resource-group dev-gomoon-node-app

# restart webapp
az webapp restart --name webapp-node-app --resource-group dev-gomoon-node-app

# stop webapp
az webapp stop --name webapp-node-app --resource-group dev-gomoon-node-app

# start webapp
az webapp start --name webapp-node-app --resource-group dev-gomoon-node-app

# delete webapp
az webapp delete --name webapp-node-app --resource-group dev-gomoon-node-app

# create webapp
az webapp create --name webapp-node-app --resource-group dev-gomoon-node-app --plan webapp-node-app-plan --runtime "node|10.14"

# create webapp plan
az appservice plan create --name webapp-node-app-plan --resource-group dev-gomoon-node-app --sku B1 --is-linux

# list webapp plan
az appservice plan list --query "[].{name: name, sku: sku.name, workers: numberOfWorkers, state: provisioningState}"

# show webapp plan
az appservice plan show --name webapp-node-app-plan --resource-group dev-gomoon-node-app

# delete webapp plan
az appservice plan delete --name webapp-node-app-plan --resource-group dev-gomoon-node-app

# list webapp deployment
az webapp deployment list-publishing-profiles --name webapp-node-app --resource-group dev-gomoon-node-app
```

## Links

Azure Web App name : webapp-node-app-5344

* <https://webapp-node-app.azurewebsites.net>
* <https://webapp-node-app.scm.azurewebsites.net/>
* <https://webapp-node-app.scm.azurewebsites.net/webssh/host>
* <https://learn.microsoft.com/en-us/azure/app-service/>

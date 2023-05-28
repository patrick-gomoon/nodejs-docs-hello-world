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

terraform plan

terraform apply

terraform destroy
```

## Manage Azure Web App via Azure CLI

```bash
# login
az login

# list webapp
az webapp list --query "[].{hostName: defaultHostName, state: state}"

# show webapp
az webapp show --name webapp-77141 --resource-group webapp-77141-rg

# browse webapp
az webapp browse --name webapp-77141 --resource-group webapp-77141-rg

# restart webapp
az webapp restart --name webapp-77141 --resource-group webapp-77141-rg

# stop webapp
az webapp stop --name webapp-77141 --resource-group webapp-77141-rg

# start webapp
az webapp start --name webapp-77141 --resource-group webapp-77141-rg

# delete webapp
az webapp delete --name webapp-77141 --resource-group webapp-77141-rg

# create webapp
az webapp create --name webapp-77141 --resource-group webapp-77141-rg --plan webapp-77141-plan --runtime "node|10.14"

# create webapp plan
az appservice plan create --name webapp-77141-plan --resource-group webapp-77141-rg --sku B1 --is-linux

# list webapp plan
az appservice plan list --query "[].{name: name, sku: sku.name, workers: numberOfWorkers, state: provisioningState}"

# show webapp plan
az appservice plan show --name webapp-77141-plan --resource-group webapp-77141-rg

# delete webapp plan
az appservice plan delete --name webapp-77141-plan --resource-group webapp-77141-rg

# list webapp deployment
az webapp deployment list-publishing-profiles --name webapp-77141 --resource-group webapp-77141-rg
```

## Links

* <https://webapp-77141.azurewebsites.net>
* <https://webapp-77141.scm.azurewebsites.net/>
* <https://webapp-77141.scm.azurewebsites.net/webssh/host>
* <https://learn.microsoft.com/en-us/azure/app-service/>

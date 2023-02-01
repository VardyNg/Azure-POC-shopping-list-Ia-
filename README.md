# Azure-POC-shopping-list-IaC
A tiny poc project to get some Azure hands on experience - IaC

### Create a resource group 
```sh
az group create \
  --location eastasia \
  --resource-group azure-poc-shopping-list
```

### Deploy template to resource group
```sh
az deployment group create \
  --name azure-poc-shopping-list-rg \
  --resource-group azure-poc-shopping-list \
  --template-file azuredeploy.json \
  --parameter @storage.parameter.json @parameter.json @apigw.parameter.json @staticwebsite.parameter.json
```

### Delete resource group
```sh
az deployment group delete \
  --resource-group azure-poc-shopping-list \
  --name azuredeploy \
  --parameter @storage.parameter.json @parameter.json @apigw.parameter.json @staticwebsite.parameter.json
```
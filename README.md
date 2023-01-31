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
  --resource-group azure-poc-shopping-list \
  --template-file azuredeploy.json
```

### Delete resource group
```sh
 az deployment group delete \
  --resource-group azure-poc-shopping-list \
  --name azuredeploy
```
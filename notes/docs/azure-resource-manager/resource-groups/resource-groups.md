# Resource Groups

## Create a new resource group
### Azure Powershell
- [New-AzResourceGroup](https://learn.microsoft.com/en-us/powershell/module/az.resources/new-azresourcegroup)

```
New-AzResourceGroup -Name APS_Test_rg -Location germanywestcentral -Tag @{Empty=$null; Certification="AZ-104"}
```

### Azure CLI
- [az group create](https://learn.microsoft.com/en-us/cli/azure/group?view=azure-cli-latest#az-group-create)

```
az group create --name ACLI_Test_rg --location germanywestcentral --tags Empty=$null Certification=AZ-104
```

## List all resource groups
### Azure Powershell
- [Get-AzResourceGroup](https://learn.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup)

```
Get-AzResourceGroup
Get-AzResourceGroup -Name APS_Test_rg
Get-AzResourceGroup -Tag @{Empty=$null}
Get-AzResourceGroup -Location germanywestcentral
```

### Azure CLI
- [az group list](https://learn.microsoft.com/en-us/cli/azure/group?view=azure-cli-latest#az-group-list)
- [az group show](https://learn.microsoft.com/en-us/cli/azure/group?view=azure-cli-latest#az-group-show)

```
az group list
az group show --resource-group APS_Test_rg
az group list --tag Empty=$null
az group list --query "[?location=='germanywestcentral']"
```

## Update an existing resource group
### Azure Powershell
- [Set-AzResourceGroup](https://learn.microsoft.com/en-us/powershell/module/az.resources/set-azresourcegroup)

```
Set-AzResourceGroup -Name APS_Test_rg -Tag @{Empty=$null; Certification="AZ-104"}
Set-AzResourceGroup -Id /subscriptions/b8ecc038-d529-47fe-910e-a8b26d9973ba/resourceGroups/APS_Test_rg -Tag @{Empty=$null; Certification="AZ-104"}
```

### Azure CLI
- [az group update](https://learn.microsoft.com/en-us/cli/azure/group?view=azure-cli-latest#az-group-update)

```
az group update --resource-group APS_Test_rg --tags Empty=$null Certification=AZ-104
az group update --resource-group APS_Test_rg --set tags.CostCenter='{"Dept":"IT","Environment":"Test"}'
```

## Delete an existing resource group
### Azure Powershell
- [Remove-AzResourceGroup](https://learn.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup)

```
Remove-AzResourceGroup -Name APS_Test_rg
```

### Azure CLI
- [az group delete](https://learn.microsoft.com/en-us/cli/azure/group?view=azure-cli-latest#az-group-delete)

```	
az group delete --resource-group ACLI_Test_rg
```
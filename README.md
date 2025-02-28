# Azure CLI Cheatsheet

## **Azure CLI Overview**
Azure CLI is a command-line tool used to manage Azure resources efficiently.

---

## **Azure CLI Setup**
```sh
az --version                  # Check Azure CLI version
az login                      # Authenticate with Azure account
az account list               # List available Azure accounts
az account set --subscription <subscription-id>  # Set the active subscription
```

---

## **Resource Group Management**
```sh
az group list                 # List all resource groups
az group create --name <rg-name> --location <region>  # Create a resource group
az group delete --name <rg-name>  # Delete a resource group
```

---

## **Virtual Machines (VMs)**
```sh
az vm list                     # List all virtual machines
az vm create --resource-group <rg-name> --name <vm-name> --image UbuntuLTS --admin-username <user> --generate-ssh-keys  # Create a VM
az vm start --name <vm-name> --resource-group <rg-name>  # Start a VM
az vm stop --name <vm-name> --resource-group <rg-name>  # Stop a VM
az vm delete --name <vm-name> --resource-group <rg-name>  # Delete a VM
```

---

## **Azure Storage**
```sh
az storage account list        # List all storage accounts
az storage account create --name <storage-name> --resource-group <rg-name> --location <region> --sku Standard_LRS  # Create a storage account
az storage container create --name <container-name> --account-name <storage-name>  # Create a storage container
az storage blob upload --account-name <storage-name> --container-name <container-name> --file <local-file> --name <blob-name>  # Upload a file to Azure Blob Storage
```

---

## **Azure Kubernetes Service (AKS)**
```sh
az aks list                    # List AKS clusters
az aks create --resource-group <rg-name> --name <aks-name> --node-count 2 --enable-addons monitoring --generate-ssh-keys  # Create an AKS cluster
az aks get-credentials --resource-group <rg-name> --name <aks-name>  # Connect to an AKS cluster
```

---

## **Azure SQL Database**
```sh
az sql server list             # List SQL servers
az sql server create --name <server-name> --resource-group <rg-name> --location <region> --admin-user <user> --admin-password <password>  # Create an Azure SQL Server
az sql db create --resource-group <rg-name> --server <server-name> --name <db-name> --service-objective S0  # Create an Azure SQL database
```

---

## **Azure Networking**
```sh
az network vnet list           # List all Virtual Networks (VNets)
az network vnet create --name <vnet-name> --resource-group <rg-name> --location <region> --address-prefix 10.0.0.0/16  # Create a VNet
az network nsg create --name <nsg-name> --resource-group <rg-name> --location <region>  # Create a Network Security Group (NSG)
```

---

## **Azure Function Apps**
```sh
az functionapp list            # List all function apps
az functionapp create --resource-group <rg-name> --consumption-plan-location <region> --runtime python --name <app-name> --storage-account <storage-name>  # Create a Function App
```

---

## **Azure Monitor & Logs**
```sh
az monitor log-analytics workspace list  # List all Log Analytics workspaces
az monitor log-analytics query --workspace <workspace-id> --analytics-query "AzureActivity | take 10"  # Query logs
```

---

## **Azure Identity & Security**
```sh
az ad user list                # List all Azure AD users
az ad group list               # List all Azure AD groups
az role assignment list        # List role assignments
```

---

## **Useful Azure CLI Resources**
- [Azure CLI Documentation](https://docs.microsoft.com/en-us/cli/azure/)
- [Azure CLI Command Reference](https://docs.microsoft.com/en-us/cli/azure/reference-index?view=azure-cli-latest)
- [Azure Best Practices](https://docs.microsoft.com/en-us/azure/architecture/framework/)

---

This cheatsheet provides a quick reference for Azure CLI commands across various services. Let me know if you have any suggestions or improvements!


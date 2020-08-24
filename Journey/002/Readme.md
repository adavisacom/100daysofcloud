# Storage Accounts Pt.2

  -Storage Replication and Powershell/Azure CLI commands

## Introduction

✍️ (Why) Explain in one or two sentences why you choose to do this project or cloud topic for your day's study.

Continuing Storage Account module in CBT Nuggets

## Use Case

- ✍️ (Show-Me) Explain in one or two sentences the use case

Covered Storage Replication in Azure as well as some Powershell and AZ CLI commands to configure Storage Accounts
  -LRS
  -ZRS
  -GRS
  -RA-GRS


## Cloud Research

- ✍️ Document your trial and errors. Share what you tried to learn and understand about the cloud topic or while completing micro-project.

Storage Replication: LRS, ZRS, GRS, and RA-GRS
  -LRS (Locally Redundant Storage)
    -Cheapest option
    -Only redundant within the datacenter (between racks)
    -Offers 11 9s uptime (99.999999999%)
    
  -ZRS (Zone Redundant Storage)
    -True High Availability
    -Replication across 3 storage clusters (availabilty zones)in a single region
    -12 9s
    
  -GRS (Geo-Redunant Storage)
    -True disaster recovery
    -Replication to a secondary region
    -Does not allow access to data in fail-over region until fail-over happens
    -15 min RPO
    
  -RA-GRS (Read-Access Geo-Redundant Storage)
    -Most expensive
    -Read access to fail-over region
    -15 9s
    
Creating Storage Accounts: PowerShell and AZ CLI
**Note when creating Storage Accounts - Storage Account name must always be unique because it can be publicly accessible.

PowerShell
  new-azstorageaccount -name (the name) -resource (the resource group) -SKUname (replication type) -location (the location) -kind (account type)
  **replication type
    -Standard_ZRS
    -Standard_LRS
    -Standard_GRS
    -Standard_RAGRS
    
    **Account Type
      -StorageV2
      -Storage
      
Azure CLI
  az storage account create --name (the name) --resource-group (the group) --location --sku (replication type) --kind (account type)

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)

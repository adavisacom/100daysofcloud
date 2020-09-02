<!-- This template removes the micro tutorial for a quicker post and removes images for a full template check out the 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

## Analyze Resource Utilization Pt.1


## Notes

Overview:

  Resource Diagnostics/Azure Monitor
  
    -Tenent Logs -> Outside Subscription ex: Azure AD
    
    -Resource Logs -> Azure Services that deploy resources within your subscriptions
    
      -Non-Compute Resources (ex: NSG, Load Balancers, Public IP Addresses)
      
          -Diagnostic Logs -> Resource Specific
          
          -Activity Logs -> Subscription Level
            
            -Insight into operations performed on resources (ex: Creating/Deleting VMs)
            
      -Compute Resources
      
          -Application -> App Logs
          
          -Guest OS -> Diagnostic Logs (Guest-OS diagnostics needs agent installed on VM)
          
          -Host VM
          
          -Activity Log -> Azure Infrastructure
          
      **To enable guest-os diagnostics, you must have a storage account to store log data into.
      

Configuring Resource Diagnostics with Powershell

   ex: Creating diagnostics for a load balancer
   
      -Need storage account
      
      -Need Resource ID of SA
      
  1.) Set variable for storage account ID
  
    $sa = (get-storageaccount -storageaccountname <name of sa> -resourcegroupname <rg name>).id
  
  2.) Set variable for Resource ID
  
    $resource = (get-azresource -name <resource name> -resourcegroupname <rg name>).id
    
  3.) Set Diagnostic Settings
  
    set-azdiagnosticsetting -resourceid $resource -storageaccountid $sa -enable $true


Configuring Resource Diagnostics with AZ CLI

  1.) $sa = az storage account show --name <name of sa> --query id
  
  2.) $resource = az resource show --name <resource name> --resource-group <rg name> --resource-type microsoft.network/loadbalancers --query id
  
  3.) az monitor diagnostic-settings create --resource $resource --name <custom name> --storage-account $sa --logs (enter parameters in json)

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

https://twitter.com/alexd43/status/1301007640387096577

<!-- This template removes the micro tutorial for a quicker post and removes images for a full template check out the 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

## Storage Accounts Pt. 4

## Use Case

- ✍️ (Show-Me) Explain in one or two sentences the use case

Covering  using Access Keys, Shared Access Signatures, and Monitoring Storage Accounts

## Cloud Research

- ✍️ Document your trial and errors. Share what you tried to learn and understand about the cloud topic or while completing micro-project.

Using Access Keys

  Storage Accounts use Access Keys to share access to the Storage Accounts for other users and services
  
  -2 Key
  
    -512 bit strings
    
  -Can use keys with APIs or PowerShell that needs to access the Storage Accounts.
  
  -Also can use with Storage Explorer
  
  - Best Practice
  
    -Reason why you have 2 access keys:
    
      -Give only 1 key to everyone at a time until it is time to regenerate. Then switch to 2nd key, alert everyone about the change, then regengerate 1st when everyone is no longer utilizing it.
      
    -Upload file from AZ CLI ex:
    
      az storage blob upload --container-name <name of container> --account-name <account name> --account-key <key copied from container> --name <name for new file> --file <path to file on computer>


Using Shared Access Signatures

  -SAS - String that contains a security token to be used with a URL.
  
  -Can specify:
  
    -What services are allowed to use SAS
    
      -Blob, file, table, queue
      
    -Allowed resource types
    
      -Service, Object, Container
      
    -Permissions
    
      -Read, Write, Delete, List, Add, Create, Update, Process
      
    -Allowed access time/date
    
    -Allowed IP Addresses
    
    -Allowed Protocols
    
    -Which key to use
    
  -AZ CLI ex:
  
    -az storage blob upload --container-name <name of container> --account-name <account name> --sas-token <generated sas token> (in quotes) --name <name for new file> --file <path to file on computer>
    
    
Monitoring your Storage Account in Azure

  -When using Activity Logs
    -Only covers Administrative Logs (Management Info)(Not in Data Plane)
      -Events
      -Security
      -Alerts
      -Advisor Recommendations

    -Log Analytics
      -Another way to see data
      -Need storage account to connect to it for dumping data

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)

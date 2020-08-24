<!-- This template removes the micro tutorial for a quicker post and removes images for a full template check out the 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# Storage Account pt. 1

## Types of Storage Accounts

✍️ (Why) Explain in one or two sentences why you choose to do this project or cloud topic for your day's study.

Choose this topic because it was the next part in my lesson in CBT Nugget course.

## Use Case

- ✍️ (Show-Me) Explain in one or two sentences the use case

Use case for Storage Accounts is to store data in an easily accessible place.

## Cloud Research

- ✍️ Document your trial and errors. Share what you tried to learn and understand about the cloud topic or while completing micro-project.

Storage Account:

  -Blob - Stores massive amounts of storage
      -Backups
      -Random Files
      
  -Azure Files -> Like file explorer (Fileshare)
      -SMB
      -Uses Port 445
      -File Sync (Like Onedrive to store cache files to save local data)
      
  -Table Storage
      -NoSQL
        -Data with no structure
        -Cheaper
        -User Data/Meta Data
        
  -Queue Storage
      -Stores messages in queue before sending to backend server
        -ie purchase order in cases like massive request for product (black friday)
        
        
        
Choosing the Right Storage Account Type:

  -Storage General Purpose V1
  
      -Supports Blob, File, Table, and Disk
      
      -Tops out at 500TB**
      
      -Not recommended by Azure. Does not have latest features
      
      -Mainly for compatibility
      
  -Storage General Purpose V2 (Recommended)
      -Can upgrade from V1->V2
      -Supports Blob, File, Table, and Disk
      -Up to 500PB
      
Block - Like files in file explorer (-replace, remove, and delete)

Append - Can only add data (Logs)

Page - Core of IaaS (Disk files for VMs - VHD)
      
  -Blob Storage (only specific use cases)
  
      -Only supports Block and Append
      
  -Premium Disk (SSDs) GenPurpV1 & V2 only supports Page Blobs
  
  -Premium Disk BlockBlob only supports block and append blobs

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

https://twitter.com/alexd43/status/1297410476444393472

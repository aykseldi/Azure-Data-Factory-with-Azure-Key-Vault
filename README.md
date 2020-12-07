# Azure-Data-Factory-with-Azure-Key-Vault

# AZURE IMPLEMNTATION 

Create 3 Objects:
1. Blob Storage 
  --Create Container and upload csv 
2. Azure PAAS Sql Database
  -- Take script and create table 
** Insert firewall rule to make you access to db 
3. Azure Data Factory 

Azure Key Vault Implementation 

1. Create Key Vault 

On Secrets 
  a. Blob Storage 
  Go to Access Keys 
  Copy Key 
  Go to Azure key Vault 
  Create new Secret 
    -Give Friendly name 
    -Paste Value --> Secret key that you copy from Access Keys

  b. Sql Server 
  Create new Secret 
    -Give Friendly name 
    -Paste the Database Password that you made while creation of DB
    
  c. Grant access to ADF to read the secrets you have created 
    - Go to access policies 
    - Add new access policy 
    - Select secret permission to get 
    - Put principal as ADF that you have created 
    
2. On Azure Data Factory 
Go to Author and Monitor
Go to Manage on the left side 
Create Linked Services for Blob Storage annd DB

3. Extract and Load

Create a pipeline 
on Move and Transform --> take Copy Data
  --Source --> Flat file csv on Blob Storage 
  -- Sink Database Table Created 
  -- Check Mappings 
  -- Before deploying Debug 
  -- Monitor

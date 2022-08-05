# Azure-Firewall-classic-to-policy
Migrating Azure Firewall with Classic rules to a Policy based Firewall 

This repository will go through how to migrate an Azure Firewall with Classic rules to a Policy based Firewall. 

Firstly, follow the steps in this guide to migrate an existing Firewall configurations to an Azure Firewall Policy resource using a Powershell Script. 
https://github.com/MicrosoftDocs/azure-docs/blob/main/articles/firewall-manager/migrate-to-policy.md 

After this script has been run you will have an Azure Firewall Policy in the Resource Group you specified. The Firewall Policy will have migrated all of the rules from the classic mode over to the Firewall Policy. 

Once this policy has been created you will need to go into Firewall Manager to manage the hubs and vnets that the policy is associated with. 

<img width="659" alt="image" src="https://user-images.githubusercontent.com/67756102/183087755-810b4050-7766-4737-b94f-e31a7b45d22f.png">

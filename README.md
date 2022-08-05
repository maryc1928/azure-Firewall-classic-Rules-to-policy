# Azure-Firewall-classic-to-policy
Migrating Azure Firewall with Classic rules to a Policy based Firewall 

This repository will go through how to migrate an Azure Firewall with Classic rules to a Policy based Firewall. 

Firstly, follow the steps in this guide to migrate an existing Firewall configurations to an Azure Firewall Policy resource using a Powershell Script. 
https://github.com/MicrosoftDocs/azure-docs/blob/main/articles/firewall-manager/migrate-to-policy.md 

After this script has been run you will have an Azure Firewall Policy in the Resource Group you specified. The Firewall Policy will have migrated all of the rules from the classic mode over to the Firewall Policy. 

Once this policy has been created you will need to associate the Hubs and Vnets to use Firewall Policy and attach the policy that was created in an earlier step. 

To do this go to Firewall Manager > Azure Firewall Policies 

<img width="659" alt="image" src="https://user-images.githubusercontent.com/67756102/183089782-af60e260-c63f-42d9-9def-e6df0a8f94ba.png">

Once there, click on the checkbox of the policy that was created in the earlier step and select the manage associations drop down.  

<img width="316" alt="image" src="https://user-images.githubusercontent.com/67756102/183091085-2f605e73-2a9f-4a47-9771-f6ff870fdbe0.png">

Here you will be able to associate your vnets and Hubs from your subscriptions with the Azure Policy. 

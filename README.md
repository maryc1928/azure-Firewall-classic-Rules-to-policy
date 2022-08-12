<h1> Migrate Azure Firewall with Classic Rules to a Firewall with Policy Manager</h1>

<h2>Objective</h2>

This guide goes through the necessary steps for migrating a Firewall with Azure Firewall Classic rules to a Azure Firewall using an Azure Firewall Manager Policy as well as possible use cases for migration.   

<h2> Customer Profile </h2> 

A company may have resources in Azure that are distributed accross many Azure Virtual Networks. To protect those resources, an Azure Firewall may be deployed in a single instance. Over time the needs of the company may grow, and they may choose to implement additional Firewalls. As the complexity of the networking resources in Azure develop, the company may look for a more simplified way to manage multiple Firewalls, this is where Azure Firewall Manager assists. 

Azure Firewall Policies can span multiple Firewall instances in both Secured Virtual Hubs and Hub Virtual Networks, as well as cross region and subscription. This makes it a popular method of deployment for organisations with many Firewalls in different regions. 

<h2> What is Azure Firewall Manager? </h2>

Azure Firewall Manager centralises the management of Firewalls into a single view and allows organisations to apply a single Firewall Policy to many Firewalls. 
This allows the configuration updates of Azure Firewalls to span across many Firewall's as opposed to updating each Firewall individual which can result in a management overhead. 

<h2> What is a Firewall Policy? </h2>

Firewall Policy is a central component of Azure Firewall Manager and can consist of NAT settings, Network rule collections, Application Rule Collections and Threat Intelligence settings. 

Once a Firewall policy is created you can apply them to Firewalls. The policies can be associated to one or more virtual networks and virtual hubs. 

<h2> Considerations for Azure Firewall Manager </h2>

<h3> Cost </h3> 




<h2> How to Migrate a Firewall with Azure Firewall Classic rules to Azure Firewall using Azure Firewall Manager Policy </h2>

Firstly, follow the steps in this guide to migrate an existing Firewall configurations to an Azure Firewall Policy resource using a Powershell Script. 
https://github.com/MicrosoftDocs/azure-docs/blob/main/articles/firewall-manager/migrate-to-policy.md 

After this script has been run you will have an Azure Firewall Policy in the Resource Group you specified. The Firewall Policy will have migrated all of the rules from the classic mode over to the Firewall Policy. 

Once this policy has been created you will need to associate the Hubs and Vnets to use Firewall Policy and attach the policy that was created in an earlier step. 

To do this go to Firewall Manager > Azure Firewall Policies 

<img width="659" alt="image" src="https://user-images.githubusercontent.com/67756102/183089782-af60e260-c63f-42d9-9def-e6df0a8f94ba.png">

Once there, click on the checkbox of the policy that was created in the earlier step and select the manage associations drop down.  

<img width="316" alt="image" src="https://user-images.githubusercontent.com/67756102/183091085-2f605e73-2a9f-4a47-9771-f6ff870fdbe0.png">

Here you will be able to associate your vnets and Hubs from your subscriptions with the Azure Policy. 

Once you have associated your Classic Firewall Vnet's with the new policy it will be able to be managed by Azure Firewall Manager and Azure Firewall Policy. 

<img width="434" alt="image" src="https://user-images.githubusercontent.com/67756102/183092361-69e7c796-9a87-4f81-959e-ddb88523d36f.png">

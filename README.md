What is this project for? 

This guide goes through the necessary steps for migrating a Firewall with Azure Firewall Classic rules to a Azure Firewall using an Azure Firewall Manager Policy.   

What is Azure Firewall Manager? 

Azure Firewall Manager centralises the management of Firewalls into a single view and allows organisations to apply a single Firewall Policy to many Firewalls. 
This allows the configuration updates of Azure Firewalls to span across many Firewall's as opposed to updating each Firewall individual which can result in a management overhead. 

What is a Firewall Policy? 

Firewall Policy is a central component of Azure Firewall Manager and can consist of NAT settings, Network rule collections, Application Rule Collections and Threat Intelligence settings. 

Once a Firewall policy is created you can apply them to Firewalls. The policies can be associated to one or more virtual networks and virtual hubs. 


Customer Profile

A company may have resources in Azure that are distributed accross many Azure Virtual Networks. To protect those resources, an Azure Firewall may be deployed in a single instance. Over time the needs of the company may grow, and they may choose to implement additional Firewalls. As the complexity of the networking resources in Azure develop, the company may look for a more simplified way to manage multiple Firewalls, this is where Azure Firewall Manager assists. 



Azure Firewall Policies can span multiple Firewall instances in both Secured Virtual Hubs and Hub Virtual Networks, as well as cross region and subscription. This makes it a popular method of deployment for organisations with many Firewalls in different regions. 

Why use Azure Manager Policy? 


Cost Considerations

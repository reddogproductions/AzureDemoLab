Please go through all recommendations to insure a smooth demo experience with your customer

## Activate your Account

To safeguard the demo environment access needs to be approved first , this can be done by joining the [RedDogProductions](https://teams.microsoft.com/l/team/19%3a6904744e8f2943ca9d221d5988d42734%40thread.tacv2/conversations?groupId=f6174a3a-7450-417c-87a9-77c85d11aa06&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) Teams channel and request your @reddogproductions.tech account login credentials.
When you receive your account credentials you will need to go through a few additional steps to complete the account setup.
Open a in-private browser session and navigate to https://www.office.com, login with the new account and follow the wizard to add your phone number and alternative email address.

Verify you can log-in to https://portal.azure.com and select the RedDogProductions tenant, you should also be able to list the 3 linked subscriptions

![login](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/azure%20account.png)

![tenant](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/azure%20directory.png)



## Start/Stop VM's

All Virtual Machines (except the GPU VM) start automatically at 9AM and shut down at 6PM by **Azure Automation**. If you have the need to work with the environment outside of these hours or you need the GPU VM, you have following options:

### Azure Mobile App

download the Azure App from your app store provider.

![mobile app](https://azurecomcdn.azureedge.net/cvt-9281d9db0c63a479d39019e02b1bc35d712622992174d8bb4dcb33f728511a17/images/page/features/azure-portal/mobile-app/panel-1.png)

### Azure PowerApp

![powerapp](https://chlams.blob.core.windows.net/public/reddogproductions/pics/powerapps/startstopvms.png)

request the PowerApp to be shared with you (Teams Channel)

###  Azure LightHouse

![lighthouse search](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighthousesearch.png)

select Manage your customers

![Lighthouse manage](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighthousemanage.png)

Select Microsoft customer (or click delegations)

![Lighthouse customers](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighthousecustomers.png)

Select the AIRS subscription

![lighthouse delegation](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/Lighthousedelegation.png)

Notice your role on the AIRS subscription and select Resource Groups, these will vary according to your rights

![lighthouse access rights](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighouseaccess.png)

![lighthouse resources](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighthouseresources.png)



Select the resource group containing the WVD resources

![wvd resources](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighthousewvdvms.png)

filter on virtual machines

![VM filter](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighthousevmfilter.png)

Select the first VM and click start

![start stop vm](https://chlams.blob.core.windows.net/public/reddogproductions/pics/intro/lighthousestartstopvm.png)



Whatever tool you are using, don't forget to shut the VM's back down when no longer needed.



## Reference links:

Azure Lighthouse: https://docs.microsoft.com/en-us/azure/lighthouse/overview

PowerApps: https://docs.microsoft.com/en-us/powerapps/powerapps-overview

Azure Mobile App: https://azure.microsoft.com/nl-nl/features/azure-portal/mobile-app/

Start/Stop VM's: https://docs.microsoft.com/en-us/azure/automation/automation-solution-vm-management






# Welcome

![Logo](https://github.com/reddogproductions/AzureDemoLab/blob/main/images/pics/rdp_logo.png)

## <https://github.com/reddogproductions/AzureDemoLab>

MSFT private Azure demo environment
[**Explore the docs 📃**](https://github.com/reddogproductions/AzureDemoLab/tree/main/labguide)

[View Demo](https://rdweb.AVD.microsoft.com/arm/webclient/index.html) • [Report Bug](https://github.com/reddogproductions/AzureDemoLab/issues)

## Audience

This demo environment is to be used by Microsoft Employees, currently the scope is limited to the Belgian subsidiary.

## About The Demo Environment

There are a few reasons why I wanted to build this demo environment, the first one is that I just like our technology and love to build and play around with it to increase my own knowledge. A second reason is the Microsoft Certified Trainer in me that would like this environment to be used by others to improve their knowledge on Azure solutions. You might have an upcoming Azure exam (TSI) and want to know how our services are configured and glued together into solutions? Then this could be a good place to start!

A less obvious reason is that some of our solutions can't be put into a single category. Look at Windows Virtual Desktop for example: Windows 10 and Azure AD (premium) are usually handled by our Modern Workplace specialist. Virtual Machines, virtual networks and firewalls fall under the category of Azure and handled by the Cloud Solution Architects. This introduces some issues when we want to demo this service: Cloud Solution Architects have access to internal Azure subscriptions, but not to Azure AD and MW specialist usually don't have access to services running on Azure (AVD, Sentinel..).

as an example: Let's have a look at the options we (CSA's) have to show Azure Virtual Desktop to your customers:

| solution                                          | pro                            | con                                        |
| ------------------------------------------------- | ------------------------------ | ------------------------------------------ |
| the AVD environment hosted by Microsoft           | Microsoft managed              | no access to Azure subscription and tenant |
| Self hosted demo environment (MSDN/Visual Studio) | flexibility, licenses included | limited budget, less data to work with     |
| Microsoft internal subscription                   | subscription with budget       | no rights on the MSFT Azure AD tenant      |
| PowerPoint clickthrough AVD demo                  | the 'safe' option              | slideware                                  |

By introducing this new 'full featured' and reusable AVD (and more) demo environment we now have a new option where you have control over everything that  a modern organization could deploy on Azure. Now, what if this demo environment would be used cross business unit? not only by the techies but also the sellers? Adding Power Platform,data solutions, DevOps,...
Each specialist can truly showcase our products/solutions/integrations between services without having to fall back on PowerPoint slides (demo guides available!) and when multiple users use the same environment, then there is even more data to work with and the results will be even more compelling!

Last but not least, look at the competitive advantage we have over our competition, how we can truly show end-to-end scenario's. Not only between different services, but also between our clouds!

Too many reasons not to give this a try right?

## Split setup approach

This demo environment has a split setup and uses both the internal AIRS subscription and Visual studio subscriptions. 
To make use of the 25 included M365 Visual Studio licenses, a new tenant was created with the custom domain reddogproductions.tech on reddogproductions.onmicrosoft.com. (if you wonder where the name came from, Red Dog was once the internal code name for Azure)
This split setup gives us best of both worlds, Azure AD without (management) limitations and a subscription with enough budget to keep the environment live during business (demo) hours. Having such budget is welcome, but still we always try to keep a low TCO in mind: Virtual machines are spot VM's and scheduled to automatically start and stop.

![cross tenant approach](https://github.com/reddogproductions/AzureDemoLab/blob/main/images/design/crosstenant.png)

Another advantage of this split setup is that you can also show what options we have to work cross tenant/subscription.

### Demo Storyline

storyline: RedDogProductions is a fictive IT service company that develops and consults on the Microsoft Azure platform.
RDP has offices in the US and Europe and share the same Azure AD, while Azure subscriptions are region bound.

While the offices have access restrictions due to Corona, RDP has enabled Azure Virtual Desktop for all employees who require access to internal applications. After a successful pilot, RDP has decided to expand the scope and also offer personalized desktops for their developers and remote apps for frontline workers.

Walk through the [demo script](https://github.com/reddogproductions/AzureDemoLab/tree/main/labguide) to showcase Azure Virtual Desktop and related Azure Services

### Request access

request your credentials in the following [Teams site](https://teams.microsoft.com/l/team/19%3a6904744e8f2943ca9d221d5988d42734%40thread.tacv2/conversations?groupId=f6174a3a-7450-417c-87a9-77c85d11aa06&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) (MSFT only)

### Prerequisites

- HTML5 browser client ([Edge Chromium](https://support.microsoft.com/en-us/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf), Google Chrome,..)

- AVD client

  - [Windows](https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/windowsdesktop#install-the-client) [Windows Store](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-microsoft-store)

  - [MacOS](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-macos)

  - [Android](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-android)

  - [iOS](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-ios)

  - [Linux clients](https://docs.microsoft.com/en-us/azure/virtual-desktop/linux-overview)

## Demo guide

Follow the [documentation](https://github.com/reddogproductions/AzureDemoLab/tree/main/labguide) that contains the demo scripts.

Following list of technology can be part of your demo:

## RedDogProductions AZURE AD

- Company branding

- 25 M365 E5 License auto assigned to dynamic group

- Azure AD Connect
  - synchronized users & groups
  - Password synchronization
  - Pass Through Authentication

- Azure AD Connect Health

- Privileged identity management
- Identity Governance
- Azure monitor + Sentinel integration
- Conditional Access Policies for AVD
- Azure AD SSO client
- Multifactor authentication

## AZURE MSDN SUBSCRIPTION

- Azure Custom Images

- Azure Shared Image Gallery (shared to other Tenant/Subscriptions)

- Azure Virtual Desktop (ARM)

  - Pooled Desktop with W10 Multi-User
  - Personal Desktops (developers)
  - Remote Applications
    - Company applications
    - GPU application (design/engineering)
  - FSLogix user profiles
  - Domain Joined Azure Files
  - App Attach

- Azure DevTest Labs

  - VNET peering to AIRS Tenant/Subscription (DC communication)
  - Custom images / Formulas
  - Policies (VM’s per user/ VM’s per lab / schedule...)

- Azure Lab Services

- Azure Security Center

- Azure Sentinel

- Azure Management Groups

- Azure Monitor (AVD service + other services integrated in Log Analytics)

## AZURE AIRS SUBSCRIPTION

- Azure vWAN + Azure Firewall

- Virtual Network for AVD Session Hosts

- virtual Network for IAM (domain controller)

- Network security Groups

- cross tenant/subscription VNET peering

- Azure Bastion for secure access

- Active Directory Domain Controller

  - DNS
  - users & computers
  - Azure AD Connect
  - Group Policies for AVD

- Azure Automation Account

  - Patching VM’s
  - Auto Start / Stop VM’s

- Azure Monitor (AVD session hosts + other services integrated in Log Analytics)

- Azure Security Center (Standard)

  - Just in Time Access
  - compliance score
  - security score

- Azure Governance

  - Policies
  - Blueprints

- Azure Cost Management + Budget Alerts

- Azure Site Recovery (DC + AVD hosts)

- Azure LightHouse

- Network Watcher

## Roadmap

the pilot starts in the Belgian sub, when successful we plan to expand this environment with more services and to more regions.

services on roadmap:

\-     SCCM/INTUNE

\-     Service Endpoints / Private Link

\-     Azure ARC

## Contributing

There are a few ways to contribute to this project:

1. help with the lifecycle management of the project

2. 'attach' your AIRS subscription to the tenant (Azure Lighthouse) and build services on top of the demo environment

3. help with documentation:

   Fork the Project

   Create your Feature Branch (`git checkout -b feature/AmazingFeature`)

   Commit your Changes (`git commit -m 'Add some AmazingFeature'`)

   Push to the Branch (`git push origin feature/AmazingFeature`)

   Open a Pull Request

Any contributions you make are **greatly appreciated**.

## Contact

Christophe Lams: christophe [dot] lams [@] Microsoft [dot] com

Cloud Solution Architect - Customer Success Unit

Azure Virtual Desktop Champ (BE sub)

Project Link: <https://github.com/reddogproductions/AzureDemoLab>

demo

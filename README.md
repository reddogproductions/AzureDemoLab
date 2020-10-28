[![Logo](https://chlams.blob.core.windows.net/public/reddogproductions/pics/rdp_logo.png)

### https://github.com/reddogproductions/AzureDemoLab

Microsoft internal Azure demo environment
**Explore the docs 📃**

[View Demo](https://rdweb.wvd.microsoft.com/arm/webclient/index.html) • Report Bug • Request Feature



## Table of Contents

[TOC]

## About The Demo

Even while WVD is a awesome service, internal employees are unable to show all related aspects due to the Azure AD restrictions in the microsoft.onmicrosoft.com tenant. 
This demo environment has been setup in a rather special way (split setup over multiple tenants and subscriptions) to circumvent these shortcomings. In the meanwhile this also gives us the opportunity to showcase cross tenant/subscription functionality that's built-in to Azure. 

![cross tenant approach](https://chlams.blob.core.windows.net/public/reddogproductions/design/crosstenant.png)



## Getting Started

storyline: RedDogProductions is a fictive IT service company that develops and consults on the Microsoft Azure platform. RDP has offices in the US and Europe and share the same Azure AD, while Azure subscriptions are region bound. 

While the offices have access restrictions due to Corona, RDP has enabled Windows Virtual Desktop for all employees who require access to internal applications. 
After a successful pilot, RDP has decided to expand the scope and also offer personalized desktops for their developers and remote apps for frontline workers.

Walk through the demo script to showcase Windows Virtual Desktop and related Azure Services



### Credentials

request your credentials in the following [Teams site](https://teams.microsoft.com/l/team/19%3a6904744e8f2943ca9d221d5988d42734%40thread.tacv2/conversations?groupId=f6174a3a-7450-417c-87a9-77c85d11aa06&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) (MSFT only)



### Prerequisites

- HTML5 browser client ([Edge Chromium](https://support.microsoft.com/en-us/microsoft-edge/download-the-new-microsoft-edge-based-on-chromium-0f4a3dd7-55df-60f5-739f-00010dba52cf), Google Chrome,..)

- WVD client

  - [Windows](https://docs.microsoft.com/en-us/windows-server/remote/remote-desktop-services/clients/windowsdesktop#install-the-client) [Windows Store](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-microsoft-store)

  - [MacOS](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-macos)

  - [Android](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-android)

  - [iOS](https://docs.microsoft.com/en-us/azure/virtual-desktop/connect-ios)

  - [Linux clients](https://docs.microsoft.com/en-us/azure/virtual-desktop/linux-overview)

    

## Usage

Follow the documentation that contains the demo scripts.

Following list of technology can be part of your demo:

**RedDogProductions AZURE AD**

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
- Conditional Access Policies for WVD
- Azure AD SSO client
- Multifactor authentication

 

**AZURE MSDN SUBSCRIPTION**

- Azure Custom Images 

- Azure Shared Image Gallery (shared to other Tenant/Subscriptions)
- Windows Virtual Desktop (Spring 2020 update)

- Pooled Desktop with W10 Multi-User
- Personal Desktops (developers)
- Remote Applications
  - Company applications
  - GPU application (design/engineering)
- FSLogix user profiles
  - Domain Joined Azure Files

- Azure DevTest Labs
  - VNET peering to AIRS Tenant/Subscription (DC communication)
  - Custom images / Formulas
  - Policies (VM’s per user/ VM’s per lab / schedule...)

- Azure Lab Services

- Azure Security Center 

- Azure Sentinel

- Azure Management Groups

- Azure Monitor (WVD service + other services integrated in Log Analytics)

  

**AZURE AIRS SUBSCRIPTION**

- Azure vWAN VPN HUB

- Virtual Network for WVD Session Hosts
- virtual Network for IAM (domain controller)

- Network security Groups

- Azure vWAN + Azure Firewall

- VNET peering to MSDN subscription

- Azure Bastion for secure access

- Active Directory Domain Controller
  - DNS
  - users & computers
  - Azure AD Connect
  - Group Policies for WVD

- Azure Automation Account
  - Patching VM’s
  - Auto Start / Stop VM’s

- Azure Monitor (WVD session hosts + other services integrated in Log Analytics)

- Azure Security Center (Standard)
  - Just in Time Access
  - compliance score
  - security score

- Azure Governance
  - Policies
  - Blueprints

- Azure Cost Management + Budget Alerts

- Azure Site Recovery (DC + WVD hosts)

- Azure LightHouse

- Network Watcher

  

## Roadmap

the pilot starts in the Belgian sub, when successful we plan to expand this environment with more services and to more regions.

services on roadmap:

\-     Proxy Server (WVD)

\-     Azure DevOps integration

\-     Integrate Teams (waiting for public preview)

\-     SCCM/INTUNE

\-     S2S VPN to show hybrid options

\-     MDATP W10 + W10 MU

\-     Service Endpoints / Private Link 

\-     Private Link Service

\-     Azure Migrate

\-     Azure ARC

\-     Azure Application Proxy

\-     NAT Gateway



## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project

2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)

3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)

4. Push to the Branch (`git push origin feature/AmazingFeature`)

5. Open a Pull Request

   

## Contact

Christophe Lams: christophe [dot] lams [@] Microsoft [dot] com

Project Link: https://github.com/reddogproductions/AzureDemoLab

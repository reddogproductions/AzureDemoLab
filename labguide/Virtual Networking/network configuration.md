
# Virtual Networking Configurations

## vWAN Configuration

The West Europe AIRS subscription counts 2 Virtual WAN hubs and provides any to any connections.  
The hub in West Europe is what we call a *secure hub*, meaning we have a firewall installed in it.
![vwanhub](<https://github.com/reddogproductions/AzureDemoLab/blob/main/images/pics/networking/vWAN%20hubs.png>)

## Virtual Networks

following virtual networks are linked to the West Europe vWAN:

- AVD vnet (session hosts)
- identity vnet (domain controller)
- lab service vnet

following virtual networks are linked to the North Europe vWAN

- AVD vnet

Internet and internal connections are protected by the Azure Firewall and its FW policy.

## cross tenant VNET Peerings (to vWAN)

peering from MSDN vnet to AIRS vWAN

- AVD vnet
- identity vnet
![crosstenantpeering](https://github.com/reddogproductions/AzureDemoLab/blob/main/images/pics/networking/crosstenantpeering.png)

**Reference Links**  
[vWAN docs](https://docs.microsoft.com/en-us/azure/virtual-wan/)  
[crosstenant peering](https://docs.microsoft.com/en-us/azure/virtual-wan/cross-tenant-vnet)  

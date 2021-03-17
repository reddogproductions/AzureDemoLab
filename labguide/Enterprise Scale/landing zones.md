
# Cloud Adoption Framework - Enterprise Scale

## Enterprise Scale In A Box

This environment has been setup according to the guidelines of[Enterprise Scale in a box](https://github.com/Azure/Enterprise-Scale/blob/main/docs/enterprise-scale-iab/README.md).
This means we used a Github CI/CD pipelines from our forked repository <https://github.com/reddogproductions/Enterprise-Scale-in-a-box/blob/main/README.md>, at current time we selected to deploy the Wingtip example (Cloud only).

### What is implemented?

By default, all recommendations are enabled and we must explicitly disable them if we don't want it to be deployed and configured.

A scalable *Management Group hierarchy* aligned to core platform capabilities, allowing you to operationalize at scale using centrally managed Azure RBAC and Azure Policy where platform and workloads have clear separation
*Azure Policies* that will enable autonomy for the platform and the landing zones.
An Azure subscription dedicated for management, which enables core platform capabilities at scale using Azure Policy such as:
A *Log Analytics* workspace and an Automation account
Azure Security Center monitoring
Azure Security Center (Standard or Free tier)
Azure Sentinel
Diagnostics settings for Activity Logs, VMs, and PaaS resources sent to Log Analytics
A landing zone subscription for Azure native, internet-facing applications and Resources, and specific workload Azure Policies such as:
Enforce VM monitoring (Windows & Linux)
Enforce VMSS monitoring (Windows & Linux)
Enforce Azure Arc VM monitoring (Windows & Linux)
Enforce VM backup (Windows & Linux)
Enforce secure access (HTTPS) to storage accounts
Enforce auditing for Azure SQL
Enforce encryption for Azure SQL
Prevent IP forwarding
Prevent inbound RDP from internet
Ensure subnets are associated with NSG
Enterprise-Scale without connectivity

[Wingtip](https://github.com/reddogproductions/Enterprise-Scale-in-a-box/blob/main/docs/reference/wingtip/media/es-without-networking.PNG)

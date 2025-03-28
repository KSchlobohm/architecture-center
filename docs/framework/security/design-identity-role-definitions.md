---
title: Team roles and responsibilities
description: Learn to define clear lines of responsibility and establish separation of duties as part of Azure identity and access management.
author: PageWriter-MSFT
ms.date: 07/09/2019
ms.topic: conceptual
ms.service: architecture-center
ms.subservice: well-architected
ms.custom:
  - article
---

# Team roles and responsibilities

In an organization, several teams work together to make sure that the workload and the supporting infrastructure are secure. To avoid confusion that can create security risks, define clear lines of responsibility and separation of duties.

Based on Microsoft's experience with many cloud adoption projects, establishing clearly defined roles and responsibilities for specific functions in Azure will avoid confusion that can lead to human and automation errors creating security risk.

Recommended role definitions include:

- Network Security
- Network Management
- Server Endpoint Security
- Incident Monitoring and Response
- Policy Management
- Identity Security and Standards

Clearly documenting and identifying the contacts responsible for each function will create consistency and facilitate communication.

**Do the teams have a clear view on responsibilities and individual/group access levels?**
***

Designate groups (or individual roles) that will be responsible for central functions, such as network and policy management, as shown in the following table:

|Central function| Responsibility|
|---|---|
| Network security | Configuration and maintenance of Azure Firewall, Network Virtual Appliances (and associated routing), Web Application Firewall (WAF), Network Security Groups, Application Security Groups (ASG), and other cross-network traffic.
| Network operations | Enterprise-wide virtual network and subnet allocation.
| IT operations| Server endpoint security includes monitoring and remediating server security. This includes tasks such as patching, configuration, endpoint security,and so on. 
| Security operations | Incident monitoring and response to investigate and remediate security incidents in Security Information and Event Management (SIEM) or source console such as Azure Security Center Azure AD Identity Protection.
| Policy management | Apply governance based on risk analysis and compliance requirements. Set direction for use of Azure role-based access control (Azure RBAC), Azure Security Center, Administrator protection strategy, and Azure Policy to govern Azure resources.
|Identity Security and Standards| Set direction for Azure AD directories, PIM/PAM usage, MFA, password/synchronization configuration, Application Identity Standards.

>![Task](../../_images/i-best-practices.svg) Application roles and responsibilities should cover different access level of each operational function. For example, publish production release, access customer data, manipulate database records, and so on. Application teams should include central functions listed in the preceding table.

## Learn more

[Clear lines of responsibility](/azure/architecture/framework/Security/governance#clear-lines-of-responsibility)

## Next

Restrict access to Azure resources based on a need-to-know basis starting with the principle of least privilege security and add more based on your operational needs.

> [!div class="nextstepaction"]
> [Azure control plane security](design-identity-control-plane.md)


## Related links

For considerations about using management groups to reflect the organization's structure within an Azure Active Directory (Azure AD) tenant, see [CAF: Management group and subscription organization](/azure/cloud-adoption-framework/ready/enterprise-scale/management-group-and-subscription-organization).

> Back to the main article: [Azure identity and access management considerations](design-identity.md)
---
title: B2B collaboration for hybrid organizations - Azure Active Directory | Microsoft Docs
description: Give partners access to both on-premises and cloud resources with Azure AD B2B collaboration.
services: active-directory
documentationcenter: ''
author: twooley
manager: mtillman
editor: ''
tags: ''

ms.service: active-directory
ms.topic: article
ms.workload: identity
ms.date: 04/20/2018
ms.author: twooley
ms.reviewer: sasubram

---

# Azure Active Directory B2B collaboration for hybrid organizations

Azure Active Directory (Azure AD) B2B collaboration makes it easy for you to give your external partners access to apps and resources in your organization. This is true even in a hybrid configuration where you have both on-premises and cloud-based resources. It doesn’t matter if you currently manage external partner accounts locally in your on-premises identity system, or if you manage the external accounts in the cloud as Azure AD B2B users. You can now grant these users access to resources in either location, using the same sign-in credentials for both environments.

## Grant B2B users in Azure AD access to your on-premises apps

If your organization uses Azure AD B2B collaboration capabilities to invite guest users from partner organizations to your Azure AD, you can now provide these B2B users access to on-premises apps.

For apps that use SAML-based authentication, you can make these apps available to B2B users through the Azure portal, using Azure AD Application Proxy for authentication.

For apps that use Integrated Windows Authentication (IWA) with Kerberos constrained delegation (KCD), you also use Azure AD Proxy for authentication. However, for authorization to work, a user object is required in the on-premises Windows Server Active Directory. There are two methods you can use to create local user objects that represent your B2B guest users.

- You can use Microsoft Identity Manager (MIM) 2016 SP1 and the MIM management agent for Microsoft Graph. (This requires an Azure AD Premium 1 subscription.)
- You can use a PowerShell script. (This solution does not require MIM or AD Premium.)

For details about how to implement these solutions, see [Grant B2B users in Azure AD access to your on-premises applications](active-directory-b2b-hybrid-cloud-to-on-premises.md).

## Grant locally-managed partner accounts access to cloud resources

Before Azure AD, organizations with on-premises identity systems have traditionally managed partner accounts in their on-premises directory. If you’re such an organization, you want to make sure that your partners continue to have access as you move your apps and other resources to the cloud. Ideally, you want these users to use the same set of credentials to access both cloud and on-premises resources. 

We now offer methods where you can use Azure AD Connect to sync these local accounts to the cloud as "guest users," where the accounts behave just like Azure AD B2B users. This solution works even if you have an on-premises identity system that lets your partners use their own external email addresses as their sign-in name.

To help protect your company data, you can control access to just the right resources, and configure authorization policies that treat these guest users differently from your employees.

For implementation details, see [Grant locally-managed partner accounts access to cloud resources using Azure AD B2B collaboration](active-directory-b2b-hybrid-on-premises-to-cloud.md).
 
## Next steps

- [Grant B2B users in Azure AD access to your on-premises applications](active-directory-b2b-hybrid-cloud-to-on-premises.md)
- [Grant locally-managed partner accounts access to cloud resources using Azure AD B2B collaboration](active-directory-b2b-hybrid-on-premises-to-cloud.md).


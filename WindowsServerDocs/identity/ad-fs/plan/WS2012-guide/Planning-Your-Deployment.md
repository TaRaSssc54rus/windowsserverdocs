---
title: Planning Your Deployment
ms.custom: 
  - AD
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.technology: 
  - techgroup-identity
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9dcfbf94-1517-4c6d-bca1-cca72f2d1865
author: billmath
---
# Planning Your Deployment
When you plan for cross\-organizational \(federation\-based\) collaboration using Active Directory Federation Services \(AD FS\), first determine if your organization will host a Web resource to be accessed by other organizations across the Internet or if you will provide access to the Web resource for employees in your organization. This determination affects how you deploy AD FS, and it is fundamental in the planning of your AD FS infrastructure.  
  
> [!NOTE]  
> Make sure that the role that organization plays in the federation agreement is clearly understood by all parties.  
  
For the [Federated Web SSO Design](../../../ad-fs/plan/WS2012-guide/map-goals-to-plan/Federated-../../../ad-fs/plan/WS2012-guide/map-goals-to-plan/web-sso-design.md), AD FS uses terms such as *account partner* \(also referred to as *identity provider* in the AD FS Management snap\-in\) and *resource partner* \(also referred to as *relying party* in the AD FS Management snap\-in\) to help differentiate the organization that hosts the accounts \(the account partner\) from the organization that hosts the Web\-based resources \(the resource partner\).  
  
In the [Web SSO Design](../../../ad-fs/plan/WS2012-guide/map-goals-to-plan/web-sso-design.md), the organization acts in both the account partner and resource partner roles because it is providing its users with access to its applications.  
  
The following topics explain some of the AD FS partner organization concepts. They also contain links to topics in the AD FS Deployment Guide that contain information about setting up and configuring account partner organizations and resource partner organizations based on your AD FS deployment goals.  
  
## In this section  
  
-   [Best Practices for Secure Planning and Deployment of AD FS](../../../ad-fs/plan/WS2012-guide/deployment/best-practices-secure-planning-deployment-ad-fs.md)  
  
-   [Planning for Interoperability with AD FS 1.x](../../../ad-fs/plan/WS2012-guide/deployment/planning-interoperability-with-ad-fs-1x.md)  
  
-   [When to Use Identity Delegation](../../../ad-fs/plan/WS2012-guide/deployment/when-use-identity-delegation.md)  
  
-   [Deploying AD FS in the Account Partner Organization](Deploying-AD-FS-in-the-Account-Partner-Organization.md)  
  
-   [Deploying AD FS in the Resource Partner Organization](Deploying-AD-FS-in-the-Resource-Partner-Organization.md)  
  

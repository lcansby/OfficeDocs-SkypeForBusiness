---
title: "Teams calling and cloud voice overview"
ms.reviewer: roykuntz
ms.date: 03/04/2025
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.topic: get-started
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.subservice: teams-calling
search.appverid: MET150
ms.collection: 
  - M365-voice
  - m365initiative-voice
  - highpri
  - Tier1
audience: Admin
appliesto: 
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
- CSH
ms.custom: 
  - Phone System
  - intro-overview
description: "Learn about Teams calling with Microsoft cloud voice services in Microsoft 365."
---

# Teams calling overview

This article is for IT administrators and IT professionals who are researching the calling workloads in Microsoft Teams.

## Native Teams calling

The Microsoft Teams application is a Microsoft 365 product that is for users who have either a legacy *Microsoft 365 E5* license or a new, stand-alone, *Microsoft Teams Enterprise* license. Microsoft Teams includes support for native 1:1 calling *and* group calling from one Teams client to any other internal or external Teams clients.

Calls between users in your organization are handled natively within Teams, and never go to the Public Switched Telephone Network (PSTN)--thereby removing long-distance costs on internal calls.

All users licensed for Teams are supported to make calls to other Teams users.

- To support users making Teams calls with users who are *external* to your organization, follow the guidance found in [Collaborate with people outside your organization](communicate-with-users-from-other-organizations.md).

The Calls app in Teams allows users to originate calls to other Teams users, view call history, and access voicemail. It also provides an alternative way to access their forwarding and audio settings.

**Voicemail** - Cloud Voicemail is automatically set up and provisioned for all Teams users. See [Set up Cloud Voicemail](set-up-phone-system-voicemail.md).

With Teams, users in your organization can use a wide range of features to call each other. They can click a name in their address book, and place Teams calls to that person. They make and receive calls using their mobile devices, a headset with a laptop or PC, or one of many certified, third-party IP phones that work with Teams.

Microsoft Teams native calling is turned on for all users, via policy, by default.

> [!NOTE]
> Calling is controlled at the tenant level, per calling policy with the setting [Make private calls](settings-policies-reference.md).
> If the **Make private calls setting** is turned off in the calling policy, users with that policy can't see the **Calls** app in their Teams client, can't escalate Chat conversations to audio calls, and can't receive incoming calls.
> With **Make private calls setting** turned on, users can call from the **Calls** app and escalate Chat conversations to audio calls.

### Administering Teams calling

When planning to support Teams calling in your enterprise, consider the following topics:

#### Administration

Delivery of the Teams calling workload is accomplished through the Microsoft 365 cloud service, and administrators manage the delivery of Teams workloads and features through remote management of that cloud service.

Administration of Teams Phone can be accomplished two ways:

- **PowerShell**
  - To learn more about connecting to Teams and administration with PowerShell, see [Teams PowerShell overview](teams-powershell-overview.md).

- **Teams admin center**
  - For Commercial and Government Community Cloud (GCC) tenants, the url to access Teams admin center is [https://admin.teams.microsoft.com](https://admin.teams.microsoft.com)
  - For Government Community Cloud High (GCCH) tenants the url to access Teams admin center is [https://admin.gov.teams.microsoft.us](https://admin.gov.teams.microsoft.us/)
  
To learn more about Teams admin center, see the following article.

> [!div class="nextstepaction"]
> [Teams admin center overview](manage-teams-in-modern-portal.md)

Administration of Teams features requires a privileged role assigned to the account that is used to access your Teams tenant. For permissions that allow you to administer your tenant (with Teams Admin Center and with PowerShell), and to learn more about Microsoft's RBAC (Role Based Access Control) for Teams, see the following article.

> [!div class="nextstepaction"]
> [Teams administrator roles](using-admin-roles.md)

#### Policies

Microsoft Teams Phone supports a wide array of features, controlled by policy. For example, traditional calling features, like call hold music, call park, call recording, and more, are all administered through policy.
Policies can be applied at a global, group, and user level.

To learn about general Teams policy administration concepts, see the following article.

> [!div class="nextstepaction"]
> [Manage Teams with policies](manage-teams-with-policies.md)

For more information about voice settings that you can manage with Teams policy, see the following article.

> [!div class="nextstepaction"]
> [Manage voice policies](teams-calling-policy.md)

#### Network preparation

For network best practices to support the optimal quality of Teams calls, see the following article.

> [!div class="nextstepaction"]
> [Prepare your organization's network for Microsoft Teams](prepare-network.md)

#### Reporting call activity

Native Teams *call history* for end-users, like other end-user activity, isn't itemized in usage reports for privacy reasons. However, with Microsoft Purview, Teams call metadata can be logged in eDiscovery investigations. To learn more about content reported in compliance investigations, see [Conduct an eDiscovery investigation of content in Microsoft Teams](/microsoft-365/compliance/ediscovery-teams-investigation). For more generic insights, you can report on the overall volume of *call activity* in the following article.

> [!div class="nextstepaction"]
> [Teams usage reporting](./teams-analytics-and-reports/teams-reporting-reference.md)

#### Reporting call performance

Microsoft Teams includes a set of tools that can be used to analyze call quality in real-time for single calls in progress or analyze performance trends of all calls across your organization. For more information on monitoring performance, see the following article.

> [!div class="nextstepaction"]
> [Monitor call quality](monitor-call-quality-qos.md#monitor-and-troubleshoot-call-quality)

#### Teams admin training

A wide range of resources are available for Teams administrators to learn more about Teams foundational and advanced topics. To view training resources for Teams admins, see the following article.

> [!div class="nextstepaction"]
> [Teams admin training](itadmin-readiness.md)

## Teams Phone and enterprise telecommunications

In addition to a rich set of native calling capabilities, Teams can also serve as your organization's telecommunications platform, allowing end users to make and receive domestic and international telephone calls.
To learn more about using Teams as a phone system, see the following article.

> [!div class="nextstepaction"]
> [What is Teams Phone](what-is-phone-system-in-office-365.md)

## Related articles

- [Teams Calling features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [Plan your Teams voice solution](cloud-voice-landing-page.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

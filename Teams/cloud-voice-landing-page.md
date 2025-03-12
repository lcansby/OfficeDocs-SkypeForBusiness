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

Microsoft Teams native calling is turned on via policy, by default.

> [!NOTE]
> Calling is controlled at the tenant level, per calling policy with the setting [Make private calls](settings-policies-reference.md).
> If the **Make private calls setting** is turned off in the calling policy, users with that policy can't see the **Calls** app in their Teams client, can't escalate Chat conversations to audio calls, and can't receive incoming calls.
> With **Make private calls setting** turned on, users can call from the **Calls** app and escalate Chat conversations to audio calls.

### Administering Teams calling

When planning to support Teams calling in your enterprise, consider the following topics:

#### Administration

Delivery of the Teams calling workload is accomplished through the Microsoft 365 cloud service, and administrators manage the delivery of Teams workloads and features through remote management of that cloud service.

To administer Microsoft Teams, a specialized role is assigned to the account that accesses your tenant.
You can use two common methods to administer the Teams service; the Teams admin center (TAC) and PowerShell.

The url for Teams admin center is [https://admin.teams.microsoft.com](https://admin.teams.microsoft.com).

For permissions that allow you to administer your tenant (with Teams Admin Center and with PowerShell), see [Teams administrator roles](using-admin-roles.md).

> [!div class="nextstepaction"]
> [Teams administrator roles](using-admin-roles.md)

#### Policies

Microsoft Teams Phone supports a wide array of features, controlled by policy. For example, traditional calling features, like call hold music, call park, call recording, and more, are all administered through policy.

For more information about settings that you can manage with policy, see [Manage voice policies](teams-calling-policy.md).

> [!div class="nextstepaction"]
> [Manage voice policies](teams-calling-policy.md)

To learn about general Teams policy administration concepts, see [Manage Teams with policies](manage-teams-with-policies.md)

#### Network preparation

For network best practices to support the optimal quality of Teams calls, see [Prepare your organization's network for Microsoft Teams](prepare-network.md).

> [!div class="nextstepaction"]
> [Prepare your organization's network for Microsoft Teams](prepare-network.md)

#### Reporting call activity

Native Teams *call history* for end-users, like other end-user activity, isn't reported for privacy reasons. However, you can report on the volume of *call activity* in the [Teams usage reporting](./teams-analytics-and-reports/teams-reporting-reference.md).

> [!div class="nextstepaction"]
> [Teams usage reporting](./teams-analytics-and-reports/teams-reporting-reference.md)

#### Reporting call performance

Microsoft Teams includes a set of tools that can be used to analyze call quality in real-time for single calls in progress or analyze performance trends of all calls across your organization. For more information on monitoring performance, see [Monitor call quality](monitor-call-quality-qos.md#monitor-and-troubleshoot-call-quality).

> [!div class="nextstepaction"]
> [Monitor call quality](monitor-call-quality-qos.md#monitor-and-troubleshoot-call-quality)

## Teams Phone and enterprise telecommunications

While Teams can provide a rich set of native calling capabilities, Teams can also be connected with the Public Switched Telephone Network (PSTN) and can provide your organization's telecommunications requirements.
To learn more about using Teams as a telephone system, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

> [!div class="nextstepaction"]
> [What is Teams Phone](what-is-phone-system-in-office-365.md)

## Related articles

- [Teams Calling features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [Plan your Teams voice solution](cloud-voice-landing-page.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

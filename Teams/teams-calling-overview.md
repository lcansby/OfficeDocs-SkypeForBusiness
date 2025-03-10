---
title: "Teams calling overview"
ms.reviewer: roykuntz
ms.date: 03/04/2025
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.topic: conceptual
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
description: "Learn about calling with Microsoft Teams in Microsoft 365."
---

# Teams calling overview

This article is for IT administrators and IT professionals who are researching the calling workloads in Microsoft Teams.

### Native Teams calling

The Microsoft Teams application is a Microsoft 365 product that is enabled for users with either a legacy *Microsoft 365 E5* license or with a new, stand-alone, *Microsoft Teams Enterprise* license. Microsoft Teams includes support for native 1:1 calling *and* group calling from one Teams client to any other internal or external Teams client(s).

All users licensed for Teams are supported to make calls to other Teams users.

- To support users making calls to Teams users who are *external* to your organization, follow the guidance found in [Collaborate with people outside your organization](communicate-with-users-from-other-organizations.md).

The Calls app in Teams allows users to originate calls to other Teams users, view call history, and access voicemail. It also provides an alternative way to access their forwarding and audio settings.

Microsoft Teams native calling is enabled in policy, by default.

> [!NOTE]
> Calling is controlled at the tenant level, per calling policy with the setting [Make private calls](settings-policies-reference.md).
> If the **Make private calls setting** is disabled in the calling policy, users with that policy can't see the **Calls** app in their Teams client, can't escalate Chat conversations to audio calls, and can't receive incoming calls.
> With **Make private calls setting** enabled, users can call from the **Calls** app and escalate Chat conversations to audio calls.

### Teams Phone calling

When you grant the **Teams Phone** capability to an account *and* equip your tenant with a Public Switched Telephone Network (PSTN) solution, then Microsoft Teams includes support for 1:1 calling and group calling from a Teams client to any PSTN telephone number.

#### Licensing Teams Phone for end user accounts

All users who need to make and receive telephone calls need to have a Teams Phone license. To learn more about Teams Phone, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

Microsoft's **Teams Phone** capabilities are accomplished by granting a user account with both **Microsoft Teams** and **Microsoft 365 Phone System** applications.

- The ***Microsoft 365 Phone System*** application unlocks additional call control features for a ***Microsoft Teams*** user. To learn about what calling capabilities are included with the base Teams Enterprise license and what additional calling capabilities are unlocked with the Teams Phone license, see [Teams Phone feature overview](here-s-what-you-get-with-phone-system.md).
- 
The following license combinations grant end users with the minimal Teams Phone licensing requirements.

- A ***Microsoft Teams Enterprise*** license combined with a ***Microsoft 365 E5*** license
- A ***Microsoft Teams Enterprise*** license combined with ***Microsoft Teams Phone Standard*** license
- A legacy ***Microsoft 365 E5*** license (includes ***Microsoft Teams Enterprise***)

The legacy and new *Microsoft 365 E5* and the *Microsoft Teams Phone Standard* licenses both include Teams Phone for accounts assigned to end users.

#### Licensing Teams Phone for resource accounts

In scenarios where you are provisioning Teams devices for PSTN calling, for example, from common area phones, shared devices, or an account that is not assigned to an end user, the following specialized licenses are prescribed:

- **Microsoft Teams Shared Devices**
  - applied to resource accounts that support common area telephones
- **Microsoft Teams Room Pro**
  - applied to resource accounts that support audio and video hardware for collaboration spaces
- **Microsoft Teams Phone Resource Account**
  - applied to resource accounts that support voice applications like Teams auto attendants and call queues.

Resource accounts that use these licenses do not require licensing for *Microsoft Teams Enterprise*.

#### PSTN solutions

- A PSTN solution defines how you choose to integrate a PSTN operator with your tenant for PSTN access and phone numbers. Microsoft Teams supports PSTN access natively with Microsoft Calling Plans and supports a variety of partner options that give you the flexibility to architect the best PSTN solution for your business.

> [!NOTE]
> A PSTN solution is separate from a Teams Phone license. A PSTN solution provides a customer's tenant with phone numbers and PSTN access to domestic, international, and emergency calling. The Teams Phone license entitles a Teams user to enhanced calling capabilities within the tenant and access to the PSTN solution.

To learn about all the ways you can connect PSTN access to your tenant, see [PSTN connectivity options](pstn-connectivity.md).

> [!div class="nextstepaction"]
> [PSTN connectivity options](pstn-connectivity.md)

### Considerations

When planning to support Teams calling in your enterprise, consider the following topics:

#### Administration

- For permissions that allow you to administer policy in your tenant (with Teams Admin Center and with PowerShell), see [Teams administrator roles](using-admin-roles.md).

> [!div class="nextstepaction"]
> [Teams administrator roles](using-admin-roles.md)

#### Policy

- To learn about general Teams policy administration concepts, see [Manage Teams with policies](manage-teams-with-policies.md).
- For more details about ***1:1 calling*** settings that you can manage with policy, see [Manage voice policies](teams-calling-policy.md).
- For more details about ***group calling*** settings that you can manage with policy, see [Meeting policy overview](meeting-policies-overview.md) and [Meeting policies reference](settings-policies-reference.md#meeting-policies).

#### Phone numbers

During and after establishing a PSTN soluiton, you will be responsible for acquiring, porting, and managing phone numbers. To learn more about phone number administration, see [Manage phone numbers for your organization](manage-phone-numbers-landing-page.md).

> [!div class="nextstepaction"]
> [Manage phone numbers for your organization](manage-phone-numbers-landing-page.md)

#### Network preparation

For network best practices to support the optimal quality of Teams calls, see [Prepare your organization's network for Microsoft Teams](prepare-network.md).

> [!div class="nextstepaction"]
> [Prepare your organization's network for Microsoft Teams](prepare-network.md)

#### Reporting

- To learn where you can analyze PSTN call usage, see [Microsoft Teams PSTN usage report](./teams-analytics-and-reports/pstn-usage-report.md).
- To learn the various ways you can report on call usage and call performance, see [Improve call quality in Microsoft Teams](monitor-call-quality-qos.md)

#### Advanced calling features

- [Plan for auto attendants and call queues](plan-auto-attendant-call-queue.md)
- [SMS overview](sms-overview.md)
- [Emergency calling](what-are-emergency-locations-addresses-and-call-routing.md)
- [Teams Premium and Copilot](intelligent-recap-calls-meetings.md)

## Related topics

- [Teams Phone features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [Plan your Teams voice solution](cloud-voice-landing-page.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

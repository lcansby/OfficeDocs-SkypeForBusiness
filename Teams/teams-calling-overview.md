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

Microsoft Teams includes support for 1:1 *and* group calling from one Teams client to any other internal or external Teams client(s).

The Calls app in Teams allows users to originate calls to other Teams users, view call history, and access voicemail. It also provides an alternative way to access their forwarding and audio settings.

Microsoft Teams native calling features are enabled by default.

> [!NOTE]
> Calling is controlled at the tenant level, per calling policy with the setting [Make private calls](settings-policies-reference.md).
> If the **Make private calls setting** is disabled in the calling policy, users with that policy can't see the **Calls** app in their Teams client, can't escalate Chat conversations to audio calls, and can't receive incoming calls.
> With **Make private calls setting** enabled, users can call from the **Calls** app and escalate Chat conversations to audio calls.

### Teams Phone calling

When licensed with **Teams Phone** and provisioned with a Public Switched Telephone Network (PSTN) solution, Microsoft Teams also includes support for 1:1 and group calling from a Teams client to any PSTN telephone number.

- A Teams Phone license unlocks additional calling features within the platform. To learn about what calling capabilities are included with the base Teams Enterprise license and what additional calling capabilities are unlocked with the Teams Phone license, see [Teams Phone feature overview](here-s-what-you-get-with-phone-system.md).

- A PSTN solution defines how you choose to integrate a PSTN operator with your tenant for PSTN access and phone numbers. Microsoft Teams supports PSTN access with Microsoft Calling Plans and a variety of partner methods that give you the flexibility to architect the best PSTN solution for your business.

> [!NOTE]
> A PSTN solution is separate from a Teams Phone license. A PSTN solution provides a customer's tenant with phone numbers and PSTN access to domestic, international, and emergency calling. The Teams Phone license entitles a Teams user to enhanced calling capabilities within the tenant and access to the PSTN solution.

### Considerations

When planning to support Teams calling in your enterprise, consider the following topics:

#### Administration

- For permissions that allow you to administer policy in your tenant (with Teams Admin Center and with PowerShell), see [Teams administrator roles](using-admin-roles.md).

#### Licensing

- All users licensed for Teams are supported to make calls to other Teams users.
  - To support users making calls to Teams users who are *external* to your organization, follow the guidance found in [Collaborate with people outside your organization](communicate-with-users-from-other-organizations.md).
- All users who need to make and receive telephone calls need to have a Teams Phone license. To learn more about Teams Phone, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

#### Policy

- To learn about general Teams policy administration concepts, see [Manage Teams with policies](manage-teams-with-policies.md).
- For more details about ***1:1 calling*** settings that you can manage with policy, see [Manage voice policies](teams-calling-policy.md).
- For more details about ***group calling*** settings that you can manage with policy, see [Meeting policy overview](meeting-policies-overview.md) and [Meeting policies reference](settings-policies-reference.md#meeting-policies).
 
#### PSTN solutions

- To learn about all the ways you can connect PSTN access to your tenant, see [PSTN connectivity options](pstn-connectivity.md).

#### Phone numbers

- To learn about acquiring and managing phone numbers, see [Manage phone numbers for your organization](manage-phone-numbers-landing-page.md)

#### Network preparation

- For network best practices to support the optimal quality of Teams calls, see [Prepare your organization's network for Microsoft Teams](prepare-network.md).

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

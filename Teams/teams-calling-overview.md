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

Microsoft Teams native calling features are enabled by default. Calling can be disabled and enabled per calling policy with the [Make private calls setting](settings-policies-reference.md).
If the **Make private calls setting** is disabled in the calling policy, users with that policy will not see the **Calls** app in their Teams client, will not be able to escalate Chat conversations to audio calls, and will not be able to receive incoming calls.

With **Make private calls setting** enabled, users will have native calling capabilities to call from the **Calls** app and escalate Chat conversations to audio calls.

The Calls app in Teams allows users to originate calls to other Teams users, view call history, and access voicemail. It also provides an alternative way to access their forwarding and audio settings.

### Teams Phone calling

When licensed with **Teams Phone** and provisioned with a Public Switched Telephone Network (PSTN) solution, Microsoft Teams also includes support for 1:1 and group calling from a Teams client to any PSTN telephone number.

- A Teams Phone license unlocks additional calling features within the platform. To learn about what calling capabilities are included with the base Teams Enterprise license and what additional calling capabilities are unlocked with the Teams Phone license, see [Teams Phone feature overview](here-s-what-you-get-with-phone-system.md).

- A PSTN solution defines how you choose to integrate a PSTN operator with your tenant for PSTN access and phone numbers. Microsoft Teams supports PSTN access with Microsoft Calling Plans and a variety of partner methods that give customers the flexibility to architect the best PSTN solution for their business.

> [!NOTE]
> A PSTN solution is separate from a Teams Phone license. The Teams Phone license entitles a Teams user to enhanced calling capabilities within the tenant, while a PSTN solution provides a customer's tenant with phone numbers and PSTN access to domestic, international, and emergency calling.

### Calling governance

Microsoft Teams communication workloads can be categorized into three areas:

- Teams meetings
- Teams calls
- Teams Phone calls

Microsoft Teams calls and Phone calls are differentiated from Microsoft Teams meetings, in that native Teams calls and Teams Phone calls are originated as ***calls***, whereas Teams meetings are originated as ad-hoc or scheduled ***events***.

The following visual represents these categories.

:::image type="content" source="media/teams-voice-calling-policy-scope-small.png" alt-text="Screenshot that shows overview of the SMS enablement process for Teams Calling Plan numbers." lightbox="media/teams-voice-calling-policy-scope-small.png":::

One key takeaway from this diagram is understanding that a Teams *1:1 call* is managed by a calling policy and a Teams *group call* is managed by a meeting policy.

In the case where a Teams user starts a 1:1 call and then adds another party to the call, Teams moves the call from a peer-to-peer connection to a Teams conference connection anchored in the Teams meeting service, and governance moves from the user's calling policy to the user's meeting policy.

> [!NOTE]
> If a user's calling policy setting is configured one way and their meeting policy is configured differently, they will have (and may report) different client experiences depending on whether they are in a call or a meeting. Microsoft recommends aligning a user's calling policy settings to match their meeting policy settings.

The scope of this calling overview includes **Teams calls** and **Teams Phone calls**. For scope related to Teams meetings, see [Overview of meetings, webinars, and town halls](overview-meetings-webinars-town-halls.md).

### Considerations

When planning to support Teams calling in your enterprise, consider the following topics:

#### Licensing

- All users licensed for Teams can make calls to other Teams users
  - To support users making calls to Teams users who are *external* to your organization, follow the guidance found in [Collaborate with people outside your organization](communicate-with-users-from-other-organizations.md).
- All users who need to make and receive telephone calls need to have a Teams Phone license. To learn more about Teams Phone, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

#### Administration

- For permissions that allow you to administer policy in your tenant (either with Teams Admin Center or with PowerShell), see [Teams administrator roles](using-admin-roles.md).

#### Policy

- To learn about general Teams policy administration concepts, see [Manage Teams with policies](manage-teams-with-policies.md).
- For more details about ***1:1 calling*** settings that you can manage with policy, see [Manage voice policies](teams-calling-policy.md).
- For more details about ***group calling*** settings that you can manage with policy, see [Meeting policy overview](meeting-policies-overview.md) and [Meeting policies reference](settings-policies-reference.md#meeting-policies).
 
#### PSTN solutions

- To learn about all the ways you can connect PSTN access to your tenant, see [PSTN connectivity options](pstn-connectivity.md).

#### Network preparation

- For network best practices to support the optimal quality of Teams calls, see [Prepare your organization's network for Microsoft Teams](prepare-network.md).

#### Reporting

- To learn where you can analyze PSTN call usage, see [Microsoft Teams PSTN usage report](./teams-analytics-and-reports/pstn-usage-report.md).
- To learn the various ways you can report on call usage and call performance, see [Improve call quality in Microsoft Teams](monitor-call-quality-qos.md)

## Related topics

- [Teams Phone features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [Plan your Teams voice solution](cloud-voice-landing-page.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

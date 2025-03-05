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

Microsoft Teams includes support for 1:1 *and* group calling from one Teams client to any other internal or external Teams client(s).

When licensed with **Teams Phone** and provisioned with a Public Switched Telephone Network (PSTN) solution, Microsoft Teams also includes support for 1:1 and group calling from a Teams client to any PSTN telephone number.

Microsoft Teams group calling is differentiated from Microsoft Teams meetings, in that meetings are originated as ad-hoc or scheduled ***events***, whereas group calls are originated as ***calls***.

Microsoft Teams communication workloads can be categorized into three areas:

 - Teams meetings
 - Teams group calls
 - Teams calls

The following visual represents these categories and the respective policies that govern their capabilities.

:::image type="content" source="media/teams-voice-calling-policy-scope-small.png" alt-text="Screenshot that shows overview of the SMS enablement process for Teams Calling Plan numbers." lightbox="media/teams-voice-calling-policy-scope-small.png":::

The scope of this calling overview includes Teams calls and group calls. For scope related to Teams meetings, see [Overview of meetings, webinars, and town halls](overview-meetings-webinars-town-halls.md).

When planning to support Teams calling in your enterprise, consider the following topics:

- Licensing
    - All users licensed for Teams can make calls to other Teams users
        - To support users making calls to Teams users who are external to your organization, follow the guidance found in [Collaborate with people outside your organization](communicate-with-users-from-other-organizations.md).
    - All users who need a dedicated phone number for making and receiving telephone calls need to have a Teams Phone license. To learn more about Teams Phone, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

- Policy
    - For permissions that allow you to administer policy in your tenant (either with Teams Admin Center or with PowerShell), see [Teams administrator roles](using-admin-roles.md).
    - To learn about general Teams policy administration concepts, see [Manage Teams with policies](manage-teams-with-policies.md).
    - For more details about 1:1 calling settings that you can manage with policy, see [Manage voice policies](teams-calling-policy.md).
    - For more details about group call settings that you can manage with policy, see [Meeting policy overview](meeting-policies-overview.md) and [Meeting policies reference](settings-policies-reference.md#meeting-policies).

- Capabilities
    - To learn about what calling capabilities are included with the base Teams Enterprise license and additional calling capabilities that are unlocked with the Teams Phone license, see [Teams Phone feature overview](ere-s-what-you-get-with-phone-system.md).
 
- PSTN solutions
    - To learn about all the ways you can connect PSTN access to your tenant, see [PSTN connectivity options](pstn-connectivity.md).

- Network preparation
    - For network best practices to support the optimal quality of Teams calls, see [Prepare your organization's network for Microsoft Teams](prepare-network.md).

- Reporting
    - To learn where you can analyze PSTN call usage, see [Microsoft Teams PSTN usage report](pstn-usage-report.md).
    - To learn the various ways you can report on call usage and call performance, see [Set up call analytics for Microsoft Teams](set-up-call-analytics.md), [What is CQD?](cqd-what-is-call-quality-dashboard.md), and [Improve call quality in Microsoft Teams](monitor-call-quality-qos.md)

## Related topics

- [Teams Phone features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [Plan your Teams voice solution](cloud-voice-landing-page.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

---
title: "Teams Phone licensing"
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
description: "Applying Teams Phone licensing."
---
# Teams Phone licensing

This article is for IT administrators and IT professionals who are managing Teams Phone workloads for an organization and want to understand the scenarios of assigning licenses to user and resource accounts.

To learn more about Teams Phone, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

### Understanding identity management for Teams Phone

The way telephone numbers get assigned to users and to shared devices is by assigning the number to the respective user's or device's user account.

A user account must exist and be licensed before a phone number can be assigned.
To learn more about creating accounts in M365, see [Add users](/microsoft-365/admin/add-users/add-users).

To learn more about assigning licenses in M365, see [Assign Microsoft 365 licenses to user accounts](/microsoft-365/enterprise/assign-licenses-to-user-accounts).

To learn more about deploying Teams as your productivity platform, see [Set up Teams in your org](deploy-enterprise-setup.md) and [Sign in to Microsoft Teams](sign-in-teams.md).

### Understanding M365 licensing for M365 Phone System

Granting an application to a user or resource account is accomplished by assigning *a license* that includes the necessary application.

For example, if you need to set up an existing user to have Teams Phone, your first step is to assign their user account with a ***Microsoft Teams Phone Standard*** license, granting the user account with an ability to use the **Microsoft 365 Phone System** application.

Alternatively, you can assign the user account with a ***Microsoft 365 E5 (no Teams)*** license, which includes--and equips the user account with an ability to use--the **Microsoft 365 Phone System** application. In the case where an M365 E5 license is used, it isn't necessary to also assign the stand-alone ***Microsoft Teams Phone Standard*** license.

To learn more about administering M365 licenses, see [Assign or unassign licenses for users](/microsoft-365/admin/manage/assign-licenses-to-users).

### Licensing Teams Phone for end users

At a minimum, all users who require their own telephone number to make and receive telephone calls must be assigned with licenses that granted the **Microsoft Teams** and **Microsoft 365 Phone System** applications.

The **Microsoft 365 Phone System** application unlocks more calling features for a **Microsoft Teams** user. To compare native calling capabilities included with Teams Enterprise to PSTN calling capabilities included with Teams Phone, see [Teams Phone feature overview](here-s-what-you-get-with-phone-system.md).

Presuming your end users need licensing that grants them **Microsoft Teams** and **Microsoft 365 Phone System**, there are various potential license assignment combinations available to meet the requirement.

Assigning the following license combinations are examples of granting end users the ability to use Teams Phone.

- A ***Microsoft Teams Enterprise*** license combined with a ***Microsoft 365 E5 (no Teams)*** license - *Microsoft 365 E5 (no Teams) includes the **Microsoft 365 Phone System** application*
- A ***Microsoft Teams Enterprise*** license combined with ***Microsoft Teams Phone Standard*** license
- A legacy ***Microsoft 365 E5*** license - *includes **Microsoft Teams** and **Microsoft 365 Phone System** applications.*
- A ***Office 365 F3*** license combined with a ***Microsoft Teams Phone Standard for Frontline Workers*** license.

There are three variations on the **Microsoft Teams Phone Standard** license, each requiring the purchase of a Prerequisite License as listed in the following table:

|**License** |**Prerequisite License(s)** |
|:-----|:-----|
|Microsoft Teams Phone Standard |Microsoft 365 Business Basic/Business Standard/Business Premium/F1/F3/E3/A3; Microsoft Teams EEA; Microsoft Teams Enterprise; Microsoft Teams Essentials (AAD Identity); Office 365 F3/E1/E3/A1/A3 |
|Microsoft Teams Phone Standard for Frontline Workers	|Microsoft 365 F1/F3; Office 365 F3 |
|Microsoft Teams Phone with Calling Plan |Microsoft 365 Business Basic/Business Standard/Business Premium/F1/F3/E3/A3; Microsoft Teams EEA; Microsoft Teams Enterprise; Microsoft Teams Essentials (AAD Identity); Office 365 F3/E1/E3/A1/A3 |

### Licensing Teams Phone for shared devices

In scenarios requiring that phone calls can be made to or from communication devices shared by many users, you can use one of the following specialized licenses:

- [***Microsoft Teams Shared Device*** license](./phones/phones-for-teams.md) - *applied to resource accounts that support common area telephones*
- [***Microsoft Teams Room Pro*** license](./rooms/rooms-licensing.md) - *applied to resource accounts that support audio and video hardware for shared collaboration spaces*

The **Microsoft 365 Phone System** application is included in each of these specialized licenses.

### Licensing Teams Phone for voice applications

In scenarios where you're provisioning voice applications, you can use the following specialized license:

- [***Microsoft Teams Phone Resource Account*** license](manage-resource-accounts.md#obtain-microsoft-teams-phone-resource-account-licenses) - *applied to resource accounts that support voice applications, like Teams auto attendants and call queues.*

## Licensing Teams Phone and adding PSTN

Assigning necessary licenses to an account is one prerequisite to setting up Teams Phone. Another key prerequisite is integrating your tenant with a Public Switched Telephone Network (PSTN) solution.

With a PSTN access to your tenant and licensed users, Microsoft Teams Phone provides support for 1:1 calling and group calling between a Teams client--and any PSTN telephone number.

> [!NOTE]
> A PSTN solution is separate from a Teams Phone license. A **PSTN solution** provides a customer's tenant with phone numbers and PSTN access to domestic, international, and emergency calling. The ***Teams Phone licensing*** entitles a Teams user to use **Microsoft 365 Phone System** application and its enhanced calling capabilities, and *access* to the PSTN solution.

If you elect to use Microsoft to provide your PSTN access and phone numbers, in addition to Teams Phone licensing, the user also requires a Microsoft Calling Plan license. To learn more, see [Microsoft Calling Plans](calling-plans-for-office-365.md).

If you elect to use a PSTN operator other than Microsoft, then Microsoft doesn't require other licensing because the PSTN costs are incurred from your preferred operator.

There is no cost to integrate third-party PSTN operators with your Teams tenant. 

To learn more, see [PSTN connectivity options](pstn-connectivity.md).

The ***Teams Phone with Calling Plan*** license bundle is Microsoft’s all-in-the-cloud solution. This option provides Private Branch Exchange (PBX) capabilities and external calls to the Public Switched Telephone Network (PSTN) with Microsoft as your carrier. If the Teams Phone with Calling Plan bundle is available in your location and you don't already have a ***Microsoft 365 E5*** or ***Office 365 E5*** license that includes the **Microsoft 365 Phone System** application, you should consider this option. But if your PSTN calling requirements are more complex, Microsoft offers several PSTN connectivity options for making external calls.

### Licensing Teams Phone for Shared Calling

Microsoft Teams can support multiple users sharing a single phone number. In this scenario, a resource account is provisioned with Teams Phone and a telephone number, and then you grant a policy to users that allows them to access the phone number of the resource account to make outbound calls.

With Shared Calling, end users don't need a dedicated phone number or a calling plan. They only require licensing described in [Licensing Teams Phone for end users](#licensing-teams-phone-for-end-users). 

Shared Calling is a cost-effective way to give users a way to make outbound calls, without allocating a calling plan and a phone number to every user.

To learn more about Shared Calling, see [Plan for Shared Calling](shared-calling-plan.md).

### Considerations

[Licensing Teams Phone for shared devices](#licensing-teams-phone-for-shared-devices) and [Licensing Teams Phone for voice applications](#licensing-teams-phone-for-voice-applications) doesn't also require licensing for the ***Microsoft Teams Enterprise*** application because they're only using the Teams calling workload.

***Microsoft Teams Shared Device*** licenses are supported only for telephone devices.

For more information about licenses to use with Teams, see [Teams add-on license options](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md).

For next steps, see [Set up Teams Phone](setting-up-your-phone-system.md).

## Related articles

- [Teams calling overview](cloud-voice-landing-page.md)
- [What is Teams Phone](what-is-phone-system-in-office-365.md)
- [Teams Phone features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

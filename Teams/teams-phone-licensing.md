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

A user account must exist and be licensed before a phone number can be assigned. To learn more about identity management and licensing in M365, see [Assign Microsoft 365 licenses to user accounts](/microsoft-365/enterprise/assign-licenses-to-user-accounts).

To support the users signing into Teams so they can use Teams Phone, see [Set up Teams in your org](deploy-enterprise-setup.md) and [Sign in to Microsoft Teams](sign-in-teams.md).

### Understanding M365 licensing for M365 Phone System

Granting an application to a user or resource account is accomplished by assigning *a license* that includes the necessary application.

For example, if you need to set up an existing user to have Teams Phone, your first step is to assign their user account with a ***Microsoft Teams Phone Standard*** license, granting the user account with an ability to use the **Microsoft 365 Phone System** application.

Alternatively, you can assign the user account with a ***Microsoft 365 E5 (no Teams)*** license, which includes--and equips the user account with an ability to use--the **Microsoft 365 Phone System** application. In the case where an M365 E5 license is used, it isn't necessary to also assign the stand-alone ***Microsoft Teams Phone Standard*** license.

To learn more about administering M365 licenses, see [Assign or unassign licenses for users](/microsoft-365/admin/manage/assign-licenses-to-users).

### Licensing Teams Phone for end users

All users who require their own telephone number to make and receive telephone calls need to be granted the **Microsoft Teams** and **Microsoft 365 Phone System** applications.

The following license combinations grant end users with the minimal Teams Phone licensing requirements.

- A ***Microsoft Teams Enterprise*** license combined with a ***Microsoft 365 E5*** license
- A ***Microsoft Teams Enterprise*** license combined with ***Microsoft Teams Phone Standard*** license
- A legacy ***Microsoft 365 E5*** license (includes ***Microsoft Teams Enterprise***)

- The ***Microsoft 365 Phone System*** application unlocks more calling features for a ***Microsoft Teams*** user. To learn about calling capabilities included with the base Teams Enterprise license and calling capabilities included with a Teams Phone license, see [Teams Phone feature overview](here-s-what-you-get-with-phone-system.md).

### Licensing Teams Phone for Shared Calling

Microsoft Teams can support multiple users sharing a single phone number. In this scenario, a resource account is provisioned with Teams Phone, and then you grant a policy to users that allows them to access the phone number of the resource account to make outbound calls.

End users only require a **Microsoft Teams** license. Shared Calling is a cost-effective way to give users a way to make outbound calls, without allocating a Teams Phone license and a phone number to every user.

To learn more about Shared Calling, see [Plan for Shared Calling](shared-calling-plan.md).

### Licensing Teams Phone for resource accounts

In scenarios where you have common area phones, shared devices, or voice applications, you can use one of the following specialized licenses:

- [Microsoft Teams Shared Devices](./phones/phones-for-teams.md) - applied to resource accounts that support common area telephones
- [Microsoft Teams Room Pro](./rooms/rooms-licensing.md) - applied to resource accounts that support audio and video hardware for shared collaboration spaces
- [Microsoft Teams Phone Resource Account](manage-resource-accounts.md#obtain-microsoft-teams-phone-resource-account-licenses) - applied to resource accounts that support voice applications like Teams auto attendants and call queues.

Resource accounts that use these licenses don't require licensing for the ***Microsoft Teams Enterprise*** application because they're only using the Teams calling workload.

For more information about licenses to use with Teams Phone, see [Teams add-on license options](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md).

## Licensing Teams Phone and adding PSTN

Assigning necessary licenses to an account is one prerequisite to setting up Teams Phone. Another key prerequisite is integrating your tenant with a Public Switched Telephone Network (PSTN) solution.

With a PSTN access to your tenant and licensed users, Microsoft Teams Phone provides support for 1:1 calling and group calling between a Teams client--and any PSTN telephone number.

> [!NOTE]
> A PSTN solution is separate from a Teams Phone license. A **PSTN solution** provides a customer's tenant with phone numbers and PSTN access to domestic, international, and emergency calling. The Teams Phone **license** entitles a Teams user to *enhanced calling capabilities* within the tenant and *access* to the PSTN solution.

One of the PSTN solutions is provided by Microsoft. If you elect to use Microsoft to integrate your tenant with the PSTN, the user requires a Microsoft Calling Plan license.

If you elect to use other Operators to integrate your tenant with the PSTN, then Microsoft will not require additional licensing, but the PSTN costs will be incurred from the Operator.

For more information on PSTN Connectivity, see [PSTN connectivity options](pstn-connectivity.md).

For next steps, see [Set up Teams Phone](setting-up-your-phone-system.md).

## Related articles

- [Teams calling overview](cloud-voice-landing-page.md)
- [What is Teams Phone](what-is-phone-system-in-office-365.md)
- [Teams Phone features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

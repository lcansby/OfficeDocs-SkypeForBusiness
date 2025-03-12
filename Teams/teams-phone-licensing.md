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

This article is for IT administrators and IT professionals who are managing Teams Phone workloads for an organization and want to understand the scenarios of assigning licenses to user and resoruce accounts.

### Identity management

The way telephone numbers get assigned to people and to shared devices is by assigning the number to a user account. A user account must exist and be licensed before a phone number can be assigned. To learn more about identity management and licensing in M365, see [Assign Microsoft 365 licenses to user accounts](/microsoft-365/enterprise/assign-licenses-to-user-accounts).
To support the users signing into Teams so they can use Teams Phone, see [Set up Teams in your org](deploy-enterprise-setup.md) and [Sign in to Microsoft Teams](sign-in-teams.md).

## Teams Phone calling

When you grant the **Teams Phone** capability to an account *and* equip your tenant with a Public Switched Telephone Network (PSTN) solution, then Microsoft Teams includes support for 1:1 calling and group calling from a Teams client to any PSTN telephone number.

### Licensing end user accounts with Teams Phone

All users who need to make and receive telephone calls need to have a Teams Phone license. To learn more about Teams Phone, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

Microsoft's **Teams Phone** capabilities are accomplished by granting a user account with both **Microsoft Teams** and **Microsoft 365 Phone System** applications.

- The ***Microsoft 365 Phone System*** application unlocks additional call control features for a ***Microsoft Teams*** user. To learn about what calling capabilities are included with the base Teams Enterprise license and what additional calling capabilities are unlocked with the Teams Phone license, see [Teams Phone feature overview](here-s-what-you-get-with-phone-system.md).

The following license combinations grant end users with the minimal Teams Phone licensing requirements.

- A ***Microsoft Teams Enterprise*** license combined with a ***Microsoft 365 E5*** license
- A ***Microsoft Teams Enterprise*** license combined with ***Microsoft Teams Phone Standard*** license
- A legacy ***Microsoft 365 E5*** license (includes ***Microsoft Teams Enterprise***)

The legacy and new *Microsoft 365 E5* and the *Microsoft Teams Phone Standard* licenses all include Teams Phone for accounts assigned to end users.

> [!NOTE]
> In addition to licensing, the user must be "voice enabled." To voice enable your users, you can use the Teams admin center or PowerShell.</br>
>
> - In the Teams admin center, go to a **Users** > **Manage users** and select the user you want to edit. Under the **Account** tab > **Assigned phone number**, turn **Enterprise Voice** to **On** and select **Save**.
> - For PowerShell, use the [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) cmdlet and set the `-EnterpriseVoiceEnabled` parameter to `$true`.

#### Licensing Teams Phone for resource accounts

In scenarios where you want to provision Teams devices for PSTN calling, for example, from common area phones, shared devices, or an account that isn't assigned to an end user, you must assign one of the following specialized licenses:

- [Microsoft Teams Shared Devices](./phones/phones-for-teams.md) - applied to resource accounts that support common area telephones
- [Microsoft Teams Room Pro](./rooms/rooms-licensing.md) - applied to resource accounts that support audio and video hardware for collaboration spaces
- [Microsoft Teams Phone Resource Account](manage-resource-accounts.md#obtain-microsoft-teams-phone-resource-account-licenses) - applied to resource accounts that support voice applications like Teams auto attendants and call queues.

Resource accounts that use these licenses don't require licensing for *Microsoft Teams Enterprise*.

For more information about licenses to use with Teams Phone, see [Teams add-on license options](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md).

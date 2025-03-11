---
title: "What is Teams Phone"
ms.reviewer: roykuntz
ms.date: 03/07/2024
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.topic: concept-article
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
  - seo-marvel-apr2020
  - intro-overview
description: "In this article, you'll learn about Microsoft Teams Phone System technology in Microsoft 365."
---

# What is Teams Phone

This article is for administrators and IT professionals who are evaluating Microsoft Teams Phone--Microsoft's technology for enabling call control and Private Branch Exchange (PBX) capabilities in the Microsoft 365 cloud.

Teams Phone works with Teams clients and certified devices. Teams Phone allows you to replace your existing PBX system with a set of features directly delivered from Microsoft 365.

Calls between users in your organization are handled internally within Teams Phone, and never go to the Public Switched Telephone Network (PSTN)--thereby removing long-distance costs on internal calls. 

For making external calls, Teams Phone provides add-on options for connecting to the PSTN. For more information about voice solutions and PSTN connectivity options, see [Plan your Teams voice solution](cloud-voice-landing-page.md) and [Connect to the PSTN](#connect-to-the-public-switched-telephone-network-pstn). 

</br>
#### Identity management

The way telephone numbers get assigned to people and to shared devices is by assigning the number to a user account. A user account must exist and be licensed before a phone number can be assigned. To learn more about identity management and licensing in M365, see [Assign Microsoft 365 licenses to user accounts](/microsoft-365/enterprise/assign-licenses-to-user-accounts).
To support the users signing into Teams so they can use Teams Phone, see [Set up Teams in your org](deploy-enterprise-setup.md) and [Sign in to Microsoft Teams](sign-in-teams.md).

## Teams Phone calling

When you grant the **Teams Phone** capability to an account *and* equip your tenant with a Public Switched Telephone Network (PSTN) solution, then Microsoft Teams includes support for 1:1 calling and group calling from a Teams client to any PSTN telephone number.

### Licensing Teams Phone for end user accounts

All users who need to make and receive telephone calls need to have a Teams Phone license. To learn more about Teams Phone, see [What is Teams Phone](what-is-phone-system-in-office-365.md).

Microsoft's **Teams Phone** capabilities are accomplished by granting a user account with both **Microsoft Teams** and **Microsoft 365 Phone System** applications.

- The ***Microsoft 365 Phone System*** application unlocks additional call control features for a ***Microsoft Teams*** user. To learn about what calling capabilities are included with the base Teams Enterprise license and what additional calling capabilities are unlocked with the Teams Phone license, see [Teams Phone feature overview](here-s-what-you-get-with-phone-system.md).

The following license combinations grant end users with the minimal Teams Phone licensing requirements.

- A ***Microsoft Teams Enterprise*** license combined with a ***Microsoft 365 E5*** license
- A ***Microsoft Teams Enterprise*** license combined with ***Microsoft Teams Phone Standard*** license
- A legacy ***Microsoft 365 E5*** license (includes ***Microsoft Teams Enterprise***)

The legacy and new *Microsoft 365 E5* and the *Microsoft Teams Phone Standard* licenses both include Teams Phone for accounts assigned to end users.

For more information about licenses to use with Teams Phone, see [Teams add-on license options](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md).

#### Licensing Teams Phone for resource accounts

In scenarios where you want to provision Teams devices for PSTN calling, for example, from common area phones, shared devices, or an account that isn't assigned to an end user, you must assign one of the following specialized licenses:

- [Microsoft Teams Shared Devices](./phones/phones-for-teams.md) - applied to resource accounts that support common area telephones
- [Microsoft Teams Room Pro](./rooms/rooms-licensing.md) - applied to resource accounts that support audio and video hardware for collaboration spaces
- [Microsoft Teams Phone Resource Account](manage-resource-accounts.md#obtain-microsoft-teams-phone-resource-account-licenses) - applied to resource accounts that support voice applications like Teams auto attendants and call queues.

Resource accounts that use these licenses don't require licensing for *Microsoft Teams Enterprise*.

#### PSTN solutions

A PSTN solution defines how you choose to integrate a PSTN operator with your tenant for PSTN access and phone numbers. Microsoft Teams supports PSTN access natively with Microsoft Calling Plans and supports a variety of partner options that give you the flexibility to architect the best PSTN solution for your business.

> [!NOTE]
> A PSTN solution is separate from a Teams Phone license. A PSTN solution provides a customer's tenant with phone numbers and PSTN access to domestic, international, and emergency calling. The Teams Phone license entitles a Teams user to enhanced calling capabilities within the tenant and access to the PSTN solution.

To connect Teams Phone to the PSTN, you can choose from one or any combination of the following options:

- [**Calling Plan**](calling-plans-for-office-365.md) - An all-in-the-cloud solution with Microsoft as your PSTN operator.
- [**Operator Connect**](operator-connect-plan.md) - With Operator Connect, PSTN operators who participate in Microsoft's Operator Connect program provide your tenant's PSTN access, phone numbers, and usage plans.
- [**Teams Phone Mobile**](operator-connect-mobile-plan.md) - With Microsoft Teams Phone Mobile, a user’s SIM-enabled phone number is also their Teams phone number.
- [**Direct Routing**](direct-routing-plan.md) - Enables you to use your own PSTN operator through a Session Border Controller intergration to your tenant, known as Direct Routing.

To learn about all the ways you can connect your tenant with the PSTN, see [PSTN connectivity options](pstn-connectivity.md).

> [!div class="nextstepaction"]
> [PSTN connectivity options](pstn-connectivity.md)

### Phone numbers

During and after establishing a PSTN solution, you might need to acquire, port, and manage phone numbers. To learn more about phone number administration, see [Manage phone numbers for your organization](manage-phone-numbers-landing-page.md).

> [!div class="nextstepaction"]
> [Manage phone numbers for your organization](manage-phone-numbers-landing-page.md)

### Advanced calling features

For information on advanced calling features, see the following articles:

- [Plan for auto attendants and call queues](plan-auto-attendant-call-queue.md)
- [SMS in Teams overview](sms-overview.md)
- [Emergency calling](what-are-emergency-locations-addresses-and-call-routing.md)
- [Teams Premium and Copilot](intelligent-recap-calls-meetings.md)
- [Queues app](manage-queues-app.md)
</br>

### Licenses and voice enablement 

To use Teams Phone features, your users must have a Teams Phone Standard or E5 license. For more information about licensing, see [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md).

In addition to licensing, the users must be "voice enabled."

To voice enable your users, you can use the Teams admin center or PowerShell.

- In the Teams admin center, go to a **Users** > **Manage users** and select the user you want to edit. Under the **Account** tab > **Assigned phone number**, turn **Enterprise Voice** to **On** and select **Save**.
- For PowerShell, use the [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) cmdlet and set the `-EnterpriseVoiceEnabled` parameter to `$true`.

## Teams Phone features

With Teams Phone, users in your organization can use Teams to place and receive calls, transfer calls, and mute or unmute calls. Teams Phone users can click a name in their address book, and place Teams calls to that person. To place and receive calls, Teams Phone users can use their mobile devices, a headset with a laptop or PC, or one of many IP phones that work with Teams. 

For more information about Teams Phone features, including which features require a user to be voice enabled, see [Teams Phone features](here-s-what-you-get-with-phone-system.md).

You can manage calling options and settings by using the Teams admin center and by using PowerShell.

## Connect to the Public Switched Telephone Network (PSTN)
  
For external calling, Teams Phone can be connected to the PSTN in one of several ways:
  
- Purchase a Microsoft Calling Plan (domestic or domestic and international). Microsoft Calling Plan is an all-in-the-cloud solution with Microsoft as your PSTN carrier. For more information, see [Teams Phone and Calling Plans](calling-plan-landing-page.md).

- Use your existing telephony infrastructure for on-premises PSTN connectivity.

  You can connect your on-premises telephony infrastructure to Teams Phone by using Operator Connect or Direct Routing. 

For more information about all PSTN Connectivity options, see [PSTN connectivity options](pstn-connectivity.md).


## Teams Phone with services

Teams Phone can be used for services and voicemail, such as:

- **Auto attendants** -  Auto attendants can be used to create a menu system for your organization that lets external and internal callers move through the system to locate and place or transfer calls to company users or departments in your organization. See [What are Cloud auto attendants?](what-are-phone-system-auto-attendants.md).

- **Call queues** -  Call queue greetings can be used when someone calls in to a phone number for your organization. These greetings include the ability to automatically put the calls on hold and to search for the next available call agent to handle the call. The people on hold can also listen to music while on hold. You can create single or multiple call queues for your organization. See [Create a Cloud call queue](create-a-phone-system-call-queue.md).

- **Voicemail** - Cloud Voicemail is automatically set up and provisioned for all Teams users. See [Set up Cloud Voicemail](set-up-phone-system-voicemail.md).

For more information about features, see [Here's what you get with Teams Phone](here-s-what-you-get-with-phone-system.md). If you're ready to get started, see [Set up Teams Phone in your organization](setting-up-your-phone-system.md).

## Related topics

- [Teams Phone features](here-s-what-you-get-with-phone-system.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [Plan your Teams voice solution](cloud-voice-landing-page.md)
- [PSTN connectivity options](pstn-connectivity.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)

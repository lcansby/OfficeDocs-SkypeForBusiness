---
title: "Acquire phone numbers for your organization"
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: pavellatif
ms.date: 2/27/2025
ms.topic: conceptual
ms.assetid: 6b61cb3c-361c-48a8-a9ef-d81bddde27bb
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
  - Skype for Business
  - Microsoft Teams
ms.localizationpriority: Medium
f1.keywords:
- CSH
ms.custom: 
  - ms.teamsadmincenter.voice.phonenumbers.overview
  - ms.teamsadmincenter.voice.searchandacquire.PSTNpartner
  - ms.lync.lac.NewNumberManualAcquisitionOpenSupportTicket
  - ms.lync.lac.VASAMissingGeoCodes
  - Calling Plans
  - seo-marvel-apr2020
description: Learn how to get telephone numbers for Microsoft Teams for your organization.
---

# Get telelephone numbers in Microsoft Teams

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Microsoft Calling Plans, Operator Connect, Teams Phone Mobile, and Direct Routing

This article provides an overview and considerations for getting phone numbers in Microsoft Teams.

Telephone numbers are not included with user accounts equipped with [Teams Phone licensing](teams-phone-licensing.md), although once you acquire telephone numbers and have them in your tenant, you can assign the numbers to licensed users.

Telephone numbers come from your chosen Public Switched Telephone Network (PSTN) service provider. To learn more about the PSTN integrations available to you, see [PSTN Connectivity options](pstn-connectivity.md).

Microsoft Teams includes a telephone number inventory and management service as part of the product. Teams supports the following methods for getting telephone numbers into your tenant.

- Acquire new numbers from Microsoft
- Acquire new numbers from an Operator Connect or Teams Phone Mobile partner
- Upload new numbers from a Direct Routing partner
- Migrate, or port in, telephone numbers that you've already acquired from an existing service provider to Microsoft Calling Plans, or to an Operator Connect, Teams Phone Mobile, or Direct Routing partner.

Once numbers are acquired and available in your tenant, regardless of PSTN connectivity solution, they can be managed in the following administrative tools:

- Teams admin center (TAC)
- Teams PowerShell
- On-premises Active Directory (for Direct Routing on-premises numbers)

To learn more, see [Manage phone numbers for users](assign-change-or-remove-a-phone-number-for-a-user.md).

## Prerequisites

Before you can get telephone numbers in Teams, you must have a phone number services agreement and a tenant integration with one or more PSTN service providers. To learn more, see [PSTN Connectivity options](pstn-connectivity.md).

### Acquiring and managing telephone numbers

How you acquire and manage telephone numbers depends on the option of your Public Switched Telephone Network (PSTN) connectivity solution. Use the following table to navigate to your PSTN solution:

|PSTN connectivity solution |Guidance for acquiring and managing numbers |
|:-----|:-----|
|Microsoft Calling Plan |[Get phone numbers with Microsoft Calling Plans](getting-phone-numbers-for-your-users.md) |
|Operator Connect |[Get phone numbers with Operator Connect](get-phone-numbers-with-operator-connect.md) |
|Teams Phone Mobile |[Get phone numbers with Teams Phone Mobile](operator-connect-mobile-configure.md#step-2-manage-phone-numbers-and-assign-licenses)|
|Direct Routing |[Get phone numbers with Direct Routing](get-phone-numbers-with-direct-routing.md) |

## Related articles

- [Set up telephone numbers with Calling Plans](manage-phone-numbers-for-your-organization/manage-phone-numbers-for-your-organization.md)

- [Set up telephone numbers with Operator Connect](operator-connect-configure.md#set-up-phone-numbers)

- [Set up telephone numbers with Teams Phone Mobile](operator-connect-mobile-configure.md#step-2-manage-phone-numbers-and-assign-licenses)

- [Set up telephone numbers with Direct Routing](direct-routing-enable-users.md#configure-the-phone-number-and-enable-enterprise-voice)

- [Manage phone numbers for users](assign-change-or-remove-a-phone-number-for-a-user.md)

- [Plan Direct Routing](direct-routing-plan.md)

- [Configure Direct Routing](direct-routing-configure.md)

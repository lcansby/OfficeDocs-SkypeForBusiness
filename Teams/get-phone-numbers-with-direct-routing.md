---
title: "Get Direct Routing phone numbers in your Teams tenant"
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: julien
ms.date: 05/05/2025
ms.topic: how-to
ms.assetid: aa2ec464-3481-4bbb-8c14-e13e18093df5
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
  - Calling Plans
description: "Learn how to get numbers in Teams with your Direct Routing partner."
---

# Get phone numbers with Direct Routing

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png) Direct Routing

When you're setting up users in your organization to make and receive telephone calls using Microsoft-supplied telephone numbers, you must first use the **Microsoft Teams admin center** and acquire telephone numbers to be assigned to users. The telephone number you assign to a user is a telephone number that you previously acquired for your organization. The number is listed in the drop-down list when you edit the properties of the user and select **Assign**.
  
Before you can assign Microsoft-supplied telephone numbers to your users, you must use the **Get new numbers** page to search for telephone numbers that are available to you. You can search by **Country (Market)**, **Number type**, and **Location**. You'll then see a list of operators that supply numbers in that country.

If you select Microsoft as your operator, you can acquire the numbers from the Teams admin center by entering the quantity of telephone numbers you'll need for your users. The page automatically limits the quantity based on how many you still have available to acquire. If you select an Operator Connect operator, you'll be directed to the landing page of your selected operator to complete the number order.

How you acquire and manage telephone numbers differs depending on your PSTN connectivity option: Microsoft Calling Plans, Operator Connect, Teams Phone Mobile, or Direct Routing.

## Considerations for getting Direct Routing numbers in your tenant

Direct Routing phone numbers can be managed in on-premises Active Directory or in Microsoft 365.

### Direct Routing numbers managed in an on-premises Active Directory

If you have or had a Skype for Business Server hybrid deployment,
your on-premises Active Directory is most likely synchronizing with Microsoft 365. This means that directory attributes on user and resource accounts are managed in the on-premises Active Directory and synchronized into Microsoft 365.

If the Direct Routing phone number is managed on the user or resource account in the on-premises Active Directory, the msRTCSIP-Line parameter on the account contains a value. You can use a tool such as ADSI Edit to view the msRTCSIP-Line parameter for a user or resource account that has a Direct Routing phone number assigned in on-premises Active Directory.

After this parameter is automatically synchronized to the user or resource account in Microsoft 365 through the directory synchronization process (Microsoft Entra Connect), you can view the phone number by looking at the OnPremLineURi parameter in the output from the [Get-CsOnlineUser](/powershell/module/teams/get-csonlineuser) cmdlet.

| Where | Parameter | Value |
| :------------| :-------| :---------|
| On-premises AD | msRTCSIP-Line | tel:+14255551234 |
| Microsoft 365 | OnPremLineURi | tel:+14255551234 |

### Direct Routing numbers managed in Microsoft 365

If you're not managing Direct Routing phone numbers in the on-premises Active Directory, then they're only managed in Microsoft 365. Because the phone numbers are not synching from on-premises to Microsoft 365, there is no visible value in the OnPremLineUri parameter in the output from the Get-CsOnlineUser cmdlet run for the user or resource account.

You can manage Direct Routing numbers in Microsoft 365 with Teams PowerShell, using the [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) and [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment) cmdlets.

### Direct Routing numbers managed in both an on-premises Active Directory and Microsoft 365

It's possible to manage Direct Routing phone numbers of some user and resource accounts in an on-premises Active Directory and Direct Routing phone numbers of other accounts in Microsoft 365. This capability depends on whether the attribute msRTCSIP-Line is set on the user or resource account in the on-premises Active Directory.

### Change where Direct Routing phone numbers are managed

To move management of Direct Routing phone numbers from on-premises Active Directory to Microsoft 365, you need to remove the phone number from the msRTCSIP-Line attribute on the user or resource account in the on-premises Active Directory.

Note that the phone number needs to be re-assigned to the user or resource account in Microsoft 365.

After the removal has been synchronized to Microsoft 365, the OnPremLineUri attribute in the output from Get-CsOnlineUser on the user or resource account will be empty.

For more information, see [Clear Skype for Business attributes for all on-premises users in Active Directory](/skypeforbusiness/hybrid/cloud-consolidation-managing-attributes#method-2---clear-skype-for-business-attributes-for-all-on-premises-users-in-active-directory.md).

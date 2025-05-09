---
title: "Get phone numbers for your users"
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: mikedav, roykuntz, jastark
ms.date: 08/29/2023
ms.topic: how-to
ms.assetid: aa2ec464-3481-4bbb-8c14-e13e18093df5
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
  - Calling Plans
description: "Learn how to get new, port, or transfer existing numbers for Teams, and how to show the changes to your users."
---

# Get phone numbers from Microsoft Teams Calling Plans

This article provides considerations and guidance for IT pros and admins who are acquiring new telephone numbers from Microsoft.

To acquire telephone numbers from Microsoft, you must have at least one Microsoft Calling Plan license assigned in your tenant.

Microsoft Teams Calling Plan licenses enable you to acquire local numbers in any country where Microsoft offers Calling Plans, supporting a variety of number usage types.

To learn more about Microsoft's Calling Plans and number usage availabilities per country and region, see [Microsoft Teams Calling Plans](calling-plans-for-office-365.md) and [Countries and region availability for Calling Plans](calling-plan-overview.md).

## Number usage types

Number usages define the services that are supported by a phone number. The following table lists the number usage types.

|Number usage type |Usage purpose |Number type supported |
|:-----|:-----|:-----|
|**User** |Person or device (for example, common area phone) |Geographic (Toll) |
|**Voice Application** |Auto attendants and call queues |Geographic (Toll) <br>Toll-free |
|**Conference** |Conference bridges |Geographic (Toll) <br>Toll-free |

## Availability of Microsoft numbers and usages by country or region

Use the drop-down to select the country/region where you're checking for availability of Microsoft Calling Plan availability. Calling Plans in general are covered in [Microsoft Teams Calling Plans overview](calling-plans-for-office-365.md) and are the prerequisite to acquiring numbers.

> [!div class="op_single_selector"]
>
> - [Albania](/microsoftteams/phone-reference/plan-availability/availability-in-albania)
> - [Algeria](/microsoftteams/phone-reference/plan-availability/availability-in-algeria)
> - [Antigua and Barbuda](/microsoftteams/phone-reference/plan-availability/availability-in-antigua-and-barbuda)
> - [Argentina](/microsoftteams/phone-reference/plan-availability/availability-in-argentina)
> - [Australia](/microsoftteams/phone-reference/plan-availability/availability-in-australia)
> - [Austria](/microsoftteams/phone-reference/plan-availability/availability-in-austria)
> - [Bahamas](/microsoftteams/phone-reference/plan-availability/availability-in-the-bahamas)
> - [Bahrain](/microsoftteams/phone-reference/plan-availability/availability-in-bahrain)
> - [Bangladesh](/microsoftteams/phone-reference/plan-availability/availability-in-bangladesh)
> - [Barbados](/microsoftteams/phone-reference/plan-availability/availability-in-barbados)
> - [Belarus](/microsoftteams/phone-reference/plan-availability/availability-in-belarus)
> - [Belgium](/microsoftteams/phone-reference/plan-availability/availability-in-belgium)
> - [Belize](/microsoftteams/phone-reference/plan-availability/availability-in-belize)
> - [Benin](/microsoftteams/phone-reference/plan-availability/availability-in-benin)
> - [Bermuda](/microsoftteams/phone-reference/plan-availability/availability-in-bermuda)
> - [Bosnia and Herzegovina](/microsoftteams/phone-reference/plan-availability/availability-in-bosniaherzegovina)
> - [Brazil](/microsoftteams/phone-reference/plan-availability/availability-in-brazil)
> - [Brunei](/microsoftteams/phone-reference/plan-availability/availability-in-brunei)
> - [Bulgaria](/microsoftteams/phone-reference/plan-availability/availability-in-bulgaria)
> - [Cambodia](/microsoftteams/phone-reference/plan-availability/availability-in-cambodia)
> - [Cameroon](/microsoftteams/phone-reference/plan-availability/availability-in-cameroon)
> - [Canada](/microsoftteams/phone-reference/plan-availability/availability-in-canada)
> - [Cayman Islands](/microsoftteams/phone-reference/plan-availability/availability-in-the-cayman-islands)
> - [Chile](/microsoftteams/phone-reference/plan-availability/availability-in-chile)
> - [China](/microsoftteams/phone-reference/plan-availability/availability-in-china)
> - [Colombia](/microsoftteams/phone-reference/plan-availability/availability-in-colombia)
> - [Costa Rica](/microsoftteams/phone-reference/plan-availability/availability-in-costa-rica)
> - [Croatia](/microsoftteams/phone-reference/plan-availability/availability-in-croatia)
> - [Cyprus](/microsoftteams/phone-reference/plan-availability/availability-in-cyprus)
> - [Czech Republic](/microsoftteams/phone-reference/plan-availability/availability-in-the-czech-republic)
> - [Denmark](/microsoftteams/phone-reference/plan-availability/availability-in-denmark)
> - [Dominica](/microsoftteams/phone-reference/plan-availability/availability-in-dominica)
> - [Dominican Republic](/microsoftteams/phone-reference/plan-availability/availability-in-the-dominican-republic)
> - [Ecuador](/microsoftteams/phone-reference/plan-availability/availability-in-ecuador)
> - [Egypt](/microsoftteams/phone-reference/plan-availability/availability-in-egypt)
> - [El Salvador](/microsoftteams/phone-reference/plan-availability/availability-in-el-salvador)
> - [Estonia](/microsoftteams/phone-reference/plan-availability/availability-in-estonia)
> - [Finland](/microsoftteams/phone-reference/plan-availability/availability-in-finland)
> - [France](/microsoftteams/phone-reference/plan-availability/availability-in-france)
> - [Georgia](/microsoftteams/phone-reference/plan-availability/availability-in-georgia)
> - [Germany](/microsoftteams/phone-reference/plan-availability/availability-in-germany)
> - [Ghana](/microsoftteams/phone-reference/plan-availability/availability-in-ghana)
> - [Greece](/microsoftteams/phone-reference/plan-availability/availability-in-greece)
> - [Grenada](/microsoftteams/phone-reference/plan-availability/availability-in-grenada)
> - [Guam](/microsoftteams/phone-reference/plan-availability/availability-in-guam)
> - [Guatemala](/microsoftteams/phone-reference/plan-availability/availability-in-guatemala)
> - [Honduras](/microsoftteams/phone-reference/plan-availability/availability-in-honduras)
> - [Hong Kong SAR](/microsoftteams/phone-reference/plan-availability/availability-in-hong-kong)
> - [Hungary](/microsoftteams/phone-reference/plan-availability/availability-in-hungary)
> - [India](/microsoftteams/phone-reference/plan-availability/availability-in-india)
> - [Indonesia](/microsoftteams/phone-reference/plan-availability/availability-in-indonesia)
> - [Ireland](/microsoftteams/phone-reference/plan-availability/availability-in-ireland)
> - [Israel](/microsoftteams/phone-reference/plan-availability/availability-in-israel)
> - [Italy](/microsoftteams/phone-reference/plan-availability/availability-in-italy)
> - [Jamaica](/microsoftteams/phone-reference/plan-availability/availability-in-jamaica)
> - [Japan](/microsoftteams/phone-reference/plan-availability/availability-in-japan)
> - [Jordan](/microsoftteams/phone-reference/plan-availability/availability-in-jordan)
> - [Kazakhstan](/microsoftteams/phone-reference/plan-availability/availability-in-kazakhstan)
> - [Kenya](/microsoftteams/phone-reference/plan-availability/availability-in-kenya)
> - [Kuwait](/microsoftteams/phone-reference/plan-availability/availability-in-kuwait)
> - [Latvia](/microsoftteams/phone-reference/plan-availability/availability-in-latvia)
> - [Lithuania](/microsoftteams/phone-reference/plan-availability/availability-in-lithuania)
> - [Luxembourg](/microsoftteams/phone-reference/plan-availability/availability-in-luxembourg)
> - [North Macedonia](/microsoftteams/phone-reference/plan-availability/availability-in-macedonia)
> - [Malaysia](/microsoftteams/phone-reference/plan-availability/availability-in-malaysia)
> - [Malta](/microsoftteams/phone-reference/plan-availability/availability-in-malta)
> - [Mexico](/microsoftteams/phone-reference/plan-availability/availability-in-mexico)
> - [Moldova](/microsoftteams/phone-reference/plan-availability/availability-in-moldova)
> - [Monaco](/microsoftteams/phone-reference/plan-availability/availability-in-monaco)
> - [Morocco](/microsoftteams/phone-reference/plan-availability/availability-in-morocco)
> - [Netherlands](/microsoftteams/phone-reference/plan-availability/availability-in-the-netherlands)
> - [New Zealand](/microsoftteams/phone-reference/plan-availability/availability-in-new-zealand)
> - [Nicaragua](/microsoftteams/phone-reference/plan-availability/availability-in-nicaragua)
> - [Nigeria](/microsoftteams/phone-reference/plan-availability/availability-in-nigeria)
> - [Northern Mariana Islands](/microsoftteams/phone-reference/plan-availability/availability-in-northern-mariana-islands)
> - [Norway](/microsoftteams/phone-reference/plan-availability/availability-in-norway)
> - [Pakistan](/microsoftteams/phone-reference/plan-availability/availability-in-pakistan)
> - [Panama](/microsoftteams/phone-reference/plan-availability/availability-in-panama)
> - [Paraguay](/microsoftteams/phone-reference/plan-availability/availability-in-paraguay)
> - [Peru](/microsoftteams/phone-reference/plan-availability/availability-in-peru)
> - [Philippines](/microsoftteams/phone-reference/plan-availability/availability-in-the-philippines)
> - [Poland](/microsoftteams/phone-reference/plan-availability/availability-in-poland)
> - [Portugal](/microsoftteams/phone-reference/plan-availability/availability-in-portugal)
> - [Puerto Rico](/microsoftteams/phone-reference/plan-availability/availability-in-puerto-rico)
> - [Qatar](/microsoftteams/phone-reference/plan-availability/availability-in-qatar)
> - [Romania](/microsoftteams/phone-reference/plan-availability/availability-in-romania)
> - [Russia](/microsoftteams/phone-reference/plan-availability/availability-in-russia)
> - [Saint Kitts and Nevis](/microsoftteams/phone-reference/plan-availability/availability-in-saint-kitts-and-nevis)
> - [Saint Lucia](/microsoftteams/phone-reference/plan-availability/availability-in-saint-lucia)
> - [Saudi Arabia](/microsoftteams/phone-reference/plan-availability/availability-in-saudi-arabia)
> - [Serbia](/microsoftteams/phone-reference/plan-availability/availability-in-serbia)
> - [Singapore](/microsoftteams/phone-reference/plan-availability/availability-in-singapore)
> - [Slovakia](/microsoftteams/phone-reference/plan-availability/availability-in-slovakia)
> - [Slovenia](/microsoftteams/phone-reference/plan-availability/availability-in-slovenia)
> - [South Africa](/microsoftteams/phone-reference/plan-availability/availability-in-south-africa)
> - [South Korea](/microsoftteams/phone-reference/plan-availability/availability-in-south-korea)
> - [Spain](/microsoftteams/phone-reference/plan-availability/availability-in-spain)
> - [Sri Lanka](/microsoftteams/phone-reference/plan-availability/availability-in-sri-lanka)
> - [Sweden](/microsoftteams/phone-reference/plan-availability/availability-in-sweden)
> - [Switzerland](/microsoftteams/phone-reference/plan-availability/availability-in-switzerland)
> - [Taiwan](/microsoftteams/phone-reference/plan-availability/availability-in-taiwan)
> - [Thailand](/microsoftteams/phone-reference/plan-availability/availability-in-thailand)
> - [Trinidad and Tobago](/microsoftteams/phone-reference/plan-availability/availability-in-trinidad-and-tobago)
> - [Tunisia](/microsoftteams/phone-reference/plan-availability/availability-in-tunisia)
> - [Türkiye](/microsoftteams/phone-reference/plan-availability/availability-in-turkey)
> - [Turks and Caicos Islands](/microsoftteams/phone-reference/plan-availability/availability-in-turks-and-caicos-islands)
> - [Uganda](/microsoftteams/phone-reference/plan-availability/availability-in-uganda)
> - [Ukraine](/microsoftteams/phone-reference/plan-availability/availability-in-the-ukraine)
> - [United Arab Emirates (UAE)](/microsoftteams/phone-reference/plan-availability/availability-in-the-united-arab-emirates-uae)
> - [United Kingdom](/microsoftteams/phone-reference/plan-availability/availability-in-the-united-kingdom-u-k)
> - [United States](/microsoftteams/phone-reference/plan-availability/availability-in-the-united-states-u-s)
> - [Uruguay](/microsoftteams/phone-reference/plan-availability/availability-in-uruguay)
> - [Venezuela](/microsoftteams/phone-reference/plan-availability/availability-in-venezuela)
> - [Vietnam](/microsoftteams/phone-reference/plan-availability/availability-in-vietnam)

## Acquiring new numbers by country or region

With a secured Microsoft Teams Calling Plan, you can request new numbers using country/region-specific acquisition guidance that might be necessary when ordering. Find the appropriate guidance for your country or region from the following drop-down menu.

> [!div class="op_single_selector"]
>
> - [Australia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-australia)
> - [Austria](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-austria)
> - [Belgium](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-belgium)
> - [Canada](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-canada)
> - [Czech Republic](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-czech-republic)
> - [Denmark](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-denmark)
> - [Estonia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-estonia)
> - [Finland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-finland)
> - [France](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-france)
> - [Germany](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-germany)
> - [Hong Kong](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-hong-kong)   
> - [Hungary](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-hungary)
> - [Ireland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-ireland)
> - [Italy](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-italy)
> - [Japan](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-japan)
> - [Latvia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-latvia)
> - [Lithuania](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-lithuania)
> - [Luxembourg](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-luxembourg)
> - [Mexico](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-mexico)
> - [New Zealand](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-new-zealand)
> - [Norway](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-norway)
> - [Poland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-poland)
> - [Portugal](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-portugal)
> - [Romania](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-romania)
> - [Singapore](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-singapore)
> - [Slovakia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-slovakia)
> - [Slovenia](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-slovenia)
> - [South Africa](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-south-africa)
> - [Spain](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-spain)
> - [Sweden](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-sweden)
> - [Switzerland](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-switzerland)
> - [Netherlands](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-netherlands)
> - [United Kingdom](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-u-k)
> - [United States & Puerto Rico](/microsoftteams/phone-reference/manage-numbers/phone-number-management-for-the-u-s)

### Request forms for new phone numbers

Each country or region has different instructions, different types of phone numbers (geographic/non-geographic and service (toll/toll-free)), and rules/regulations for getting phone numbers so they can be used in Microsoft Teams.

Sometimes (depending on your country or region) you won't be able to get new user or service phone numbers using the Microsoft Teams admin center, or you might need specific phone numbers (vanity requests) or specific area codes.

## How many telephone numbers can you get?

The number of phone numbers you can get from Microsoft for your organization depends on the types of phone numbers and types of licenses you've bought and assigned. For information about Teams Phone and Audio Conferencing licensing, see [Add-on licenses](teams-add-on-licensing/microsoft-teams-add-on-licensing.md). For more information about Calling Plans, see [Microsoft Calling Plans](calling-plans-for-office-365.md).

The following table applies to Microsoft Calling Plans, [Audio Conferencing](deploy-audio-conferencing-teams-landing-page.md), and voice apps, such as [Call Queues and Auto Attendants](plan-auto-attendant-call-queue.md).

> [!IMPORTANT]
> The limits in the following table don't include phone numbers you have ported to Microsoft.

|Here's the type of phone number |How do you get the total phone numbers? |Here's an example |
|:-----|:-----|:-----|
|User (subscriber) number   |The number of phone numbers is equal to the total number of **Domestic Calling Plan** and/or **International Calling Plan** licenses multiplied by 1.1 + 10 extra phone numbers. If you have pay-as-you-go licenses, you can only acquire 1 phone number per license. |If I have 50 users in total with 30 of them on a Domestic Calling Plan or International Calling Plan, and 20 of them on a Pay-As-You-Go Calling Plan, you can acquire **63** phone numbers **(30 x 1.1 + 10) + 20**. |
|Toll service number   | The number of phone numbers is equal to the total number of **Teams Phone** and **Audio Conferencing** licenses and uses the following: <br/>  If there are **1-25 licenses**, then **5** phone numbers are given. <br/>  If there are **26-49 licenses**, then **10** phone numbers are given. <br/>  If there are **50-99 licenses**, then **20** phone numbers are given. <br/>  If there are **100-149 licenses**, then **30** phone numbers are given. <br/>  If there are **150-199 licenses**, then **40** phone numbers are given. <br/>  If there are **200-499 licenses**, then **65** phone numbers are given. <br/>  If there are **500-749 licenses**, then **90** phone numbers are given. <br/>  If there are **750-999 licenses**, then **110** phone numbers are given. <br/>  If there are **1,000-1,249 licenses**, then **125** phone numbers are given. <br/>  If there are **1,250-1,499 licenses**, then **135** phone numbers are given. <br/>  If there are **1,500-1,999 licenses**, then **160** phone numbers are given. <br/>  If there are **2,000-2,999 licenses**, then **210** phone numbers are given. <br/>  If there are **3,000-6,999 licenses**, then **420** phone numbers are given. <br/>  If there are **7,000-9,999 licenses**, then **500** phone numbers are given. <br/>  If there are **10,000-14,999 licenses**, then **600** phone numbers are given. <br/>  If there are **15,000-19,999 licenses**, then **700** phone numbers are given. <br/>  If there are **20,000-49,999 licenses**, then **1000** phone numbers are given. <br/>  If there are **50,000+ licenses**, then **1500** phone numbers are given. <br/> <br/> For **Audio Conferencing with dial-out to USA/CAN subscription licenses (free in select geographies)**, 1 toll service number is given in addition to the numbers that are automatically granted when onboarding to the service, regardless of the number of licenses acquired. <br/>|If you have a total of **51** **Teams Phone** and **Audio Conferencing** licenses, you can get **20** toll service numbers.  |
|Toll-free service number   | The number of phone numbers is equal to the total number of **Teams Phone** and **Audio Conferencing** licenses and uses the following: <br/>  If there are **1-25 licenses**, then **5** phone numbers are given. <br/>  If there are **26-49 licenses**, then **10** phone numbers are given. <br/>  If there are **50-99 licenses**, then **20** phone numbers are given. <br/>  If there are **100-149 licenses**, then **30** phone numbers are given. <br/>  If there are **150-199 licenses**, then **40** phone numbers are given. <br/>  If there are **200-499 licenses**, then **65** phone numbers are given. <br/>  If there are **500-749 licenses**, then **90** phone numbers are given. <br/>  If there are **750-999 licenses**, then **110** phone numbers are given. <br/>  If there are **1,000-1,249 licenses**, then **125** phone numbers are given. <br/>  If there are **1,250-1,499 licenses**, then **135** phone numbers are given. <br/>  If there are **1,500-1,999 licenses**, then **160** phone numbers are given. <br/>  If there are **2,000-2,999 licenses**, then **210** phone numbers are given. <br/>  If there are **3,000-6,999 licenses**, then **420** phone numbers are given. <br/>  If there are **7,000-9,999 licenses**, then **500** phone numbers are given. <br/>  If there are **10,000-14,999 licenses**, then **600** phone numbers are given. <br/>  If there are **15,000-19,999 licenses**, then **700** phone numbers are given. <br/>  If there are **20,000-49,999 licenses**, then **1000** phone numbers are given. <br/>  If there are **50,000+ licenses**, then **1500** phone numbers are given.  |If you have a total of **1001** **Teams Phone** and **Audio Conferencing** licenses, you can get **125** toll-free service numbers. <br/> <br/> **Important:** [Communications Credits billing](set-up-communications-credits-for-your-organization.md) is required to reserve and use toll-free phone numbers.          |

> [!NOTE]
> You can see the quantity of telephone numbers you can get from Microsoft during the search and acquire process in the Microsoft Teams admin center (**Add phone numbers**).

## Get new phone numbers

**Using the Microsoft Teams admin center**

You must be a Teams service admin to make these changes. See [Use Teams administrator roles to manage Teams](./using-admin-roles.md) to read about getting admin roles and permissions.

1. Sign into the [Microsoft Teams admin center](https://admin.teams.microsoft.com).

2. In the left navigation, go to **Voice** > **Phone numbers**, and then select **Add**.

> [!IMPORTANT]
> For you to see the **Voice** option in the left navigation in the Teams admin center, you must first buy at least one **Enterprise E5 or E3 license**, one **Phone System** add-on license, or one **Audio Conferencing** add-on license. 

3. Enter a name for the order and add a description.

4. On the Location and quantity page, do the following:
    1. Under **Country or region**, select a country or region.
    1. Under **Number type**, see [Number usage types](#number-usage-types).
    1. Under **Operator**, select **Microsoft** as the operator.
    1. Under **Quantity**, enter the number of numbers that you want for your organization.
    1. Under **Search for new numbers**, select a location by searching for city name, area code, or postal code. If you need to create a new location, select **Add a location**.
    1. Under **Area code**, select an area code.
    1. Select **Next** to select your numbers.

5. Select the numbers you want. You have 10 minutes to select your phone numbers and place your order. If you take more than 10 minutes, the phone numbers will be returned to the pool of numbers.

6. When you're ready to place your order, select **Place order**.

    > [!IMPORTANT]
    > The number of phone numbers for users (subscribers) is equal to the total number of **Domestic Calling Plan** and **International Calling Plan** licenses you have assigned multiplied by 1.1, plus 10 additional phone numbers. For example, if you have 50 users in total with a Domestic Calling Plan and/or International Calling Plan, you can acquire **65** phone numbers **(50 x 1.1 + 10)**. Note that if you have a Pay-As-You-Go Calling Plan, you can only acquire 1 phone number per license assigned.
    >
    > For details, see [How many phone numbers can you get?](./how-many-phone-numbers-can-you-get.md). If you need to get more phone numbers than this, [contact Support Contact for Business Products - Admin Help](/microsoft-365/admin/contact-support-for-business-products).

## Assign phone numbers to users or services

After you get your phone numbers, you'll need to assign a number to each of your users. For more information, see [Manage phone numbers for users](./assign-change-or-remove-a-phone-number-for-a-user.md) and [Change the phone numbers on your Audio Conferencing bridge](./change-the-phone-numbers-on-your-audio-conferencing-bridge.md).

### Supported rate centers and coverage for Calling Plans in the United States

A rate center is a term used in the United States for a geographical area that traditionally defines boundaries for local calling, billing rates, and phone number assignment for the PSTN. In many cases, with the industry moving to all inclusive plans or bundles of minutes, the rate center has become less important for billing but is still used by some US PSTN operators.

The [Supported rate centers and coverage matrix for North America](https://www.microsoft.com/download/details.aspx?id=102534) spreadsheet lists the rate centers that we support. When you're getting new phone numbers or when you're transferring phone numbers from your existing provider to Teams, download the spreadsheet and use it to look up rate centers. If you don't know your rate center, you can look it up on the internet based on your area codes (NPAs) and prefixes (NXX)s.
If you're getting new numbers and we don't have the numbers that you've requested, we'll attempt to offer you numbers from the same rate center.

If you're getting new numbers and we don't have the numbers that you've requested, we'll offer you numbers from the same rate center.

## Related articles

[Transferring phone numbers common questions](./phone-number-calling-plans/port-order-overview.md)

[Different kinds of phone numbers used for Calling Plans](./different-kinds-of-phone-numbers-used-for-calling-plans.md)

[Manage phone numbers for your organization](/microsoftteams/manage-phone-numbers-for-your-organization)

[Emergency calling terms and conditions](./emergency-calling-terms-and-conditions.md)

[Emergency Calling disclaimer label](https://download.microsoft.com/download/9/9/0/990e24c1-eb49-4b52-9306-dbd4c864ed91/emergency-calling-label-(en-us)-(v.1.0).zip)

[Get phone numbers into your tenant](manage-phone-numbers-landing-page.md)

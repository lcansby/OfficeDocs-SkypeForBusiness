---
title: "Microsoft Teams Dial plans for phone call routing"
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: roykuntz
ms.date: 03/31/2025
ms.topic: article
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
ms.localizationpriority: Medium
f1.keywords:
- CSH

description: "Learn about Microsoft Teams dial plans and how they help route phone calls."
---

# Planning Teams dial plans for Teams Phone

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png)Microsoft Calling Plans, Operator Connect, Teams Phone Mobile, and Direct Routing

This article is for IT Admins and IT Pros who are researching and planning to use Teams dial plans for routing Teams Phone calls.

An overview of inbound and outbound call routing is provided for context in relation to how Teams translates numbers that are received so that they can be processed for routing to a person or to a PSTN (Public Switchted Telephone Network) resource.

Understand the concepts in this article are a prerequisite for [creating Teams dial plans](create-and-manage-dial-plans.md) and [normalization rules](phone-normalization-rules.md).

## What are dial plans?

Dial plans are what enables Teams to route phone calls, *regardless of how they were dialed*.

A dial plan is a named set of one or more digit-manipulation rules that translate called number strings into alternate (desired) formats, so that Teams can route the calls.

Teams dial plans ensure that numbers orginating from various input formats are translated into standardized formats (typically E.164) for purposes of matching called numbers to resources that the user is authorized to use, and for routing the calls.

The translation rules are optionally applied to phone numbers that:

- An individual user dials
- Are sent across PSTN connections ('trunks') between your Direct Routing PSTN integration and your tenant.

The rules within a dial plan are known as [**normalization rules**](phone-normalization-rules.md).

A normalization rule in one dial plan can be translated differently than a normalization rule in another dial plan, so depending on which dial plan is assigned to a given user or trunk, a dialed number may be translated and routed differently.

## Dial plan classification

Dial plans can be classified into two main categories.

A **trunk based dial plan** applies to a voice route between a Direct Routing SBC (Session Border Controller) and Teams, and supports normalizing inbound called number-strings.

A **user's effective dial plan** is an inherited set of hierarchical dial plans applied to numbers that a user dials from their Teams client.

## Trunk-based dial plans - for inbound calls

Routing an inbound phone call to a Teams user uses a process called **Reverse Number Lookup (RNL)**; instead of referencing a Teams user's contact name to lookup their number, RNL looks in your directory for the dialed number-string of a call, finds the user or resource account in your tenant that is assigned with the same number-string, and sets up the incoming call with that user or resource.

If the SBC providing the inbound call's number-string isn't offering a number format matching the numbers you've assigned to your users or resources, you can apply a trunk-based dial plan to the SBC and normalize the inbound, called number into your expected format.

Trunk-based dial plans are configured on the voice route using the SBC.

To learn more about configuring a trunk-based dial plan, refer to Direct Routing [Step 4: Translate phone numbers](direct-routing-translate-numbers.md).

## User effective dial plans - for outbound calls

Outbound telephone calls from Teams users are routed based on a series of assigned configuration items, including their assigned dial plan. and their voice routing policy.

Teams supports three scopes of dial plans, outlined in the following table:

|Dial plan scope |Configurable |Description |
|:-----|:-----|:-----|
|Globally-scoped dial plan |No |Microsoft-managed for the Teams Phone service. Defined for every country or region where Teams Phone is available. Each user is automatically assigned the service country/region dial plan that matches the usage location assigned to the user. |
|Tenant-scoped dial plan |Yes |If a tenant defines a tenant-scoped dial plan but doesn't assign a user-scoped dial plan, then that user will be provisioned with an effective dial plan of the user's service country/region dial plan and the tenant dial plan. |
|User-scoped dial plan |Yes |If a tenant defines and assigns a user-scoped dial plan, that user will be provisioned with an effective dial plan of the user's service country/region dial plan and the assigned user dial plan. |

Using the hiearchy of the three user-based dial plans, each Teams user inherits an "effective" dial plan.

For example, you can't change the globally-scoped dial plan for the Teams Phone service, but you can create tenant-scoped dial plans, which augment the globally-scoped dial plan. As clients are provisioned, they obtain an "effective dial plan," which is a combination of the globally-scoped dial plan for their country or region and the appropriate tenant-scoped dial plan. Therefore, it's not necessary to define all normalization rules in tenant-scoped dial plans as the rules might already exist in the globally-scoped dial plan.

The possible user ***effective dial plans*** are outlined in the following table:

|User's effective dial plan |Description |
|:-----|:-----|
|**Service Country** |If no tenant-scoped dial plan is defined and no user-scoped dial plan is assigned to the user, the user inherits only the globally-scoped dial plan and receives an *effective dial plan* mapped to the service country/region associated with their usage location. |
|**Tenant Global - Service Country** |If a tenant-scoped dial plan is defined and no user-scoped dial plan is assigned to the user, the user receives an *effective dial plan* consisting of a merged tenant-scoped and globally-scoped (for their country/region) dial plans. |
|**Tenant User - Service Country** |If a user-scoped dial plan is defined and assigned to a user, the user will receive an *effective dial plan* consisting of the merged user-scoped and globally-scoped (for their country/region) dial plans. |

> [!NOTE]
> In the scenario where no dial plan normalization rules apply to a dialed number, the dialed string is still normalized to prepend "+CC" where CC is the country/region code of the dialing user's usage location. This applies to Calling Plans, Direct Routing, and PSTN Conference dial-out scenarios. Additionally, if a tenant dial plan normalization rule results in a number that doesn't start with "+", the Teams cloud calling service will attempt to normalize the number received from the Teams client based on the tenant-scoped dial plan, and if not matched, on the Global-scoped dial plan. To avoid double normalization, it's recommended that Direct Routing customers normalize numbers to include a + and then remove the + using a Trunk-based dial plan.
 
With Microsoft Calling Plans, Operator Connect, and Teams Phone Mobile, dial plans and voice routing policies are preconfigured and administration for dial plans and voice routing policies isn't generally necessary, if the users are instructed to place calls by dialing as they normally would for any call in their country or region.

When you are deploying extension dialing or Direct Routing, the **user's effective dial plan** provides admins with the ability to configure a set of rules that help translate the user's dialed digits into a number that is resolved to a destination where Teams can route the call.

Clients get the appropriate dial plan through provisioning settings that are automatically provided when users sign in to Teams. As an admin, you can manage and assign dial plan scope levels by using the Microsoft Teams admin center or Remote PowerShell. For more information, see [Create and manage dial plans](create-and-manage-dial-plans.md).

## Planning for tenant dial plans

To plan custom dial plans, follow these steps:

- **Step 1** Decide whether a custom dial plan is needed to enhance the user dialing experience. Typically, the need for one would be to support non-E.164 dialing, such as extensions or abbreviated national dialing.

- **Step 2** Determine whether tenant global or tenant user scoped dial plans are needed, or both. User scoped dial plans are needed if users have different local dialing requirements.

- **Step 3** Identify valid number patterns for each required dial plan. Only the number patterns that aren't defined in the service level country/region dial plans are required.

- **Step 4** Develop an organization-wide scheme for naming dial plans. Adopting a standard naming scheme assures consistency across an organization and makes maintenance and updates easier.

## Creating your new dial plan

When you create a new dial plan, you must put in the information that is required.

### Name and simple name

For user dial plans, specify a descriptive name that identifies the users to which the dial plan will be assigned.

The dial plan Simple Name is an attribute of the dial plan that is prepopulated with a string that is derived from the dial plan name. The Simple Name field is editable in PowerShell, which enables you to create a more descriptive naming convention for your dial plans. The Simple Name value can't be empty and must be unique.

A best practice is to develop a naming convention for your entire organization and then uses this convention consistently across all sites and users.

We recommend that you type the common, recognizable name of the ***geographic location*** or ***group of users*** to which the corresponding dial plan applies.

## Dial plans and routing considerations

There can be a maximum of 1,000 tenant dial plans per tenant.

User effective dial plans for outbound translations behave different than trunk-based dial plans for inbound translations. For example,

- With user effective dial plans, the Teams client will normalize numbers that start with "+" and calls placed from call history.
- With trunk-based dial plans, the Teams service will not normalize numbers that start with "+".

### Number lookup

Routing inbound calls to users is supported when all Teams user and resource accounts have unique number and extension values assigned for their telephone number.

The unique values of the user's telephone number can have two parts, as follows:

- **Number** - For inbound calls to resolve to users with Microsoft Calling Plan and Operator Connect solutions, the number value is designated as a number in E.164 format. For example, *+14255551212*. For Direct Routing solutions, the number value is designated as a number between 3 and 38 digits without common symbols.

- **Extension** - added to the *number* and separated by the ";ext=" delimiter (case insensitive), between 1 and 12 digits. For example, *+14255551212****;ext=12345***

An extension isn't necessary; only a unique number is required for Reverse Number Lookup. If multiple end-users are sharing a single, main number, and a [Teams Shared Calling](shared-calling-plan.md) policy is *not* being used, then a then unique extensions must be assigned to each user. Otherwise, *extensions are neither required or recommended*.

For example, assume that a user is assigned the phone number +14255551212. If a PSTN caller dialed +14255551212, RNL finds the number-string match, and the call is connected to that user.

If the user is assigned a phone number with an extension, +14255551212;ext=12345, the inbound dialed number ***must include*** the extension for matching to work.

If the dialed number isn't matched, either because the number isn't assigned to an account or the number dialed doesn't exactly match any number string assigned to an account, the call fails to route or is routed according to [unassigned number routing](routing-calls-to-unassigned-numbers.md), if configured.

When you have a Direct Routing deployment with no digit translation configured on the SBC, and if the calls are not presenting numbers in the format that you've designated for your users, use a trunk-based dial plan to normalize the inbound called number to a format that matches what is assigned to your users.

If you want internal users who call a phone number that is assigned to a resource account, to bypass the Reverse Number Lookup logic and route the call externally through the PSTN instead of routing to the resource account, you can enable the **skip RNL** option for the phone number assignment using the **Set-CsPhoneNumberAssignment** PowerShell cmdlet with `-ReverseNumberLookup`. For more information, see [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) and [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment).

### Direct Routing

If you deploy Calling Plan, Operator Connect, or Teams Phone Mobile for your PSTN connectivity, your PSTN service provider manages most call routing. **If you deploy Direct Routing for your PSTN connectivity, more steps are required to configure call routing.**

- For Direct Routing, you must configure call routing by specifying the voice routes and assigning voice routing policies to users. You can configure dial plans for number translation at the trunk level to ensure interoperability with Session Border Controllers (SBCs). For more information, see [Configure voice routing for Direct Routing](direct-routing-voice-routing.md), [Manage voice routing policies](manage-voice-routing-policies.md), and [Translate phone numbers](direct-routing-translate-numbers.md).

- You can assign a Direct Routing online voice routing policy to Calling Plan and Operator Connect users and may want to do this, for example, to enable users to dial in to a directly connected call center. You can set up a Direct Routing trunk to the call center.

### Direct Routing online voice-routing policy
If a user has a Calling Plan license, that user’s outgoing calls are automatically routed through the Microsoft Calling Plan PSTN infrastructure. If you configure and assign a Direct Routing online voice-routing policy to the user, Teams checks the user’s outgoing calls against the Direct Routing online voice-routing policy to determine whether their dialed number matches a number-pattern that is defined in the online voice-routing policy. If there’s a match, the call is routed through the Direct Routing trunk. If there’s no match, the call is routed through the Calling Plan PSTN infrastructure.

For more information, see [Direct Routing voice routing policy considerations](direct-routing-voice-routing.md#voice-routing-policy-considerations).

## Related topics

[Create and manage dial plans](create-and-manage-dial-plans.md)

[Normalization rules](phone-normalization-rules.md)

[Route calls to unassigned numbers](routing-calls-to-unassigned-numbers.md)

[PSTN connectivity options](pstn-connectivity.md)

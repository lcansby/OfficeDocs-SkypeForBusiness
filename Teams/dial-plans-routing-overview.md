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

This article is for IT Admins and IT Pros who are researching and planning to use:

- Teams dial plans (with normalization rules) for ensuring user-dialed numbers get processed into a standard phone number format
- Trunk number translation rules, for adapting numbers to expected formats as negotiated between Teams and a Direct Routing integration with the PSTN (Public Switched Telephone Network).

An overview of outbound and inbound called number processing is provided for context in relation to how Teams translates called numbers so that they can be processed for routing to a person or to a PSTN resource.

Understand the concepts in this article are a prerequisite for [creating Teams dial plans](create-and-manage-dial-plans.md) and [normalization rules](phone-normalization-rules.md).

## What are dial plans?

Dial plans are what enables Teams to route phone calls, *regardless of how they were dialed*.

A dial plan is a named set of one or more number-string translation rules that translate called number-strings into alternate (desired) formats, so that Teams can process and route the calls.

Teams dial plans ensure that numbers originating with various user-input formats are translated into standardized formats (typically E.164) for the purposes of matching called numbers to resources that the user is authorized to use, and for routing the calls.

The rules within a dial plan are known as **normalization rules**, and their purpose is to support users dialing numbers in a variety of patterns, and resolving their nonstandard number format into an expected, standardized format.

A normalization rule in one dial plan can be translated differently than a normalization rule in another dial plan, so depending on which dial plan is assigned to a given user, a dialed number may be translated and routed differently.

Normalization rules and examples are addressed in a later article; see [Normalization rules](phone-normalization-rules.md).

## Dial plan scopes and a user's effective dial plan

Outbound telephone calls from Teams users are routed based on a series of assigned configuration items, including their assigned dial plan.

Teams supports three distinct scopes of dial plans, outlined in the following table:

|Dial plan scope |Configurable |Description |
|:-----|:-----|:-----|
|Service dial plan |No |Microsoft-managed for the Teams Phone service. Defined for every country or region where Teams Phone is available. Each user is automatically assigned the service dial plan that matches the usage location assigned to the user. |
|Tenant dial plan |Yes |If an admin doesn't assign a user-scoped dial plan, then that user will be provisioned with an effective dial plan of the user's service country/region dial plan and the tenant's default dial plan (named *Global*). Normalization rules can be managed in the Global (default, tenant level) dial plan. |
|User dial plan |Yes |If an admin defines and assigns a user-scoped dial plan, that user will be provisioned with an effective dial plan of the user's service country/region dial plan and the assigned user dial plan. |

A user is always assigned to the service dial plan and a user is always assigned to either a tenant dial plan or a user dial plan, but can't be assigned to a tenant dial plan and user dial plan at the same time.

In the priority of processing normalization rules for a dialed number, the user dial plan takes precedence over the tenant (Global) dial plan, and the tenant dial plan takes precedence over the service dial plan.

Teams applies a hierarchy of the three dial plan scopes, and each Teams user inherits what's known as their "effective" dial plan.

The possible effective dial plans for users are outlined in the following table:

|User's effective dial plan |Description |
|:-----|:-----|
|**Service Country** |If the tenant (Global) dial plan *isn't modified* and no user dial plan is assigned to the user, the user inherits an *effective dial plan* consisting of only the *service* dial plan for the country/region associated with their usage location. |
|**Tenant Global - Service Country** |If the tenant dial plan is modified and no user dial plan is assigned to the user, the user inherits an *effective dial plan* consisting of a merged *tenant and service* dial plan (for their country/region). </br>The normalization rules in the tenant's Global dial plan will take precedence over rules in the service dial plan. |
|**Tenant User - Service Country** |If a user dial plan is defined and assigned to a user, the user inherits an *effective dial plan* consisting of a merged *user and service* dial plan (for their country/region). </br>The normalization rules in the tenant's user dial plan will take precedence over rules in the service dial plan.  |

You can't change the service dial plan for the Teams Phone service, but you can edit the tenant (Global) dial plan or you can create custom user dial plans, which augment the service dial plan. As clients are provisioned, they obtain an "effective dial plan," which is a combination of the service dial plan for their country or region and the user's assigned dial plan. It's not necessary to define all normalization rules in the tenant or user dial plans as the rules might already exist in the service dial plan for the country/region.

Clients get the appropriate dial plan through provisioning settings that are automatically provided when users sign in to Teams. As an admin, you can manage and assign dial plan scope levels by using the Microsoft Teams admin center or Remote PowerShell. For more information, see [Create and manage dial plans](create-and-manage-dial-plans.md).

## Route-based number translations - for outbound calls

A route, in this case, references the virtual phone line between your tenant and the PSTN. Number translation rules are optionally applied to called numbers that are passed through this route, to keep number formats synchronized between your tenant and your Direct Routing PSTN solution.

Once a user dials a number, it processes through the effective dial plan, Teams matches the normalized number to an approved PSTN usage for routing to the PSTN, and the call is directed to a voice route. The voice route is associated with an SBC (Session Border Controller), and there may be instances where you want to manage the format in which your SBC receives the called number-string.

To translate a called number-string into an alternate format, create an outbound number translation rule and apply it to the SBC's profile (also known as PSTN gateway) in Teams.

To learn more about creating outbound translation rules and assigning to SBCs, refer to Direct Routing [Step 4: Translate phone numbers](direct-routing-translate-numbers.md).

> [!NOTE]
> In the scenario where no tenant or user dial plan normalization rules apply to a dialed number, the Teams service dial plan prepends "+CC" to the number, where CC is the country/region code of the dialing user's usage location. This applies to Calling Plans, Direct Routing, and PSTN Conference dial-out scenarios. </br>To avoid double normalization (from the user's effective dial plan and a route-based number translation rule), it's recommended that Direct Routing customers use dial plans to normalize numbers to include a + and then remove the + using a route-based translation rule.

## Route-based number translations - for inbound calls

Routing an inbound phone call to a Teams user uses a process called [Reverse Number Lookup (RNL)](#number-lookup). Instead of referencing a Teams user's contact name to look up their number, RNL looks in your directory for the dialed number-string of a call, finds the user or resource account in your tenant that is assigned with the same number-string, and sets up the incoming call with that user or resource.

If the Direct Routing SBC providing the inbound call's number-string isn't offering a format matching to the number-string standardized for your Teams user and resource accounts, you can apply a route-based number translation rule to the SBC's voice route and normalize the inbound, called number into your expected format.

To learn more about creating inbound translation rules and assigning to SBCs, refer to Direct Routing [Step 4: Translate phone numbers](direct-routing-translate-numbers.md).

## Planning for tenant dial plans

To plan custom dial plans, follow these steps:

- **Step 1** Decide whether a custom dial plan is needed to enhance the user dialing experience. Typically, the need for one would be to support non-E.164 dialing, such as extensions or abbreviated national dialing.

- **Step 2** Determine whether tenant global or tenant user scoped dial plans are needed, or both. User scoped dial plans are needed if users have different local dialing requirements.

- **Step 3** Identify valid number patterns for each required dial plan. Only the number patterns that aren't defined in the service level country/region dial plans are required.

- **Step 4** Develop an organization-wide scheme for naming dial plans. Adopting a standard naming scheme assures consistency across an organization and makes maintenance and updates easier.

## Dial plans and routing considerations

There can be a maximum of 1,000 tenant dial plans per tenant.

Number normalization in user effective dial plans behaves different than number translation in route-based rules. For example,

- The Teams client normalizes numbers for all outbound calls, including calls placed from call history or from telephone-number links, based on user effective dial plans.
- With route-based translation rules, the Teams service doesn't normalize numbers that start with "+".

### Number lookup

Routing inbound calls to users is supported when all Teams user and resource accounts have unique number and extension values assigned for their telephone number.

The unique values of the user's telephone number can have two parts, as follows:

- **Number** - For inbound calls to resolve to users with Microsoft Calling Plan and Operator Connect solutions, the number value is designated as a number in E.164 format. For example, *+14255551212*. For Direct Routing solutions, the number value is designated as a number between 3 and 38 digits without common symbols.

- **Extension** - added to the *number* and separated by the ";ext=" delimiter (case insensitive), between 1 and 12 digits. For example, *+14255551212***;ext=12345**

An extension isn't necessary; only a unique number is required for Reverse Number Lookup. If multiple end-users are sharing a single, main number, and a [Teams Shared Calling](shared-calling-plan.md) policy *isn't* being used, then unique extensions must be assigned to each user. Otherwise, *extensions aren't required or recommended*.

For example, assume that a user is assigned the phone number +14255551212. If a PSTN caller dialed +14255551212, RNL finds the number-string match, and the call is connected to that user.

If the user is assigned a phone number with an extension, +14255551212;ext=12345, the inbound dialed number ***must include*** the extension for matching to work.

If the dialed number isn't matched, either because the number isn't assigned to an account or the number dialed doesn't exactly match any number string assigned to an account, the call fails to route or is routed according to [unassigned number routing](routing-calls-to-unassigned-numbers.md), if configured.

When you have a Direct Routing deployment with no digit translation configured on the SBC, and if the calls aren't presenting numbers in the format that you designated for your users, use a route-based number translation rule to normalize the inbound called number to a format that matches what is assigned to your users.

If you want internal users who call a phone number that is assigned to a resource account, to bypass the Reverse Number Lookup logic and route the call externally through the PSTN instead of routing to the resource account, you can enable the **skip RNL** option for the phone number assignment using the **Set-CsPhoneNumberAssignment** PowerShell cmdlet with `-ReverseNumberLookup`. For more information, see [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) and [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment).

### User dial plans with Calling Plans and Operator Connect

When you're deploying Calling Plan, Operator Connect, or Teams Phone Mobile for your PSTN connectivity, dial plans and voice routing policies are preconfigured at the service level and administration isn't necessary.

> [!TIP]
> Ensure that you inform users to dial numbers as they normally would for any call in their country or region.

### User dial plans with Direct Routing or extension dialing

 **If you deploy Direct Routing for your PSTN connectivity or are supporting extension dialing requirements, more steps are required to configure call routing.**

When you're deploying Direct Routing or extension dialing, the **user's effective dial plan** provides admins with the ability to configure a set of rules that help translate the user's dialed digits into a number that is resolved to a destination where Teams can route the call.

- You must configure call routing by specifying the voice routes and assigning voice routing policies to users. You can configure number translation rules at the route level to ensure interoperability with Session Border Controllers (SBCs). For more information, see [Configure voice routing for Direct Routing](direct-routing-voice-routing.md), [Manage voice routing policies](manage-voice-routing-policies.md), and [Translate phone numbers](direct-routing-translate-numbers.md).

- You can assign a Direct Routing online voice routing policy to Calling Plan and Operator Connect users and may want to do this, for example, to enable users to dial in to a call center that is directly connected with Direct Routing.

### Direct Routing online voice-routing policy with Calling Plan

If a user has a Calling Plan license, that user’s outgoing calls are automatically routed through the Microsoft Calling Plan PSTN infrastructure. If you configure and assign a Direct Routing online voice-routing policy to the user, Teams checks the user’s outgoing calls against the Direct Routing online voice-routing policy to determine whether their dialed number matches a number-pattern that you've defined in the online voice-routing policy. If there’s a match, the call is routed through the Direct Routing route. If there’s no match, the call is routed through the Calling Plan PSTN infrastructure.

For more information, see [Direct Routing voice routing policy considerations](direct-routing-voice-routing.md#voice-routing-policy-considerations).

## Related topics

[Create and manage dial plans](create-and-manage-dial-plans.md)

[Normalization rules](phone-normalization-rules.md)

[Route calls to unassigned numbers](routing-calls-to-unassigned-numbers.md)

[PSTN connectivity options](pstn-connectivity.md)

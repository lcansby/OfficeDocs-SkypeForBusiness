CSH---
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

An overview of inbound and outbound call routing is provided for context in relation to how Teams translates numbers that are received so that they can be processed for routing to a person or to a PSTN resource.

Understand the concepts in this article are a prerequisite for [creating Teams dial plans](create-and-manage-dial-plans.md) and [normalization rules](phone-normalization-rules.md).

## Routing phone calls to users in Microsoft Teams

Routing telephone calls in Teams Phone is accomplished by matching dialed number strings to resource objects assigned with the dialed number string.

Teams inbound phone calls are routed to users through a process called **Reverse Number Lookup (RNL)**. Reverse number lookup uses strict number string matching to find a user or resource account that matches the dialed number of an incoming PSTN call.

Inbound calls to users are supported when all Teams user and resource accounts have unique number and extension values.

The unique values can have two parts, as follows:

- **Number** - Designated in E.164 format, between 3 and 38 digits without common symbols. For example, *+14255551212*

- **Extension** - added to the *number* and separated by the ";ext=" delimiter (case insensitive), between 1 and 12 digits. For example, *+14255551212;ext=12345*

An extension isn't necessary; only the E.164 number is required for Reverse Number Lookup. If multiple end-users are sharing a single, main number, unique extensions must be assigned to each user. Otherwise, *extensions are neither required or recommended*.

For example, assume that a user is assigned the phone number +14255551212. If a PSTN caller dialed +14255551212, RNL finds the number string match and the call is connected to that user.

If the user is assigned a phone number with an extension, +14255551212;ext=12345, the inbound dialed number ***must include*** the extension for matching to work.

If the dialed number isn't matched, either because the number isn't assigned to an account or the number dialed doesn't exactly match any number string assigned to an account, the call fails to route or is routed according to [unassigned number routing](routing-calls-to-unassigned-numbers.md), if configured.

## Routing dialed phone calls for Teams users

Outbound telephone calls from Teams users are routed based on a series of assigned configuration items, including their assigned dial plan and their voice routing policy.

With Microsoft Calling Plans, Operator Connect, and Teams Phone Mobile, dial plans and voice routing policies are preconfigured and administration for dial plans and voice routing policies isn't generally necessary, if the users are instructed to place calls by dialing as they normally would for any call in their country or region.

When you are deploying extension dialing or Direct Routing, Microsoft Teams provides admins with the ability to configure a set of rules that help the dialed digits resolve to a destination that Teams can find and route to. The feature that Teams uses to accomplish this is dial plans.

## What are dial plans?

A dial plan is a named set of digit-manipulation rules that translate a set of provided numbers into another format (or another set of numbers) that Teams uses to route the calls.

The translation rules are optionally applied to phone numbers that:

- An individual user dials
- Are sent across PSTN connections ('trunks') between your tenant and PSTN routing integrations.

Teams dial plans change numbers from various input formats into alternate formats (typically E.164) for purposes of call authorization and voice routing.

A dial plan consists of one or more rules that normalize how phone numbers expressed in various formats are translated to an alternate format. The rules within a dial plan are known as [**normalization rules**](phone-normalization-rules.md).

A normalization rule in one dial plan can be translated differently than how it's translated in another dial plan, so depending on which dial plan is assigned to a given user or trunk, a dialed number may be translated and routed differently.

There can be a maximum of 1,000 tenant dial plans.

## Dial plan scopes

A dial plan's scope determines the hierarchical level at which the dial plan can be applied. Clients get the appropriate dial plan through provisioning settings that are automatically provided when users sign in to Teams. As an admin, you can manage and assign dial plan scope levels by using the Microsoft Teams admin center or Remote PowerShell.

In Teams, there are two types of dial plans - service-scoped or tenant-scoped.

- Service-scoped--A service-scoped dial plan is defined for every country or region where Teams Phone is available. Each user is automatically assigned the service country/region dial plan that matches the usage location assigned to the user. You can't change the service country/region dial plan, but you can create tenant scoped dial plans, which augment the service country/region dial plan. As clients are provisioned, they obtain an "effective dial plan," which is a combination of the service country/region dial plan and the appropriately scoped tenant dial plan. Therefore, it's not necessary to define all normalization rules in tenant dial plans as they might already exist in the service country/region dial plan.

- Tenant dial plans--A tenant dial plan (better for your organization) can be further broken into two scopes - user-scope or tenant-scope.
  - User-scope--If a tenant defines and assigns a user-scoped dial plan, that user will be provisioned with an effective dial plan of the user's service country/region dial plan and the assigned user dial plan.
  - Tenant-scop--If a tenant defines a tenant-scoped dial plan but doesn't assign a user-scoped dial plan, then that user will be provisioned with an effective dial plan of the user's service country/region dial plan and the tenant dial plan.

The following is the inheritance model of dial plans in Teams.

![How dial plans are inherited in Teams.](media/b2744f33-ebbd-4c23-bfba-1747312ab178.png)

The following are the possible effective dial plans:

 **Service Country**--If no tenant scoped dial plan is defined and no tenant user scoped dial plan is assigned to the provisioned user, the user will receive an effective dial plan mapped to the service country/region associated with their usage location.

 **Tenant Global - Service Country**--If a tenant user dial plan is defined but not assigned to a user, the provisioned user will receive an effective dial plan consisting of a merged tenant dial plan and the service country/region dial plan associated with their usage location.

 **Tenant User - Service Country**--If a tenant user dial plan is defined and assigned to a user, the provisioned user will receive an effective dial plan consisting of the merged tenant user dial plan and the service country/region dial plan associated with their usage location.

> [!NOTE]
> In the scenario where no dial plan normalization rules apply to a dialed number, the dialed string is still normalized to prepend "+CC" where CC is the country/region code of the dialing user's usage location. This applies to Calling Plans, Direct Routing, and PSTN Conference dial-out scenarios. Additionally, if a tenant dial plan normalization rule results in a number that doesn't start with "+", the calling service will attempt to normalize the number received from the Teams client based on the tenant dial plan, and if not matched, on the region dial plan. To avoid double normalization, it's recommended that Direct Routing customers normalize numbers to include a + and then remove the + using Trunk Translation rules. 

## Planning for tenant dial plans

To plan custom dial plans, follow these steps:

- **Step 1** Decide whether a custom dial plan is needed to enhance the user dialing experience. Typically, the need for one would be to support non-E.164 dialing, such as extensions or abbreviated national dialing.

- **Step 2** Determine whether tenant global or tenant user scoped dial plans are needed, or both. User scoped dial plans are needed if users have different local dialing requirements.

- **Step 3** Identify valid number patterns for each required dial plan. Only the number patterns that aren't defined in the service level country/region dial plans are required.

- **Step 4** Develop an organization-wide scheme for naming dial plans. Adopting a standard naming scheme assures consistency across an organization and makes maintenance and updates easier.

## Creating your new dial plan

When you create a new dial plan, you must put in the information that is required.

### Name and simple name

For user dial plans, you should specify a descriptive name that identifies the users to which the dial plan will be assigned.

The dial plan Simple Name is prepopulated with a string that is derived from the dial plan name. The Simple Name field is editable, which enables you to create a more descriptive naming convention for your dial plans. The Simple Name value can't be empty and must be unique.

A best practice is to develop a naming convention for your entire organization and then uses this convention consistently across all sites and users.

We recommend that you type the common, recognizable name of the ***geographic location*** or ***group of users*** to which the corresponding dial plan applies.

### External access prefix

You can specify an external access prefix of up to four characters (#, *, and 0-9) if users need to dial one or more additional leading digits (for example, 9) to get an external line.

> [!NOTE]
> If you specify an external access prefix, you don't need to create an additional normalization rule to accommodate the prefix.

See [Create and manage dial plans](create-and-manage-dial-plans.md) to create your tenant dial plans.

## Dial plans and routing considerations

If you want internal users who call a phone number that is assigned to a resource account, to bypass the Reverse Number Lookup logic and route the call externally through the PSTN instead of routing to the resource account, you can enable the **skip RNL** option for the phone number assignment using the **Set-CsPhoneNumberAssignment** PowerShell cmdlet with `-ReverseNumberLookup`. For more information, see [Set-CsPhoneNumberAssignment](/powershell/module/teams/set-csphonenumberassignment) and [Get-CsPhoneNumberAssignment](/powershell/module/teams/get-csphonenumberassignment).

If you deploy Calling Plan, Operator Connect, or Teams Phone Mobile for your PSTN connectivity, your PSTN service provider manages most call routing. If you deploy Direct Routing for your PSTN connectivity, more steps are required to configure call routing.

- For Direct Routing, you must configure call routing by specifying the voice routes and assigning voice routing policies to users. You can configure dial plans for number translation at the trunk level to ensure interoperability with Session Border Controllers (SBCs). For more information, see [Configure voice routing for Direct Routing](direct-routing-voice-routing.md), [Manage voice routing policies](manage-voice-routing-policies.md), and [Translate phone numbers](direct-routing-translate-numbers.md).

- You can assign a Direct Routing online voice routing policy to Calling Plan and Operator Connect users and may want to do this, for example, to enable users to dial in to a directly connected call center. You can set up a Direct Routing trunk to the call center.

If a user has a Calling Plan license, for example, that user’s outgoing calls are automatically routed through the Microsoft Calling Plan PSTN infrastructure. If you configure and assign a Direct Routing online voice-routing policy to the user, Teams checks the user’s outgoing calls to determine whether their dialed number matches a number-pattern that is defined in the online voice-routing policy. If there’s a match, the call is routed through the Direct Routing trunk. If there’s no match, the call is routed through the Calling Plan PSTN infrastructure.

For more information, see [Direct Routing voice routing policy considerations](direct-routing-voice-routing.md#voice-routing-policy-considerations).

## Related topics

[Normalization rules](phone-normalization-rules.md)

[Create and manage dial plans](create-and-manage-dial-plans.md)

[Route calls to unassigned numbers](routing-calls-to-unassigned-numbers.md)

[PSTN connectivity options](pstn-connectivity.md)

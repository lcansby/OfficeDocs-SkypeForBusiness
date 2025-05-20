---
title: Set up call priorities for call queues
author: mkbond007
ms.author: mabond
manager: pamgreen
ms.reviewer: colongma
ms.topic: how-to
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.subservice: teams-calling
audience: admin
ms.date: 05/19/2025
ms.collection: 
- M365-voice
- m365initiative-voice
- Tier1
f1.keywords:
- CSH
appliesto: 
- Microsoft Teams
ms.localizationpriority: medium
search.appverid: MET150
description: Learn how to set up call priorities for call queues in Microsoft Teams.
---

# Set up call priorities for call queues

Call priorities for Call queues in Microsoft Teams allow you to set the order in which calls are routed to agents within a call queue. This is useful for ensuring that high-priority calls are answered first, while lower-priority calls are held in a queue until an agent becomes available.

Before reading this article, make sure you have read [Plan for Teams Auto attendants and Call queues](plan-auto-attendant-call-queue.md).

## Overview

Call Queue Call priorities provide a way for calls to be prioritized within the same call queue. The priority of the call controls the order in which it is presented to the agents.

When an agent becomes available to take a call, they receive the highest-priority call that has been waiting the longest. If there are multiple calls with the same priority level, the one that has been waiting the longest is presented to the agent first.

The call with the highest priority that has been waiting the longest is at the front of the queue and is the next call presented to the agents.

As an IT admin, you can assign different levels of call priority on a scale of 1 to 5, with 1 being the highest priority and 5 being the lowest priority.:

1. **Very High**
1. **High**
1. **Normal** (default priority)
1. **Low**
1. **Very Low**

### Priority Assignment Conditions

Priority is assigned to a call in the following situations:

- When an Auto Attendant transfers the call to another Voice App or Resource Account
- Based on the Resource Account assigned to the call queue
- When Call Queue Exception handling transfers the call to another Voice App or Resource Account

### Priority Usage

The way a call queue determines which priority to apply depends on how the call reaches it.

- If a call queue *receives a transferred call*, the receiving call queue applies the priority set by the auto Attendant or the previous call queue.
- If a call queue *answers calls directly* (not transferred), the call queue uses the priority defined on the associated resource account.

## Configure call priorities

Call priorities can currently only be configured using PowerShell. You can set the priority for a call queue by using the `INSERT CMDLET HERE` cmdlet.

## Call priority call flow scenarios

### Scenario 1: Priority to callers based on dialed number

In this scenario, Contoso Support has a single Technical Support call queue that's open 24/7. Contoso's website and documentation provides their customers with the general number for all support requests. However, customers who sign-up for "enhanced support" are given a dedicated number to call. The enhanced support customers are given priority over other customers based on the level of enhanced support purchased (or not purchased).

Constoso Support defines the following call priorities for their resource accounts:

- **Priority 4** - Any customer calling the general support phone number.
- **Priority 3** - Customers call the Bronze level support phone number.
- **Priority 2** - Customers calling the Silver level support phone number.
- **Priority 1** - Customers calling the Gold level support phone number.

Customers in the call queue are presented to agents in the order of their priority. The Gold level customers are all presented first, followed by Silver, Bronze, and finally General support customers.

The following command shows how to set the call priority for a call queue based on the dialed number (Gold, Silver, Bronze, General):

```powershell
# Assign Resource Accounts to Call Queue
$callQueueID = (Get-CsCallQueue -NameFilter "Support").Identity
$goldID = (Get-CsOnlineUser -Identity contoso-support-gold@contoso.com).Identity
$silverID = (Get-CsOnlineUser -Identity contoso-support-silver@contoso.com).Identity
$bronzeID = (Get-CsOnlineUser -Identity contoso-support-bronze@contoso.com).Identity
$generalID = (Get-CsOnlineUser -Identity contoso-support-general@contoso.com).Identity

New-CsOnlineApplicationInstanceAssociation -Identities @($goldID) -ConfigurationID $callQueueID -ConfigurationType CallQueue -CallPriority 1
New-CsOnlineApplicationInstanceAssociation -Identities @($silverID) -ConfigurationID $callQueueID -ConfigurationType CallQueue -CallPriority 2
New-CsOnlineApplicationInstanceAssociation -Identities @($bronzeID) -ConfigurationID $callQueueID -ConfigurationType CallQueue -CallPriority 3
New-CsOnlineApplicationInstanceAssociation -Identities @($generalID) -ConfigurationID $callQueueID -ConfigurationType CallQueue -CallPriority 4
```

### Scenario 2: Priority to callers based on Auto attendant menu choices

In this scenario, Contoso Travel has a single Travel Support call queue for all travel inquiries. This call queue is associated with an auto attendant that provides callers with the following options:

> Thank you for calling Contoso Travel.
If you are currently traveling and need immediate assistance, press 1.
If you are calling to inquire about an existing booking, press 2.
To make a new booking, press 3.
For all other inquiries, press 4.

Callers who press 1 are assigned the highest priority level and are all presented to agents first, followed in order by those who press 2, 3, and then 4, with each number representing a progressively lower priority.

The following command shows how to set the call priority for a call queue based on the Auto attendant menu choices (immediate assistance, existing booking, new booking, other inquiries):

```powershell
# Create the Auto Attendant[CL2.1]
$callQueueID = (Get-CsCallQueue -NameFilter "Travel").Identity
$callableEntity1 = New-CsAutoAttendantCallableEntity -Identity $callQueueID -Type ConfigurationEndpoint -CallPriority 1
$callableEntity2 = New-CsAutoAttendantCallableEntity -Identity $callQueueID -Type ConfigurationEndpoint -CallPriority 2
$callableEntity3 = New-CsAutoAttendantCallableEntity -Identity $callQueueID -Type ConfigurationEndpoint -CallPriority 3
$callableEntity4 = New-CsAutoAttendantCallableEntity -Identity $callQueueID -Type ConfigurationEndpoint -CallPriority 4

$greetingPrompt = New-CsAutoAttendantPrompt -TextToSpeechPrompt "Thank you for callign Contoso Travel"
$menuPrompt = New-CsAutoAttendantPrompt -TextToSpeechPrompt "If you are currently travelling and require immediate assistance, press 1. If you are calling to inquire about an existing booking, press 2. To make a new booking, press 3. For all other inquiries press 4."

$menuOption1 = New-CsAutoAttendantMenuOption -Action TransferCallToTarget -DtmfResponse Tone1 -CallTarget $callableEntity1
$menuOption2 = New-CsAutoAttendantMenuOption -Action TransferCallToTarget -DtmfResponse Tone2 -CallTarget $callableEntity2
$menuOption3 = New-CsAutoAttendantMenuOption -Action TransferCallToTarget -DtmfResponse Tone3 -CallTarget $callableEntity3
$menuOption4 = New-CsAutoAttendantMenuOption -Action TransferCallToTarget -DtmfResponse Tone4 -CallTarget $callableEntity4

$defaultMenu = New-CsAutoAttendantMenu -Name "Default menu" -Prompts @($menuPrompt) -MenuOptions @($menuOption1, $menuOption2, $menuOption3, $menuOption4)
$defaultCallFlow = New-CsAutoAttendantCallFlow -Name "Default call flow" -Greetings @($greetingPrompt) -Menu $defaultMenu
New-CsAutoAttendant -Name "Contoso Travel" -LanguageId en-US -TimeZoneId "Eastern Standard Time" -DefaultCallFlow $defaultCallFlow 
```

### Scenario 3: Priority to agents transferring calls to another call queue

In this scenario, Contoso Finance Customer Service agents triage calls and they often transfer these calls to Tier 2 support groups. Tier 2 support groups can also take calls directly from customers. Constoso wants calls transfers from Customer Service to 

The following command shows how to set the call priority for a call queue based on the agent transferring calls to another call queue:

```powershell
Need example?
```

## Considerations

Keep in mind the following considerations when configuring call priorities:

- Agents always receive calls with the highest priority first, regardless of how long lower priority calls have been waiting.
- Currently, authorized users can't change call queue call priorities.
- Keep the highest and lowest call priorities available for future use. **(why?)**
- Agents don't receive notifications about which calls are what priority. The priority is only used to determine the order in which calls are presented to agents.

## Related articles

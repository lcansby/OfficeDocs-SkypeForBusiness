---
title: "Teams Phone features"
ms.reviewer: 
ms.date: 01/21/2025
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
msreviewer: jastark, roykuntz
ms.topic: article
ms.assetid: bc9756d1-8a2f-42c4-98f6-afb17c29231c
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
description: "Learn about the features, availability, and how to plan and set up Microsoft Teams Phone for your business."
---

# Teams Calling features

This article describes Microsoft Teams calling and Teams Phone features. For more information about using Teams Phone as your Private Branch Exchange (PBX) replacement, and options for connecting to the Public Switched Telephone Network (PSTN), see [What is Teams Phone](what-is-phone-system-in-office-365.md). This article is for administrators and IT professionals.

Clients are available for PC, Mac, and mobile, which provides features on devices from tablets and mobile phones to PCs and desktop IP phones. For more information, see [Get clients for Microsoft Teams](get-clients.md).

> [!NOTE]
> For details about Teams phone systems on different platforms, see [Teams features by platform](https://support.microsoft.com/office/teams-features-by-platform-debe7ff4-7db4-4138-b7d0-fcc276f392d3).

## Licensing

The features listed below indicate whether or not a license for Teams Phone is required.

Microsoft Teams Enterprise includes native calling features, and Teams Phone unlocks even more features.

To review licensing scenarios, see [Teams Phone licensing](teams-phone-licensing.md)

For features where a Teams Phone license is required, a connection with the Public Swithced Telephone Network (PSTN) and phone number is also required.

> [!NOTE]
> A PSTN solution is separate from a Teams Phone license. A PSTN solution provides a customer's tenant with phone numbers and PSTN access to domestic, international, and emergency calling. The Teams Phone license entitles a Teams user to enhanced calling capabilities within the tenant and access to the PSTN solution.
  
## Teams calling features

**Microsoft Teams Enterprise** provides the following calling features:

No - ![Image of a x for no](/office/media/icons/cancel-teams.png)
Yes - ![Image of a checkmark for yes](/office/media/icons/success-teams.png)


  
|Teams calling features  |Description |With Microsoft Teams Enterprise license|With Microsoft Teams Enterprise license + Teams Phone license|
|:-----|:-----|:-----|:-----|
|[Auto attendants](what-are-phone-system-auto-attendants.md)  |Lets you create a menu system that enables external and internal callers to locate and place or transfer calls to company users or departments in your organization.  <br/> Note that users *do not* need to be voice enabled to receive calls from the auto attendant dial by name, dial by number directory search. Users *do* need to be voice enabled to receive calls from the auto attendant menu options. |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)</br>See [Teams Phone Resource Account licenses](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)|
|[Call queues](create-a-phone-system-call-queue.md) <br> |Lets you configure how call queues are managed for your organization: for example, set up greetings and music on hold, search for the next available call agent to handle the call, and so on.  <br/> Note that users *do* need to be voice enabled to receive calls from a call queue.|![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)</br>See [Teams Phone Resource Account licenses](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)|
|[Voicemail](set-up-phone-system-voicemail.md)  | When a user receives a voicemail, it is delivered to their Exchange mailbox as an email with the voicemail message as an attachment. Users can listen to their messages on their certified desktop phone, and on all Teams applications. Support for voicemail transcription is enabled by default for all organizations and users. <br><br> Note that users *do not* need a Teams Phone license, *nor* do they need to be voice enabled to use Voicemail features.    |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Voicemail user settings](https://support.office.com/article/manage-your-call-settings-in-teams-456cb611-3477-496f-b31a-6ab752a7595f?ui=en-US&rs=en-US&ad=US)  | Lets users configure their client settings for voicemail greetings, call answering rules, and greeting language, including out-of-office greetings. <br> Note that users *do not* need a Teams Phone license, *nor* do they need to be voice enabled to use Voicemail features.   |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Music on hold](music-on-hold.md) | Plays default music defined by the service, streaming music, or custom music uploaded by the tenant administrator when an external call from the Public Switched Telephone Network (PSTN) is placed on hold. This feature works for one-to-one PSTN-to-Teams calls in addition to calls made to a call queue. This feature provides on-hold notification parity with other platforms.  |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|Call answer/initiate (by name or extension)   |Lets users answer inbound calls with a touch, and place outbound calls either by dialing the full phone number or by clicking a name in the client.|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|Call answer/initiate (by PSTN phone number)   |Lets users answer inbound calls with a touch, and place outbound calls either by dialing the full phone number or by clicking a name in the client.  |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Call forwarding options and simultaneous ring - REQUIRES PHONE SYSTEM](user-call-settings.md)  |Lets users set up forwarding rules so calls can go with them anywhere, or calls can be forwarded to colleagues or to voicemail.   |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Member of call sharing and group call pickup-TEST WITHOUT PHONE SYSTEM LICENSE RE MEMBER OF GROUP CALL PICKUP, reword desc](call-sharing-and-group-call-pickup.md)  | Lets users share incoming calls with colleagues so that the colleagues can answer calls that occur while the user is unavailable. Less disruptive to recipients than other forms of call sharing (such as call forwarding or simultaneous ringing) because users can configure how they want to be notified of an incoming shared call. |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Create and manage call sharing and group call pickup](call-sharing-and-group-call-pickup.md)|add desc|![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Shared Line Appearance](user-call-settings.md)  | Let a phone line be shared amongst multiple users so that another user can make and receive calls on their behalf.|![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Transfer a call and consultative transfer](https://support.office.com/article/b7f40f14-e083-46b9-b739-68038c8f73a0)  |Lets users transfers calls to another person or their voicemail. Or, if they need to leave their office but want to continue the conversation, they can transfer the calls from their PC or IP phone to their cell phone.  <br/> Note that users *do not* need to be voice enabled to receive transferred calls from another user. |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Call park and retrieve](call-park-and-retrieve.md)   | Lets users place a call on hold in the Teams service. When a call is parked, the service generates a unique code for call retrieval. The user who parked the call or someone else can then use that code and a supported app or device to retrieve the call.  |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Caller ID](how-can-caller-id-be-used-in-your-organization.md)   |Calls from inside the company display a detailed caller ID that pulls information from the corporate directory, showing picture ID and job title instead of just a phone number. For calls from external phone numbers, the caller ID as provided by the phone service provider is displayed. If the external phone numbers are secondary numbers in the corporate directory, then the information from the corporate directory will be displayed.   |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|Device switching   |Lets users play a call or meeting on another HID device that is connected to Teams; for example, switching from their PC speakers to a headset.    |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|Presence-based call routing  |Controls inbound communications with presence, enabling the user to block all incoming communication except from those specifically indicated.   |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Integrated dial pad](https://support.office.com/article/use-the-dial-pad-in-teams-27bc60b5-74c0-4e9c-808b-da4db9514d89)  | Lets users dial by name or by number anywhere in the search bar and in the dial pad, speeding up the process of making outbound calls.   |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|Federated calling   |Lets users securely connect, communicate, and collaborate with users in federated tenants.   |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Make and receive a video call](https://support.office.com/article/abf62493-670f-4b0d-b2cf-fe03b49caf42)  | If the user's account is enabled for video calls, the user can make face-to-face video calls with their contacts. All they need is a camera, their computer’s speakers and microphone. Users can also use a headset if their computer doesn’t have a built-in audio device. |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Secondary ringer](https://support.office.com/article/Manage-your-call-settings-in-Teams-456cb611-3477-496f-b31a-6ab752a7595f)  | Users with multiple speaker devices connected to their PC can choose to set a secondary device to ring in addition to their default speaker. For example, a user with a headset connected to the PC and desk speakers can choose to have both headset and desk speakers ring when a call comes in so that they don’t miss a call. |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Distinctive ring alerts](https://support.office.com/article/Manage-your-call-settings-in-Teams-456cb611-3477-496f-b31a-6ab752a7595f) |Lets users choose separate ringtones for  normal calls, forwarded calls, and delegated calls so they can distinguish the type of call.    |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Busy on Busy-TEST THIS ONE](inbound-call-routing.md)| A calling policy that lets you configure how incoming calls are handled when a user is: <ul><li>in a call </li><li>in a conference</li><li>has a call placed on hold. </li></ul> The caller will receive one of the following responses: <ul><li>hear a busy signal when the callee is on the phone</li> <li>will be routed accordingly to the user's unanswered settings. One option lets the caller leave a voicemail for the user who is already on a call.</li></ul> The callee gets a missed call notification but isn't able to answer incoming calls. This feature is disabled by default, but can be turned on by the tenant admin. |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Call blocking](https://support.office.com/article/manage-your-call-settings-in-teams-456cb611-3477-496f-b31a-6ab752a7595f?ui=en-US&rs=en-US&ad=US)  | Lets users add PSTN phone numbers to a blocked list so that the next call from that number is blocked from ringing the user. |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Common area phones](set-up-common-area-phones.md)  | A common area phone is typically placed in an area like a lobby or conference room making it available to multiple people. Common area phones are set up as devices rather than users, and can automatically sign into a network. |![Image of a checkmark for yes](/office/media/icons/success-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Media bypass support](direct-routing-plan-media-bypass.md) (for Teams Direct Routing only)  | For better performance, media is kept between the Session Border Controller (SBC) and the client instead of sending it through  Teams Phone.  |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Unassigned number routing](routing-calls-to-unassigned-numbers.md) | Allows routing of unassigned numbers to users, auto attendants, call queues or a custom announcement.  |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Emergency calling](what-are-emergency-locations-addresses-and-call-routing.md) | Provides location support for first responders when emergency calls are made from Teams. |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|
|[Manage telephone numbers for your organization](manage-phone-numbers-landing-page.md) | Administer number types, number acquisition, and number management. |![Image of a x for no](/office/media/icons/cancel-teams.png)|![Image of a checkmark for yes](/office/media/icons/success-teams.png)|

## Additional Teams Phone functionality

Optional features are available to enhance your organization's Teams Phone experience, including the following:

**[SMS in Teams overview](sms-overview.md)**

- Assign users with a number acquired through a Microsoft Calling Plan in the United States (including Puerto Rico) or Canada to provide SMS support.

**[Teams Premium and Copilot](intelligent-recap-calls-meetings.md)**

- Add Teams Premium and Microsoft 365 Copilot to Teams Phone to give end users enhanced capabilities:
  - Additional AI capabilities
  - Greater administrative insights to reporting, with alerting
  - Enhanced supervisory capabilities and insights into Call Queues with the Microsoft [Queues app](manage-queues-app.md).

## Availability in GCC High and DoD clouds

The following capabilities aren't yet available in GCC High and DoD Clouds.

- [Call settings for secondary ringer, voicemail, and enhanced delegation](https://support.office.com/article/Manage-your-call-settings-in-Teams-456cb611-3477-496f-b31a-6ab752a7595f)
- [Transfer to voicemail mid call](https://support.office.com/article/Transfer-a-call-in-Teams-b7f40f14-e083-46b9-b739-68038c8f73a0)
- Call phone number from search bar
- Microsoft Entra ID reverse number lookup

## Related articles

- [What is Teams Phone](what-is-phone-system-in-office-365.md)
- [Cloud voice in Microsoft Teams](cloud-voice-landing-page.md)
- [Set up Teams Phone](setting-up-your-phone-system.md)
- [Which Calling Plan is right for you?](calling-plan-landing-page.md)
- [Monitor and manage call quality](monitor-call-quality-qos.md)
- [Microsoft Teams add-on licensing](./teams-add-on-licensing/microsoft-teams-add-on-licensing.md)
- [Pricing for Teams Phone](https://products.office.com/microsoft-teams/voice-calling#requirements)
- [Teams for Virtualized Desktop Infrastructure with callings and meetings](teams-for-vdi.md#teams-on-vdi-with-calling-and-meetings)

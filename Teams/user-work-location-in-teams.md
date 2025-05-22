---
title: User work location in Teams
author: DaniEASmith
ms.author: danismith
manager: jtremper
ms.topic: article
ms.service: msteams
audience: admin
ms.reviewer: seema.bansal
ms.date: 05/22/2025
description: Learn how users can set up and use their daily work location in Microsoft Teams.
ms.localizationpriority: medium
search.appverid: MET150
ms.custom: 
  - seo-marvel-apr2020
  - chat-teams-channels-revamp
  - teams-chat-and-channels
ms.collection: 
  - M365-collaboration
f1.keywords:
- NOCSH
appliesto: 
  - Microsoft Teams
---

# User work location in Teams

Work location is part of a user's profile in Microsoft Teams (and throughout Microsoft 365). Users can set up work locations for the day in Microsoft Teams and share visibility for the days they're in the office or working from home, making it easier to coordinate in-person meetings. By default, anyone in the organization using Teams can see (in nearly real time) locations set by others.

## Work location states in Teams

|Options |Representation |
|---|---|
|Working remotely |![house icon](./media/work-location-remote.png)|
|Working from office |![building icon](./media/work-location-office.png) |
|Working from office with building details |![add building icon](./media/work-location-add-building-update.png)|

> [!Note]
> Setting location with building details requires the tenant admin to add buildings to Microsoft Places. For more information, go to [Configure buildings and floors](/places/get-started/quick-setup-buildings-floors) in the Microsoft Places documentation.

Users set up a reccuring work plan when they [set work location and work hours in Outlook](https://support.microsoft.com/office/set-your-work-hours-and-location-in-outlook-af2fddf9-249e-4710-9c95-5911edfd76f6). When a user sets a recurring work plan, their work location and work hours are also set automatically in Teams. When changes occur in a user's schedule, the user can update their work plan in Outlook or Teams. Any changes are reflected in both apps.

> [!NOTE]
> In Exchange hybrid environments, Places features are only available for users with a mailbox managed in Exchange Online. Users with an on-premises mailbox can't use work plans (or many other Places features). These users can continue to use Room Finder in Outlook, but any metadata added to rooms or workspaces won't display. To learn more about limitations on on-premises resource mailboxes, go to [Set-PlaceV3](/places/powershell/set-placev3).

## Location details in Teams

Users can learn where coworkers are working on a given day from the profile card details. [Profile cards](https://support.microsoft.com/office/profile-cards-in-microsoft-365-e80f931f-5fc4-4a59-ba6e-c1e35a85b501) make it easier for others in your organization to quickly get an overview of your online status, your next available time to meet, your work hours, the local time, and your work location.

People you interact with in a group chat will also have location details displayed in the list view. To learn more about setting work locations, see [Set your work location in Microsoft Teams](https://support.microsoft.com/office/set-your-work-location-in-microsoft-teams-6c14a0f5-3cd6-427d-b1d2-aa0365aebf88).

Users who are using chat from the same location as the chat recipient will see details displayed on the top header area of the chat message window.

## User settings to edit location sharing

By default, setting the user work location is an opt-in experience. By setting up work locations, users enable anyone in their organization to view this information. Users can set different sharing controls for each work location. For more information, see [Access your Account Privacy Settings](https://support.microsoft.com/office/access-your-account-privacy-settings-3e7bc183-bf52-4fd0-8e6b-78978f7f121b).

## Related topics

[Set your work hours and location in Outlook](https://support.microsoft.com/office/set-your-work-hours-and-location-in-outlook-af2fddf9-249e-4710-9c95-5911edfd76f6#:~:text=Set%20work%20hours%20and%20location%20from%20Settings)

[Show your hybrid-work location, availability to meet, work hours, and more](https://support.microsoft.com/office/show-your-hybrid-work-location-availability-to-meet-work-hours-and-more-c861198d-f82e-41d7-88ec-c2e716be5ede)

[User presence in Teams](./presence-admins.md)

---
title: Release notes for devices in Microsoft Teams
author: mstonysmith
ms.author: tonysmit
manager: pamgreen
ms.reviewer: eviegrimshaw
ms.date: 03/12/2025
ms.topic: release-notes
ms.service: msteams
ms.subservice: itpro-devices
audience: Admin
appliesto:
  - Microsoft Teams
ms.collection:
  - teams-rooms-devices
  - Teams_ITAdmin_Devices
  - Tier1
f1.keywords:
  - CSH
ms.localizationpriority: medium
search.appverid: MET150
description: Learn about what's new in Microsoft Teams devices.
---

# What's new in Microsoft Teams devices

This article contains updates for Microsoft Teams devices. To view feature updates for Microsoft Teams desktop, web, or mobile, go to [What's new in Microsoft Teams](https://support.microsoft.com/office/what-s-new-in-microsoft-teams-d7092a6d-c896-424c-b362-a472d5f105de).

To view feature updates for Microsoft Teams Rooms, go to:

- [Release notes for Microsoft Teams Rooms on Windows](../rooms/rooms-release-note.md)
- [Release notes for Microsoft Teams Rooms on Android](../rooms/rooms-release-note.md)

## [Teams panels](#tab/panels)

## March 2025

**Applies to:** *Teams app version: 1449/1.0.97.2025021101*

- Fixes for check-in and auto-release.

## January 2025

**Applies to:** *Teams app version: 1449/1.0.97.2024122401*

> [!IMPORTANT]
> Required updates coming to the session flows. Starting June 2025, clients more than five months old will no longer work.

- **Custom name**  IT admins can customize the display name shown on Teams panels through the Teams Rooms Pro Management portal. This feature is only available with the Teams Rooms Pro and Teams Shared Device Licenses. To learn more about custom names, see [Add a custom name for Teams panels](custom-names.md).
- Fix for Room Equipment not populating.

### November 2024

**Applies to:** *Teams app version: 1449/1.0.97.2024102301*

- Authentication fixes and check-in reliability improvements.

### September 2024

**Applies to:** *Teams app version: 1449/1.0.972024081207*

- **Custom backgrounds**  IT admins can upload custom background images on the Teams Admin Center to reinforce company brand on Teams panels devices. PNG, JPG, and JPEG formats are supported. This feature is only available with the Teams Rooms Pro and Teams Shared Device Licenses. To learn more about custom backgrounds, see [Set up and manage custom backgrounds on Teams panels](custom-background-panels.md).

- **Daily device restart window**  By default, the device restarts anytime between 2:00 AM and 3:00 AM based on its local time zone. If the device is in use during this window and the restart-window period ends, the restart is rescheduled the following day. IT admins can turn off this functionality or change the restart window from the device settings or remotely in Teams Admin Center.
- Bug fix for remotely changing "Release room if no one checks in" syncing to the device.

### July 2024

**Applies to:** *Teams app version: 1449/1.0.97.2024071105 (Logitech, Crestron, Neat, EPOS, AudioCodes, Poly, Yealink with CP 5484 and 6061)*

- Authentication and other check-in bug fixes.

### June 2024

**Applies to:** *Teams app version: 1449/1.0.97.2024061108*

- Company Portal 6152 (available to Yealink, Crestron, Logitech, AudioCodes, EPOS, and Poly panels on Company Portal 5484, 5882, or 6061). Fixes for authentication issues, including a fix for sign-in failures immediately following sign out.
- Multi-panel check-in support. (Generally available and for GCC. GCCH and higher aren't supported at this time) If a resource account is being shared across multiple panels, the check-in status for the meeting will remain in sync across the panels. This ensures the room is released or not released correctly. To learn more on the check-in feature, see [Check-in and auto release on Microsoft Teams panels](check-in-and-auto-release.md).

> [!NOTE]
> For every panel device, regardless of whether it's part of a multi-panel room, when you initially download this app, the current setting for Release room, if no one checks in, will be updated in Exchange. Allow 48 hours for this sync to happen. Be sure you download the app when there are no meetings scheduled within the next 48 hours.
> [!NOTE]
> Going forward, when auto release is enabled, disabled, or adjusted, it can take up to 48 hours for this change to take effect. For this reason, it's recommended that you adjust the settings when no meetings are scheduled for the next 48 hours.

### April 2024

**Applies to:** *Teams app version: 1449/1.0.97.2024040202 (Logitech, Neat, AudioCodes, EPOS, Poly, Crestron, and Yealink Room Panel with CP 5.0.5484)*

- More bug fixes for room reservations.

### March 2024

**Applies to:** *Teams app version: 1449/1.0.97.2023121202 (Yealink Room Panel and Yealink Room Panel Plus with Company Portal 5.0.5882.0)*

- Significantly reduce sign-out errors due to Workplace Join failures, timeout issues, and memory leaks.

### February 2024

**Applies to:** *Teams app version: 1449/1.0.97.2024010401 (Crestron, Logitech, Neat, AudioCodes, EPOS, and Yealink Room Panel with Company Portal 5.0.5484.0)*

- Authentication fixes for room reservations

### December 2023

**Applies to:** *Teams app version: 1449/1.0.97.2023111003 (Crestron, Logitech, Neat, Poly, AudioCodes, EPOS)*

- Turn on and off the QR code remotely via the Teams Admin Center.

### August 2023

**Applies to:** *Teams app version: 1449/1.0.97.2023080401*

- **QR code reservations on Teams Panels**  Teams Panels with a Teams Shared Device License or a Teams Rooms Pro License allows people to reserve the room using a QR code on the Panel. If you're signed into your Teams app on mobile, upon scanning from your mobile device, you can schedule a new meeting with the room prepopulated. You can also easily see the room's availability for your meetings and book the room with one click. This feature is enabled by default and can be disabled under **Device settings** > **Admin settings** > **Meetings**. To learn more about using QR code reservations, see Reserve a room using a QR code on a Teams Panel.
- The recommended version of Teams on your Android phone is 1416/1.0.0.2023153001 and above. On iOS, the recommended version is 5.15.0 and above.

> [!NOTE]
> The following instructions are for an Android mobile phone with an Android work profile (AWP).

- You can scan the QR code using the camera app on your Android mobile phone. However, the feature may not work if you have both work and personal profiles on your Android phone. In this case, your admin must add a mobile system OS scanner in the work profile.

To add a mobile system OS scanner:

1. In the Intune Admin Center, go to **Apps** > **Android**, and add.

2. Select **Android enterprise system app**.

3. Enter the type of Android phone. Then, Google and paste the OS camera package name.

4. Assign to an individual or group.

5. Download and install the camera app from the app store in your work profile.

- **Loading sign when creating a reservation**  When making a reservation on the Panel using the green **Reserve** button, you see a loading sign after you confirm the end time of your reservation to let you know the reservation is being made.

### June 2023

**Applies to:** *Teams app version: 1449/1.0.97.2023060102*

- To align with Microsoft Teams Rooms on Windows calendar experience, with this update on panels, if a reservation is scheduled to begin within 10 minutes or less, you no longer can book the room in an ad-hoc fashion on the device.
- When an admin changes the panel display name in the Microsoft Admin Center, it updates without an admin needing to log in again on the device.
- Enabling and disabling room reservations on Panels remotely in Teams Admin Center.

### April 2023

#**Applies to:** *Teams app Version: 1449/1.0.97.2023041403*

- IT admins can use Teams panels with their Government Community Cloud High (GCC-H) accounts.
- Fix for settings syncing with the Teams Admin Center and reset issues.
- Other bug fixes and improvements.

### December 2022

**Applies to:** *Teams app version - 1449/1.0.97.2022748302*

- Bug fixes.

### December 2022

**Applies to:** *Teams app version - 1449/1.0.97.2022747803*

- After an admin pairs a panel to a supported occupancy sensor through Device settings, you can see whether a room is occupied and auto check-in when check-in is enabled by your admin. If the room is available and someone's in the room, a message is displayed that the room is occupied. If the room is reserved but no one is in the room, you see a message that the room is unoccupied.
- Yealink's Room Sensor and Crestron CEN-ODT-C-POE are supported. For more information, check with your OEM.
- Support for Teams Shared Device License.
- Improvements and bug fixes.

### September 2022

**Applies to:** *Teams app version - 1449/1.0.97.2022739908*

- Improvements and bug fixes.
- Support for Microsoft Teams Rooms Pro Licenses.

### July 2022

**Applies to:** *Teams App version: 1449/1.0.97.2022739901*

- If you finish a meeting early, you can check out of the meeting room. This makes it available so others can reserve and use the space. Select **Manage** > **Check out**. If you need a few more minutes, if the room is free after your scheduled meeting time, you can extend your reservation for up to 15 minutes. Select **Manage** > **Extend room reservation**.
- This feature is turned off by default and requires the admin to enable the setting in the Teams admin settings. The setting to control this feature in the Microsoft Teams Admin Center will be available at a later time.
- A new Admin setting was added to disable room reservation from the panel. When the setting is enabled, a banner on the panel notifies people that the room can't be reserved with the Teams panels device.
- You can tap and pull down on a meeting tile to manually refresh the Teams panel calendar.

### April 2022

**Applies to:** *Teams App version: 1449/1.0.97.2022733702*

- New warning when a room reaches max capacity. This requires pairing the panel to a Teams rooms device (currently supported on Teams Rooms on Android with app version 1449/1.0.96.2022011305 or later) that supports people counting. This can be enabled in admin settings. To learn more, see How to use Microsoft Teams panels.
- New calendar look to help you quickly see a room's availability.
- View a list of equipment available on a panel. Admins must enable this setting in the Device Teams Admin settings, then turn on the setting per device. Admins can use the following instructions to make sure that devices are properly to display available resources: [Set-Place](/powershell/module/exchange/set-place) and [Manage resource mailboxes in Exchange Online](/exchange/recipients-in-exchange-online/manage-resource-mailboxes).

### February 2022

**Applies to:** *Teams app version: 1449/1.0.97.2022730007*

- To help ensure your meeting spaces are getting maximum use, we're enabling a way to check in to claim a room from a Teams panel. Users can check into the room by tapping the "check in" button on the panel. If no one checks into the room, it's released back to the room inventory for others to reserve and use.
- When paired with a Microsoft Teams Rooms on Android, joining a meeting from the Teams Room is considered as checking in and the room won't be released (it requires the Teams Room on Android app version 1449/1.0.96.2022011305 or above). Support with Teams Rooms on Windows will be available at a later time.
- The room check-in notification provides the end user with the ability to check in to their meeting when the panel is paired with a Teams Rooms on Android. After the user checks in, when the scheduled meeting starts and the previous meeting is running over, a notification appears on the Teams Room front-of-room display to inform the in-room participants their meeting is over and people are waiting for the space. This feature will be initially available on Teams Rooms on Android (it requires Teams app version 1449/1.0.96.2022011305 or above) and will be available on Teams Rooms on Windows at a later date.
- Calendar layout update to combine consecutive available time slots into one time slot.
- The calendar layout is updated to combine consecutive available time  slots from an hourly view into a single time slot. For example, the 12-3 PM time slot is combined into a single time slot to improve readability.
- Wallpaper refresh.
- The preset wallpapers have been refreshed in this app release to align with our Teams devices family.

### August 2021

**Applies to:** *App version: 1449/1.0.97.2021070601*

- Teams Extensibility and Line of Business (LOB) app support to tailor the Teams panels experience.
- IT Admins can do remote provisioning and remote sign in of Teams panels from the Teams Admin Center.
- Hide meeting names for sensitive spaces. This setting is off by default (the **Show meeting names** setting is on). The tenant admin can enable it through **Settings** > **Device settings** > **Admin Settings** > **Panels App Settings** > **Meetings** > **Show meeting names**. When meeting names is turned off, the meeting name is replaced with the meeting organizer's name.

## [Teams phones](#tab/phones)



## March 28, 2025

**Applies to:** *Teams app version: 1449/1.0.94.2025084203 (Poly, Audiocodes)* 

> [!NOTE]
> This update introduces a new versioning format, moving away from using dates. Going forward, this format will be used **1449/1.0.94. <year of release><internal codes>**



- Line keys are now available on touch phone devices. They will appear as an app on the home screen alongside other apps such as Calls, People, Calendar, and more. Users can assign speed dials by long pressing. For assigned contacts, users can manage and remove assignments by long pressing as well. Once assigned, outgoing calls can be placed to speed dials by pressing the line key. Additionally, the line key app can now be pinned, making it the default view on the home screen. 

Note: This experience is not applicable to sidecars and ONLY includes experience on the Teams app running on touch phone devices. 

![](data:image/png;base64,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)![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAMMAAAFcCAYAAAB1OAqIAAAAAXNSR0IArs4c6QAAIABJREFUeF7tfQl4XMWV9dHa2vfFkiXZMnjfsTFgGy9AALOGPYQ1fybLkAxhkkky2ckkmfknE4YsQwIMGZJJSMIQIEMwYHYM2BibHWO84lWSte8tdatb/39u+4l2061+T+ru9yTd+j59krrrVd06dU/dW+9110kaHBz0A0iCFkVgYiPgT1IyTGwP0NEPIaBkUGdQBI4hoGRQV1AElAzqA4rA8QhoZFCPUAQ0MqgPKAIaGdQHFIGwCGiapI6hCIwqTfL7/di1axemTZuG9PR0RVMRGA8IWI8MPp8PTz/9NN544w18/vOfR0FBgSUgeH1vby8yMjKQlpY2dO3BgwdRUVFx3GtmG+7q6pLrXC4XkpKS0NbWJn9nZWWZbULrKQLWyEBH3rBhA5555hmsXbsWH/vYx8TprBQ6/W9/+1tcfPHFWLBgwdClN910E/gzb948K81J3R/84AdYtmwZzjjjDLz00kv4zW9+g3/+53/G5MmTLbelF0xYBMyTwSDCCy+8gDVr1mDVqlXIzs62jNy7776Lr33ta/jKV76CM888c+j6X/7ylzjvvPMkYrjdboke/f39mDt3rhCuo6MDe/bsQWZmJmpra+W3UXgdyUVC3HzzzbjooovwhS98QaIF07menh7MnDkTAwMD0k5VVZW0z7+Li4vR2tqKQ4cOobKyEjU1NUhJSbE8Lr1gzCNgjgwkwpNPPonnn38eZ511FlasWDHiFCQSGS644AJ873vfw2uvvYaHH34Ys2fPxpEjR3D22WfLD6PJ3r17MTg4KDZcfvnlQzaQDKeddho2btyIxYsX45vf/Ka897vf/Q7r16+X9IskY50tW7bg2muvxY4dO6S9qVOnYtOmTVJ/586d+OpXv4rly5crIRzm29ynNjQ0IDc3Fzk5OZIOcxHzer0oLy8Xa7l4Hj16VDKCESxo5shAx7n99tvFUbmSBq/KwZjRobgir1y5MiKUkcgwY8YM3H333ZLm0GH/9V//FQ8++KA47GWXXYZ77rkH11xzjaz0zc3N+NznPieEYSEZ3nvvPQHi97//vdTnvuGcc87B9ddfj7KyMjzyyCOYNWsW6urqJD1ju9zv0ObNmzfj6quvBgFnBGG7IwDTYe4zvsx57rnnZEFk5KaP8cbNl770JbS3t4vfcC7vuOOOobmkD1gs5sjAlIJ5OMlAp5k+fbowM7QkJyejqKho2Khhhgzvv/8+7rrrLtx333146qmncO655+KHP/whli5dKg7LNOnTn/70cWRg3yQU0zjuaZhq8X/ubejwTLVIGqZaJBxTIv7P1OpPf/oTnn32WWn7Rz/6kUQXJYNFV4pz9b/85S/4+c9/LnP//e9/X8hAh2d0ePzxx1FSUoLvfve7Mv+f+cxn8NnPftaqRebIwFaZd9977704cOCA3EXibdVwhIhmgRkyMF258847hQxcEa688kqJDF//+tcl5aHTcoUwIhSdmj8k6hVXXCGA/eQnP5F9zZe//GWsW7cOTU1Nsldge9/61rfE4b/97W9j+/btknoxheL/jB633HJLxOgXbXz6fnwQ4IK8e/duyUzoA/Q9ZgncB86ZM0f+5xzTPxnZmUpZLObJYORkDEU0io45ZcoUy4QgGRjmtm3bhtTUVLH3oYceEib/+te/llU7mAzcp9x222342c9+hvvvv1+c9MYbbxT2FxYWDqVJ3EDfcMMNOHz4sKz2XEUYLb7xjW/INUyN/u3f/k1Ifeutt8pdK46BdnClIZDMP0lCEkMjg0VXSkB1LlrBCzD/Zwl9bSSLNABrZGDHdJhf/OIXkm7wliaZmojCgXN1YLFyF8vj8QgBmFOyjbfeeksiDm8CXHLJJdIebxDwWQXbDX72kYhxaR+OQcA6GWg6QxNzM66gY+nBFonA5w/V1dVy18i4C+GY6VBD7ERgZGSw0+LR9M2oxo01N9NWHxaOpl+9dkwgMLHIMCamRI20CwElg13Ia7+OQ0DJ4LgpUYPsQkDJYBfy2q/jEFAyOG5K1CC7EFAy2IW89us4BJQMjpsSNcguBJQMdiGv/ToOAX9SX1+fHjzsuHlRg2xAwJ/U3d2tZLABee3ScQgoGRw3JWqQXQgoGexCXvt1HAJKBsdNiRpkFwJKBruQ134dh4CSwXFTogbZhYCSwS7ktV/HIaBkcNyUqEF2IaBksAt57ddxCCgZHDclapBdCCgZ7EJe+3UcAkoGx02JGmQXAkoGu5DXfh2HgJLBcVOiBtmFgJLBLuS1X8choGRw3JSoQXYhoGSwC3nt13EIKBkcNyVqkF0IKBnsQl77dRwCSgbHTYkaZBcCSga7kNd+HYeAksFxU6IG2YWAksEu5LVfxyGgZHDclKhBdiGgZLALee3XcQgoGRw3JWqQXQgoGexCXvt1HAJKBsdNiRpkFwJKBruQ134dh4CSwXFTogbZhYCSwS7ktV/HIaBkcNyUqEF2IaBksAt57ddxCCgZHDclapBdCCgZ7EJe+3UcAkoGx02JGmQXAkoGu5DXfh2HgJLBcVOiBtmFgJLBLuS1X8choGRw3JSoQXYhoGSwC3nt13EIKBkcNyVqkF0IKBnsQl77dRwCSgbHTYkaZBcCSga7kNd+HYeAksFxU6IG2YVAgAyDg4NJg4ODSEpK+oghfJ0l+L1wr7FO6OvG/0aj4doIbdtoJ5wtZlCKNI5w15odc6TxWhlzMBaRcB7pmM3gEs5W4zorcxzazkjn2Ow8xxuTIOz8Sb29vUIGs4BqPUUgkQiQbFYWuFHY5mdE8HPhH0UjeqkiEHMESAC/34+BgQH54d+MEnGMFEqGmM+iNhhTBEgKr9cLj8cjESI5OTmm7R+XJmlkiBe22m6sECAJ3G63RAiSIU7RQSNDrCZM24kvAn19fRIdSIQ4RQclQ3ynUFuPFQL9/f0gIUgEJUOsUNV2xiQCBhkYGVJSUuIxBo0M8UBV24w9AkqG2GOqLY5RBEgGbqKZImlkGKOTqGbHBgElQ2xw1FbGAQKaJo2DSdQhxAYBR0SG5uZ+9PQOoLwsAxkZcdnFxwYtbWVcI+CIW6s7d3WhqakPc+fmo7Ag3TTg/f0+tLZ6kJWVivz8NFPX9ff7sf29Dpy0uNBUfaPSrt1daO/wYub0HOzZ24MlJ1m7/sWXm1BVmYmammykpOjHtCyBn6DKjogMIyEDP/W9Z28Xfnfffpy0uAgXX1gpTw69Xj+83kFxuLT0JLCep98vv12uZLR3ePCXR47g0zdOw8CAHx7PIJKSgZRkPnVMwoAvUJfump7Ohy8Bx33uhUbU1buxcnkJnnu+ETdeX4tetw8pyYDPD7iO1WWb7D81NQlpaXysH5jJO/9zLxYuyMeihYXStsuVEujf6xdb09OS4fH4pU/2P+AblNfCfOI9Qa4x8bqxJTL4/YPgCk1HYNm7txstLf2YOTNvaIXPzEg5zplCp6avz4dXt7bgyWeOYvoJObjg/EpkZabizbfasHdfNwoL03HKsmKJHG+82SZ9nXJyMUpKXFj/WB2uurIGr7/Rit27u5CZmYq8vDTUVGdhx/ud8Pvp4H6cuqwYNdXZHyHDpleacdXlNbjrnr04YVo2Ghv7sXBBIWqnZuOtd9qwb18PKioysHhRIYqLXENkmDcnD+muFLS09GHlilK8/kYb9u/vQUFBOpaeVIitr7XhtFOL0dXlxQf7e3D6ylJkuDRtTBQtbYkMbrcP7+/sxIFDvTJO2TP0HNszZAYmf/GCAlRVZUVMKRqb+vD4E/Xi9GxvypRslBan4+XNzSgry0BbmweLFhVi48ZGlJdnIjMzBV3dXiw/tQS3/XQn/vGrs/Dz/9iNC8+vRGNTvxBo8eJCvPFGG5adXCSOOmtmHtasKhMbjMiweFGBRKMf3roAn/vCNnz209PQ3OrBrl1dWLOqFBuebMD8+fk4cLAXM2fk4ow15UNkyHAlo67BjUsvrgIXhHvu3YerrqjBK1taUDEpQyIDx8P+uroGcPml1RoZEsUEALaQgY7Q2+uTTTPLvg+6ZQWfMT1XVmiW/Lw0SSXCpQm8fseOTjzw0CGcekoxDh7qRW5uKlavLMXW11rR1uZFcXE6lpxUBKZgbD8nJxUzTsxFeXkGfnL7TnzpC9Nx93/txT99dz7e29GB5zc2YuHCQhw80IPz1lXiiQ31KClJx9rV5RKhwpHhpptfw20/XiTtP7q+DiuWl+CJDQ0gYVpaPZg7Jw+nryiV9I1p0t59XaianIlrrp6K115vw/MvNMrehZGgqCgdk8oz8dQzDZhWm4358wqwYH5BAl1Bu7KFDKGwW90zkERPPtWA/Qd6MP3EXDS39GPA6xcHSk5JAjfWL29qljSDewgSgSv34SO94oiMDF//h9m48+7d+PhFVThS58buPV0SSUZKBkaps8+ahI0vNuKUZSWS+3O1r6jIHIoMpaXpOHzYDaZL+fnpeHxDPS44rxIDA4OSVnGv8Ms7d2NKTTY+efUU5OWauymgbhwbBMYkGbq7B8C7MyeekBMgQ3O/3CFKTUuWlKm7m1/U8GPZyYwaPZIycVNbWuoSwvzvX4/g6itr8MxzR9HW7kFHhxc+3yDOXFuOpuZ+yd+ZJuXmpUn91JQkvLO9A62t/ZhWmyNR5JpPTMFd/7kXn7qhFg1H+/Dmm21YtaoMW7e2yF0nRqrZs/JlH8HyxJP18jc35NzXnLG2HE8/exTpqcngN8AZIej8tK2wME1IqiWxCDiCDA0NfZLPT67MlNuk0QrTJO4xWJf5tbEh512hJCShu8crG0+jrfZ2D/yDQGFBmqy+3bw2MwVvvNWGujo3Oju9yMlJw3nnVkhbfNbBDTqjjCs9kKox2vCuUVpaEty9Pknn2C5v6XJl5w0BRiCSkO0zMmRnpQ6lebSX6Rav7+wcQGZWipCspcWDjMxksfftdzuwfXs7lp9WghNPyI0Gg74fYwQcQQafn1/IDtzeTNStRKZP29/rRMNRtzj/zBl5ktbYVfo9frzzbrvcBl66pEjIpCWxCDiCDIkd8vG9MRIEvgRupxWQVMnv4/dvjz8yx16rJlbvE54ME2u6dbTDIaBkUP9QBI4hoGRQV1AElAzqA4rA8QhoZFCPUASOIcCTMYzTMfRrn+oWExqBnp4eOTcpNTVVj4qZ0J4wwQfv8/nQ2dkpx0umpaUpGSa4P0zY4fPA4a6uLvnUanp6ukSGuB0v6ff79Uj6Cetqzh04ScC0iOkRIwOJEMeoQCD8SfX19X6Px5NkHPkdC3hicZ7+aNsY7fXEIRZtjAbPWPcfy/Zi0Va4NozXjDNVGQlIAoMIcYoKATK0trb6fT6fKPcEF6PT0NfNTC6vNXudlbpm+h5NnZHaYhWrkfYzmrFFunaktli5biT4GFoMxqFhcdZmCJChs7NzKE0KN8BQJgazOVj+yHg9GgmCgQnuzyxgkeoZbYW2ORzJrbYVKVqYGXM4rAwHtXJ9uAUr1K5wYw7tP5QcwfMc6zmOZt9wtiSABEb3H2q68RUlQwCXSMRSMgQ+OGmGvOEIYHXBi0ckHKZNVftMMODanXMRUDI4d27UsgQj4E/q6uqKKnA4nLxpcN4bmndG27QNtx8xm2cOt++I1v5wYIfugcK1ZaRUhq1WU6zgPD5cChbOhkivGWOJlPtHc6xwqU80/Ibbh4Sbl+HGGIxhMK6hf0cbxyje9yf19fVFJcMoOtBLFYERIUCi8Ye3/GNxG9eEESpWYgIkrWIDAgYZ+MCNap8kRZyjhJLBhnnWLi0iQDLw4xgkSJz03GiRksHivGh1GxAgCfjxbZJCpW9tmADt0lkIqPSts+ZDrbERAVtO4bZxvNq1IhARAZWxUudQBI4hoN+BVldQBJQM6gOKwPEIaJqkHqEIOCky8LxTfu+Hx7XbfeapesbERcARewbqG1BzoZJH0h+TsTIzJSRQ4ODgAJHMFF7D4+WtSuzyqHmeFk4hQ/5t9XqKIaYdEz00Y6fWSTwCjiCDVeUeAyYSaP+BbhQVuoRIZgrFTChEQskpK4ViKK1tHsydnYcd73dZvv7pZxpE9vaEaTkqfWsF+ATWHbNkYEQgie774wHRULv4wqpjwoBeEQd0ZSSjID9dFHmouEOxkpLidNGRe+TROtxwba38TdUeioZQD4HSuD29PrmGgSa/IF0iAYuh6Xb68hK88GITrrtmqshf8RpqKlCYkH9TqKSrk0IqKSJoYmg+G9K3c2bnS2QqKXaJ4Ep7uxcZmSkoyKf4iVdUeyh+wkhCIRRqVmhJDAK2bKCpcdzR7hHHYdl/oFekpk44IQd5uQHlHkrGZmd/qHwTCkdv7wA2v9KCLdtaUD05C2edWS4p1utvtqG52SPOffLSIhw+4sahQ72i73zitBxMnZqNPz90SMhAOSqq76SmJovmcu20bGzf3inO2dPtxclLi0Umi2mYQYblpxbj2Rca8anravHvP9uJhQsK0NTUj6lTsjFzZq4IF3IslLGiQGHV5CwxnWSYNSMX3gG/tLdkcRE2vtQkmnNM3RbMz8c773bg5CVFgsuBgz0484xJQ2RMjDtM7F5sIQMloqiQyZWV5WhjYM9QMYkyVgHp2zmzqaSTGXEvUN/Qh0fXHxF5XAqdT67MQk1VpqzaublpspegTtrGF5uQls4owaNAkjFvbr4IHH7ty7PwH7/ajauvqhE7qP9MgcN33gnISG15tUWkpNasLpPIEU7t8/Nf3IabvzAdRxv78fY77Vh9eikee6Je+qACKcdw1hmTxPlJBq/XB36147JLqiQi/e4P+3H+ukrReONYKaTOvQ9lehkdLrpgst5QSCA/bUmTDA02koKFGsyUiqVuMiVvWRgVIkk50VHofH955DAWLSxEXb1bnH3V6aWi2tnRMYCBgYAcFN+jaKFvYBCFBemYPTtPpG9v+eIM3HXPHnz/u/OECKOWvn2sDitPK8UzzzZg+fIS0W2jYDqF0fmNLJKhocGN7OwUXHv1VLz7XocQlYqkjHJMiUTg8JEjEiEp6E4dai2JQ8AWMoQOz+oGmlFk/eN1knPTuRsb+9HS0i+bU97xodggV9u1a8okDyepDh7sFWVPipAzMnzza7Nx96/3iiIo0xyKrI9W+parPBVEqWfNu01U92T6ZKRJ1IBmP4X56TjxxBw8+PBhrF5VBq/HL/9T5JA2VVZk4tpPTh2Kkolzh4ndk3PI0NyHuXPyZfWOViio/sabraKXHEiTvNi3r1vSDAoFUr2TImlz5+ajqalPIgOjyaRyF6ZMyRGt5nM+VoFXj8nUNjX3yaabzsw9xOxZeXh/Z5es4kyVuAnes7db2p08OROvvd6KdedU4sGHD+HCCyrR2uKRzfySJUXYsSNw1yk3JxUnTMvFpGOiiZtfaZY7XrTxvR2dsjd48+12IQIle5lSMY0jyUuKXFh3bkU0GPT9GCPgCDK0tnrQ6x5AaYkLLldgzzBcMdIs3r1hjs0NqMfrlztALH39PnEsytay8K7RoB/IyUmRukzPUlKS8fLmJuzf3yObWJLkjLVlUi89PQkeT0BskO2wsA7vSHH/QMJxs27I79IePnswcn22T6fnWIyHiMZr7NftHkC6K0Xs7eoOyOQmJyWBhNmzr0uIWl0V2HhrSRwCjiADnYklcLJZYgbP26eHDvdKJKAzVlZkoaAgsF+xo5BsvINEuxhRSCYtiUXAEWRI7JCP742RIlEEjDZOp8jwRrNzvL4/4ckwXidWx2UdASWDdcz0inGKgJJhnE6sDss6AkoG65jpFeMUASXDOJ1YHZZ1BNxut5ydRNlblb61jp9eMY4Q6O7ulkPEVPp2HE2qDsU6AiQBycCiZLCOn14xDhDgYcM8eJhEGBgYEJHDuErf9vf3q/TtOHCc8TQE4wRuEoB7Bf5vECFO+wXCF5C+HRgYEOlbMyWSplckPbhwYnmh/YQTPTSjHRbcTjgdNuP9SKKKZsbLOmZtsSLYaFbfbDgbI415tOON1Odwc2zgxN/DCZ8Ei60M50t8j4cMMxIYP3E8dDhABkrf+v3+j3zYJp4CEaFtx7MvY2JDVXJCJzzeNiR6zNHGazhtqDqP2QXCaj2r+BoqnySAQYI42xqQsRocHLT1k2dWgbI6EcGrVZwBjWiaE8kwEhxHes1I5jh4rhIwb8dL34ZLK8wO3koqESmURkprQutHSjFCbbCSilipGy0lCJcGjlQuNhiTSNp64aKAlf7smOPg9DMc9glw/tBhq9qnWUfQeuMegdiSYSShMB4QR7LDrH1m68XD9khtjtSmkV4XazsSidUI+zK3ZwgHqNnXRmhY2MvMTqzZelYnPFzeH5wyxXKsid7nmJ3P0WIbDaPQ9o2NdLTrYvC+P8nr9dq+gY7BQLSJcYYAScEfPmswc2csBsNXgcMYgKhNxAkBkoBPoD0ej/yOc5RQMsRpHrXZGCLA6MBPrJIcKn0bQ2C1qbGJAD+WodK3Y3Pu1OoYI6DStzEGVJsbuwio9O3YnTu1PMYI6Nc+YwyoNjd2EVAyjN25U8tjjICSIcaAanNjFwElw9idO7U8xgg4ggzBSppmVTtjjIM2pwjAFhmrUNwpI0Xtg5rqLFHsMVt4UC9Pr+Yx72ZPreY1VNWxeuI2j45nX9Rd4FH0BSZ0JILH0dzSj8yMFGRlRdapMzturRcfBBxBBqvKPQYUFBJ8+9120UOjWo6ZQkfevKVZtNasFAqL0KEXzs/HW291iKCilfLoY3WYVpuNGdPzTBPXSvtad/QIjFkyUMfgvR0d+OP9B0Vx85KLq8TJKElFpZ6cnFQhCbXdKDbI+pSU8nh9WP9YPa755BS0tXpAoUTqM1B8hNdQdcfrDQiVUGknOysQqYakb1eU4KWXm3H1VVOkf0YyEoyqnryecloUPCwsSEN5ecaQ2IkhfUslIEZBqg61tvWjrs4tErmUruLfkydnod/jEwHEikkZokSqJTEI2EIGpht0Qq7sLIeP9Mrk00HoUCxVVZkiaRVpD0Fdt5debsL7u7pQWpKOlStKRTnn9dfbREWHSj4UOKTgIWWvmB6xvblz8/D7PxzA5/7mBPx1fZ0QiBoNJMuMGbl46+12FBe70Nzcj6UnFWLe3ILjpG9PXVaExzfU46bPTccP/mU7VpxaguYWj6RdJOXmLS3gl72p+UBZLkrnspAMFDyk5FZZqQtzZuVh/RP1mFSWIeKOlM7atbtTBBupAU253vPOrRgiU2LcYWL3YssGms5K1RxK3rJQkZN5fHVV5tCegZrNJSWuiGQ4csQtap9UCG1s7kdZaYb8TYFBSk1xtaX07YsvNYmucmlpBiaVZ8i+5Lbbd+Irt8zEr+7eg8/8n2nYf7AHb77VLgKH1GSj6CBX/6lTsrBmVZmszuGkb//2i9vw9a/OQl19n0jlnr6iVDTZ6Ngc34J5BTjn7Ioh6VuKs2dmpeCKS6tFn/p//nwQq08vw85dnRIFKNlLbTkqfzJaUc7KKUIqE4EmtpCBKzGjA1dvlj17umR1nT0zD/nHpKQyXNwUh08ReC3Fx/+6/siQ2mdRYTpWrypFY1O/OBSjDUUEufEl+Zjv+wb8WLG8VKRv//7mGfjVXR9K377wYiMWLizEwQM9OG9dJZ7YUI+SknSsXV0uq3M4Mtx082u47ceLRNN6PaVvl5eC7Zx1Rjncbp+IIQZE1QPSt52dTMH8uO6TU7FrTxde3tSMdedWor/PJxGRUeq+Px6Qa6hUOq02ZyL4oGPGaEuaFDp6qxvozi6v6CUzz1+woEBSLqp9VlRkiOh4f79P0qOPnTVJVmAW7iU8Hh8uu6RapG+/8405uOfevaianC05vLvPh8WLR04GkufiC6uw4UmSyCWytYwQM2cEtJyNNKmj04ue7gGcdmox/vu+/Vh6UrHYyxSLd6ju/e0+lJZk4Lprp8KVrvuFRDLFOWSwIH1LNc/du7tQUZGJkmKXbGCZajGScMNMvef0tGTUTs1BV5cXDY19In07uTIDRUUuvP12u+wnduzsRGeHV67lpvfSj1dJW1NqsmTTTS3nyZWZkqrx9i9VQ9kfibZsaTFefKkRp51aApLz0CE3Zs3MlfSIe4Cc7FRR7GTKw7J9R4dI2jL9oQg89yfcMLe1e5GZkYxp1LAeGMSGpxpkT3HGWmt3qxLpNOO1L1vSpFAwA6mMD3m5aaY2jEyz6PR0fubUxgbYyK/5Hp89UL+ZRdKxQUraHpOxHfDD7xvEk083YNfuLqm35KQirDitRNri/9xQsz2jDf7P93iXiX8zdWL6xTa5OTdeCzz7GERKCk9z/nBlJxl5LYnF65gSMX1iVGAffP+pZxrAvdDll1ajtNQ1Xn3OseNyBBnoZCyJ3Cz6BwfR1Tkg+tN02tzcVGSY0KCO10ySTLytS/oWFUW+ixav/rVdyBNoftuNX/uM0+HD+h1os47mJBleszaPp3r65Z7xNJs6llEhoJFhVPDpxeMJASXDeJpNHcuoEHDErdVRjUAvVgRihABPxyAhDL2GGDUb3IxuoOMAqjYZBwR4J8kgg95NigPA2uTYQIAn6fX09Kj07diYLrUyXgiQCDxrlWTgg1CVvo0X0tquYxEgCSi6SSL09vbK3+np6fLALU6qPv6knp4eETiMJnvkWNTUsHGJgHECN89X5d8kQhyjAjH0JzU0NIj0rZJhXPrUmB0UV39GAf6QBPwdd+nbtra2sNK3YxZFNXxcIBAsfWv8Haf0yMDLnIyVWXTNKn6abW+81RsP+CRqDAmWvQ2kSd3d3fxKm6060OPN6XU8YxIBJcOYnDY1Oh4IxI4M8VaBNDN6J9hgxs6xWmec4+tP6uzsjEmaNBxQCVJrlFtwcd5kmfbjRNmSqH44cDvmOM6ihsHz6U/y+XwxIYNpL9GKioAJBIznDBQ3TIDSZ2ADPTg4qGQwMTlaxR4E+OSZH9AjKeIcJZQM9kyx9moFAUYGfoSbxFDpWyvIad1xiYBK347LadVBjQRgHJ1oAAAZJklEQVQBpkr8YaoUp+igadJIJkavSTwCejpG4jHXHh2KgB4I4NCJUbMSj4CSIfGYa48ORUDJ4NCJUbMSj4CSIfGYa48ORcARZKCwB0U8qIRpVrXToXiqWWMYAUeQgVoI7e0e1NbmiLSs2cKTq3mkO0/RNo6bj3Ytr6FwyaRJGdGqHvd+S2u/CKGUFKfLadkUT7RSOEae9F2Qn+aYD/pZsX8i1DXIYHz9Mw5jjv6cwapyj2FkY2MfXtrUJKIkixcVmrKd4iXPb2zEhedPNlXfqLT1tVY0NfWJTtzWbW248PxKS9f/+aFDIs87Z3a+Rj9LyCWusiMiw0jIQHGPd95tx/0PHMSC+QWiusPowBWYSpmFhek4YVqOCIPseL8T3gE/5s/Np2YJHn+iHp+4sgYNDW7s3dcjKqEUF6Ri59GjPGLQj+QUgDK1+XkB5Z1g6dvNr7Tgystr8PLmJlnpqVQ6Y0aeqIkeqevFgYO9KC9zYeqUHLhcAcESQ/q2pjobjU19mDcnX+S3qGdH2SvaumdvtxCGmhHUpuNrVCDSkhgEbCEDU5sP9veg4WhA7ZO/KUpIyShqobHMnJ4rOsqRpG+pjfbCxkZxXooDUpaKTr3ttVZkZqSKlBVX8bffaZfXSQJ+dnbZyUW457/24eYvTscf/nRAVDY9nkFRBJ0zOw9vvNmO6uosHD7cK9FmyeJCscEgw8lLi0Rl9B9umYVvfPttnH1WOVrbvGLzsqVF2PhSk4iNUPJq1ow8IapBBspjUQ6L/VCTmkSm3SQB1U0PHOzBvLn5ko5RoPHjFwW0rbUkBgFbyMDNMmVvW1o+1IGmPvLUIB3omupMEfyL9EUaRgCmHnR4Sj8VFqaJhvKGp+olGlBTmu9RwpZ1qSs9Z1a+rP6G2udd9+zFl2+egd17uvHqthZR+6RWHNU66fwk55rVZUiLJH37d9tw63fmiY7b8y80ihb1o+uPYMb0PHFmkun8dZSvDah9HjjQLQqgV11egx3vdwmpliwpEoVR7mFI/sOH3SJhRS24M9aorltiaBDoxRYyiAabf1B01Vioq0YR8tmzA6kGC1fESFGBzr55S7OkO0wlWto8Ijy4+vRSIQJXZUrjchWnI1I1k6KCTIsuvGCy6ED//Zdm4I47d+P735mH93d2iWTtaKVvqQP98uZm2U8wjeNmmyKMBhkovcsU6fprpmL/wV4w3brismoMeP3IyEyRO2p337NXFELPP68CVZOzEukLE74vW8gQirrVPQOjyIMPH0JNVRaWLi2SlIbpTV5+Gropltjvk3Rk3bkV2LmzUwQOmYZxT3ERyfDTnfjet+fiv367D6nJySJ7y/dGI3274ckGXH5pFf66vk7EFXOyUyQyBKdJc2bloq/fLzZddOFk3PmfezBzep68tvzUYkyalInf/2G/RMQbrp06JK444b00QQA4525Sc2BTSUeIVriCUq6WG8/srFSJBrzdaShztrT0yzOL8rIMUQXlptbnA6qrMpGaliwbbAqOH67rRVenF/sP9OCD/b345CemiOooowzbSEtPRlGhS4QX2X6/xy+3frnHOaE2Bzt3dYqAuds9IClfVVWW7FUY5bKzA/0bt3yZNuXmpCEjI1nSKkYM2s0Uj3sepmTctzz73FFMKs/EiuUl0WDQ92OMgCMiA53M7/PD5eLxfuY2jKFigMGKoaHqoeH+7+vz4aG/HBZ95pysVJxzdoXsMVgMOV3jbwNzo8/Q33w/2J5w6qWh7xvKpoGDDJLQ2zuAhx85gtaWfnzqhlq5u6UlsQg4ggyJHfKHvdEPA1/zC2gy21loi8frQ2qQfrWd9kzEvvX7DBNx1nXMYRGY0JFBfUIRCEZAyaD+oAgcQ0DJoK6gCCgZ1AcUgeMR4LlJ/OHJGKr2qd4xoRHguUkkg6HmEwcwon+EOw6dapOKgCUE+Lynu7t7SPpWI4Ml+LTyeEGARGBEoOInU6Q4ihxqZBgvTjPexkES8LBh42Ebx5eWlhZf6duOjo7j1D6tanYFPx0eiWJocH+R/rYy0VbtZ9uh10RrwxhzpPEa18diPFbGHqluuPGxrpX5ijZms3ZawYSfQOAPrzGkb+P4aQR/UmNjY0ykb6M5kFmwxkq9aOON9v5YGWewnYkck3GmqiF7G8fvPhtD9Ce1t7f7BwcHw+pAW1kNhgPKSjt2O4lZW6PVi/a+3eM0+rdi53B1rbQTbexGW/xtkCKOEeFDMnR1dalYSZjZSaQ8VDTnmMjvJ4AEH5JBpW8nsqvp2IMQiJ3ap8KqCIxxBJQMY3wC1fzYIfCh9K2V22yx619bUgQiI2Ao9CRo36AP3dQZnYmAIX3r8XhU+taZU6RWJRoBkoJPob1er0rfJhp87c95CPApND+1qtK3zpsbtcgGBPhhPaZM3EfEaQ+hewYb5lW7HAECejrGCEDTS8YnAvod6PE5rzqqESCgZBgBaHrJ+ERAyTA+51VHNQIEjD0DN8/6tc8RAKiXjB8ElAzjZy51JKNEwBFkoOggj2fPy0tDmmqYjXJK9fKRIuCIPcMHH/Sgta1ftA5ICLOF6jg8yp0aCBkZAS24aIXXUB+hdmp2tKrHvU89iN5eHyorMnD0aD9qa61d//7OThQVpoumhNlj9y0ZqJVHjYAjyGBVuccYNYU+HnuiDrNm5uH0laWmwGjv8GDDUw2iq2albHqlWcQUKZC4aVMzrrB4PRV5KNNFJR9qxGlxHgJjlgxU73nzrXY88OBBzJ9XgEsvqUKGK0X04ShSWFqWgfnzqJzpw7ZtrSJlddopxaLc8+RTlJyqFnXNd7d3iPoPpXIpLMjX+tx+pKQmYcH8fBQXuWTWDLXPVStLsGVrKy77eDUeffzIMZUfj0hWlZW6sPeDbuzc2YXqqixR9TQiliF9S1WeQ4d6cMqyYhw40CtqpBUVtLUAb73TjsULC9Hd7cXhOrdI9VLARUtiELCFDG63Dzt2dooKJwtln3p6BkT2iUJ/LIsWFIhDGdJUoXC0tXnw7PNH4e7zIy01SSRjKXG7dVsrysqomtkrGm1btrSIvBS1SNjP2jVl+I9f7cbXvjwLVPskYXp6fGhu6ZdVm9K5M2fmCaEWLSzA8lNLjpO+pRTu/X8+iO98Yy5u/vLruPTiKpGuohTvyuWleO75oyKRdbSpT9K+U04uFtNJhsmVGdi1pxurV5aIjb/+zQe4+MLJQtaa6iw0HHVL39w/1dX14aorqjWlSgwPpBdbyODzDYpGWkdHQPqWIuJ0KDpRXm6qvEZi5OSkiROHK/v39+BP/3NQ0qN9+7tFa+20U0vw2ON1oADiwgUFWLK4CC9tasJbb7dj2rQcrFwecOyf3P4+bv7CDNxz7z5855tzsGNHJ158uUnUPvd/0I1zz6mQ6EGHXUvp27TkociweFEBfnfffvzw1gW46ebX8H9/tEA04Z7YUI/lp5XgkUfrcOIJOaLVRrVRKn+yT5KBIu7z5+fj6iumiNQu1Urp/I2NfSJ9y33M9u0dQt5J5RlYsdxc6pdAfxnXXdlCBiJq6J7xbwoFNjX3Y+6c/CHp2+FUpSiqTvHxJ59uEHlYrsrlpS6sXlUm0YGp0frH68UZ8/PSZNP62uutePfdDtxwfa1I337llpn4xS93iY4z9yyxkL5dtbIUr25txZWXVyPp/5OOip95eQHBRpLB5UrCrl1douRZ19AndW+8vhaD/kG5CcBx/PtPd2L2rDxceXmNpG1aEoeAbWQIHqLVDTSjyAMPHsLCeQU45ZRiSbe4stOh2tu9In3LNOr88yvx5lttkgYx9aDQ+LpzKvDTX+zC9741F/993wdoafGKIij3DEtOKpQ9w3nnVIq4enGxC2tWBSLDCxsbcaTejcULC3DfHw/g+9+bj7+75XX8+F8WgnfDnnq6AVdeUY3//esRkd+lQOEpJxdhyUlFMtS7f71X0jB+kWTji01CiJ/dsQtVlVmS6p2xthRTqrPxpwcOIic7DTdcNzVxXqA9DaVJxpH0xtdBYwxN9I9w79nbLVKzvCtEh41WeHuUt2IpoE5HZdpFB0xO4YFQkLYoM1tQEGiLt0UpfVtVlSl1W1v7UVqSgboGNzraPZKmHT7sFulbn88vjsxnH6mpySJhyzYpS0vScEPc0eGVNK6uzi3pDYnG/hmBuB/i/iMrK2VINpc2tLR6kJkRuAV8tLFPJH6512HfeXmpKCnOEMH0l15uwpSabCxdEiCRlsQh4IiHbt4Bv6QKdOw4faniI4gylXp8Q73cfaLDn7GmXO7+2FX4vOTxDQ3o6vTgyitqRMdaS2IRcAQZEjvkD3sLSN8OIjk5cDCwnYW2cFFITUnSO0g2TYQj9gw2jV27VQSOQ0DJoA6hCBxDQMmgrqAIKBnUBxSB4xHQyKAeoQgcQ0Clb9UVFIFjCFDgkNFBBQ7VJSY0AjxJr6urS85cpcihbU+gJ/Qs6OBtR4AfkWFU4PGSPAhAI4PtU6IGJBoBRgNK35IETI8YDaj4GdfjJZubm02rfUbTOTM0Hux8YhxsYzR7Qyc4tL6Z8VjtYyRONdI+zFwXbszDzZ8ZTEYyxuGuYUQwNKDjlCKxe39SU1OT3+fzhVX7tDKoRMqiWrFL68YOgUTOsaHySSIYsreG+mfsRnRcSwHpW+qC8+VQ9Z5oK0Sw3Gk4oMy8ZtQJ11Zw/+GUhSJdExodwoEXybbhgA4XdYLtGq7NcPVC64eONxib0BXZsCXc70jjHQtzHDxmw/njTAIDruiabpHCYrTXQyckeOJD/zbD9EgyW6FkCteWFZIbDhNuIQg35uHsCm3LTNoSbH+wowe/bnXM0dLWaHMZen1w/UiLQazmOJrtZnzHZJ3oZDDZkFZTBMY6AkqGsT6Dan/MEAiQYXBwMClSfhopDRiNCcG5fmj4N/6PlCJE6jec/VZtDLVrtBvGcOlMpJQtGs6xGl8orqMd43DzEW2PMtx+J4Hp0fF7BpLBquOEOu1Irx+L11nN/cfiGMPtXRI9jpHsO0ZhY/TvQI+icb1UERgxAlxw+ODNkL41GopjxFAyjHi29MKEIEBSkBD8YYnrQ7fBwcGh5wwJGZ12oghYRMCQvuUH9eIkVEKLNDJYnBetbhMCKn1rE/DarfMQUOlb582JWmQTAvq1T5uA126dh4CSwXlzohbZhICSwSbgtVvnIaBkcN6cqEU2IaBksAl47dZ5CDiCDNRb4KnYRUUuuNJV/M95bjIxLHIEGXbvOabPMCsPBSb0GYypochhV7dXhA3NHuHOa6gHQXUcK4VSVV3dA6idkoWDh9yWj69//Y02lJW5UDEpM6JOnRV7tG7sEXAEGawq9xgwiK7bAwdFDJE6bGYKRU4eefQIbrxumpnqQ3VeeLEJ9Q1urDi1WPTdrr+21tL11I+jmOJJiwpV+N0Scomr7IiHbiMhA9VyXn+jFX9+6DDmzskTKVtGB8rHvv12OyZPzsSyk4tFSef5FxrR7/Hh7DMnITMrBU89fRSXfrwKu3Z3ioxtXm6a6KdVVGSKyifFz1NTk3DqKcWi0MPyofRtKba93ioqnff94YAIEVKJh2KEkysz8d6ODpHkPWFajshiGRHLkL6lXNaePd0464xy0ZJ7ZUuzKPVQCnfzlmasOK0UHZ0e7NvfI0qhmSbF3hPnMuO3J1siQ0/vgOgf7/ugR5Cl8qe714fi4vQh3WTqodVOzYmYUlCq6qlnGpCeniLyUpSZpXQURQOnTskWPWbqrz2/sUlSGkrofrC/RzTdbvvpTnzrH2fj9p/twtrVpWhr9+LwEbdI5b66tUU0nSmGSB1miibyWoMMwWqfn71pK667ZqroyB063IO1q8tFdJGSuUyrSIjVp5fJGEmGspJ0vPteJy6+sFKUTO+4czf+5lPT8OzzjaiclCF21NZmi9TW0aP9uObqGttFVMav6390ZLYo93CymetTB42FTkpCUDKW6pwsRUXpyMwI6KmFFqrc7NnbJdK3dNZ9H3SLsPmq00uFICTKvDkFsjK/+lor3nyzDdXVWbLqcsUX6dubAtK3P7h1ngijP7+xUaRvDx7owXnrKkXKtqQkXRx8OOnb2368SPp/dH2dSN/+dX0dZs7IRcPRPixdXCjpmyF9+/Y7bSJyePVVU7D5lWY8/cxRzJyZi7Y2asS5RPp285YWITNlgKlWqiVxCNhChtDhWU2TmPpQEJ0C5jU12Whv9wgZTllWBFdGCvr7/NjwdAOWn1Is/xcVposWNCV2b7iuViLDV/9+Fu64cxdu+vx0Uetk6rNo0cjJ8Njj9aIZTSdfd26lkK6wIE3ukBmRIT8vVTbv5549SUQRX3ipCZ+4Yop8wSQvL01Sup/+fJdEuauvqhEFUi2JQ2BM7hk6O7147Il6zJmVhwULClBf7xZn5gre1cXjAn3o6RnA2jVleH9nJzq7vPB6BlFUlCa5/W/+ez+++LfT8fAjh2RVprigy5WCFctLRBmUqc2LLzWhsJDytcWi+sn06WhTP+bMyhXh8y99cQb+6Ufb8bV/mIVDh914eVMTzl9XiWeeO4rOzgERd2e6NGd2vszm/Q8cFAF0Brotrzbj4xdX4Y/3H0Bhvku03BhVeLfpwYcPyx7mE1fWJM4LtCdBwBGR4eDBXrR3eFBbm4PcnOgql0yzKCBOh6Oj8v9etw8pyQHpW7bFjavRFgXX/X5IKsLffL8gPx2793ahqakPjY39QqBLL6mC3zco15Ig3CtkZgZSNbd7AAM+iNZ0d7cXxUUukaotKXbJnoWbbsrZ9vX7ZA9BmVsKohtpHuVyXa5k+aEMLm1j9Khv6BO1URKA6eLWbS2YP68A8+YGSKQlcQjYsoEOHd6Ab1Ckb+kccfz+6XHd9nv82LS5WUTQszJTsHRJMabVZicO+ZCe3H0+bNrULCT82FmThm4k2GbQBOzYEWSwE3dK3waOFrTTCh67CQz4/BLduOHWkngEHJEmJX7Y2qMi8FEElAzqFYrAMQQmfJqknqAIGAgoGdQXFAGNDOoDisDxCKj0rXqEInAMAZW+VVdQBACRvKX0LT8ao9K36hITFgESoKenB0yT4ixyqMdLTlgvc/jAjRO4SQRK4FL/2SBDnEz3J9XX1/u9Xm8SO49FiSREEou2Y9FGPOyLR5uxGKvRRjzsi5fICW0OFjY0SGCkR3H8SJA/iTrQlL61Cr5V/WC2Hw8N4UjCIfEQFAmnIhptcuJthzFv8cLWcE5j/syMN/gaq34VTGAeP8+fYOnbkbZn4jp/UkdHh8hYmajs2CqRVql4rl52gxFubPGIAHaM0xiHESFiQS4T4/hQ083oMFTKNLSRcJpk4eRPw8mlDqcbF6p/Fk5eNVTWKHQ1DKcDF+6aSPpokVa94cYcTrctNApG0lEbDo9I8xFtzMON1+wcB9s/nB3h5jg0kgRfb3WOE0QCw8VV7dPEiqFVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgKRVJgYCSoaJMc86ShMIKBlMgCRV4vHFfrN9j7ZePA4LGK1NDrxeyRBtUuhIPLeHPxkZGQlTL4pml5X3vV6v2O9yueS0CS1hEVAyRHMMj8cjJ7rx3J7s7OwRkYFtGJGFx57wJ5HFGEN6ejoyMzOVEOHBVzIM55TBRMjKyhqxE+3fv1+u5Q8PxSooKJAok8hCfQOSmtFBCaGRwZLvxYoI7HTr1q2YNGmSOGJbW5v8njx5sjgnTzKkc5IcPE/U7XYPkYYENF5jNMnLyxsxIWkHCcHTrDVCKBlMk8FwGqZGo4kIRofbtm3D1KlTpa3GxkZxSpKjtbVVTpgmOfLz84UozO1JEEaR8vJyNDQ0SDThNWVlZSgsLDQ9jnAVDQUcthmLsY3KGGddrGlSuPno6OgQp2Q6E4v8npGBTkyn52Y2NzdX2u3s7JS9BKMQIwN/0+G5evM91qurq0NFRYUQhXVOPPHEUbtQd3e3kIuRhoTXIggoGSKtnkY6wdUz2vmi0ZyJZKBDcwNO52Oa0tLSIk5PUtAx+RojAqMBX29vb5f0qampCZWVlUIarualpaXRuhv2fRKO7Wtk+AhMSoZInhPLVIlp0owZM2QlZmHUYfpDhycJmCoxcnDFNm7lsh4JxMhAUpCQxcXFEi1GWmK5DxqpDQ6+Tskw3OTEihDcG9CJjZSEDs+NMZ3fuMPEFIjqNCQKUyQ6/5QpU6Qe7eD/JBPJM5ISq7GMpO8xco2SIdpExeI5Q6Q+gp8MM0ViSsT9CiOFsVkmWUb7BFmfM0SbZd0zmEKIjmg8wTXSFVMXWqxkbKTZF6MAI0UsNu80g2Qw7lrpE+iIE6ORwazP6meTzCI1ZuspGcbs1KnhsUZAyRBrRLW9MYuAkmHMTp0aHmsElAyxRlTbG7MIKBnG7NSp4bFGQMkQa0S1vTGLgJJhzE6dGh5rBJQMsUZU2xuzCAgZ7h+z5qvhikAMEUiKYVvalCIwphH4fxaNciArPsC4AAAAAElFTkSuQmCC)

- Shared line history is now available on phone devices. With shared line history, a delegate can now view call history of the entire shared line in the “Shared line appearance” app. A delegator/boss can view call history of the entire shared line on the Calls app.  

- You can now pin apps of your choice to your home screen using settings named “Home screen”.  This is only available for touch phones. 

  ![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAOMAAAGUCAYAAADH3pWBAAAAAXNSR0IArs4c6QAAIABJREFUeF7tnQm8ltP6/lfhECeEDo6QsTIV4mTooESmohAhhSLFocgsQ4pKNIpCopBMpU6DKRInjrHBUSEq85FjytT+fb73/6zO+9+2vZ/37dl61nqv5/PZn/Z+32e417XWte57rbf3uqqUlJSsdM5VcTqEgBBYkwiUVBEZ1yT+erYQWIWAyKjBIAQygsCvyfjjjz+6n376ya211lpuvfXWcytXrnTff/+9cyUlbv0NNnBVquRf0X733Xd2Hfcr7/qff/7ZffHFF65atWpu0aJFbpdddnHrrruuYVVSUmJxrLPOOm7ttde2+/zyyy/uhx9+cFW5d7VqGcFUYYSAAGPHj3PGE2Pvyy+/tDG6wQYb2PjngA+MO97ntQ033ND+/s9//uOqV69uY9Wf689nTP7xj3+067/79lvnqlSx86pWrepWrFhh45Zx/Ic//CEXql+T8euvv3Y39unjDjzwQNf8iCNssN8yYIDbbrvt3Ilt2hg5+aEBHP5vfucBpclGI+6++263ztpru5NOPtkCIBhPMP7++aefXMl/7/XMM8+4PfbYwz388MOuffv21mDOnzZ1qnv99dfdkUcd5XbffXdr2KeffupG3HGHO/iQQ9wBBxwQwhhQjBlA4KuvvnJ/nzzZfbhkievQvr2rsckm7pGHH7YJf9myZa7NSSe5TTfd1Ei2dOlSd9+997o6deva302aNHGj7r7bbb/DDm7OW2+5zuee6zbaaCNrFeP0jTfecOMefNBdetllRlx+f++999yF3bpZYuG5L7zwgr3P2M45fk1GZoebb77Zbbzxxu7cc891n332mbv7rrvctttu61q1bu2efvppB2F33HFHy1xPTp/uVpaUGONbtGhh1+UezCC33XabZa+T27Z1G1av7iZMmOD+sO66NtscccQR7uWXX3Zkz+1q17bA99xrL/fYo4+69h06WENp5DvvvONmzpzp9t57b1e/fn279qFx49wHH3zgGu23n4GkQwgkQYDx+/7777uHx49355xzjtt0s83cNT17uiuuvNLNmTPHffTRR26LLbZw61er5qpUrWrjtXnz5q7WVltZdcgYrVWrlhsxYoQ7/fTT3eabb26P/fbbb40r66+/vmvQoIFrsOee7p5R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)
  
- App also includes multiple bug fixes and improvements. Bug fixes impacting user experience are: 

  - With this release, you will be able to resume held calls using a single entry point 
    
  - Joining a meeting via dial-info on calendar is now fixed  
    
  - Deleted groups from People app will now sync across clients  
    
  - For non-touch phone devices, the Resume button will now be one of the four keys below the display. It can be triggered using the corresponding hard key on the device. 
    
  - Issue on walkie talkie app and Teams channel is fixed 
    
  - Fixed auto-dial issue on emergency calls for non-touch devices 
    
  - Fixed issue on blind transfer for non-touch devices 
    
  - For Advanced calling experience on common area phones, issue on “Default to home screen” setting is fixed  
    
## February 26, 2025

**Applies to:** *Teams app version: 1449/1.0.94.2024121004 (Poly, Audiocodes)* 

> [!IMPORTANT]
> Starting in June 2025, Teams applications that are older than five (5) months will no longer work be able to connect to the service. Please refer to the Message Center Post, MC969451 for more details.

- App is available for government clouds (GCCH and DoD).

- Speed dial on line keys: With this update, you will be able to configure custom contacts and speed dial using the line key buttons on non-touch phones certified for Microsoft Teams. You can quickly access frequently dialed numbers and contacts, using one-touch dialing, as well as easy management of contact lists on line keys.

- **Queues app**: With this update, you will be able to use Queues app on phone devices. This is a Teams solution that empowers organizations to efficiently manage customer engagements, starting with calls on certified Teams Phones. The experience is primarily for agents and includes a dedicated Queues app on the home screen. This app allows agents to view and opt in or out of all the call queues an agent is part of. Agents can also view others on the line along with call history of the call queue.

> [!NOTE]
> The Queues app is enabled by default for all Teams users in your organization who are assigned both a Teams Premium and Teams Phone license and who are voice enabled. To learn more about managing the Queues app, see [Manage Queues app for Microsoft Teams](/microsoftteams/manage-queues-app).

- Lightweight calling experience on non-touch phones.

- Bug fixes and other improvements. 

## February 25, 2025

**Applies to:** *Teams app version: 1449/1.0.94.2025021303 (Poly, Yealink, AudioCodes)*



Back-end telemetry fixes and improvements  
## February 11, 2025

**Applies to:** *Teams app version: 1449/1.0.94.2025020301 (Poly, Yealink, AudioCodes)*

> [!IMPORTANT]
> Starting June 2025, Teams applications older than 5 months will no longer work. Please refer to the Message Center Post, MC969451 for more details.

Bug fixes including improvements in font rendering on side cars among others   

Contacts on Teams app and sidecar will now be sorted alphabetically

### January 8, 2025

**Applies to:** *Teams app version: 1449/1.0.94.2024122303 (Poly, Yealink, AudioCodes)*

> [!IMPORTANT]
> Starting June 2025, Teams applications older than 5 months will no longer work. Please refer to the Message Center Post, MC969451 for more details.

##### Queues app

We're excited to announce the Queues app for desk phones, a Teams solution that empowers organizations to efficiently manage customer engagements, starting with calls on certified Teams Phones. The experience is primarily for agents and includes a dedicated Queues app on the home screen. This app allows agents to view and opt in or out of all the call queues an agent is part of. Agents can also view others on the line along with call history of the call queue.

> [!NOTE]
> - The Queues app is enabled by default for all Teams users in your organization who are assigned both a Teams Premium and Teams Phone license and who are voice enabled. To learn more about managing the Queues app, see [Manage Queues app for Microsoft Teams](../manage-queues-app.md).

##### Circular delegation

Circular delegation now allows users to share lines with each other as a group on Teams Phone devices. This feature is useful for scenarios where multiple users need to manage shared lines. In a typical circular delegation setup, User A delegates to User B, and User B delegates to User A, allowing them all to share the line with each other. This setup can be configured using cmdlets because the Teams client and Teams Admin Center don't currently support this feature.

##### Multi-banner updates

The multiple-banners feature improves the user experience by managing notifications more effectively on phone devices. When users receive multiple notifications, the system allows users to collapse all notifications or clear them in bulk, providing a cleaner and more organized interface.

### December 18, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024121004 (Poly, Yealink, AudioCodes)*

- Bug fixes related to transfer flow, among other issues.

### December 18, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024063004 (Yealink T5x/CP960, AudioCodes C488HD/450HD, Yealink MP52/VP59, Crestron UC-P8/ UC-P8-C/ UC-P10/ UC-P10-C/ UC-2)*

- Banner notifications to inform users about their device support coverage status.

### December 10, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024112802 (Poly, Yealink, AudioCodes)*

- Bug fixes on lock screen, password expiration, LED issues on nontouch devices, among others, are included.

### November 25, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024062906 (Yealink - T5x, CP960, MP52, VP59; AudioCodes - C488HD/450HD, Crestron -UC-P8x, UC-P10x, UC-2)*

- Bug fixes on several minor issues reported by customers.

### November 13, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024103101 (Touch phones - AudioCodes, Poly, Yealink)*

- Bug fixes and improvements to line keys, calls, and Enhanced 911 calls, among others.

### October 29, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024101709 (Yealink, Poly, AudioCodes)*

Today, on Teams Phone devices, you're able to configure custom contacts and speed dial on-the-line key buttons on nontouch phones and sidecars phone devices certified for Microsoft Teams. You can quickly access frequently dialed numbers and contacts, using one-touch dialing, as well as easy management of contact lists on both line keys and sidecars.

:::image type="content" source="media/new-in-microsoft-teams-devices/nontouch-linekeys-empty.png" alt-text="Screenshot showing how to assign phone lines and Teams desk phones.":::

- Bug fixes and improvements on live captions.
- Privacy link updates for recordings and transcription.

### October 1, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024092304 (Yealink, Poly, AudioCodes)*

- Bug fixes and improvements on contacts sync, presence, and transfer flows, among others.

### September 5, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024082806 (Yealink, Poly, AudioCodes)*

- Enhancements in the call parking and retrieval feature to make both faster.
- Lightweight calling experience on nontouch phones.
- Bug fixes and improvements for compliance, recording scenarios, and other issues.

### September 3, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024062811 (Yealink T5x, CP960 & Poly Trio 8800/8500)*

- Bug fixes and improvements for end-of-certification and end-of-best-effort support phones.

### August 27, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024062702 (Yealink T5x, CP960 & Poly Trio 8800/8500)*

- To support incoming call notifications and voicemail, migrate end-of-certification and end-of-best-effort support phones from the discontinued call-notification service to the new notification service.

This update also includes these features, which were already available for certified Teams Phones:

- Improvement was made to show caller information on incoming emergency call notification.
- The date-time format specified under Device Settings is the same on the home screen.
- When the **Explicit Recording Consent** policy is enabled, audio conference phones support auto consent.
- The Public Switched Telephone Network (PSTN) calling issue on the new shared-line-appearance experience is fixed.
- When there are fewer than four apps on a given account, they appear on the home screen instead of being hidden under the More menu.
- Caller ID now shows incoming PSTN calls on call queues.
- You can now continue dialing a number when there's an incoming call.
- When ending a call or turning off your speaker, you won't be navigated to the home screen. Instead, you can continue from the previous screen.
- A new back button was introduced on the calling screen so you can easily navigate away from an ongoing call.
- View and join active calls handled by delegates as a delegator.
- Grant delegates permission to join active calls and resume calls.
- A delegate can view shared call history per a delegator's line, easily switch between different lines, and view other delegates managing a line.
- The presence on the device and sidecar gets updated in near real time.
- Live captions are supported on PSTN calls.
- You can program Teams Phone devices to autodial a preconfigured PSTN number, or directory contact, when the handset is picked up. You can configure a common-area phone as a hotline phone by navigating to **Settings** > **Device Settings** > **Calling** > **Hotline**, and specifying the autodial contact and display name.
- A redesigned dial pad helps reduce unnecessary mistakes while dialing a phone number. It offers a new dial-pad-only view in large-screen landscape phones.
- Simplified navigation improves the performance and reduces page-navigation time by replacing the bottom navigation bar with a new home screen navigation experience. You can easily go to the home screen from any app and navigate to different apps from the home screen. You can also use **More** to reorder apps.
- The user experience on the calls app and sidecar was made lighter weight to improve performance.
- Date and time are now displayed on the title bar across apps.
- Support added for reverse number lookup of PSTN numbers on call-queue calls.
- The issue of autodialing on a partially entered number is fixed.
- Option to sign out on common area phones. Advanced calling experience requires an admin PIN.
- Lighter weight meeting reduces the time it takes users to get connected to a meeting on selecting **Join**.
- Support added for reverse number lookup of PSTN contacts added via the Teams desktop.
- Performance of the phones attached to expansion modules is improved.
- The "Resume call" reliability is improved on consult transfer.
- Audio conferencing isn't supported on Teams Phone devices with the Meeting Teams Room Basic license.
- You can add and edit your emergency location on phones.
- Emergency service disclaimers specified by admins in the Teams Admin Center (TAC) as part of emergency policy is shown on the desk phones.
- Busy-on-Busy when users are in a call setting enabled by admins in TAC will be honored on phone devices (excluding the User-controlled option).
- Admins can configure app restart settings from TAC for optimal phone performance (not currently available for Government cloud accounts).
- Record one-on-one PSTN calls.
- License enforcement.
- Faster call joining.

### August 16, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024080808*

- Bug fixes and improvements on transfer scenarios, contacts, among others, are included.

### July 16, 2024

**Applies to:** *Teams app version -1449/1.0.94.2024071104*

- This app is available for government clouds (GCCH and DoD).
- **Updates on user experiences** We changed the default home-screen experience for the meeting sign-in mode. It's now like the personal sign-in mode experience. Additionally, updates to remove the dial pad on the Calls app for touch phones with physical buttons.
- **Explicit Consent for Recording**  Users see a notification on Teams Phone devices when a participant starts recording or transcription, asking for participant consent. This feature is turned off by default but can be enabled by admins. Admins can turn on this policy for users in your tenant by clicking on the highlighted switch on "Require participant agreement for recording, transcription, and Copilot."

  :::image type="content" source="media/new-in-microsoft-teams-devices/recording-and-transcription.png" alt-text="Screenshot showing the option to require participant agreement for recording transcription." lightbox="media/new-in-microsoft-teams-devices/recording-and-transcription.png":::

- **Private Line**  The Private Line feature allows bosses to have a second private phone number on their Teams device, ensuring privacy for important calls. These calls are distinct in the call history. To learn more, see Configure private lines in Microsoft Teams.
- **Lightweight People App**  The updated People app provides a faster and simplified experience for managing contacts, allowing users to switch between different contact lists and to create contact groups.

- **Rich Call History**  Call-history updates include better logging for ignored, missed, and forwarded calls, with clear labeling for different call types.
- **Call Transfer Improvements**  Improvements to call transfers include viewing a list of speed dials during transfer, and better handling of keyboard overlap on touch phones. Also, for phones that don't have touch screens, there are improvements to finish transfers using call-transfer hard keys on phones.

### July 5, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024062301 (AUDC: C448HD, C450HD. Yealink: MP52, VP59. Crestron: UC-2, UC-P8, UC-P10, UC-P8-C, and UC-P10-C)*

- Intermittent issue on meeting join while using Better Together is fixed for touch phones
- Intermittent issue on a device getting locked out is fixed for nontouch phones.
- Issue of remote user not hearing music while on hold in nontouch phones is fixed.
- Fixes for authentication issues, including a fix for sign-in failures immediately following signing out.
- Issue of pin lock appearing when disabled is fixed.

### July 3, 2024

**Applies to:** *Teams app version - 1449/1.0.94.2024062010 (touch phones: AudioCodes, Poly, Yealink. For nontouch phones: AudioCodes C435, Poly CCX350)*

- Bug fixes and improvements on the enforce pin-lock feature.
- This app is also available for customers in government clouds (GCCH and DoD).

### June 18, 2024

**Applies to:** *Teams app version - 1449/1.0.94.2024061301*

- Minor updates in the people and calls apps.
- Bug fixes and improvements.

### June 4, 2024

**Applies to:** *Teams App version: 1449/1.0.94.2024051306 (Touch phones - AudioCodes, Poly, Yealink)*

- Bug fixes for crash issues.

### May 21, 2024

**Applies to:** *Teams App version: 1449/1.0.94.2024051306 (Nontouch phones - Poly CCX350, AudioCodes C435HD)*

- You can park and unpark a call.
- You can turn on the Advanced Calling and Auto Restart settings.
- You can add contacts and contact groups.
- Admin's can turn on call forwarding on home screens via **Teams Admin Center** > **Configuration** > **Display call forwarding on home screen**, allowing Teams Phone device users to setup call forwarding directly from their home screens.
- Admin's can turn off call-quality serveys on Teams Phone devices from **Teams Admin Center** > **Configuration**, and by turning off **Call quality survey**.

  :::image type="content" source="media/new-in-microsoft-teams-devices/turn-off-call-serveys.png" alt-text="Screenshot showing the option to turn off call quality serveys on Teams Phone devices." lightbox="media/new-in-microsoft-teams-devices/turn-off-call-serveys.png":::

- Send incoming calls to voicemail from the incoming call screen (configurable by calling a policy through PowerShell). You can control how you want to handle a secondary incoming call through the Busy-on-Busy setting (configurable by calling a policy in the Teams Admin Center).
- When a contact has multiple numbers, you can choose which one to call.
- People can control how they want to handle second incoming calls through the Busy-on-Busy setting. Admins can allow people to configure the Busy-on-Busy setting by selecting **Let users decide** in **Teams Admin Center** > **Calling policy**.

  :::image type="content" source="media/new-in-microsoft-teams-devices/how-to-handle-second-incoming-calls.png" alt-text="Screenshot showing how users can handle second incoming calls." lightbox="media/new-in-microsoft-teams-devices/how-to-handle-second-incoming-calls.png":::

### May 5, 2024

**Applies to:** *Teams app version: 1449/1.0.94.2024042905 (Touch Phones - AudioCodes, Poly, Yealink)*

- Send incoming calls to voicemail from the incoming call screen.

  :::image type="content" source="media/new-in-microsoft-teams-devices/incoming-call-screen.png" alt-text="Screenshot showing the incoming call screen.":::

> [!NOTE]
> Admins can control rollout of this option on selected accounts by configuring the AllowCallRedirect parameter in the Teams calling policy associated with the account: `PS C:\WINDOWS\system32> Set-CsTeamsCallingPolicy -Identity Global -AllowCallRedirect Enabled`

- People can control how they want to handle a second incoming call through the Busy-on-Busy setting. Admins can allow people to configure the Busy-on-Busy setting by selecting **Let users decide** in **Teams Admin Center** > **Calling policy**.

  :::image type="content" source="media/new-in-microsoft-teams-devices/busy-on-busy-setting.png" alt-text="Screenshot showing the Busy-on-Busy setting.":::

  :::image type="content" source="media/new-in-microsoft-teams-devices/busy-on-busy-let-users-decide.png" alt-text="Screenshot showing the Busy-on-Busy setting that lets users decide." lightbox="media/new-in-microsoft-teams-devices/busy-on-busy-let-users-decide.png":::

- Admins can allow call the forwarding option on home screens via **Teams Admin Center** > **Configuration** by turning on **Display call forwarding on home screen.** The same setting can be configured on the phone device. This allows people using a device (including common-area phones) to set up call forwarding directly from their home screen.

> [!NOTE]
> These features will be rolled out gradually.

- Admins can notify people to set or change their phone lock PIN by enabling a configuration profile setting in Teams Admin Center. They can also lock the phone device via the menu on home screen.

> [!NOTE]
> These features will be rolled out gradually.

- Survival Branch Office (SBA) will be supported on Voice over Internet Protocol (VoIP) calls.
- Admins have the option of disabling call-quality surveys on Teams Phone devices from **Teams Admin Center** > **Configuration**.

  :::image type="content" source="media/new-in-microsoft-teams-devices/disabling-call-quality-surveys.png" alt-text="Screenshot showing how to disable call-quality serveys." lightbox="media/new-in-microsoft-teams-devices/disabling-call-quality-surveys.png":::

> [!NOTE]
> These features will be rolled out gradually.

- The issue of Better Together on the new Teams desktop app is fixed.
- After consult transfer, the issue of an ongoing call going to the banner for the remote caller is fixed.

### March 15, 2024

**Applies to:** *Teams App version: 1449/1.0.94.2024031102 (Yealink, Poly, AudioCodes)*

> [!NOTE]
> For AudioCodes phones, this app update applies to firmware version 1.19.705.

- Improvement to show caller information on incoming emergency call notification.
- Issue of not ending hot-desk on timeout is fixed.
- Issue of showing an incorrect call-recording string and a localized calling string is fixed.
- Issue related to the hard-key hold button is fixed.

### March 12, 2024

**Applies to:** *Teams App version: 1449/1.0.94.2024011601, 1449/1.0.94.2024020601 (AudioCodes)*

> [!NOTE]
> The update applies to AudioCodes phones on firmware version 1.19.516 or higher.

- Significant reduction in sign-out and authentication errors due to Workplace Join failures, timeout issues, and memory leaks.

### January 24, 2024

**Applies to:** *Teams App version: 1449/1.0.94.2024011003 (Poly, Yealink, Crestron, AudioCodes)*

- The issue of active call moving to banner on merging a call is fixed.
- The issue of consult transfer icon not being clickable sometimes is fixed.

> [!NOTE]
> This update applies to AudioCodes phones on firmware versions 1.19.456 and earlier.

### December 5, 2023

**Applies to:** *Teams App version: 1449/1.0.94.2023112704 (Crestron, Poly, Yealink)*

- The date and time format specified under **Device Settings** is the same on the home screen.
- When the **Explicit Recording Consent** policy is enabled, audio conference phones support auto consent.
- The PSTN calling issue on the new shared line appearance experience is fixed.
- When there are fewer than four apps on a given account, they appear on the home screen instead of being hidden under the **More** menu.

### November 28, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023111407 (AudioCodes)*

> [!NOTE]
> This update applies to AudioCodes phones on firmware version 1.19.584.

- Improvements to reduce issues with workplace join authentication.

### November 6, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023100602 (AudioCodes)*

> [!NOTE]
> This update applies to AudioCodes firmware version 1.19.584 and is available for phones previously on firmware version 1.19.516. A Teams app release for AudioCodes phones currently on other firmware versions will be released soon.

- Enhanced call-delegation experience, faster presence update in the app, and live captions on PSTN calls. For a list of call-delegation updates, see the August 29, 2023, update.

### October 9, 2023

**Applies to:** *Teams App version: 1449/1.0.94.2023091801 (Yealink)*

- Caller ID shows for incoming PSTN calls on call queues.
- You can continue dialing a number when there's an incoming call.
- When ending a call or turning off your speaker, you won't be navigated to the home screen. Instead, you can continue from previous screen.
- A new back button on the calling screen which allows you to easily navigate away from an ongoing call.

### August 29, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023082303 (Crestron, Poly, and Yealink Audio Touch Phones)*

Today, on Teams Phone devices, delegators can share their phone line with their assistants and delegates to make and receive calls on their behalf. Call delegates can also:

- View and join active calls handled by delegates, as a delegator.
- Grant delegates permission to join active calls, and resume calls.
- View shared call history, per the delegator's line.
- Easily switch between different lines.
- View other delegates managing a line.
- The presence on the device and sidecar is updated in near real time.
- Live captions are supported on PSTN calls.
- The issue of resolving caller ID on call-queue calls is fixed.
- The issue of showing the "Add location" banner when the emergency policy "External location lookup mode" is turned off is fixed.

### July 31, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023072509 (AudioCodes, Crestron, and Poly audio phones)*

- You can program Teams Phone devices to autodial a preconfigured PSTN number or directory contact when the handset is picked up. You can configure a common area phone as a hotline phone by navigating to **Settings** > **Device Settings** > **Calling** > **Hotline** and specifying the auto-dial contact and display name.

> [!NOTE]
> To configure a phone as hotline phone, the logged in account on the phone device must have **Teams Shared Device License** assigned. **Sign In Mode** must be set to **CommonAreaPhoneSignIn**. The option to configure a hotline phone through the Teams Admin Center will be supported soon.

- Redesigned dial pad helps reduce unnecessary mistakes while dialing a phone number and offers a new dial-pad-only view in large-screen landscape phones.
- Simplified navigation improves performance and reduces page-navigation time by replacing the bottom navigation bar with a new home-screen navigation experience. You can easily go to the home screen from any app and navigate to different apps from the home screen. You can also use **More** to reorder apps.
- The user experience on the calls app and sidecar was made lightweight to improve performance.
- Date and time are now displayed on the title bar across apps.
- Support added for reverse number lookup of PSTN numbers on call-queue calls.
- The issue of autodialing on partially entered number is fixed.
- Option to sign out on common area phones. The advanced calling experience requires an admin PIN.
- Lightweight meeting reduces the time it takes users to get connected to a meeting by selecting **Join**.

### July 12, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023063003*

- Support added for reverse-number lookup of PSTN contacts added via Teams desktop.
- Performance of the phones attached to expansion modules is improved.

### June 15, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023060906*

- Audio Conferencing is supported on the Microsoft Teams Room Pro License.

> [!NOTE]
> When multiple licenses are assigned to a Teams Phone device account, configure IPPhonePolicy and SignInMode for the desired experience.

- Issue of displaying wrong caller information for incoming Auto Attendant Call Queue calls is fixed on nontouch screen phones.

### May 9, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023050205 (doesn't include TrioC60 on GCC-H cloud)*

- "Resume call" reliability is improved on consult transfer.
- Issue of persisting "Advanced calling" setting in common area phones when signing back in is fixed.
- The intermittent issue of an emergency location banner showing on the phone when "External location lookup mode" is disabled in the Teams Admin Center is fixed.
- Intermittent issue of badge notifications not clearing on the home screen is fixed.

### April 14, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023041203*

- Intermittent issue of the app restarting on F SKUs (frontline worker) and Business SKUs (SMB) is fixed.

### April 4, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023032903 (AudioCodes, Crestron, Poly)*

- Audio conferencing isn't supported on Teams Phone devices with the Meeting Teams Room Basic License.
- You can add and edit your emergency location on phones.
- Emergency service disclaimers specified by admins in the Teams Admin Center (TAC) as part of the emergency policy shown on desk phones.
- Busy-on-Busy when in a call setting enabled by admins in the Teams Admin Center is honored on phone devices (excluding the User controlled option).
- Admins can configure app-restart settings from the Teams Admin Center for optimal phone performance (not currently available for Government cloud accounts).
Record one-on-one PSTN calls
- Faster call joining.
- Issue of defaulting to alphanumeric characters on the Dialpad while dialing a number on Poly CCX 350 is fixed.
- Intermittent issue of boss not getting notification when delegates put a call on hold is fixed.
- Intermittent issue of screen freezing while in a call is fixed.

### February 21, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023020602*

- Dial tone and mute LED sync issue is fixed on audio-conferencing phones.
- Calling resiliency is improved.
- Intermittent issue around graying out of call controls is fixed.
- Intermittent issue around not being able to end calls is fixed.

### January 25, 2023

**Applies to:** *Teams app version: 1449/1.0.94.2023010607*

> [!NOTE]
> This update is for public cloud deployments and non-audio-conferencing phones.

- Reliability improvements around authentication.
- Showing detailed error messages around authentication.
- Call button display issue is fixed.
- Emergency notification issue is fixed.

### November 30, 2022

#**Applies to:** *Teams app version: 1449/1.0.94.2022110803*

- Fixes sign-in issues on nontouch devices.
- Fixes caller ID and caller display name issues.
- Fixes calling related issues on GCCH deployments.

### September 21, 2022

**Applies to:** *Teams app version: 1449/1.0.94.2022090705 (for nonvideo touch phones only)*

- Simplified look for incoming and outgoing calls with improved performance.

### July 14, 2022

**Applies to:** *Teams app version: 1449/1.0.94.2022062103*

- Several intermittent app-crash issues have been resolved.

### July 6, 2022

**Applies to:** *Teams app version: 1449/1.0.94.2022061702 (Crestron, Poly, Yealink)*

- We're enhancing the existing Common Area Phone offering to include all advanced calling features at no extra cost or changes to the original purchased license. Common Area Phone supports calling features including call park, call queues, auto attendants, Intune enrollment into Endpoint Manager, and more, when the device is updated to the minimum app version: 1449/1.0.94.2022061702.
- Emergency calling on GCC-H deployments is supported.

### April 13, 2022

#**Applies to:** *Teams app version: 1449/1.0.94.2022041102*

- Fixes missing names on phone sidecars.
- Fixes common-area phone dial pad and audio routing issues between the handset and speaker.
- Fixed issues occurring in the Teams Admin Center.

### March 24, 2022

**Applies to:** *Teams app version: 1449/1.0.94.2022030501*

- Support end-to-end encryption in one-on-one calls.
- Contact name along with phone number for saved contacts show on calls made via PSTN (Public Switched Telephone Network).
- Hold music during blind-call transfers and consultative-call transfers made via VoIP (Voice over Internet Protocol).
- Customize app restart time from **Settings**.

### March 3, 2022

**Applies to:** *Teams app version: 1449/1.0.94.2022022305*

- Resiliency added for location fetch mechanism on devices.

### February 7, 2022

**Applies to:** *Teams app version: 1449/1.0.94.2022020202*

- Teams Phones with touch screen have instant push-to-talk communication via the new Walkie-Talkie feature.
- Teams Phones with touch screen improvements for multiple incoming, held, and parked calls.
- Teams conference phones in portrait mode updates for better meeting experience.
- Performance enhancements for screen navigation and sidecar issues.
- Bug fixes for Teams Android devices showing as offline in Teams Admin Center.
- Bug fix to held calls when placing the handset back in the cradle.
- Known issues with ongoing calls when Walkie-Talkie calls interrupt.

### December 16, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021121302*

- More improvements in dial-pad experience for touch-screen phones.
- Improvements in dial-tone management.
- Improvements to audio routing when switching between handset and speaker.

### December 6, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021112302*

- More improvements in dial-pad experience for touch-screen phones.
- Improvements in dial-tone management.
- Improvements to audio routing when switching between handset and speaker.

### November 22, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021110101*

- Improvements in dial-pad and dial-tone experiences for touch-screen phones.

### November 3, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021101205*

- Admins can provision devices from the Teams Admin Center to remotely sign in and sign out from devices.
- Branch office survivability for Teams Phones to make PSTN calls even when the internet connection is down.
- Admins can download all (company portal, device management, and media) logs from the Teams Admin Center.
- Bug fixes related to authentication.
- Bug fixes preventing devices from going offline in the Teams Admin Center.

### June 10, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021052803*

- Performance updates for meeting experiences on low-end hardware.

### June 8, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021051303*

- Transfer a Teams call to another device without hanging up.
- Change your background during a video call or meeting from a set of pictures available in phones with video capability.
- Contacts whose numbers are saved in Outlook are available in the People section of Teams Phones with read-only access. You need to manually dial the number.
- Enforcement of authentication policies and tenant-based policies set by your admin. Login is blocked if the device doesn't meet the necessary policy requirements.
- During a call, select the active-call icon to show more options. Additionally, when a contact has multiple numbers saved, you can choose the number you want to dial from the dropdown list.
- To facilitate quick responses for autoattendant scenarios, dial pad is available for early media scenarios.
- Extending the live captions feature to calls, Teams detects what's said in a call and presents real-time captions in one-on-one calls.
- Ongoing enhancements to improve user experience when using a delegate on touch screens.
- Bug fixes for Link Layer Discovery Protocol (LLDP) for Enhanced 911 (E911) and authentication.

### March 30, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021033002*

- Fixed authentication library crash.

### March 26, 2021

**Applies to:** *Teams app version: 1449/1.0.94.2021022403*

- New and improved sign-in experience. Sign in from any browser or smartphone with a prominent device code. Or you can sign in from the device with your username and password.
- Sign-in support and authentication into specialized clouds is available. Choose the **Settings** gear on the sign-in page to see the options for your account.
- IT admins can remotely provision and sign in to a Teams device that's previously not been provisioned.
- Call controls now visible during meetings. You can also switch between Gallery and Together mode and send reactions during meetings.
- Teams devices connected to the network via ethernet will dynamically update location information for emergency calling services based on changes to network attributes, including chassis ID and port ID.
- On video phones, you can change your background during meetings and calls from a select set of images.
- Calling enhancements that improve the usability of touch screens.
- All phone numbers that are part of meeting invites, or from a person's contact card, can be dialed by selecting them on screen.
- Directly transfer a call to someone's work voicemail without ringing them.

### December 8, 2020

**Applies to:** *Teams app version: 1449/1.0.94.2020111101*

- Video features including 3x3 layout support, gallery view and together mode, background blur, and spotlight.
- Meeting features including request-to-speak and the ability to view screen sharing on select models of audio phones.
- Proximity joining on conference phones.
- Beta release for Sidecars on AudioCodes and Yealink phones.
- Meet-now button on phones.
- Policy support for enabling and disabling home screen and syncing a phone to a computer.
- Support for M365 Government (GCC deployments).

### October 12, 2020

**Applies to:** *Teams app version: 1449/1.0.94.2020091801*

- Better-together feature with meeting support.
- Bug fix related to authentication after signing in.
- Bug fix related to device automatically signing out after 90 days.

### August 31, 2020

**Applies to:** *Teams app version: 1449/1.0.94.2020071702*

- Home screen shows meeting reminders.
- Ability to customize default apps in the phone and the default view in Calls.
- Support for a Teams button on specific phone models.
- Enable auto accept with video for prescheduled meeting requests.
- Sign-in enhancements with the Company Portal application.
- Bug fixes to the Teams application and the Device management admin-agent application.

> [!NOTE]
> If the phone is stuck on the "Verifying a few things" screen, try turning the phone off and on again.

### June 27, 2020

**Applies to:** *Teams app version: 1449/1.0.94.2020051601*

- Contacts and contact groups management in People.
- Live captions for meetings.
- Raise virtual hand in meetings.
- Transfer directly to speed dial.
- Connect to computer for simultaneous lock and unlock.
- Auto dismiss for a call ended and rate-my-call screens.
- Network banner at the top of screen to show network loss.
- Bug fixes to the Teams application and the Device management admin-agent application.

### April 23, 2020

**Applies to:** *Teams app version: 1449/1.0.94.2020031901*

- Favorites (speed dial) added to Calls.
- New settings support on Teams Phones for: Custom ringtone, Manage Delegates, and auto dial for extension dialing.
- Device-management updates to support device categorization in Teams Admin Center.
- Bug fixes to the Teams application and the Company Portal application.

### February 18, 2020

**Applies to:** *Teams app version: 1449/1.0.94.2020020601*

- Support for dynamic emergency calling on the phone lock screen.
- Hot-desk feature bug fixes to address network-outage scenarios.
- Sign-in improvements.
- Device-management bug fixes to address firmware version reporting.
- Bug fixes to the Teams application.

## [Teams displays](#tab/displays)

> [!IMPORTANT]
> End of certification for Teams display devices is September 3, 2025. Microsoft will make commercially reasonable best efforts to maintain compatibility with the most recent version of the Teams apps provided to manufacturers for a period of two (2) years from this date. For details, see the [Microsoft Product and Services Lifecycle](/lifecycle/products/).

### September 2024

**Applies to:** *Teams app version: 1449/1.0.95.2024062804*

- Bug fixes.

### November 2023

**Applies to:** *Teams app version: 1449/1.0.95.2023101102*

- Support for QR code sign in for scenarios without reserving the hot desk.
- Improvements to support meeting continuity through hot-desk reservation end times.
- UI and layout enhancements to the hot-desk ambient and display screen.
- Bug fixes and other enhancements.

### June 2023

**Applies to:** *Teams app version: 1449/1.0.95.2023061601*

- Streamlined experiences on Teams-certified displays based on assigned licenses.
- Bug fixes and improvements on meeting and calling experiences.

### May 2023

**Applies to:** *Teams displays app version: 1449/1.0.95.2023042701*

> [!NOTE]
> This release is an app-only update. Work with device manufacturers to confirm timelines on full feature functionality on your devices.

- QR code sign in on Teams-certified displays for hot-desking. All Teams Displays with hot-desking capability allow people to sign in using a QR code for a reserved time slot. This feature is enabled by default and can be disabled under **Device settings** > **Admin settings** > **Meetings**. While hot-desking, you can seamlessly sign in to the Teams display during your session by scanning a QR code using the Teams app on your mobile phone.

The recommended version of Teams on your Android phone is 1416/1.0.0.2023092901 and above. On iOS, the recommended version is 5.9.1, it's (100772023093201), and above.

> [!NOTE]
> The following instructions are for those who use an Android mobile phone with an Android work profile (AWP).

- You can scan a QR code using the camera app on your Android mobile phone. However, the sign-in might not work if you have both work and personal profiles on their Android phones. If so, you need to add a mobile system OS scanner in your work profile.

To add a mobile system OS scanner:

1. In the Intune Admin Center go to **Apps** > **Android**, and add.

2. Select **Android enterprise system app**.

3. Enter the type of Android phone, Google, and paste OS camera package name.

4. Assign it to an individual or group.

5. Download and install the camera app from the app store in your work profile.

- **Virtual front-desk experience on Teams-certified displays**  The Virtual front desk enables staff to greet and serve visitors or employees via video call on a Teams display. It can be used for virtual reception, helpdesk, and various use cases across industries. IT admins can easily configure the Virtual front desk with contact and routing information. This feature is available on Teams certified displays on the Teams Shared Devices License. Recommended for accounts without CA policies.
- Admins can now customize the message on display screens and the call button, in addition to configuring a PSTN or VoIP contact on the device itself via **Settings**. They can also use Teams advanced calling capabilities such as call transfer, call forwarding, call queues, etc., if enabled for the configured contact account.
- Improvements to handle multi-call banner scenarios and to ambient UI.
- Bug fixes and improvements.

### January 2023

**Applies to:** *Teams app version: 1449/1.0.95.2023011001 (Crestron)*

- Fix for intermittent app crashes occurring in the previous app update (1449/1.0.95.2022102603) for Crestron devices.

### December 2022

**Applies to:** *Teams app version: 1449/1.0.95.2022120505 (Neat Frame)*

- Hot desking in portrait mode is  supported. Hotdesking on a Teams display makes finding a space to work easier by allowing you to locate and reserve flexible workspaces.
- Teams Shared Devices License on Teams displays offers hot desking experience. The Teams IP Phone policy setting for hot desking is disabled for displays. You can invoke hot desking using Teams accounts with the Teams Shared Device Licenses.
- Bug fixes and improvements for app crashes.

### November 2022

**Applies to:** *Teams app version: 1449/1.0.95.2022102603 (Crestron)*

- Teams Shared Devices License on Teams displays offers a hot-desking experience. The Teams IP Phone policy setting for hot desking is disabled for displays. You can invoke hot desking using Teams accounts with the Teams Shared Device Licenses.
- Bug fixes and improvements for app crashes, reliability of muting and unmuting your microphone during a call, and more.

### December 2021

**Applies to:** *Teams app version: 1449/1.0.95.2021111203*

- Teams displays support portrait mode for all calling and meeting screens. Meeting layouts are optimized for portrait videos of individual people. All incoming videos always fit-to-frame when the device is used in portrait orientation.
- Teams displays enabled live event attendee view to allow producer and presenter to join with a quick join link. They have the same capability in displays as in the Teams mobile app. The attendee can access the live event with the event link provided in the calendar details.
- Organizers, presenters, and attendees have the webinar invite on calendar, and can join directly from the calendar event through the **Join** button, which appears on the event when it's about to start.
- The following Teams display settings moved under **Teams Admin Settings** while using a shared account: calling, sign out, and wallpaper.
- Teams displays have the ability to use end-to-end encryption for calls (must be enabled by IT admin).
- IT admins can remotely provision, sign in, and sign out of a Teams device that has previously not been provisioned.

### June 2021

**Applies to:** *Teams app version: 1449/1.0.95.2021042103*

- Contact phone numbers created in Outlook are available in the People section of Teams displays with read-only access.
- During a call, select the active-call icon to show more options. Additionally, when a contact has multiple numbers saved, you can choose the number you want to dial from the dropdown list.
- Choose a background for your video calls and meetings from a select set of images in Teams.
- Extending the live-captions feature to calls. Teams can now detect what's said in a call and present real-time captions in one-on-one calls.
- On Android devices, presenters can control a participant's camera and mic. Participants no longer need to use Raise hand to request to be unmuted.
- New wallpaper images.
- Bug fixes related to authentication.

### March 2021

**Applies to:** *Teams app version: 1449/1.0.95.2021021104*

- Sign in from any browser or smartphone with a device code. Or sign in from the device with a username and password directly on the device.
- Call controls are docked at the bottom of the screen. You can also switch between gallery and together mode views and send reactions during meetings.
- Producer, presenter, and attendee can join live events as attendees on Teams displays. Producer and presenter can join the live event through the ****Join button in the calendar. Everyone else can join through the attendee link shared in a Teams channel, chat, or on the invite details tab.
- Change your background during meetings or calls from a select set of images.
-All phone numbers that are a part of a meeting invite or a person's contact card can be dialed directly by tapping on them.
- Directly transfer a call to someone's work voicemail without ringing them.
- Zero calendar events page is displayed for days with no meetings.
- Dots on dates are displayed for days that have meetings.
- Send reactions from the ambient screen.
- Suggested replies to messages from the ambient screen.
- Call someone back from the ambient screen after you miss their call.
- Indicator of important and urgent messages on the ambient screen.
- Notification badges on the home icon indicate that there are new notifications coming in when in another app on the device.
- Sent messages are displayed in your notifications.
- Set quiet hours for notifications.
- Ask Cortana and get answers to questions about topics such as current weather, calculations, currency conversions, language translations, and time conversions.
- Cortana voice support expanded to new English locales: United Kingdom, Canada, India, and Australia. Use your voice to join meetings, make phone calls, send messages, and check your schedule.

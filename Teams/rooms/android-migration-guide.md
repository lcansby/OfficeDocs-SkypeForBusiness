---
title: Migration guide Android AOSP management for Microsoft Teams Android devices
author: mstonysmith
ms.author: tonysmit
ms.reviewer: tjaved
ms.date: 3/28/2025
manager: pamgreen
audience: Admin
ms.topic: upgrade-and-migration-article
ms.service: msteams
ms.subservice: itpro-rooms
ms.collection:
  - M365-collaboration
  - teams-rooms-devices
  - Tier1
f1.keywords:
  - NOCSH
ms.localizationpriority: medium
description: Learn about how to migrate Teams Android devices to AOSP Device Management.
---

# Migrating Teams Android Devices to AOSP Device Management from Device Administrator

This document describes how IT administrators can prepare their environment for a migration from Android Device Administrator to the new mobile device enrollment (MDM) method called Android Open Source Project (AOSP) Device Management for Teams Android Devices. This new MDM enrollment method replaces the legacy Device Administrator enrollment method and serves as the basis for new features and functionality. For this migration to be successful, IT administrators have specific actions they must take and all of which are covered in this article.

This article covers:

- How to set up new AOSP Device Management enrollment profiles
- How to create new Intune compliance policies
- Considerations prior to deploying migration firmware
- How to deploy the new AOSP Device Management firmware

### Prerequisites

To migrate from Android Device Administrator to Android AOSP Device Management, you will need:

- Intune licenses assigned to your Teams Android devices.
- Teams Android Devices deployed which are enrolled using Device Administrator.
- Teams Android Devices that are supported with AOSP Device Management. Confirm with this article for the full list of unsupported devices: [Moving Teams Android Devices to AOSP Device Management](https://techcommunity.microsoft.com/blog/microsoftteamssupport/moving-teams-android-devices-to-aosp-device-management/4140893)
- Intune admin permissions in your Microsoft 365 environment.

> [!IMPORTANT]
> If your organization doesn't enroll Teams Android devices in Intune (Either because you're using Teams Rooms Basic licenses which do not include Intune or by disabling the Intune license on your resource accounts) then there is no need to set up an enrollment profile or create AOSP Device Management policies. Just upgrade your devices to the AOSP Management capable firmware at release to stay on current firmware but no Intune configuration is required.

## Step 1 - Set up a new AOSP device management enrollment profile

In order for Teams Android Devices to enroll in AOSP Device Management successfully, an enrollment profile must be created.

> [!NOTE]
> These steps are specific to Teams Android devices. If you have non-Teams devices, refer to the Intune guidance for setting up profiles: [Set up Android (AOSP) device management in Intune for corporate-owned user-associated devices - Microsoft Intune | Microsoft Learn](/mem/intune/enrollment/android-aosp-corporate-owned-user-associated-enroll)

### Setup AOSP management enrollment profiles

1. Sign in to the Intune Management Console using an account with Intune administrator permissions: [https://intune.microsoft.com/](https://intune.microsoft.com/).
2. Select **Devices** > **Enrollment** > then **Android**.
3. Under **Android Open Source Project (AOSP)** > **Enrollment Profiles**, select **Corporate-owned, user-associated devices**.
4. Select **Create policy**.
5. Use the following settings for the profile configuration:

   - **Name** Give the profile a name like 'AOSP – Teams Devices'.
   - **Description** Put in a description so others in the organization know what this enrollment profile is used for. Use something like 'This AOSP Management enrollment profile is to allow Teams Android Devices to enroll in Intune'.
   - **Token expiration date** This defaults to 65 years into the future and is best left at 65 years to avoid expiration which would block new enrollments.
   - **Wi-Fi** Select **Not configured**.
   - **For Microsoft Teams devices** Select **Enabled**.

   ![Screenshot of AOSP enrollment profile.](media/android-migration-guide/aosp-enrollment-profile.png)

> [!NOTE]
> An expired enrollment token will prevent devices from completing a successful sign-in and will block new devices from enrolling.

6. Select **Next**.
7. Review the profile and then select **Create**.

The enrollment profile has been created and is now ready to enroll devices.

## Step 2 - Set up AOSP Device Management Compliance Policies (if required)

If your organization uses [Conditional Access](/intune/intune-service/protect/conditional-access) with Intune Compliance as a requirement for successful sign in, you need to create a new AOSP DM Compliance Policy and assign it to all devices in your tenant to ensure devices are marked compliance post migration. If you do not create a compliance policy while requiring compliance as an authenication factor, the device will sign out after migration.

> [!NOTE]
> These steps are specific to Teams Android devices. For non-Teams devices, please refer to the Intune guidance for setting up profiles:  [Android (AOSP) compliance settings in Microsoft Intune | Microsoft Learn](/mem/intune/protect/compliance-policy-create-android-aosp)

### Applicable Intune Compliance Factors

Only some AOSP Device Management compliance factors are applicable to Teams Android Devices enrolled with AOSP Device Management:

- **Device Health** Rooted devices (Block).
- **Device Properties** Minimum OS version.
- **Device Properties** Maximum OS version.
- **System Security** Require encryption of data storage on device.

### Creating a AOSP Management Compliance Policy

1. Sign in to the Intune Management Console with an account with Intune administrator permissions: [https://intune.microsoft.com/](https://intune.microsoft.com/).
2. Select **Devices** > **Compliance**, then **Create policy**.
3. Under **Platform** > **Android (AOSP)**, then select **Create**.
4. Provide a name and description for the policy.
5. Select **Next**.
6. Enable the desired compliance settings from the applicable list.
7. Select **Next**, then select **Next**.
8. Assign this profile to all devices in the organization or a group of devices.
9. Select **Next**, then select **Create**.

> [!NOTE]
> In step 8, if you assign to "All Devices" this will only assign this compliance policy to all devices in your organization enrolled using AOSP DM. In most scenarios, this is acceptable as Teams Android devices are the first large group of devices using AOSP DM. If you have other AOSP DM enrolled devices, ensure you do not have conflicting compliance policies or assign your policies to groups of devices instead.

## Step 3 - Considerations prior to deploying AOSP DM capable migration firmware

- There is no end user noticable change on the devices after this migration is completed.
- Firmware capable of completing this migration is being released slowly over several months, review to our Tech Community article for firmware availability and more information about why this migration is occuring: [Moving Teams Android Devices to AOSP Device Management](https://techcommunity.microsoft.com/blog/microsoftteamssupport/moving-teams-android-devices-to-aosp-device-management/4140893)
- This migration is intended to be completed without any user intervention. However, if your organization conditional access policies require user-interactive multi-factor authencation, after the migration, your device will be signed out and the user will need to sign in their device.
- If any of your Teams devices are signed in using an account configured as a Device Enrollment Manager (DEM) account, you must remove those accounts as DEM accounts prior to completing this migration: [Device Enrollment Manager](/mem/intune-service/enrollment/device-enrollment-manager-enroll#android-open-source-project-aosp).
- Device Code Flow (DCF) (also known as microsoft.com/devicelogin) no longer supports user-interactive MFA. If user-interactive MFA is enforced by conditional access policies, users will need to login on their device directly not via the web.

## Step 4 - Complete the migration by deploying AOSP Device Management capable device firmware

As supporting fimwares are released, IT admins can install the firmware on their devices via Teams admin center. This firmware update will complete the migration.

### How to update a device

1. Sign in to Microsoft Teams admin center with an account with Teams device administrator permissions: [https://admin.teams.microsoft.com/](https://admin.teams.microsoft.com/).
2. Select **Teams** then **Devices**.
3. Select the desired device type.
4. Select the display name of the device you wish to update.
5. Select **Update software**.
6. Open **Manual updates**.
7. Select the new firmware update labeled with **AOSP**, then you can choose to **update immediately** or **during a maintenance window**.
8. Select **Update**.
9. Allow time for your device to update.

Once the device updates, it should automatically sign back in to Teams and function as normal.

### How to confirm the migration was successful

1. Log in to Microsoft Teams admin center with an account with Teams device administrator permissions: [https://admin.teams.microsoft.com/](https://admin.teams.microsoft.com/).
2. Select **Teams**, then select **Devices**.
3. Select the desired device type.
4. Select the display name of the device you wish to update.
5. Select **History**.
6. Look for a recent Software update action and confirm the status is **Successful**.
7. When it's successful, select the **Health** tab.

A 'Microsoft Intune App' and 'Authenticator App' should be listed under software type and tagged as **Up to date** this message confirms that the device is now running an AOSP Device Management capable firmware.

   ![Screenshot of AOSP upgrade complete.](media/android-migration-guide/aosp-upgrade-complete.png)

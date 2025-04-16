---
title: Set up Facilitator in Microsoft Teams
author: DaniEASmith
ms.author: danismith
manager: jtremper
ms.reviewer: solomon.alex, grace.culver
ms.date: 03/05/2025
ms.topic: install-set-up-deploy
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
ms.collection: 
  - M365-collaboration
  - magic-ai-copilot
ms.custom:
  - admindeeplinkTEAMS
  - admindeeplinkMAC
f1.keywords:
- NOCSH
appliesto: 
  - Microsoft Teams
ms.localizationpriority: high
search.appverid: MET150
description: Learn about how Facilitator in Microsoft Teams enables group collaboration powered by Copilot.
---

# Set up Facilitator in Microsoft Teams

> [!IMPORTANT]
> The following Facilitator capabilities are currently in public preview:
>
> - AI-generated notes for chats and meetings
> - Document summarization for meetings
> - Document question and answer (Q&A) for meetings
> - Moderator for meetings
>
> Features in preview might not be complete and could undergo changes before becoming available in the public release. They're provided for evaluation and exploration purposes only.
>
> For more information about Teams features in public preview, see [Microsoft Teams Public preview](public-preview-doc-updates.md).

Facilitator is a collaborative communication agent available to your users in Teams conversations. It combines the power of large language models (LLMs) and Teams data to help users be productive during collaboration.

Use Facilitator in peer-to-peer:

- Chats
- Meetings
- [Teams Rooms](./rooms/facilitator-teams-rooms.md)

## How Facilitator behaves in Teams

Facilitator behaves differently than Copilot in Teams.

A user's prompts to Copilot in Teams and Copilot's responses are private to that individual user. Copilot in Teams also has its own set of features and use cases.

However, Facilitator acts like an assistant sitting in your users' chats and meetings. If a user prompts Facilitator, all users can view that communication, just like if the user was talking with another person in the chat. Facilitator then displays its response within the group's conversation for everyone to see.

Facilitator also continuously updates as the conversation progresses. For example, Facilitator displays the options the team is considering and then replaces those options with a single choice once the group decides.

Users are shown a notice when their prompts are private or shared with others.

## Security, Compliance, and Privacy

Facilitator, Copilot, and Microsoft 365 are built on Microsoft's comprehensive approach to security, compliance, and privacy. When you use Microsoft Purview for your security and compliance management, Facilitator is supported in the following ways:

In preview, Facilitator in chats and meetings supports sensitivity labels and encrypted files in the same way as Microsoft Copilot chat supports your sensitive data. For example, Facilitator can't access labeled and encrypted files if the person requesting the information from Facilitator and all the participants don't have the EXTRACT usage right, and any referenced items display their sensitivity label. For more information, see [Microsoft Purview strengthens information protection for Copilot](/purview/ai-microsoft-purview#microsoft-purview-strengthens-information-protection-for-copilot) and [Information protection considerations for Copilot](/purview/ai-microsoft-purview-considerations#information-protection-considerations-for-copilot).

Additionally, just like [Copilot protection with sensitivity label inheritance](/purview/ai-microsoft-purview#copilot-protection-with-sensitivity-label-inheritance), AI-generated notes inherit the [highest priority sensitivity label](/purview/sensitivity-labels#label-priority-order-matters) from the chat or meeting, 

Facilitator AI-generated notes are supported by [auditing events](/purview/audit-log-activities#microsoft-teams-activities) that surface in [Data Security Posture Management for AI](/purview/ai-microsoft-purview#data-security-posture-management-for-ai-provides-insights-policies-and-controls-for-ai-apps) and can be used by [eDiscovery with a KQL query](/purview/edisc-keyword-query-language).

To [automatically retain or delete](/purview/retention) Facilitator in chats and meetings, and for AI-generated notes in chat, use a Microsoft Purview Data Lifecycle Management retention policy with the **Teams chat** location. Because Facilitator data in meetings is [stored in OneDrive](#facilitator-data-storage), these notes can be automatically retained or deleted with a retention policy or retention labels with the **OneDrive accounts** location.

Other Microsoft Purview solutions either aren't applicable for Facilitator or aren't yet supported.

For more information about security and privacy in Microsoft 365 Copilot, see the following articles:

- [Data, Privacy, and Security for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-privacy) for Microsoft 365 Copilot in your organization (work or school).
- [Microsoft Purview data security and compliance protections for generative AI apps](/purview/ai-microsoft-purview).
- [Copilot Pro: Microsoft 365 apps and your privacy](https://support.microsoft.com/office/copilot-pro-microsoft-365-apps-and-your-privacy-6f0d8d80-f4bb-4c9f-989e-64a4adfd62e5) for Microsoft 365 Copilot apps at home.

## Facilitator licensing and permission requirements

The following list contains the prerequisites for users to be able to access Facilitator features in Teams chats and meetings. Users must meet all of the following requirements:

### Licensing requirements

- An eligible *Microsoft 365* base license.
  - For the list of eligible base licenses, see [Understand licensing requirements for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-licensing).
- Have an eligible *Microsoft Teams* license.
  - Teams licenses might be included in your *Microsoft 365* subscription. If you have *Microsoft 365 (no Teams)* licenses, you need to purchase separate Teams licenses.
- Have a *Microsoft 365 Copilot* license.
  - For information on how to acquire *Microsoft 365 Copilot* licenses, see [Where can I get Microsoft Copilot?](https://support.microsoft.com/topic/where-can-i-get-microsoft-copilot-40a622db-6d25-4266-b008-4bbcb55cf52f)

### User requirements

- Be a Microsoft Teams Public preview participant.
  - For information on how to access Teams Public preview features, see [Microsoft Teams Public preview](/microsoftteams/public-preview-doc-updates).
- [Have Loop experiences in Teams for Facilitator in meetings turned on](#3-turn-on-loop-experiences-in-teams-for-facilitator-in-meetings).
- Have transcription enabled and keep it on for Facilitator in meetings.

## Facilitator data storage

Facilitator data in meetings is stored as a `.loop` file in a OneDrive folder titled **Meetings** of the user who initiated Facilitator in Teams. This data is treated as meeting transcript data. To learn more about how this data is handled, see [Summary of governance, lifecycle, and compliance capabilities for Loop experiences](/microsoft-365/loop/loop-compliance-summary).

Facilitator data in chats is stored as messaging data in each users' Exchange mailbox. This data is treated like all other Teams chat data.

## Turn on Facilitator for chats and meetings

As an admin, you control whether Facilitator is available to your entire organization or to a certain group of users.

Facilitator is turned on by default. However, if all apps are blocked for your organization, Facilitator is also blocked.

To turn off or on Facilitator for users, complete the following steps:

### 1. Allow Facilitator in the Teams admin center

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard) with your Teams admin credentials.
1. In the left rail navigation, select **Teams apps** > **Manage apps**.
1. In the apps list's search box, search for **Facilitator**.
1. Select **Facilitator** from the app list.
1. In the actions menu, select **Allow** or **Block**.
1. In the pop-up, select the **Allow** or **Block** button.

You can also use [app centric management](/microsoftteams/app-centric-management) to allow and block, create policies, and assign users.

For more information about managing apps in Teams, see [Manage apps](manage-apps.md).

### 2. Allow Facilitator for a group of users

To allow Facilitator for users, a new app policy needs to be created and then assigned to users.

Follow the instructions at [Use app permission policies to control user access to apps](teams-app-permission-policies.md) to create a new app policy for Facilitator.

You can then assign the policy to your entire tenant or to a select group of users. Follow the instructions at [Add or modify app availability for users](/microsoftteams/app-centric-management#add-or-modify-app-availability-for-users) to assign the policy to users using app-centric management.

### 3. Turn on Loop experiences in Teams for Facilitator in meetings

*Loop experiences in Teams* need to be turned on in order for Facilitator to be used in meetings.

To turn on Loop experiences in Teams, follow the instructions at [Settings management for Loop functionality in Teams](/microsoft-365/loop/loop-components-configuration#settings-management-for-loop-functionality-in-teams).

## Manage users' access to Facilitator skills

If there are certain Facilitator skills you would like to manage for your users, review the following details.

### Turn off AI-generated notes for chats

AI-generated notes for chats is turned on by default.

You can turn off Facilitator's ability to take notes in chats by completing the following steps.

1. Sign in to the [Teams admin center](https://admin.teams.microsoft.com/dashboard) with your Teams admin credentials.
1. In the left-side menu, expand the **Messaging** section and select **Messaging settings**.
1. On the **Messaging settings** page, find the **Messaging notes** toggle.
1. Change the toggle to the **Off** position to turn off AI-generated notes for chats.
1. Select the **Save** button.

You can also use PowerShell to manage the `MessagingNotes` setting with the [`Set-CsTeamsMessagingConfiguration`](/powershell/module/teams/set-csteamsmessagingconfiguration#-messagingnotes) cmdlet. For information about using PowerShell to manage users' Teams experience, see [Assign policies to users and groups](assign-policies-users-and-groups.md#use-powershell-method).

### Turn off AI-generated notes for meetings

*Loop experiences in Teams* control AI-generated notes for meetings, which is enabled by default.

You can manage this control using the `IsCollabMeetingNotesFluidEnabled` setting in PowerShell. This setting applies to your entire tenant and can't be configured at the user level. This means that if you disable this setting, AI-generated notes for meetings is turned off for all users in your organization.

For instructions on managing this setting, see [Settings management for Loop functionality in Teams](/microsoft-365/loop/loop-components-configuration#settings-management-for-loop-functionality-in-teams).

### Block web search for Facilitator

For users to ask Facilitator questions grounded in web search information, ensure **Allow the use of additional optional connected experiences in Office** and **Allow web search in Copilot** settings are enabled.

The **Allow the use of additional optional connected experiences in Office** setting enables Microsoft services to connect with one another, including connecting to Bing. This setting is controlled by the [Cloud Policy service for Microsoft 365](/microsoft-365-apps/admin-center/overview-cloud-policy). For more information about how to manage the optional connected experiences setting, see [Configure the policy setting by using Cloud Policy](/microsoft-365-apps/privacy/office-web-privacy-controls#configure-the-policy-setting-by-using-cloud-policy).

The **Allow web search in Copilot** setting controls users' access to web search information in their Copilot experiences. For more information, see [Controls available to manage web search](/copilot/microsoft-365/manage-public-web-access#controls-available-to-manage-web-search).

## Facilitator limitations

Facilitator currently has the following limitations:

- Only [licensed users](#facilitator-licensing-and-permission-requirements) can initiate Facilitator.
  - Unlicensed users can't prompt Facilitator, but they can see others' prompts to Facilitator and Facilitator's responses.
  - Unlicensed users can't see Facilitator's notes in chats, but they can see Facilitator's notes in meetings.
- If a licensed user doesn't have the full chat history, they can't @mention Facilitator.
- Currently, Facilitator isn't supported in [external chats and meetings](trusted-organizations-external-meetings-chat.md).
- Retention labels aren't supported for cloud attachments in AI-generated notes.
- Facilitator only supports the languages listed at [Supported languages for Microsoft Copilot](https://support.microsoft.com/office/supported-languages-for-microsoft-copilot-94518d61-644b-4118-9492-617eea4801d8).

### Document skills limitations

Currently, document skills includes summarization and question and answer (Q&A).

- Document skills only support Word, PowerPoint, and PDF files.
- Document skills are only triggered if everyone in the chat has permission to the document.
- Document skills are limited to chats with 30 people or less. If there are more than 30 people in the chat, document skills aren't available.

### Facilitator for meetings limitations

- Facilitator's AI-generated notes for meeting aren't automatically collected as cloud attachments in [Microsoft Preview eDiscovery](/purview/ediscovery-cloud-attachments) because it isn't currently supported.
- When a user turns on AI-generated notes during a meeting, they are prompted to select the language participants are speaking during the meeting. The language selected must match the spoken language during the meeting, or notes aren't generated.
- Currently, AI-generated notes for meetings only supports meetings where a single language is spoken. If multiple languages are spoken during the meeting, notes are only taken for the portions of the meeting that are spoken in the selected meeting language.
- Meeting settings like [Prevent copy and paste](manage-chat-sensitive-meetings.md#prevent-copying-or-forwarding-chat-captions-and-transcripts) and [Watermarks](watermark-meeting-content-video.md) aren't applied to Facilitator's responses or AI-generated notes in meetings.
- AI-generated notes for meetings don't inherit the meeting's sensitivity label; however, a sensitivity label can be applied to the notes' Loop component in the [Loop app or OneDrive](/purview/sensitivity-labels-loop). If a sensitivity label is applied to the notes outside of Teams, the note's file can't be accessed in Teams.

## Related articles

- [Keep track of chats with AI notes in Microsoft Teams](https://support.microsoft.com/office/keep-track-of-chats-with-AI-notes-in-Microsoft-Teams-0b7efbd0-fd3e-48e7-9a4b-4ea22cdc12c0)
- [Automate note-taking in Microsoft Teams meetings](https://support.microsoft.com/office/automate-notetaking-in-Microsoft-Teams-meetings-37657f91-39b5-40eb-9421-45141e3ce9f6)
- [What is responsible AI?](https://support.microsoft.com/topic/what-is-responsible-ai-33fc14be-15ea-4c2c-903b-aa493f5b8d92)
- [Frequently asked questions: AI, Microsoft Copilot, and Microsoft Designer](https://support.microsoft.com/topic/frequently-asked-questions-ai-microsoft-copilot-and-microsoft-designer-987b275d-f6f2-4d5d-94c5-e927cffae705)
- [Providing feedback about Microsoft Copilot with Microsoft 365 apps](https://support.microsoft.com/topic/providing-feedback-about-microsoft-copilot-with-microsoft-365-apps-c481c26a-e01a-4be3-bdd0-aee0b0b2a423?ocid=CopilotLab_SMC_Privacy_Feedback)

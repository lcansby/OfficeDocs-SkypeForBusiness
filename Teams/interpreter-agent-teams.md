---
title: Manage Interpreter agent for your organization 
author: wlibebe
ms.author: wlibebe
manager: pamgreen
ms.reviewer: harinlee
ms.date: 3/31/2025
ms.topic: how-to
ms.tgt.pltfrm: cloud
ms.service: msteams
audience: Admin
ms.collection: 
  - m365initiative-meetings
  - magic-ai-copilot
ms.custom:
  - admindeeplinkTEAMS
f1.keywords:
- NOCSH
appliesto: 
  - Microsoft Teams
ms.localizationpriority: high
search.appverid: MET150
description: Learn how to manage Interpreter agent in Microsoft Teams to provide translation during meetings.
---

# Manage Interpreter agent for your organization

**APPLIES TO:** ![Image of a checkmark for yes](/office/media/icons/success-teams.png) Meetings ![Image of a x for no](/office/media/icons/cancel-teams.png) Webinars ![Image of a x for no](/office/media/icons/cancel-teams.png) Town halls

> [!IMPORTANT]
> This feature is currently in Teams Public preview.
>
> Features in preview might not be complete and could undergo changes before becoming available in the public release. They're provided for evaluation and exploration purposes only.

The Interpreter agent for Microsoft Teams meetings acts as a translator, allowing participants with a Microsoft 365 Copilot license to listen to the meeting in their chosen language. It listens to the spoken language in the meeting and translates it into another language in real-time. This allows participants who speak different languages to understand each other and collaborate effectively. To represent their voices, participants can choose to have Interpreter simulate their own voice when translating to others or select one of the following pre-set automated voices:  Voice 1 (female), Voice 2 (male), Voice 3 (neutral).

As an admin, you can control whether your organization can use Interpreter agent and select the default setting for voice representation.

## Supported languages

The Interpreter agent supports the following languages for speaking and listening: Chinese (Mandarin), English, French, German, Italian, Japanese, Korean, Portuguese (Brazil), Spanish.

## Prerequisites and licensing for Public preview

The following list contains the prerequisites for users to access Interpreter agent in Teams meetings. Users must meet all the following requirements:

- An eligible *Microsoft 365* base license.
  - For the list of eligible base licenses, see [Understand licensing requirements for Microsoft 365 Copilot](/copilot/microsoft-365/microsoft-365-copilot-licensing).
- An eligible *Microsoft Teams* license.
  - Teams licenses may be included in your *Microsoft 365* subscription, or you may need to purchase a separate Teams license if you have *Microsoft 365 (no Teams)* licenses.
- A *Microsoft 365 Copilot* license.
  - For information on how to acquire *Microsoft 365 Copilot* licenses, see [Where can I get Microsoft Copilot?](https://support.microsoft.com/topic/where-can-i-get-microsoft-copilot-40a622db-6d25-4266-b008-4bbcb55cf52f)
- Be a Microsoft Teams Public preview participant.
  - For information on how to access Teams Public preview features, see Microsoft Teams Public preview. 

## Data, security, and privacy

When your users allow Interpreter agent to simulate their voice, their voice sample isn’t stored.

### How Interpreter agent works

The Interpreter Agent in Teams performs real-time speech-to-speech (STS) translation using Azure Cognitive Services. Interpreter agent auto-detects spoken languages in a meeting, supports multi-speaker, mixed-language conversations, and currently supports 9 different languages, with more to come.

Her's how it works:

1. Speech Recognition (ST)- Converts spoken language into English text.
2. Translation (MT)- Translates English text into the selected language(s).
3. Voice Generation (TTS)- Produces translated speech in the chosen language. TTS can simulate the speaker’s voice or use a predefined voice based on user preference and the admin policy.
4. A bot transmits meeting audio for cloud-based processing and returns translations instantly.

### How the Interpreter agent uses your users' voices

When a user turns on voice simulation in the Interpreter agent, other participants hear translated speech in the speaker’s own voice.

When a user turns on voice simulation in the Interpreter agent, other participants hear the translated speech in the speaker’s own voice.

Here's how it works:

1. **Admin policy**- You use the **`-VoiceSimulationInInterpreter`** parameter to set the default value for the **Your voice representation** setting to **Simulate my voice** for all users in your organization.
2. **User Interpreter settings**- Users can choose whether to use voice simulation during meetings.
3. **Privacy-first design**- The system samples brief segments of the speaker’s voice to simulate their tone, style, and voice characteristics, without adding emotional sentiments. This processing happens in real-time, with no biometric data stored. It preserves the speaker's natural tone, pitch, and style, creating a familiar, immersive experience. It does not exaggerate emotions or infer meaning beyond what is spoken.
4. **Voice simulation**- AI generates a simulated voice in the selected language for seamless end-to-end translation.

## Manage Interpreter agent using PowerShell

You must use PowerShell to manage Interpreter agent for your entire organization.

To manage Interpreter agent for your entire organization, you can the -**`-AIInterpreter`** and -**`-VoiceSimulationInInterpreter`** parameters in PowerShell. To use **`-VoiceSimulationInInterpreter`**, you must first set **`-AIInterpreter`** to **Enabled**.

### Turn interpreter agent on or off

The org- wide **`-AIInterpreter`** parameter controls whether your users with a Copilot license can use Interpreter agent during meetings in your organization. **This parameter is enabled by default.**

To turn off Interpreter agent for your entire organization, use the following script:

```PowerShell
Set-CsTeamsMeetingPolicy -Identity <policy name> -AIInterpreter Disabled
```

To turn on Interpreter agent for your entire organization, use the following script:

```PowerShell
Set-CsTeamsMeetingPolicy -Identity <policy name> -AIInterpreter Enabled
```

### Set the default value for voice representation

The org- wide **`-VoiceSimulationInInterpreter`** parameter controls your users' default value for **Your voice representation** in **Interpreter settings**. **By default, this parameter is set to disabled.**

Here's the user experience for Interpreter agent depending on the value you choose:

- **Enabled**: Sets the default value for **Your voice representation** to **Simulate my voice**. When users turn on Interpreter agent, it automatically simulates their voices when translating to others in meetings. Participants also have the option to select an automated voice.

- **Disabled**: Sets the default value for **Your voice representation** to **Automated voice**. When users turn on Interpreter agent, they choose one of the automated voices that is translated to others. Participants can also choose to allow Interpreter to simulate their voice. **This is the default value.**

To set the org-wide default value for the **Your voice representation** setting to **Simulate my voice**, use the following script:  

```PowerShell
Set-CsTeamsMeetingPolicy -Identity <policy name> -VoiceSimulationInInterpreter Enabled
```

To set the org-wide default value for the **Your voice representation** setting to **Automated voice**, use the following script:

```PowerShell
Set-CsTeamsMeetingPolicy -Identity <policy name> -VoiceSimulationInInterpreter Disabled
```

## Related articles

- [Manage Microsoft 365 Copilot in Teams meetings and events](copilot-teams-transcription.md)
- [Set up Facilitator in Microsoft Teams for collaborative AI-generated notes](facilitator-teams.md)
- [What is responsible AI?](https://support.microsoft.com/topic/what-is-responsible-ai-33fc14be-15ea-4c2c-903b-aa493f5b8d92)
- [Frequently asked questions: AI, Microsoft Copilot, and Microsoft Designer](https://support.microsoft.com/topic/frequently-asked-questions-ai-microsoft-copilot-and-microsoft-designer-987b275d-f6f2-4d5d-94c5-e927cffae705)
- [Providing feedback about Microsoft Copilot with Microsoft 365 apps](https://support.microsoft.com/topic/providing-feedback-about-microsoft-copilot-with-microsoft-365-apps-c481c26a-e01a-4be3-bdd0-aee0b0b2a423?ocid=CopilotLab_SMC_Privacy_Feedback)

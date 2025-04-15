---
title: Create a Brand for SMS in Microsoft Teams
author: sfrancis206
ms.author: scottfrancis
manager: pamgreen
ms.reviewer: nijait, julienp
ms.date: 02/24/2025
ms.topic: article
ms.tgt.pltfrm: cloud
ms.service: msteams
ms.collection:
  - M365-voice
  - m365initiative-voice
  - Tier1
search.appverid: MET150
audience: Admin
appliesto:
  - Microsoft Teams
ms.localizationpriority: medium
f1.keywords:
  - CSH
description: Learn how to set up an SMS Brand to enable SMS in Microsoft Teams.
---

# Create a Brand for SMS in Microsoft Teams

> [!NOTE]
> Service update: If you receive a Brand or Campaign rejection, our Telephone Number Services team is aware and managing a case with you through the [Phone Number Service Center](https://pstnsd.powerappsportals.com) portal. Due to a high volume of requests for SMS in Teams, processing times to facilitate approvals of rejected Brand and Campaign applications for SMS in Teams may take 4 to 6 weeks.  We appreciate your patience as we work diligently to address all requests.

This article is for IT administrators and IT professionals who are enabling Short Message Service (SMS) in Teams.

Use this article while creating a brand in Microsoft's Teams admin center to verify and register your company.

Before reading this article, make sure you've read [Plan for SMS in Teams](sms-overview.md).

> [!NOTE]
> SMS in Teams is only available on Calling Plan phone numbers in the United States (including Puerto Rico) and Canada. 
> Customers must have an approved Brand and Campaign before enabling SMS on Teams Calling Plan numbers. 

## Prerequisites

Ensure fundamental understanding of the *purpose* for your Brand, as described in [Learn about SMS Texting in Teams](sms-overview.md).

Administrators must have one of the following role-based access control (RBAC) roles assigned:

- Teams Administrator
- Teams Communications Administrator
- Teams Telephony Administrator

## Create a Teams SMS brand in Teams admin center

The 10DLC (10-digit long code) registration process involves verifying your organization's identity. To get your organization verified, you build an organization profile as your "Brand" in the Teams admin center.

1. In the Teams admin center, go to **Voice** > **Service configuration** > **SMS** > **Step 1: Create brand**.
1. Select **Create your brand to start / Update brand / View details** to open a right-side configuration slide-out and populate the fields with your company's information.

The form fields change dynamically depending on your company's country/region and status. For example, if your company is registered in the US and is a *publicly traded* company, more fields are required to disclose your company's stock symbol. However, if you have a private company, a stock symbol isn't required.

Populate your Brand application according to the field headers as follows:

### Description

In the first section of the brand form, provide details of your company, as denoted in its country/region.

|Form field |Description |
|:-----|:-----|
|Brand legal name |Enter your company's official name as it's legally registered in your country or region. Ensure that your company name matches your corporation registration and is spelled correctly. |
|Brand display name|Enter how your company's *Doing Business As* name or *trade* name of your company.|
|Tax ID issuing country |Enter the country/region where your company business ID is issued.|
|Tax ID |Enter the Tax ID of your company, respective to the country/region of your company registration.<br><br>**United States** - US companies (and companies with a US EIN), enter your Tax ID's nine-digit EIN.<br>**Canada** - For companies based in Canada, enter your nine-digit Canadian Business Number (BN) issued by the CRA, Corporation/Incorporation Number, or Registry ID.<br>**Outside the United States and Canada** - Businesses outside US & Canada should enter the numeric part of their VAT ID.|
|Brand legal address |Enter the legal address in which the company is registered. If you already defined your legal address as an address in **Locations**, select **Use existing** and search for the address by the city or by the location description. If the address isn't already added, select **Add new** and enter it here.<br>Ensure that your legal address matches your corporation registration and is spelled correctly. |
|Website |Enter your company's website.|

### Brand Information

Within the brand information, provide context about your company's business.

|Form field |Description |
|:-----|:-----|
|Organization Legal Form |Select the legal structure of your company.<br><br>**Private company** - A private company is owned by individuals or groups and doesn't sell shares to the public.<br>**Publicly Traded Company** - A publicly traded company sells shares on stock exchanges.<br>**Non-Profit Organization** - A non-profit operates for charitable purposes without distributing profits. Only US-based non-profits or non-profits with a US EIN are accepted. Non-US non-profits should register as private companies. For example, if you're a non-profit organization located in Canada, you register as a **Private company**.|
|Brand segment |From the drop-down, select the industry that best categorizes your company's business.|


> [!NOTE]
> Brand registration for US Government entities is currently not supported. Non-US Government should register as private companies 
> Brand registration for Sole Proprietor entities is currently not supported.  

Additional information are required to register **Publicly Traded** brands:

|Form field |Description |
|:-----|:-----|
|Brand stock symbol |If your company is a publicly traded company, enter your company's stock symbol.|
|Brand stock exchange |If your company is a publicly traded company, select the exchange where it's listed and traded.|
|Business email contact for Two Factor Authentication (2FA) |Brands with a Public Profit entity type are required to complete a two-factor authentication (2FA) process as part of the verification process. Provide the email that will receive the verification email. It cannot be personal or free email or a distribution list such as sales or support.|

### Contact Information

If there are issues with the registration of your brand, Microsoft Support will reach out to a point of contact that you designate. Enter your contact information according to the field headers as follows:

|Form field |Description |
|:-----|:-----|
|First name | Enter the first name of the point of contact for this application process. |
|Last name | Enter last name. |
|Phone number | Enter the phone number in E.164 format of the point of contact for inquiries related to this application process.<br><br>E.164 is the international phone number format that starts with a plus sign (+) followed by your country code, area code, and local number with no spaces, dashes, or parentheses. For example, a US phone number of (202) 555-0123 should be written as: +12025550123. |
|Email address | Enter the email address of the *point of contact* for inquiries related to this application process. We recommend entering a distribution or group list here over a personal email. |


### Terms and Conditions

Once the fields are accurately filled out, select the box to accept Microsoft's terms and conditions.

The terms as follows relate to Microsoft sharing your brand information with an operator, in this case, The Campaign Registry.

> Teams SMS services involve an integration between Microsoft and the underlying carrier, aggregator, or operator ("Operator"). Microsoft must share application details and/or brand information with the Operator to ensure that the program meets regulatory guidelines and standards set by operators. The Operator is the final reviewer and approver of your service application. If the details you provide on your application change, it's your responsibility to resubmit your application with up-to-date information. By submitting an application, you agree that Microsoft may share the application details as necessary for provisioning the Teams messaging service.

### Brand submission and status

After filling out all the applicable fields, select **Submit**.

Your Brand's **Status** should now show as **Submitted** and the brand information can no longer be modified.

After reviewing your Brand's details and accepting Microsoft's terms and conditions, select **Submit**.

After submission, the Brand status shows as **Submitted** and the brand information can't be modified.
> [!IMPORTANT]
> If you designated your organization's legal form as *Publicly Traded Company*, you are required to complete a two-factor authentication (2FA) process as part of the verification process. 
> Once the brand is submitted, the Business Contact Email will receive an email with a verification link and PIN from **noreply@auth.campaignregistry.com**. They should click the link, enter their first name, last name, job title, and the PIN, and complete the form to verify your brand. 
> If the Business Contact does not receive the two-factor authentication (2FA) email, please check your junk mail and your company's firewall rules. Alternatively, you can request Microsoft to resend the email.

If approved, your brand status will be updated to "**Approved**" and you can move on to [Step 2: Create a campaign](sms-setup-campaign.md).
If not approved, the status will change to "**Microsoft Support Engaged**," and our support team may contact the support representative of your brand for further assistance.

The review and approval process may take 2 business days. These timelines are for informational purposes only and may vary.
If you submitted incorrect brand information, [contact Microsoft's Telephone Number Services - Service Desk](contact-tns-service-desk.md).

> [!NOTE]
> If your brand is not approved, a case is automatically opened on your behalf with Microsoft's Telephone Number Services - Service Desk. You can view your case by navigating to the [Phone Number Service Center](https://pstnsd.powerappsportals.com), and selecting the tab for **My Company Cases**. Open the case, and you can interact with the Telephone Number Services (TNS) - Service Desk team about the details and status of the case.

## Related topics

- [Microsoft Calling Plan Overview](calling-plan-overview.md)

- [Getting numbers with Microsoft Calling Plan](manage-phone-numbers-landing-page.md)

- [Learn about SMS texting in Teams](sms-overview.md)

- [Step 2: Create a campaign](sms-setup-campaign.md)

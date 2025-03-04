---
title: "Validate app protection settings on Android or iOS devices"
f1.keywords:
- NOCSH
ms.author: sharik
author: skjerland
manager: scotv
audience: Admin
ms.topic: article
ms.service: o365-administration
ms.localizationpriority: medium
ms.collection: 
- M365-subscription-management
- M365-identity-device-management
- Adm_TOC
ms.custom:
- Adm_O365
- Core_O365Admin_Migration
- MSB365
- OKR_SMB_M365
- AdminSurgePortfolio
search.appverid:
- BCS160
- MET150
ms.assetid: f3433b6b-02f7-447f-9d62-306bf03638b0
description: "Learn how to validate the Microsoft 365 Business Premium app protection settings in your Android or iOS devices."
---

# Validate app protection settings on Android or iOS devices

> [!NOTE]
> Microsoft Defender for Business is rolling out to Microsoft 365 Business Premium customers, beginning March 1, 2022. This offering provides additional security features for devices. [Learn more about Defender for Business](../security/defender-business/mdb-overview.md)

Follow the instructions in the following sections to validate app protection settings on Android or iOS devices.
  
## Android
  
### Check that the app protection settings are working on user devices

After you [set app protection settings for Android or iOS devices](../business-premium/m365bp-app-protection-settings-for-android-and-ios.md) to protect the apps, you can follow these steps to validate that the settings you chose work. 
  
First, make sure that the policy applies to the app in which you're going to validate it.
  
1. In the Microsoft 365 Business Premium [admin center](https://admin.microsoft.com), go to **Policies** \> **Edit policy**.
    
2. Choose **Application policy for Android** for the settings you created at setup, or another policy you created, and verify that it's enforced for Outlook, for example. 
    
    ![Screenshot showing all the apps for which this policy protects files.](../business-premium/media/b3be3ddd-f683-4073-8d7a-9c639a636a2c.png)
  
### Validate Require a PIN or a fingerprint to access Office apps

In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require a PIN or fingerprint to access Office apps** is set to **On**.
  
![Make sure that the Require a PIN or fingerprint to access Office apps is set to On.](../business-premium/media/f37eb5b2-7e26-49fb-9bd6-d955d196bacf.png)
  
1. In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials.
    
2. You'll also be prompted to enter a PIN or use a fingerprint.
    
    ![Enter a PIN on your Android device to access Office apps.](../business-premium/media/9e8ecfee-8122-4a3a-8918-eece80344310.png)
  
### Validate Reset PIN after number of failed attempts

In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Reset PIN after number of failed attempts** is set to some number. This is 5 by default. 
  
1. In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials.
    
2. Enter an incorrect PIN as many times as specified by the policy. You'll see a prompt that states **PIN Attempt Limit Reached** to reset the PIN. 
    
    ![Screenshot indicating after too many incorrect PIN attempts, you need to reset your PIN.](../business-premium/media/fca6fcb4-bb5c-477f-af5e-5dc937e8b835.png)
  
3. Press **Reset PIN**. You'll be prompted to sign in with the user's Microsoft 365 Business Premium credentials, and then required to set a new PIN.
    
### Validate Force users to save all work files to OneDrive for Business

In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Force users to save all work files to OneDrive for Business** is set to **On**.
  
![Verify that Force users to save all work files to OneDrive for Business is set to On.](../business-premium/media/7140fa1d-966d-481c-829f-330c06abb5a5.png)
  
1. In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials, and enter a PIN if requested.
    
2. Open an email that contains an attachment and tap the down arrow icon next to the attachment's information.
    
    ![Tap the down arrow next to an attachment to try to save it.](../business-premium/media/b22573bb-91ce-455f-84fa-8feb2846b117.png)
  
    You'll see **Cannot save to device** on the bottom of the screen. 
    
    ![Warning text that indicates cannot save a file locally to an Android.](../business-premium/media/52ca3f3d-7ed0-4a52-9621-4872da6ea9c5.png)
  
    > [!NOTE]
    > Saving to OneDrive for Business is not enabled for Android at this time, so you can only see that saving locally is blocked. 
  
### Validate Require user to sign in again if Office apps have been idle for a specified time

In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require users to sign in again after Office apps have been idle for** is set to some number of minutes. This is 30 minutes by default. 
  
1. In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials, and enter a PIN if requested.
 
1. You should now see Outlook's inbox. Let the Android device idle untouched for at least 30 minutes (or some other amount of time, longer than what you specified in the policy). The device will likely dim.

1. Access Outlook on the Android device again.

1. You'll be prompted to enter your PIN before you can access Outlook again.

### Validate Protect work files with encryption

In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Protect work files with encryption** is set to **On**, and **Force users to save all work files to OneDrive for Business** is set to **Off**.
  
1. In the user's Android device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials, and enter a PIN if requested.

1. Open an email that contains a few image file attachments.

1. Tap the down arrow icon next to the attachment's info to save it.

    ![Tap the down arrow to save the figure file to the Android device.](../business-premium/media/08a9e21e-4022-45d5-acff-59cface651e7.png)
  
1. You may be prompted to allow Outlook to access photos, media, and files on your device. Tap **Allow**.

1. At the bottom of the screen, choose to **Save to Device** and then open the **Gallery** app.

1. You should see an encrypted photo (or more, if you saved multiple image file attachments) in the list. It may appear in the Pictures list as a gray square with a white exclamation point within a white circle in the center of the gray square.

    ![An encrypted image file in the Gallery app.](../business-premium/media/25936414-bd7e-421d-824e-6e59b877722d.png)
  
## iOS
  
### Check that the App protection settings are working on user devices

After you [set app configurations for iOS devices](../business-premium/m365bp-protection-settings-for-windows-10-devices.md) to protect apps, you can follow these steps to validate that the settings you chose work. 
  
First, make sure that the policy applies to the app in which you're going to validate it.
  
1. In the Microsoft 365 Business Premium [admin center](https://admin.microsoft.com), go to **Policies** \> **Edit policy**.

1. Choose **Application policy for iOS** for the settings you created at setup, or another policy you created, and verify that it's enforced for Outlook for example. 

    ![Screenshot that shows all the apps for which this policy protects files.](../business-premium/media/842441b8-e7b1-4b86-9edd-d94d1f77b6f4.png)
  
### Validate Require a PIN to access Office apps

In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require a PIN or fingerprint to access Office apps** is set to **On**.
  
![Make sure that the Require a PIN or fingerprint to access Office apps is set to On.](../business-premium/media/f37eb5b2-7e26-49fb-9bd6-d955d196bacf.png)
  
1. In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials.

1. You'll also be prompted to enter a PIN or use a fingerprint.

    ![Enter a PIN on your IOS device to access Office apps.](../business-premium/media/06fc5cf3-9f19-4090-b23c-14bb59805b7a.png)
  
### Validate Reset PIN after number of failed attempts

In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Reset PIN after number of failed attempts** is set to some number. This is 5 by default.
  
1. In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials.

1. Enter an incorrect PIN as many times as specified by the policy. You'll see a prompt that states **PIN Attempt Limit Reached** to reset the PIN.

    ![Screenshot warning PIN reset after too many incorrect attempts.](../business-premium/media/fab5c089-a4a5-4e8d-8c95-b8eed1dfa262.png)
  
1. Press **OK**. You'll be prompted to sign in with the user's Microsoft 365 Business Premium credentials, and then required to set a new PIN.

### Validate Force users to save all work files to OneDrive for Business

In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Force users to save all work files to OneDrive for Business** is set to **On**.
  
![Verify that Force users to save all work files to OneDrive for Business is set to On.](../business-premium/media/7140fa1d-966d-481c-829f-330c06abb5a5.png)
  
1. In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials, and enter a PIN if requested.

1. Open an email that contains an attachment, open the attachment and choose **Save** on the bottom of the screen. 

    ![Tap the Save option after you open an attachment to try to save it.](../business-premium/media/b419b070-1530-4f14-86a8-8d89933a2b25.png)
  
1. You should only see an option for OneDrive for Business. If not, tap **Add Account** and select **OneDrive for Business** from the **Add Storage Account** screen. Provide the end user's Microsoft 365 Business Premium to sign in when prompted.

    Tap **Save** and select **OneDrive for Business**.

### Validate Require user to sign in again if Office apps have been idle for a specified time

In the **Edit policy** pane, choose **Edit** next to **Office documents access control**, expand **Manage how users access Office files on mobile devices**, and make sure that **Require users to sign in again after Office apps have been idle for** is set to some number of minutes. This is 30 minutes by default.
  
1. In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials, and enter a PIN if requested.

1. You should now see Outlook's inbox. Let the iOS device untouched for at least 30 minutes (or some other amount of time, longer than what you specified in the policy). The device will likely dim.

1. Access Outlook on the iOS device again.

1. You'll be prompted to enter your PIN before you can access Outlook again.

### Validate Protect work files with encryption

In the **Edit policy** pane, choose **Edit** next to **Protection against lost or stolen devices**, expand **Protect work files when devices are lost or stolen**, and make sure that **Protect work files with encryption** is set to **On**, and **Force users to save all work files to OneDrive for Business** is set to **Off**.
  
1. In the user's iOS device, open Outlook and sign in with the user's Microsoft 365 Business Premium credentials, and enter a PIN if requested.

1. Open an email that contains a few image file attachments.

1. Tap the attachment and then tap the **Save** option under it. 

1. Open **Photos** app from the home screen. You should see an encrypted photo (or more, if you saved multiple image file attachments) saved, but encrypted. 

## See also

[Best practices for securing Microsoft 365 for business plans](../admin/security-and-compliance/secure-your-business-data.md)
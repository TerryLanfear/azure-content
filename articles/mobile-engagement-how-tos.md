<properties 
   pageTitle="Azure Mobile Engagement How To Guides" 
   description="How To Guides for Azure Mobile Engagement" 
   services="mobile-engagement" 
   documentationCenter="mobile" 
   authors="v-micada" 
   manager="mattgre" 
   editor=""/>

<tags
   ms.service="mobile-engagement"
   ms.devlang="Java"
   ms.topic="article"
   ms.tgt_pltfrm="mobile"
   ms.workload="required" 
   ms.date="02/17/2015"
   ms.author="v-micada"/>

# Azure Mobile Engagement - How To Guides

## Introduction

The following How To Guides for the Azure Mobile Engagement [User Interface][Link 1] assume that you are familiar with the basic [Concepts][Link 6] of Azure Mobile Engagement and will only work after you have integrated the Azure Mobile Engagement [SDK][Link 5] into your application. If you have difficulty with any of these Walkthroughs please consult the Azure Mobile Engagement [Troubleshooting Guides][Link 2].

## Do Your First Push Notification Campaign
-    Confirm that your Reach is integrated into your app with the SDK. 
-    Select your application
 
![First1][1]

-    Go to the "Reach" Section and Click "New announcement"
 
![First2][2]

-    Create a new campaign and name it
 
 ![First3][3]

-    Select how the notification should be delivered, as In-app only
 
![First4][4]

-    Create the message you want to push
 
![First5][5]

-    You may write a title on the notification (Optional).
-    Write push message content.
-    You can upload an image. Be aware that the size of the file cannot exceed 32,768 bytes.
-    You also have the ability to select further options, but for the focus of this tutorial, we will see that later.

-    Select the content type as Notification only
 
![First6][6]

-    Create your push campaign and it will appear in your campaign list.
 
![First7][7]

## Test Your Push Notification Campaign
 
![Test1][8]

-    Register your device.
-    Click on the checkbox of the device you want to push.
-    Click on the "Test" button to send the push to the device.
 
![Test2][9]

-    Activate the campaign
 
![Test3][10]

-    Now that you have created your campaign you just need to activate it for the notification to be pushed to your users.
 
## Send Personalized Pushes
-    This example creates a push where a custom rebate code is entered into the push notification.
 
![Personalize1][11]

Personalization works by replacing a marker by from an app info tag so, you'll have to make sure the user has the proper app-info defined first. In this example the targeted users will have an app info tag named rebate_code defined.
As you see above the push notification content includes the marker ${rebate_code} which will indicate that it is to be replaced by the actual content of the app info tag.

> Warning: If the app info tag is not defined for the user, the user will not receive the push.

-    Result
 
![Personalize2][12]

### You can further personalize the text your notification
 
![Personalize3][13]

-    Including the title of the notification,
-    And the content of the message.
-    Choose the type of announcement (Text view or Web view)
 
![Personalize4][14]

### The body of an announcement may also be personalized with:
-    The action URL, should you want to customize the landing page
-    The title,
-    The body of the message.
 
 
## Differentiate Your Push Notification (in or out of app)

-    Choose the type of notification you will push, select your application, go to the "Reach" section, select or create a push campaign and go to the "Notification" section.
 
-    Click on the "delivery mode" you want.
-    Click on the "Restrict Activities" checkbox when you want the notification occurs on specific activities (screens).

![Differentiate1][15]

### "Out of App Only" delivery mode
 
![Differentiate2][16]

"Out of App Only" delivery mode provides push notification when the application is closed. This is the standard push notification.
When you select "out of app only" ,you must have already provided the certificates from the platform that your application is building on (APNS or GCM).

**See also:** 

-  [Apple Push Notification Service – Certificates](http://developer.apple.com/library/mac/#documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ApplePushService/ApplePushService.html#//apple_ref/doc/uid/TP40008194-CH100-SW9), Google Cloud Messaging – Certificate](http://developer.android.com/google/gcm/index.html) 

### "in-App Only" delivery mode
 
![Differentiate3][17]

"In-App Only" delivery mode provides push notification when the application is running.
For this notification, you do not need to go through the APNS and GCM system.
You can use the in-app delivery system to reach your end-users.
You can fully customize the notification and decide in which activity (screen) the notification will appear.

### "Anytime" delivery mode
You can choose an "Anytime" delivery mode, ensures you to reach your end-user whether the application is running or not.
When you select "Anytime" , you must have already provided the certificates from the platform that your application is building upon (APNS or GCM). 
 
## Schedule a Push Campaign
 
### Plan to Start a campaign
 
![Shedule1][18]

It is the 21st of March and you have an announcement to make and planed for the 22nd of March at midnight. 
You don’t have to stay in front of the interface to do a push! You can plan in advance the exact minute notifications will be sent.
-    Un-check the "None" checkbox and select a start time 
-    Choose the date and the time you want to start the push campaign.
### Plan to end a campaign
 
![Shedule2][19]

You want your campaign to stop on the 25th of March at 3.00 pm but you know you won't be there to do it.
You don’t have to stay in front of the interface to push! You can plan in advance the exact minute your campaign will stop.
-    Click on the "None" checkbox or select a end time
-    Choose the date and the time you want to finish the push campaign.
### End a campaign manually
 
![Shedule3][20]

By default, the "None" check-boxes are selected.
This means that the campaign will start as soon as you activate it in the reach section and will end when you will stop it on the reach section.
 
> Note: Campaigns created without an end date store the push locally on the device and show it the next time the app is opened even if the campaign is manually ended.

## Enhance a Push Notification with a Text View

### What is a Text View?
 
![TextView1][21]

A text view is a pop-up with text content. This pop-up appears after the end-user has clicked on the push notification.
A text view allows you to present more content to your end-user. This is also the opportunity to present a call to action such as jumping to a page of your app, redirecting to a Store, opening a web page, sending an e-mail, starting a geo-localized search, etc...

### Example: Text View
-    Create your Push notification campaign in the "Reach" section and give your campaign a name
 
![TextView2][22]

-    Write the message that will appear on the notification.
-    Select the Announcement Content Type of “text”
 
![TextView3][23]

> Note: when you push a text view, it always comes with a notification first. 

- Define the text (After having selected the text announcement content, the sub-section will appear, allowing you to define the text you want to be displayed.)
 
![TextView4][24]

-    Write the title that will appear at the top of the message.
-    Write the main content of the text view.
-    Write the content that will appear on the action button (an action button enables the application to make a specific action such as opening a page of the application, redirecting to an App store or any kind of sources you can provide).
-    Write the content that will appear on the exit button (by clicking on the exit button, the text view will disappear.)
 
-    Create your push notification campaign and it will appear on the campaign list.
 
![TextView5][25]

-    Activate your push notification campaign to send the text view to your users.
 
![TextView6][26]

-    Result
 
![TextView7][27]

-    The user receives the notification and click on it.
-    The text view appears as a pop-up allowing the user to interact with it.

## Enhance a Push Notification with a Web View

### What is a Web View?
 
![WebView1][28]

A web view is a pop-up with web content. This pop-up appears when the end-user has clicked on the push notification.
A web view allows you to have more interaction with the end-user.
This is also the opportunity to present a call to action such as redirection to App Store, opening a web page, sending an e-mail, starting a geo-localized search, etc...

### Example: Web View

-    Create your Push campaign in the "Reach" section and give your campaign a name.
 
![WebView2][29]

-    Write the message that will appear on the notification.
-    Select the Announcement Content Type as “web”
 
![WebView3][30]

**About Announcement types:**

- Notification only: It is a simple standard notification. Meaning that if a user clicks on it, no additional view will appear, but only the action associated to it will occur.
- Text announcement: It is a notification that engages the user to have a look at a text view.
- Web announcement: It is a notification that engages the user to have a look at a web view.
Select the "Web announcement" content.

> Note: When you push a web view, it always comes with a notification first.

- Define the web content (After having selected the web announcement content, the subsection will appear, allowing you to define the web view content you want to be displayed.)

 
![WebView4][31]

-    Write the title that will appear at the top of the message (optional).
-    Write your HTML code here.
-    Click on the source editing mode button to switch edition and see how it looks like.
-    Write the content that will appear on the action button (an action button enables the application to make a specific action such as opening a page of the application, redirecting to a Store or any kind of sources you can provide).
-    Write the content that will appear on the exit button (by clicking on the exit button, the web view will disappear).
 
-    Result
 
![WebView5][32]

-    The user receive the notification and click on it.
-    The text view appears as a pop-up allowing the user to interact with it.

<!--Image references-->
[1]: ./media/mobile-engagement-how-tos/First1.png
[2]: ./media/mobile-engagement-how-tos/First2.png
[3]: ./media/mobile-engagement-how-tos/First3.png
[4]: ./media/mobile-engagement-how-tos/First4.png
[5]: ./media/mobile-engagement-how-tos/First5.png
[6]: ./media/mobile-engagement-how-tos/First6.png
[7]: ./media/mobile-engagement-how-tos/First7.png
[8]: ./media/mobile-engagement-how-tos/Test1.png
[9]: ./media/mobile-engagement-how-tos/Test2.png
[10]: ./media/mobile-engagement-how-tos/Test3.png
[11]: ./media/mobile-engagement-how-tos/Personalize1.png
[12]: ./media/mobile-engagement-how-tos/Personalize2.png
[13]: ./media/mobile-engagement-how-tos/Personalize3.png
[14]: ./media/mobile-engagement-how-tos/Personalize4.png
[15]: ./media/mobile-engagement-how-tos/Differentiate1.png
[16]: ./media/mobile-engagement-how-tos/Differentiate2.png
[17]: ./media/mobile-engagement-how-tos/Differentiate3.png
[18]: ./media/mobile-engagement-how-tos/Schedule1.png
[19]: ./media/mobile-engagement-how-tos/Schedule2.png
[20]: ./media/mobile-engagement-how-tos/Schedule3.png
[21]: ./media/mobile-engagement-how-tos/TextView1.png
[22]: ./media/mobile-engagement-how-tos/TextView2.png
[23]: ./media/mobile-engagement-how-tos/TextView3.png
[24]: ./media/mobile-engagement-how-tos/TextView4.png
[25]: ./media/mobile-engagement-how-tos/TextView5.png
[26]: ./media/mobile-engagement-how-tos/TextView6.png
[27]: ./media/mobile-engagement-how-tos/TextView7.png
[28]: ./media/mobile-engagement-how-tos/WebView1.png
[29]: ./media/mobile-engagement-how-tos/WebView2.png
[30]: ./media/mobile-engagement-how-tos/WebView3.png
[31]: ./media/mobile-engagement-how-tos/WebView4.png
[32]: ./media/mobile-engagement-how-tos/WebView5.png

<!--Link references-->
[Link 1]: ../mobile-engagement-user-interface/
[Link 2]: ../mobile-engagement-troubleshooting-guide/
[Link 3]: ../mobile-engagement-how-tos/
[Link 4]: http://go.microsoft.com/fwlink/?LinkID=525553
[Link 5]: http://go.microsoft.com/fwlink/?LinkID=525554
[Link 6]: http://go.microsoft.com/fwlink/?LinkId=525555

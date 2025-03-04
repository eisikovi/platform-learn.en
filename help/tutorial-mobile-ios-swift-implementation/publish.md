---
title: Publish your tag property
description: Learn how to publish your tag property from the Development environment to the Staging and Production environments. This lesson is part of the Implement the Experience Cloud in Mobile iOS Swift Applications tutorial.
exl-id: eaca9b17-2f65-47fd-a1f6-26b28ad4eef7
---
# Publish your tag property

Now that you have implemented some key solutions of the Adobe Experience Cloud in your Development environment, it's time to learn the publishing workflow.

>[!NOTE]
>
>Adobe Experience Platform Launch is being integrated into Adobe Experience Platform as a suite of data collection technologies. Several terminology changes have rolled out in the interface which you should be aware of while using this content:
>
> * Platform Launch (Client Side) is now **[[!DNL tags]](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html)** 
> * Platform Launch Server Side is now **[[!DNL event forwarding]](https://experienceleague.adobe.com/docs/experience-platform/tags/event-forwarding/overview.html)** 
> * Edge configurations  are now **[[!DNL datastreams]](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/datastreams.html)**

## Prerequisites

Your tags user account needs permission to "Approve" and "Publish" in order to complete this lesson. If you are unable to complete any of these steps because the user interface options are not available to you, reach out to your Experience Cloud Administrator for access. For more information on tag user permissions, see [the documentation](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/user-permissions.html).

## Learning Objectives

At the end of this lesson, you will be able to:

1. Publish a Development library to the Staging environment
1. Update your app to load different tag environments
1. Publish a Staging library to the Production environment

## Publish to Staging

 Now that you have created and validated your library in the Development environment, it is time to publish it to Staging.

1. Go to the **[!UICONTROL Publishing]** page

1. Open the dropdown next to your library and select **[!UICONTROL Submit for Approval]**

   ![Submit for Approval](images/mobile-publishing-submitForApproval.png)

1. Click the **[!UICONTROL Submit]** button in the dialog:

   ![Click Submit in the Modal](images/mobile-publishing-submit.png)

1. Your library will now appear in the [!UICONTROL Submitted] column in an unbuilt state:

1. Open the dropdown and select **[!UICONTROL Build for Staging]**:

   ![Build for Staging](images/mobile-publishing-buildForStaging.png)
1. Once the green-dot icon appears, the library can be previewed in the Staging environment.

In a real-life scenario, the next step in the process would typically be to have your QA team validate the changes in the Staging library.

**To Validate the Changes in the Staging Library**

1. In your tag property, open the [!UICONTROL Environments] page

1. In the [!UICONTROL Staging] row, click the Install icon

   ![Install icon](images/mobile-launch-installIcon.png) to open the modal
   ![Go to the Environments page and click to open the modal](images/ios/swift/mobile-publishing-getStagingCode.png)

If you use a different workspace for your Staging app, you would need to make sure that this workspace has all of the Pods and app updates that you made throughout this tutorial. At this point, the only difference in the installation instructions from your development environment is the tag reference in the Core Configuration, as highlighted in the screenshot above. You would need to update the corresponding line in your AppDelegate.swift file and rebuild your app.

In real-life, once your QA team has signed off by reviewing the changes in the Staging environment it is time to publish to production.

## Publish to Production

1. Go to the [!UICONTROL Publishing] page

1. From the dropdown, click **[!UICONTROL Approve for Publishing]**:

   ![Approve for Publishing](images/mobile-publishing-approveForPublishing.png)

1. Click the **[!UICONTROL Approve]** button in the dialog box:

   ![Click Approve](images/mobile-publishing-approve.png)

1. The library will now appear in the [!UICONTROL Approved] column in the unbuilt state (yellow dot):

1. Open the dropdown and select **[!UICONTROL Build and Publish to Production]**:

   ![Click Build &amp; Publish to Production](images/mobile-publishing-buildAndPublishToProduction.png)

1. Click the **[!UICONTROL Publish]** in the dialog box:

   ![Click Publish](images/mobile-publishing-publish.png)

1. The library will now appear in the [!UICONTROL Published] column:

   ![Published](images/mobile-publishing-published.png)

Again, notice that the Production environment uses a tag reference in the Core Configuration, as highlighted in the screenshot below. If you use a different workspace for your Staging app, you would need to make sure that this workspace has all of the Pods and app updates that you made throughout this tutorial.
   ![Go to the Environments page and click to open the modal](images/ios/swift/mobile-publishing-getProductionCode.png)

>[!WARNING]
>
>The next time you make changes to your tags configuration you will need to create a new Library in the Development environment. Remember, that adding and removing extensions will require updates to the app itself. Be careful about keeping your tag environments and app code in sync with each other to avoid issues.

That’s it! You've completed the tutorial and published your first mobile property in tags!

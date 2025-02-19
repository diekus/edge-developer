---
description: New features and origin trials for Progressive Web Apps (PWAs).
title: What's New in Progressive Web Apps
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/23/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, pwas, pwa, progressive web apps, origin trials
---
# What's New in Progressive Web Apps

[!INCLUDE [contact DevTools team note](includes/edge-whats-new-note.md)]


<!-- ====================================================================== -->
## What's New in Microsoft Edge 94

Microsoft Edge version 94 release moved to Stable on Sept 23, 2021.  This release cycle was short—just<!-- em dash --> 3 weeks from Microsoft Edge 93 Stable to Microsoft Edge 94 Stable as we snapped to the new [four week release cycle][4weekReleaseBlog].  This new release cadence matches the new cadence of Chromium milestones, described in [Speeding up Chrome's release cycle][Chromium4weekM].

Due to the shortened release cycle of Microsoft Edge version 94, we focused on stabilizing the release cycle logistics, and we shifted feature development to Microsoft Edge version 95.

The origin trials remain active for the following features:
*  [Window Controls Overlay for desktop PWAs](#window-controls-overlay-origin-trials).
*  [URL Handlers](#url-handlers-origin-trial).

We expect the [protocol handlers origin trial](#protocol-handlers-origin-trial) to end with Microsoft Edge version 94 as we take final feedback and get ready to move the protocol handlers feature to Stable.  In case you are enrolled in the origin trial for protocol handlers, we plan to end the trial period after Microsoft Edge version 94.  We'll then determine when this feature will become Stable.


<!-- ====================================================================== -->
## What's New in Microsoft Edge 93

Microsoft Edge version 93 became the Stable channel of Microsoft Edge on September 2, 2021. This article lists updates we made to Progressive Web Apps (PWAs) from both a developer and consumer point of view.

### Measure usage of your Store-installed PWA

Microsoft Edge now includes a referrer header with the request for the first navigation of your Microsoft Store-installed PWA.

This feature was first introduced in Microsoft Edge version 91, and we shipped a bug fix in Microsoft Edge version 93.

Learn more in [Publish your Progressive Web App to the Microsoft Store][StoreandPWAs].

### Window Controls Overlay origin trials

To have more control over the title bar area that's currently displayed in standalone display mode, you may want to experiment with Window Controls Overlay. Window Controls Overlay (WCO) is a set of features that work together to provide just the essential controls needed for the app window. This layout frees up more space for the web content layer. WCO is available for installed desktop PWAs.

Learn more about experimenting with Window Controls Overlay at [Experimental features in Progressive Web Apps (PWAs)][ExpWCO].

Register your origin for the **Web App Window Controls Overlay** trial at our [Origin Trials Developer Console][WCOOT].

### URL Handlers origin trial

Developers can now use the experimental feature Web App URL Handlers in origin trial. This feature allows the registration of an installed PWA to open links from other apps that refer to its scope.

Learn more about experimenting with URL handlers at [Experimental features in Progressive Web Apps (PWAs)][ExpURLHandler].

Register your domain for the **Web App URL Handlers** trial at our [Origin Trials Developer Console][URLHandlerOT].

### Support for the Share API on macOS

We have implemented support for the `navigator.share` API for macOS. The feature is rolling out to stable Microsoft Edge browsers on macOS over the coming weeks.

Learn more about the [navigator.share() API][mdnShareAPI].


<!-- ====================================================================== -->
## What's New in Microsoft Edge 92

Microsoft Edge version 92 became the stable channel of Microsoft Edge on July 22, 2021. This article lists updates we made to Progressive Web Apps (PWAs) from both a developer and consumer point of view.

### Protocol handlers origin trial

You can now register your PWA to handle specific protocols with the host operating system. The Windows trial for protocol handlers is now available. You can register your origin for the **Web App Protocol Handler** trial at the [origin trial signup page][MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration].

Learn more about using protocol handlers with your PWA at [Experimental features in Progressive Web Apps (PWAs)][ExpProtocolHandlers].

### Streamlined App Info menu

When a user selects the ellipses (**...**) button in the app's title bar, the **App info** menu is displayed.  We've updated the **App info** menu and streamlined the user experience in the following ways, to provide a user experience that's more like a desktop app than a browser UI:
*  Moved the app **Publisher** information to the top level and made it the first thing a user sees.

   :::image type="complex" source="media/app-info.png" alt-text="The new, streamlined App Info menu" lightbox="media/app-info.png":::
      The new, streamlined **App info** menu
   :::image-end:::

*  Moved the privacy information and controls into a dedicated 2nd-level **Privacy** menu.

   :::image type="complex" source="media/privacy-menu.png" alt-text="Privacy controls in the dedicated Privacy menu" lightbox="media/privacy-menu.png":::
      Privacy controls in the dedicated **Privacy** menu
   :::image-end:::

*  Moved content-related tools into a dedicated 2nd-level **More tools** menu.

   :::image type="complex" source="media/more-tools.png" alt-text="Content-related tools are now found in the More Tools menu" lightbox="media/more-tools.png":::
      Content-related tools are now found in the **More tools** menu
   :::image-end:::

### Post-install flyout dialog box

After a PWA is installed from the Microsoft Edge browser on Windows, users can now select from four options to easily launch their apps:
*  **Pin to taskbar**
*  **Pin to Start**
*  **Create Desktop shortcut**
*  **Auto-start on device login**

For convenience, this flyout dialog box is shown the first time the app is launched.

:::image type="complex" source="media/postInstallFlyout.png" alt-text="The post-install flyout dialog box with options for Pin to taskbar, Pin to Start, Create Desktop shortcut, and Auto-start on device login" lightbox="media/postInstallFlyout.png":::
   The post-install flyout dialog box with options for **Pin to taskbar**, **Pin to Start**, **Create Desktop shortcut**, and **Auto-start on device login**
:::image-end:::

This feature is being rolled out gradually to all users. In the meantime, if you'd like to use this feature, navigate to `edge://flags` and enable the flag **Web Apps Post Install Dialog**.

### Restore Web Apps

Installed sites and PWAs that were running before an unexpected shutdown will now restore (that is, they will be restarted) when the system recovers.

An unexpected shutdown can occur due to process failure, system restart, or power outage. Before this change, installed sites and PWAs had indeterminate behavior upon system restore.


<!-- ====================================================================== -->
<!-- links -->
[StoreandPWAs]: ../microsoft-store.md#measure-usage-of-your-store-installed-pwa "Measure usage of your Store-installed PWA - Publish your Progressive Web App to the Microsoft Store"

[ExpWCO]: ../experimental-features/index.md#window-controls-overlay-for-installed-desktop-web-apps "Window Controls Overlay for installed desktop web apps - Experimental Features"

[ExpProtocolHandlers]: ../experimental-features/index.md#uri-protocol-handling "URI Protocol Handling - Experimental Features"

[ExpURLHandler]: ../experimental-features/index.md#url-link-handling "URL Link Handling - Experimental Features"

<!-- external links -->
<!-- origin trials -->
[MicrosoftDeveloperMicrosoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Origin Trials | Microsoft Edge Developer"

[MicrosoftDeveloperMicrosoftEdgeOriginTrialsWebAppProtocolHandlerRegistrationRegistration]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-protocol-handler-registration/registration "Register for Web App Protocol Handler origin trial | Microsoft Developer"

[URLHandlerOT]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-url-handlers/registration/ "Register for Web App URL Handler origin trial | Microsoft Edge Developer"

[WCOOT]: https://developer.microsoft.com/microsoft-edge/origin-trials/web-app-window-controls-overlay/registration/ "Register for Web App Window Controls Overlay origin trial | Microsoft Edge Developer"

<!-- other -->
[mdnShareAPI]: https://developer.mozilla.org/docs/Web/API/Navigator/share "navigator.share() method of the Web Share API | MDN"

[4weekReleaseBlog]: https://blogs.windows.com/msedgedev/2021/03/12/new-release-cycles-microsoft-edge-extended-stable/ "Serving our customers more effectively with new release cycles for Microsoft Edge | Microsoft Edge Blog"

[Chromium4weekM]: https://blog.chromium.org/2021/03/speeding-up-release-cycle.html "Speeding up Chrome's release cycle | Chromium Blog"

<!--[ArchiveMicrosoftEdgeLegacyDeveloperPWAsIndexRequirements]: /archive/microsoft-edge/legacy/developer/progressive-web-apps/index#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->

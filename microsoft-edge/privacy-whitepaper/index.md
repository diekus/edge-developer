---
description: Microsoft Edge Privacy Whitepaper
title: Microsoft Edge Privacy Whitepaper
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, privacy, whitepaper, trust
ms.localizationpriority: high
no-loc: [Cast, Google Cast]
---
# Microsoft Edge Privacy Whitepaper

Our browser privacy promise is to provide you with the protection, transparency, control, and respect you deserve.  To uphold commitments to give you transparency into Microsoft products, the Microsoft Edge team provided a privacy whitepaper that explains how Microsoft Edge features and services work and how each may affect your privacy.  The goal of the Microsoft Edge team is to give you a full understanding into how your data is used, how to control the different features, and how to manage your collected data, so you have the info you need to make the right privacy decisions for you.

In certain sections of the paper, the Microsoft Team provides steps to go to Microsoft Edge settings and other pages.  For consistency, the Microsoft Edge team used a shortened format throughout the whitepaper:  You should see URLs that begin with `edge://` such as `edge://favorites` or `edge://settings/privacy`.  To go to the pages, type the bolded text directly into the Microsoft Edge address bar.  The pages are only viewable in Microsoft Edge.

The whitepaper focuses on the desktop version of Microsoft Edge, and parts of the paper may include features or experiences that are not available for all users.  In addition, the whitepaper discusses features and services that exist in the product today, but may be subject to change in the future.  Microsoft practices data collection minimization, which means your data is kept for the minimum amount of time, but retention times may vary depending on the feature or service being used and may change over time.

## Address bar and suggestions

The address bar allows you to enter website URLs and search the web.  By default, the address bar provides search and site suggestions using the characters you type.  You should see suggestions from your favorites, browsing history, previous searches, and default search provider.

:::image type="complex" source="./media/address-bar.png" alt-text="Address bar" lightbox="./media/address-bar.png":::
   Address bar
:::image-end:::

To make browsing and searching faster, as you type in the address bar, the typed characters are sent to your default search provider for the search provider to send back suggested search queries.  The address bar categorizes your entry as a URL, search, or unknown.  The information, along with which suggestion you select, position of selection, and other address bar data is sent to your default search provider.  If your search provider is Bing, a resettable identifier unique to your browser is sent with the data to understand the search query and query session.  Other autosuggest service identifiers are sent to your default search engine to complete the search suggestions.  Your IP address and cookies are sent to your default search provider to increase the relevance of the search results.  A signal is sent to your default search provider when you select the address bar to signal to the provider to get ready to provide suggestions.  The typed characters and search queries are not sent to Microsoft unless your search provider is Bing.  To enable sending data to your default search provider, navigate to `edge://settings/privacy` and under **Services** select **Address bar** and turn on the **Show me search and site suggestions using my typed characters** setting.  If you turn off the setting, your typed characters are no longer sent to your default search provider.  Your search queries are still sent to your default search provider to provide search results.  If Microsoft Edge detects typing in the address bar that may contain sensitive information, such as authentication credentials, local file names, or URL data that is normally encrypted, it does not send the typed text.  If you want Microsoft Edge to collect diagnostic data about the address bar including the number of offered queries for all search providers, navigate to `edge://settings/privacy` and under **Personalize your web experience** turn on the **Improve your web experience by allowing Microsoft to use your browsing history from this account for personalizing advertising, search, news, and other Microsoft services** setting.

Typed characters and the websites you visit are stored locally on the device per profile.  To delete the data, navigate to `edge://settings/clearBrowserData` and on the **Clear browsing data** window  select **Browsing history** checkbox and select **Clear now** button.  If Bing is your default search provider and you are signed into Bing, you may delete your searches through the [Microsoft Privacy dashboard][MicrosoftAccountPrivacy].  To clear your browsing history and delete websites from appearing as suggestions in the address bar, navigate to `edge://history` and select **Clear browsing data**.  To clear the data Microsoft collects from the address bar and search suggestions features on Windows 10, open **Start** > **Settings** > **Privacy** > **Diagnostics & feedback** and under **Delete diagnostic data** select **Delete**.  All other data is deleted after 36 months.

If you are signed into Microsoft Edge with a Microsoft work or school account, and Microsoft Search is available, an anonymous token representing your account is sent with the query to provide account-specific functionality, such as results specific to your company.

All data is transmitted securely over HTTPS.  If [Bing][BingMain] is your default search provider, the searches and typed characters are saved for up to six months.

If you search for a single word in the address box, Microsoft Edge may send the single word to your DNS server to see whether it corresponds to a host on your network, and may try to connect to the corresponding host.  The option allows you to navigate to the specific host instead of searching.  For example, if your router uses the hostname `router` and you type `router` in the address bar, you are provided the option to navigate to `https://router`, as well as to search for the word `router` with your default search provider.  The feature is not controlled by the **Show me search and site suggestions using my typed characters** setting since it does not involve sending data to your default search engine.

Another way to enable \(or disable\) sending data to your default search provider, navigate to `edge://settings/search` and turn on \(or off\) the **Show me search and site suggestions using my typed characters** setting.  To change your default search engine, navigate to `edge://settings/search` and select the **Search engine used in the address bar** drop-down menu.  If you are browsing while using InPrivate or Guest mode, your autosuggestions are turned off.  InPrivate shows suggestions from your local browsing, such as browsing history or past searches, but no typed characters are sent to your default search engine.  Guest mode does not display any suggestions or send typed characters to your default search engine.

Data collected by other search providers follow the privacy policy of the company.

## Autofill

Autofill in Microsoft Edge helps you be more productive by letting you save passwords, payment information, addresses, and other form entry data, for example birthdays.  When you visit a site and start to fill out a form, Microsoft Edge uses form fill info to match your saved autofill data to the form.  Microsoft Edge offers form entry data you previously saved when you encounter similar forms.  Passwords and credit card info are only saved with your explicit permission for each password and card.

Addresses and other form entries are saved by default.  To disable saving and autofill of address and other form data, navigate to `edge://settings/addresses` and turn off the **Save and fill addresses** setting.

To prevent Microsoft Edge from prompting you to save passwords, navigate to `edge://settings/passwords` and turn off the **Offer to save passwords** setting.  If you do not want Microsoft Edge to autofill existing saved passwords and want to delete your saved passwords, navigate to `edge://settings/passwords` and select **Saved passwords**.  To delete all autofill data, navigate to `edge://settings/clearBrowserData`, select **Autofill form data**, select the desired time range, and then select **Clear now**.

If you have turned on sync for your profile, your autofill data is synced across all versions of Microsoft Edge where you are signed in with the same credentials.  When sync is turned on, all autofill data is stored on encrypted Microsoft servers.  The autofill data stored on Microsoft servers is used only for sync purposes.  To turn off syncing of your autofill data, navigate to `edge://settings/profiles/sync` and next to your Profile select the **Turn off sync** button.  If you turned on sync for autofill, deleting autofill data from a device while you are signed into Microsoft Edge removes the autofill data from all other devices that you are signed in the same account.

When you visit a webpage and submit a form, Microsoft Edge sends info about the form, such as a hash of the hostname and autofill entry types \(for example, box 1 is looking for an email address, box 2 is looking for a password, and so on\), to the Microsoft form fill service.  No user-entered info or user identifiers are sent to the service.  The info helps Microsoft Edge correctly identify forms across different webpages.  The data is used to help match your saved autofill data to the form.

When you use Guest mode, autofill is not available and new autofill entries are not added.  When you browse InPrivate, Microsoft Edge offers autofill entries, but new autofill entries are not added.

## Cast

Cast in Microsoft Edge allows you to display your media to another screen using Google Cast.  To access the Cast feature, open **Settings and more (...)** > **More tools** and select **Cast media to device**.  Cast relies on the Media Router extension that is not included in Microsoft Edge by default.  When you first use Cast, Microsoft Edge prompts for permission to install the Media Router extension.

Select **restart** to install the Media Router extensions from the Chrome Web Store.  To keep the Media Router extension up to date, on startup of Microsoft Edge and at regular intervals, Microsoft Edge send update requests to the Chrome Web Store that include basic data about your version of Microsoft Edge.  Google may collect some data associated with the Media Router extension.  To uninstall the Media Router extension, navigate to `edge://flags` and disable the **Edge-On-Demand-Media-Router**.  This also stops the updates from the Chrome Web Store.  The extension is hidden and does not appear on the **Installed extensions** list.  For the **Installed extensions** list, navigate to `edge://extensions`.

## Collections

You may collect sites, text and images on the web, and organize the content with Collections in Microsoft Edge.  All collections data is stored locally on the device and organized per Microsoft Edge profile.  If you have sync turned on for Collections, your collections created, including any notes or comments, are available across all signed-in and syncing versions of Microsoft Edge.

Every 24 hours Microsoft Edge downloads a list of supported sites for which special entity extraction templates exist.  The templates are specific to each website.  When you create a new item in your collection, Microsoft Edge verifies that the site from which you are creating the new collection item is on the list of supported sites.  If the site is on the list, Microsoft Edge pings the entity extraction service for the template of the specific site.  No user identifiers are associated with the request to the service.  The template attempts to identify the name, price, ratings, primary image, and other data about the item being collected.  If the site from which you are creating a new collection item is not on the supported list site, Microsoft Edge does not download a template.  The templates enable the creation of all collection items locally on the device.  No data about the collection items are sent to the service to create the collection.

To delete the templates stored on the device and clear the cache data, navigate to `edge://settings/privacy` and under **Clear browsing data** next to **Clear browsing data now** select the **Choose what to clear** button, select the desired time range and type of data, then select the **Clear now** button.  Another way to delete cached data, navigate to `edge://settings/clearBrowserData` select the desired time range and type of data, then select the **Clear now** button.

To If you turn on the **Show suggestions from Pinterest in Collections** setting, if you want to see Collections performs a Microsoft Bing search using the title of your collection to find relevant Pinterest Topic pages.  Microsoft Edge does not send data about your collections to Pinterest.  To remove the suggestions and stop searches for Pinterest Topic pages, navigate to `edge://settings/privacy` and turn off the **Show suggestions from Pinterest in Collections** setting.

Collections is not available when using InPrivate browsing or in Guest mode.

## Crashes

If optional diagnostic data, including crash reports, are turned on, Microsoft collects diagnostic data when Microsoft Edge crashes or encounters other reliability problems.  The diagnostic data is used to diagnose and fix reliability problems of Microsoft Edge and other Microsoft products and services.

:::image type="complex" source="./media/crashes2.png" alt-text="Crashes" lightbox="./media/crashes2.png":::
   Crashes
:::image-end:::

The diagnostic data collected is in the form of crash dumps, which contains device and software state captured at the time Microsoft Edge encountered the reliability problem.  The crash dump contains information about what was happening at the time of the reliability problem.  Information such as the website you were visiting at the time of the crash or your CPU usage may be included in the diagnostic data.  The crash diagnostic data is stored locally on the device and sent to Microsoft using an encrypted link when crash reporting is turned on.  Each crash dump contains an identifier unique to your device, a resettable identifier unique to your browser, and extra diagnostic data \(such as the URL, CPU usage, and network usage\) to help identify the problem.  The extra diagnostic data is attached to the crash dump to help diagnose the reliability problem, such as understanding how many devices are encountering the problem and the severity.

Crash dumps are sent to Microsoft and stored on secure Microsoft servers for up to 30 days and then deleted.  To request to delete the diagnostic data on Windows 10 devices, open **Start** > **Settings** > **Privacy** > **Diagnostics & feedback** and under **Delete diagnostic data** select **Delete**.  Aggregated crash information, such as a count of types of crashes occurring, are stored for reporting and product improvement purposes.

To clear the crash diagnostic data stored locally from the file system on the device, navigate to `edge://crashes` and select the **Clear all** button.

To turn off crash diagnostic data collection on Windows 10, open **Start** > **Settings** > **Privacy** and select **Diagnostics & feedback**.  For versions of Microsoft Edge on all other platforms, navigate to `edge://settings/privacy` and turn off the **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports** setting.  The diagnostic data collection feature may also be turned off for enterprises through [group policies managed by your organization][DeployedgeEnterprisePrivacySettings].

## Developer tools

Microsoft Edge Developer Tools provide tools for website debugging and testing. To access Developer Tools, open **Settings and more (...)** > **More tools** and select **Developer tools**.  When you turn on certain features in Developer Tools, Microsoft Edge requests modules from Microsoft servers and download them to your device.  The request for the modules sent is over a secure HTTPS connection and contains a non-unique identifier representing the version of Microsoft Edge being used.  Specific experiences that require the remote download include 3D View and the Elements tool Accessibility pane.  Webhint integration requires a remote module that is automatically requested when Developer Tools is opened.

## Diagnostic data

Microsoft uses diagnostic data to improve our products and services and keep our products secure, up to date, and performing as expected. Whenever we collect data, we want to make sure it's the right choice for you. Microsoft believes in and practices information collection minimization. We strive to gather only the info we need, and to store it only for as long as it's needed to improve our products and services.

Microsoft Edge collects a set of required diagnostic data that's necessary to keep the product secure, up to date, and performing properly. The required diagnostic data includes data such as device connectivity, configuration information, software setup, and inventory data. Microsoft uses this required diagnostic data to troubleshoot issues and keep Microsoft products and services reliable, secure, and operating normally. For more information about diagnostic data on managed devices, navigate to [Configure Windows diagnostic data in your organization][WindowsPrivacyConfigureDiagnosticDataOrganization] and [Microsoft Edge diagnostic data group policy](/deployedge/microsoft-edge-enterprise-privacy-settings).

:::image type="complex" source="./media/diagnostic-data2.png" alt-text="Diagnostic data" lightbox="./media/diagnostic-data2.png":::
   Diagnostic data
:::image-end:::

Additionally, you may choose to share optional diagnostic data. As you use Microsoft Edge features and services or other applications that use the Microsoft Edge web platform, Microsoft Edge sends optional diagnostic data about how you use those features and the websites you visit. With your permission, this optional diagnostic data is sent to Microsoft to improve Microsoft products and services for everyone. This data is not collected or stored with your Microsoft account.

Optional diagnostic data includes information like your feature usage, performance data, site load times, memory usage, and websites you visit. For example, if you favorite a website, optional diagnostic data includes info that the favorite button was selected and a favorite was successfully added, but not which site was set as a favorite.

Information about websites you visit in Microsoft Edge helps us understand how quickly sites load and increases the relevance of search results for all users. The data includes information about the website such as the URL of the page you visit, website metrics, title of the page, how you accessed the page, info about the content of the page, and other relevant info about the page navigation.

Diagnostic data is sent using HTTPS and stored on Microsoft servers. On Windows devices, diagnostic data is sent with an identifier unique to your device. On other devices, the diagnostic data is associated with a resettable identifier unique to your browser which is randomly generated and does not contain your personal information.

The Microsoft Edge team respects the sensitivity of diagnostic data by restricting data access or removing personally identifiable information. To reset the identifier unique to your browser on Windows 10 devices, navigate to **Start** > **Settings** > **Privacy** > **Diagnostics & feedback** and select **Delete** under **Delete diagnostic data**, or change your setting under **Diagnostic data** from **Full** to **Basic** or turn off **Optional diagnostic data**.

On other platforms, to generate a new resettable identifier \(ID\) that is unique to your browser, navigate to `edge://settings/privacy` and turn off the **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports** setting. The reset \(ID\) functionality may be different for devices managed with group policies set by your organization.

If you're using Windows 10 version 1803 (April 2018 Update) or later, to view product data shared with Microsoft in the Diagnostic Data Viewer, navigate to **Start** > **Settings** > **Privacy** > **Diagnostics & feedback** and select **Open Diagnostic Data Viewer** under **View diagnostic data**.

For other platforms or versions of Windows 10 version 1803 and earlier, navigate to `edge://data-viewer` to view diagnostic data. To view the data that's periodically sent to Microsoft since the last time the viewer was opened, navigate to `edge://data-viewer`. To see what data has been sent to Microsoft for your specific session, refresh the viewer. The data used to populate `edge://data-viewer` is stored locally on the device. To clear the data in the viewer, close the `edge://data-viewer` tab.

To help us improve Microsoft products and services, de-identified and aggregated diagnostic data is stored for up to two years. Because the diagnostic data is not collected from or stored with your Microsoft account, the diagnostic data may not be viewed or deleted from your [Microsoft privacy dashboard][MicrosoftAccountPrivacy]. To delete the diagnostic data on Windows 10, navigate to **Start** > **Settings** > **Privacy** > **Diagnostics & feedback** and select **Delete** under **Delete diagnostic data**. The delete diagnostic data functionality is only supported on Windows 10 version 1803 or later. For more information, navigate to [Diagnostics, feedback, and privacy in Windows 10][MicrosoftSupport4468236].

For Microsoft Edge on Windows 10, sending Optional diagnostic data is determined by your Windows diagnostic data setting. The setting is reflected in `edge://settings/privacy`. Change the Windows settings by going to **Start** > **Settings** > **Privacy** > **Diagnostics & feedback**. On all other platforms, to control the collection of diagnostic data, navigate to `edge://settings/privacy` and turn on or off **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports**. The setting is used for all profiles associated with the installation of Microsoft Edge on your device.  The setting is not synced across devices. The setting applies to InPrivate browsing and Guest mode. Info about websites you visit is never sent while browsing InPrivate or in Guest mode. If your device is managed with group policies set by your organization, it's reflected in `edge://settings/privacy`.

## Digital Rights Management and Media Licenses

When a website offers media content that is protected by Digital Rights Management \(DRM\), Microsoft Edge uses a secure playback pipeline to ensure the content is not copied or accessed improperly.  As part of the feature, Microsoft Edge may store DRM-related data on your device, including a unique identifier and media licenses, and may transmit the unique identifier to a media licensing server specified by the content provider.  When you use the website, Microsoft Edge retrieves the DRM info to make sure you have permission to use the content.  The data helps to validate access to the protected content and ensure a seamless media experience.

Microsoft Edge supports DRM using the Encrypted Media Extensions API \(EME API\) for HTML5 sites.  The EME API allows websites to communicate with a DRM provider called a Content Decryption Module \(CDM\).  Different DRM systems, such as Widevine by Google or PlayReady by Microsoft, may be supported by the CDM implementation of the developer.  Content providers may choose to support one or more potential DRM systems and may utilize the functionality of the EME API to decide which DRM system to use for a specific client.  For more information about EME privacy, navigate to [Encrypted Media Extensions Privacy][W3cEncryptedMediaPrivacy].

Microsoft Edge supports PlayReady DRM only on Windows 10.  PlayReady is a DRM implementation to deliver media experiences such as 4K video and Dolby Atmos audio.  Microsoft Edge uses the Windows Platform Media Foundation APIs to support PlayReady.  To validate access to protected content, Microsoft Edge utilizes the Windows 10 operating system, which uses a unique identifier \(ID\) and communicates the ID with the PlayReady service.  All EME, CDM, and browser data for PlayReady that persists on the device is stored and maintained on Microsoft Edge.  For more information about PlayReady, navigate to [Simple End to End System][PlayreadyOverviewSimpleEndSystem].

Microsoft Edge supports Widevine by Google DRM and the option is on by default.  Microsoft Edge periodically fetches updates for Widevine from Google servers.  The use of Widevine may include communications to Google.  To opt-out of using Widevine in Microsoft Edge, navigate to `edge://flags/#edge-widevine-drm` and turn off the Widevine DRM setting.  Widevine has the capability to create a unique device identifier and transmit it to Google.  For more specific information on Widevine and privacy, navigate to the Google privacy policy.

Microsoft Edge supports the Flash Access DRM by Adobe, which is used by some sites instead of HTML5.  You must give permission to allow Adobe Flash when a site requests it.  When a site uses the Flash Access DRM by Adobe, Microsoft Edge gives Adobe access to a unique device identifier.  To clear and reset any locally stored instances of the identifier, navigate to `edge://settings/privacy` and under **Clear browsing data** select **Choose what to clear**, select the checkbox for **Cookies and other site data**, and select **Clear now** to remove any stored identifiers.  To stop Adobe Flash DRM from ever being used, navigate to `edge://settings/content/flash`.

When you request access to encrypted HTML5 media like an online movie, Microsoft Edge creates a license request to decrypt the media.  The CDM being used creates the license request that contains a request ID.  The request is sent to the license server.  No part of the license request contains any personally identifiable information, and the license request is not stored on the device.

When returning the media license, a media identifier is created which is unique to the user and the site.  The ID is not shared between sites and is different for each site.  A session ID, used to identify a playback session, is sent with the media identifier to decrypt the media.  The media identifier is stored locally on the device and may be stored with the content provider.

To disable all DRM and content protections, navigate to `edge://settings/content/protectedContent` and turn off the **Allow sites to play protected content (recommended)** and **Allow identifiers for protected content (computer restart may be required)** settings.

*   Turning off the **Allow sites to play protected content** setting disables playback for CDM-based DRM systems such as PlayReady and Widevine, but not for non-CDM-based systems like Flash Access DRM.  To manage Flash site permissions, navigate to `edge://settings/content/flash`.  Turning off the setting causes media functionality to stop working properly.
*   Turning off the **Allow identifiers for protected content** setting prevents the creation of identifiers for Flash Access DRM and prevents Widevine from periodically fetching updates from Google.  Turning odd the setting may cause some media functionality on some sites to stop working properly.

## Do Not Track

To enable **Do Not Track** on Microsoft Edge, navigate to `edge://settings/privacy` and turn on the **Send "Do Not Track" requests** setting.  If you enable the **Do Not Track** feature, Microsoft Edge sends a DNT:1 HTTP header with your outgoing HTTP, HTTPS, and SPDY browsing traffic requests to websites you visit to request that each does not use trackers.  However, enabling the **Send "Do Not Track" requests** setting does not guarantee that the websites are not able to track you.  Some sites may honor the request by showing you ads not based on any previous browsing.  Microsoft Edge does not control if the request is honored or not.  To help prevent websites from tracking you, navigate to `edge://settings/privacy` and change the **Tracking prevention** setting to **Balanced** or **Strict**.

When you use Guest mode, Microsoft Edge does not send **Do Not Track** requests.  When you use InPrivate browsing, Microsoft Edge only sends **Do Not Track** requests if the **Send "Do Not Track" requests** setting is turned on for the profile you are using.

## Downloads

Microsoft Edge lets you download files safely and securely.  To choose where files are downloaded on your device, navigate to `edge://settings/downloads`.  If SmartScreen is enabled, info about your file, such as the file name and URL, are sent to SmartScreen to check the reputation of the file.  The reputation check helps you avoid accidentally downloading known malware that is known to hurt your device.  To turn on \(or off\) SmartScreen, navigate to `edge://settings/privacy` and turn on \(or off\) SmartScreen.  For more information about SmartScreen, navigate to the [SmartScreen](#smartscreen) section.

To view the history of your previous downloads, navigate to `edge://downloads`.  To clear your browsing data and delete your download history, navigate to `edge://settings/clearBrowserData`.  Deleting your download history from Microsoft Edge does not remove the files from your device.  Deleting downloaded files from your device does not remove the files from your download history.  When you use InPrivate browsing or Guest mode, the download history from the session is cleared when you close the InPrivate or Guest windows, but the files are saved on the device.

## Extensions and Microsoft Edge Add-ons

You may install extensions in Microsoft Edge to add functionality to the browser.  When you install an extension from the Microsoft Edge Add-ons website or another extension store, Microsoft collects information about the extension to help developers and Microsoft understand how the extension is used.  Microsoft Edge collects aggregated data including the number of times an extension was downloaded and information about how it is performing, such as crash data.  Microsoft shares the aggregated data with the developers of the extension.  Comments and reviews from users are public on the Add-ons website and are also shared with the developers. If you are signed into Microsoft Edge, installed extensions from the Microsoft Edge Add-ons website are associated with your account to provide extension recommendations.  The data is used in aggregate to understand the popularity of extensions.

If you want your extensions and preferences for your extensions to sync across all your signed-in syncing versions of Microsoft Edge, navigate to `edge://settings/profiles/sync` and select the **turn on sync** button.

Installing extensions is optional, and to uninstall any extension at any time, navigate to `edge://extensions`.  When an extension is installed, it specifies what user data it needs to access, and Microsoft Edge asks for your permission before installing the extension.  Always make sure an extension is credible and secure before installing it and review the privacy policy of the developer for the specific extension.

Extensions are updated using the Microsoft Edge update service.  Microsoft Edge sends a list of installed extensions to the update service to check if an update is available.  If you install an extension from the Chrome Web Store, requests are sent to the Chrome Web Store at regular intervals to check for extension updates.  The extension identifier, extension version, and info about Microsoft Edge are included in the request to look for updates.  To stop requests to the Chrome Web Store, navigate to `edge://extensions` and under **From other sources** uninstall extensions.

When importing extensions from other browsers like Google Chrome, if an extension is available in the Microsoft Edge Add-ons website, Microsoft Edge automatically installs the extension from the Microsoft Edge Add-ons website and turns it on if you previously had the extension turned on.  If the extension is not available from the Microsoft Edge Add-ons website, Microsoft Edge locally copies and installs your extension from Google Chrome without turning it on or connecting to the Chrome Web Store.  Microsoft Edge asks for your permission to turn on the extension and to allow extensions from other stores.  If you granted permission, Microsoft Edge allows installation of extensions from other stores and updates to your extensions using the Chrome Web Store.  To enable \(or disable\) the option, navigate to `edge://extensions` and turn on \(or off\) **Allow extensions from other stores** setting.

## Family safety

Microsoft offers a number of tools to help families stay connected and keep kids safer on Windows 10, Xbox, and Android devices running Microsoft Launcher.

Within a family group, there are family settings that should be enabled for children while using Microsoft Edge.  The family group organizer must enable the settings for users in the group.  The three main features offered to a family group are web filtering, activity reporting, and safe search.

Web filtering protects children in the family group from going to mature websites or websites specifically blocked by the family organizer.

Activity reporting records info about the websites children visit, as well as searches, screen time, devices used, and attempts to visit blocked sites.  The family group organizer may see the info at [family.microsoft.com][MicrosoftAccountFamilyMain].  The data is collected, encrypted in transit, sent to Microsoft and stored on secure Microsoft storage servers.  The data is collected with the child's Microsoft account so it may be properly managed.  Activity reports are stored on [family.microsoft.com][MicrosoftAccountFamilyMain] for up to 30 days and then deleted after.

Safe search adds a safe keyword to the header request to search engines.  Bing reads the safe keyword and filters search results returned to the child.  Other search engines may return filtered results due to the keyword as well.  All of the child's searches are collected and made available for the family organizer to view in activity reports or at [family.microsoft.com][MicrosoftAccountFamilyMain].  The data is collected with the child's Microsoft account so it may be properly managed.

The child's browsing data is stored on secure Microsoft servers and made available to parents for up to 30 days, then immediately deleted.  The data may be deleted at any time from the [Microsoft privacy dashboard][MicrosoftAccountPrivacy].  To clear browsing data stored locally on a device, navigate to `edge://settings/clearBrowserData`.

The child must be signed into Windows 10 with a Microsoft account, and the activity reporting setting must be turned on by the family organizer, to enable collection of the data and sharing with the family group organizer.  You do not need the child signed into Microsoft Edge for collection of the data.  If family safety features are not available on your version of Windows 10, you may update to the most recent version of Windows to get the features.

Guest mode and InPrivate browsing are disabled if web filtering or activity reporting is turned on.

The family group organizer may stop the data collection from the family safety portal.  For more information about Microsoft family safety features, navigate to [What is a Microsoft family group?][MicrosoftSupport12413]

## Geolocation

Microsoft Edge supports the [Geolocation API][W3cGeolocationApiMain], which allows websites to access your location information with your permission.  Websites may ask for your location, for example, when trying to find the closest coffee shop near you.  Microsoft Edge always asks for your permission before granting websites access to your location.  To manage the permission or to always block sites from accessing your location, navigate to `edge://settings/content/location`.

On the right side of the address bar, Microsoft Edge indicates when your location is or is not being shared.

:::image type="complex" source="./media/geolocation2.png" alt-text="Location" lightbox="./media/geolocation2.png":::
   Location
:::image-end:::

If you allow sharing of your location with a site, Microsoft Edge sends local network information such as your IP address and nearby Wi-Fi access points to the Microsoft location service.  The Microsoft service uses the information to estimate your geolocation coordinates.  The geolocation estimate is shared with the site with which you agreed to share your location.  To specify that Microsoft Edge provides the requesting site with a more precise location on Windows 10, open **Settings** > **Privacy** > **Location** and turn on the **Allow access to location on this device** and **Allow apps to access your location** settings.  If you turn off the **Allow access to location on this device** and **Allow apps to access your location** settings, Microsoft Edge provides an approximate location to the requesting site.  The information is only shared with a requesting site if you previously allowed to see your location.  For more information about Windows location settings, navigate to [Windows 10 location service and privacy][MicrosoftSupport4468240].

A new randomly generated ID is used when making requests to the Microsoft Edge location service.  Microsoft Edge location service does not store your geolocation coordinates for any period of time.

InPrivate browsing uses the location permission setting of the profile from which the InPrivate session was launched.  Guest mode always asks you for permission before granting the site your location.

## Import browser data

Microsoft Edge offers an interactive and seamless experience when you launch the browser for the first time.  As part of the experience, you have the option to import your browser data to Microsoft Edge from another browser.  During the import experience, you may either keep your imported data or delete it and start fresh.  The data includes your favorites, browsing history, autofill data, extensions, settings, and other browsing data.  Your browsing data from older versions of Microsoft Edge is automatically imported when you update to the new Microsoft Edge.  With your confirmation, Microsoft Edge imports browser data from other browsers such as Google Chrome, Mozilla Firefox, or Internet Explorer, and which browser it imports from is determined based on your most used browser as defined by your OS.  Importing your data is all completed locally on your device, stored locally, and is not sent to Microsoft unless you agree to sync your browsing data.

:::image type="complex" source="./media/migration.png" alt-text="Import" lightbox="./media/migration.png":::
   Import
:::image-end:::

When importing your extensions from a different browser such as Google Chrome, Microsoft Edge imports a local copy and asks for permission before it is turned on if the extension is not available on the Microsoft Edge Add-ons website.  The permissions for some of the extensions may have changed.  To review the extension permissions, navigate to `edge://extensions`.

To import data from another browser at any time, navigate to `edge://settings/importData`.

## Install and update

You may download and install Microsoft Edge on platforms such as Windows and macOS.  Microsoft Edge uses the updater service to keep your version of Microsoft Edge up to date and secure.

When you download and install or update Microsoft Edge, information about your device, such as your release channel, basic hardware information, update identifiers, an identifier unique to your device, and a resettable identifier unique to your browser are sent to Microsoft during the installation or update process.  The IP address of the device is sent to the updater service, but the last decimal is scrubbed for added privacy protections.  During each browsing session, a new randomly generated token is created to install updated versions of Microsoft Edge.  The token is not associated with any personal information and is only used for the installation and update process and to improve the updater service.

Microsoft Edge pings the Microsoft Edge updater service about the progress of installation and update.  If an installation or update fails and crash reporting is turned on, a log is created and sent to Microsoft.  For more information about sending crash reports to Microsoft, navigate to the [Crashes](#crashes) section.  Microsoft collects info about how you downloaded Microsoft Edge, the success of the installation, and any uninstalls to better understand the success of Microsoft Edge downloads.

Automatic updates are turned on by default for all Microsoft Edge users.  On all platforms, Microsoft Edge checks for updates on startup and periodically while running.  On macOS devices, Microsoft AutoUpdate checks for updates for Microsoft products periodically as well.  Additional controls and configurations are available for organizations.  For more information about additional controls and configurations, navigate to [Update][DeployedgeUpdatePoliciesUpdate].

## Internet Explorer mode

Microsoft Edge offers a simplified experience with the integration of Internet Explorer \(IE\).  Microsoft Edge only supports IE 11, and IE mode is only available on Windows.  The IE mode feature is available for organizations through group policies.  The administrator chooses to open certain sites in IE mode in Microsoft Edge.

:::image type="complex" source="./media/ie-mode.png" alt-text="IE mode" lightbox="./media/ie-mode.png":::
   IE mode
:::image-end:::

Microsoft Edge downloads the list of sites from a location defined by the administrator through a policy, and caches the file that determines which sites must be opened in IE mode.  Depending on your Windows or IE 11 settings, Microsoft Edge collects diagnostic data about the use of IE mode, such as which sites users go to, performance data, reliability data, and feature usage data.  On Windows 10, the diagnostic data is collected according to your Windows Diagnostic data setting.  On Windows 8.1, website info is collected if the user has opted into the Flip Ahead or Suggested Sites feature in IE.  IE mode may not follow the same data collection settings in the Microsoft Edge Privacy settings.

If your administrator turned on Enterprise Site Discovery, browsing history data is collected periodically to help administrators review the sites that users visit and ensure that any system upgrades continue to support those sites.  For more information about Enterprise Site Discovery in IE11, navigate to [Collect data using Enterprise Site Discovery][InternetExplorer11DeployGuideCollectDataEnterpriseSiteDiscovery].

Non-enterprise users on Windows devices may also access IE mode.  To turn on IE mode, navigate to `edge://settings/defaultBrowser` and select the **Allow sites to be reloaded in Internet Explorer mode** setting.  To open tabs in IE mode, open **Settings and more (...)** > **More tools** and select **Reload in Internet Explorer mode**.  After you turn on IE mode, Microsoft Edge periodically requests a list of unsupported sites from a Microsoft service.  The request is sent over HTTPS and does not contain any identifiers.

Internet Explorer browsing data is stored locally in Microsoft Edge and Internet Explorer.  To delete browsing data while browsing in IE mode, navigate to `edge://settings/privacy` and clear the data from both **Clear browsing data** and **Clear browsing data for Internet Explorer**.


## Intrusive ads

To provide a better browsing experience, Microsoft Edge offers to block advertisements from loading on sites that show intrusive or misleading ads.  When Ads Blocking is turned on, Microsoft Edge periodically downloads from Microsoft servers the most recent list of sites that show intrusive or misleading ads and stores it locally on your device.  No user identifiers are included in the download request.  If you visit a site that is on the list, Microsoft Edge blocks all ads on the site and you should see the `Ads blocked` message.  To allow ads for the site, navigate to `edge://settings/content/ads` and change the settings.  Other than downloading the list of sites with intrusive ads, the Ads Blocking feature does not send additional information to Microsoft or request additional information from Microsoft while you are browsing the web.

## Jump list

The jump list in Microsoft Edge lets you easily find your most recently closed sites by hovering on the Microsoft Edge icon in the task bar and opening a contextual menu \(right-click\).  The last three closed tabs are stored locally for each profile.  To delete sites from the jump list in Windows 10, hover on each site and open a contextual menu \(right-click\).  To clear or change the display of your recently closed tabs in the jump list, navigate to `edge://settings/privacy` and select the **Choose what to clear every time you close the browser** setting.  When using an InPrivate window, Microsoft Edge does not add closed tab information to the jump list.  When using Guest mode, the jump list is not available.  For more information about clearing your browsing data, navigate to [View and delete browser history in Microsoft Edge][MicrosoftSupport10607].

## Kids Mode

Kids Mode is a convenient browsing mode designed for kids inside Microsoft Edge.  With the kid-friendly features and safety guardrails in place, Kids Mode is a great place for children to safely explore the web.  Kids Mode includes features like custom browser themes, kid-friendly content, browsing based on an allow list, Bing SafeSearch set to strict, and a password requirement to exit.  Kids Mode doesn't require a child account or profile, therefore you are not able to sign into Kids Mode.

:::image type="complex" source="./media/kids-mode.png" alt-text="Kids Mode" lightbox="./media/kids-mode.png":::
   Kids Mode
:::image-end:::

Browsing in Kids Mode is limited to a default list of kid-friendly websites.  Upon navigation, the website is compared to a local list of allowed websites.  The websites visited in Kids Mode are not viewable on [family.microsoft.com][MicrosoftAccountFamilyMain] since the browsing in Kids Mode is not associated with any account.  Allowed website exceptions may be added through the profile in which Kids Mode was launched.  Those exceptions are synced, if sync is turned on, to the profile in which Kids Mode was launched.

To enhance the Kids Mode experience, Microsoft Edge adds a safe keyword to the header request to Microsoft Bing and Microsoft News.  The safe keyword helps filter out inappropriate search results and news.  Kids Mode sets preferences for Microsoft Edge settings such as setting tracking prevention to Strict to block most trackers on websites.  Clear browsing data on close has also been turned on which clears things like Cookies and other website data when Kids Mode closes.  To clear browsing data at any time within Kids Mode, complete the following actions.

1.  Choose **Settings** > **Privacy**.
1.  Choose **Choose what to clear**.

Kids Mode does not collect data for personalization of the news feed or other Microsoft services.  You may not change the privacy settings for Kids Mode.  Other settings like Windows Defender SmartScreen and diagnostic data are configured according to the profile in which Kids Mode was launched.  For more information about diagnostic data about how you use the browser and Windows Defender SmartScreen, navigate to the [Diagnostic Data](#diagnostic-data) and [SmartScreen](#smartscreen).

## Microsoft Edge Driver

Microsoft Edge Driver allows developers to drive the Microsoft Edge browser using the [WebDriver protocol][WebDriverProtocol].  The Microsoft Edge Driver is an executable file `msedgedriver.exe` separate from Microsoft Edge that developers call from their client code, such as a test script.  By default, Microsoft Edge Driver sends diagnostic data such as the status of the [New Session WebDriver command][WebDriverProtocolNewSession] to Microsoft.  To turn off the diagnostic data collection for Microsoft Edge Driver, set the `MSEDGEDRIVER_TELEMETRY_OPTOUT` environment variable to `1`.  For more information about Microsoft Edge Driver, navigate to [Use WebDriver to automate Microsoft Edge automation][WebDriverDoc].

## Network time

Microsoft Edge uses a Microsoft network time service to track time from an external source such as a time server.  At random intervals or when Microsoft Edge encounters an expired SSL certificate, Microsoft Edge may send requests to Microsoft to obtain the time from a trusted source.  The requests occur more frequently if Microsoft Edge detects the system clock is inaccurate.  A system clock inaccuracy happens if the user changes the time on the operating system and that conflicts with the correct time zone.  The Microsoft network time service is used to get the Coordinated Universal Time \(UTC\).  The requests contain no cookies or user identifiers, and no data is logged.

## New tab page

Microsoft Edge provides an engaging and user-centric new tab page experience with a search box powered by [Bing][BingMain], quick link tiles for the sites you visit most frequently, and relevant content from Microsoft News or Office 365.  Customize the appearance of the new tab page by selecting the customize button.  Your new tab page preferences are set for each profile and stored locally on your device, and the preferences are not synced across devices.

To enhance the load times of the new tab page, the Microsoft new tab page may be loaded in the background to make it faster. The content that is loaded might include cookies, if you allow cookies. To disable loading the Microsoft new tab page in the background, navigate to `edge://settings/newTabPage` and turn off the setting **Preload the new tab page for a faster experience**.

:::image type="complex" source="./media/n-t-p1.png" alt-text="New tab page" lightbox="./media/n-t-p1.png":::
   New tab page
:::image-end:::

### Microsoft News

To tailor content to your interactions and preferences, the new tab page in Microsoft Edge stores cookies with randomly generated identifiers on the device.  A scrubbed version of your IP address is also used to tailor the content to your general region.  TO clear the cookies that persist on your device, navigate to `edge://settings/siteData`.

To prevent ads from being personalized, navigate to [Ad settings][MicrosoftAccountPrivacyAdSettings] on the [Microsoft privacy dashboard][MicrosoftAccountPrivacy] and turn off the **See personalized ads in your browser** setting.  To turn off the quick link tiles, open **customize button** > **Custom** and turn off the **Show quick links** setting.  Microsoft Edge uses your local browsing history to personalize the quick link tiles, and you may delete or create new tiles.  The data is only stored locally on the device, per profile.

The search box on the new tab page performs a Bing search based on the search query you type.  To automatically provide search suggestions and results, Microsoft Edge shares your typed characters, search query, IP address, and search identifiers with Bing.  The search box may be configured with group policies to provide search results from Microsoft Search, returning information from your organization such as documents and intranet content.  To provide an integrated search experience, Microsoft Edge stores cookies locally on the device.

If you are signed into Microsoft Edge with your Microsoft account, you may manage your browsing activity associated with the new tab page from the [Microsoft privacy dashboard][MicrosoftAccountPrivacyAdSettings].

Microsoft Edge collects diagnostic data about how you use the new tab page, such as interactions with the search box and selections on quick link tiles.  To enable collection of diagnostic data about how you use the new tab page, navigate to `edge://settings/privacy` and turn on the **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports** setting.  The browser sends diagnostic data about how you use the Microsoft News page to Microsoft to help understand user interactions with news content and improve Microsoft products.  You may turn off Microsoft News content by selecting the customize button on the new tab page.  News data is sent to Microsoft using HTTPS and stored for up to 13 months, after which it is aggregated and made anonymous.

The new tab page also allows you to set a custom image as the background.  The image is stored locally on the device and may be deleted by removing the image or uploading a new image.  No info about the image is sent to Microsoft.

### Office 365

If you are signed into Microsoft Edge with a work or school account, your organization may turn on Office 365 as an option for page content on the new tab page.  The feature is currently available only for commercial customers, and is governed under the [Microsoft Online Services Terms (OST)][MicrosoftLicensingProductProducts].  For more information about privacy for Office 365, navigate to [Overview of privacy controls for Microsoft 365 Apps for enterprise][DeployedgePrivacyOverviewControls].

InPrivate browsing and Guest mode offer alternative new tab page experiences.

## On startup

Microsoft Edge lets you pick up your browsing where you left off by opening your last open tabs from your previous browsing session, including session cookies, remains available on startup to restore tabs from your previous session and keep you signed into sites you visited.  To enable opening your last open tabs from your previous browsing session, navigate to `edge://settings/onStartup` and turn on the **Continue where you left off** setting.  If you select the **Continue where you left off** setting and clear browsing data each time you close the browser, the data you specified is deleted but the URL persists for the next session.

You may also set Microsoft Edge to open specific pages on startup.  The pages you specify are stored locally on your device and are profile-specific.  If you turned on sync for Settings, the specified pages are synced across all versions of Microsoft Edge where you are signed-in.  To enable syncing your settings, navigate to `edge://settings/profiles/sync` and turn on the **Settings** setting.

InPrivate and Guest mode tabs are not restored on startup.

## Password Monitor
Microsoft Edge is committed to keeping you safe on the web.  To help keep your personal information private and secure, if you are signed into Microsoft Edge, Password Monitor alerts you if your credentials have been exposed in a third-party data breach.  If Password Monitor is turned on, your saved credentials are hashed and encrypted locally on your device, sent to Microsoft servers over HTTPS, and compared against an encrypted list of known breached credentials.  Your signed-in account identifier is securely sent along with your hashed and encrypted credentials to the Password Monitor service.  If a credential is found in the list of known breached credentials, Microsoft sends an encrypted response back to your version of Microsoft Edge to warn you that your credential was detected as part of a hack or breach.  No data is stored on Microsoft servers after the check is complete.

The feature is only available for users signed into Microsoft Edge.  Microsoft Edge asks for your permission to turn on Password Monitor.  To turn Password Monitor on \(or off\), navigate to `edge://passwords`.

## Payments

Microsoft Edge helps you be more productive by letting you save your payment info to your browser profile and offering to automatically fill in payment forms with the info when you need it while browsing.  When you encounter a similar payment form, Microsoft Edge offers to fill in the form with the saved info.  Credit cards and other payment info is only saved with your explicit permission.

Microsoft Edge asks you if you want to store your payment info if payment autofill is turned on.  The info is encrypted locally on your device.  To delete saved payment information, navigate to `edge://settings/payments`.  When you delete saved payment info, the info no longer appears as an autofill suggestion.  To not save any payment information, navigate to `edge://settings/payments` and turn off the feature.

Microsoft Edge supports the PaymentRequest API by letting you pay for purchases with payment info you previously saved using autofill.  PaymentRequest API allows the merchant to request the following information: credit card number, credit card expiration, full name, billing address, email address, phone number, and shipping address.  The API tells the merchant that the user has credit card info saved but does not share any info with the merchant until you agree.  To turn off the Payments feature, navigate to `edge://settings/privacy`.

If you previously saved payment info to your Microsoft account, it is also available for autofill in the browser.  Payment info stored in your Microsoft account syncs across devices.  If you previously made any Xbox or Microsoft Store purchases, you may already have payment info saved to your Microsoft account.  During payment autofill, a card from your Microsoft account is masked and is only fully revealed after two-factor authentication.  The masking provides additional security while retrieving your payment info.

## Personalizing advertising, search, news, and other Microsoft services

If you allow personalization, the Microsoft Edge team collects and uses your Microsoft Edge browsing history to personalize experiences and advertising on [Bing][BingMain], Microsoft News, and other Microsoft services.  Personalization provides more relevant and useful search results, ads, and news content.  For example, if the Microsoft Edge team infers based on your browsing that you prefer shopping at a particular store, the ads you see may be tailored to products from the specific store.  Similarly, if you frequently look at travel blogs and read travel articles, your news feed may include more relevant news content about traveling.

The feature is only available for users with a non-child Microsoft account.  The feature is not available for users signed into Microsoft Edge with a work or school account.

Your browsing history is collected and used for personalization only if all four conditions are met:

*   The user is signed into a non-child Microsoft account.
*   The user has granted permission for the collection and use of the data for personalization.
*   The user's group policies managed by the organization \(employer, school, and so on\) allow personalization.
*   The user is not using the browser in Guest mode or InPrivate.

Your browsing history and other relevant data is transferred over HTTPS and attached to your Microsoft account info.  Your browsing history is stored on secure Microsoft servers.  You may view and delete previously shared browsing history by going to the [Microsoft privacy dashboard][MicrosoftAccountPrivacy].  Your browsing history is stored on secure Microsoft servers for up to 45 days.  After 45 days the data is deleted and not used for personalization.

You may modify your interests or opt-out of personalized ads from the [Ad settings][MicrosoftAccountPrivacyAdSettings] on the [Microsoft privacy dashboard][MicrosoftAccountPrivacy].

> [!NOTE]
> Opting out of personalized ads on the [Microsoft privacy dashboard][MicrosoftAccountPrivacy] does not turn off the collection and use of your browsing history for personalization of search results and content in your news feed.  To disable the collection and use of your Microsoft Edge browsing history for personalized search results and news, navigate to `edge://settings/privacy` and under **Personalize your web experience** turn off the **Improve your web experience by allowing Microsoft to use your browsing history from the account for personalizing advertising, search, news and other Microsoft services** setting.  If you stop sharing the data, Microsoft no longer collects and uses your browsing history to personalize ads, search results, and news. For more information about personalization in Microsoft Edge, navigate to [Microsoft Edge browsing history for personalized advertising and experiences][MicrosoftSupport4532583].

## Print

Microsoft Edge lets you print webpages, PDF files, or other content using a variety of devices and applications.  When you print to a printer, application, or PDF, Microsoft Edge sends the commands and file info to the operating system of your device.  The info is not sent to Microsoft, and all data sent to the operating system of your device for printing is deleted immediately after printing is completed or canceled.  To change your printing destination, navigate to `edge://settings/printing`.

You may also print webpages and files to a PDF using Microsoft Print to PDF, which does not send any data about the file back to Microsoft.  Any annotations made to the PDF file are saved locally to the file.

## Profiles

Profiles in Microsoft Edge allow you to separate your browsing data into independent profiles.  Data associated with one profile is separate from data associated with other profiles.  Your personal favorites and history, for example, are not synchronized with your work account if you set each up in different profiles.

However, users are able to easily switch between existing profiles in Microsoft Edge without the need for passwords.  If users have access to the same device, users may create another profile on the same version of Microsoft Edge without the permission of the current profile owner.  Removing the profile from Microsoft Edge settings permanently deletes browsing data for the specific profile stored on the device, such as browsing history, favorites, form fill data, and passwords.  Data synced to your account may still be stored in the Microsoft cloud and may be cleared from the [Microsoft privacy dashboard][MicrosoftAccountPrivacy].

Guest mode is a temporary instance of a fresh profile.  It allows you to browse on another user's device without modifying the signed-in profile.  Browsing data from Guest mode such as favorites, browsing history, passwords, and form fill data does not persist after you close all Guest mode windows.  Downloaded files are stored on the device, but the history of the downloads is deleted.  Guest mode allows you to browse the web without being signed into other sites automatically.  Microsoft Edge does not send websites any info to indicate that the user is browsing in Guest mode.  When you use Guest mode, permission to collect diagnostic data about how you use the browser and websites you visit is taken from the profile of Microsoft Edge from which the Guest mode session was launched.  All browsing data for the specific Guest mode session is cleared after all Guest windows are closed.

InPrivate browsing is a private browsing mode in which no browsing history, download history, cookies and site data, and form fill data are remembered.  Microsoft Edge saves downloaded files as well as any new favorites created while browsing InPrivate.  By default, while browsing InPrivate, Microsoft does not collect any info about websites you visit for product improvement purposes.  Your school, workplace, or internet service provider may still be able to see your browsing activity.  Browsing data for the specific InPrivate session is cleared after all InPrivate windows are closed.  When using the Windows Input Method Editor \(IME\) keyboard for typing and inking, data may be collected to improve language recognition and suggestion capabilities.  To stop inking and typing data from being collected by Microsoft while using the Windows IME keyboard in InPrivate and normal browsing windows, open **Start** > **Settings** > **Privacy** and select **Inking & typing personalization**.  For more information about InPrivate browsing, navigate to [Browse InPrivate in Microsoft Edge][MicrosoftSupport4533513].

## Read aloud

Microsoft Edge offers Read aloud, which reads the content of a webpage to the user.  To start Read aloud, hover on anywhere on the page and open the contextual menu \(right-click\) or open **Settings and more (...)** and select **Read aloud**.  Read aloud offers multiple voices that may be used to read the webpage content.  If you are using voices that are [installed on Windows 10][OfficeSupport4c83a8d8748642f78e462b0fdf753130] under the **Time & Language** section of Windows 10 Settings and want to clear the local cache for any voices you previously used, navigate to `edge://settings/clearBrowserData`.

When you start Read aloud, Microsoft Edge uses the [Web Speech API][GithubW3cIncubatorCommunityGroupSpeechApi].  Depending on the voice you select, the contents of the page are converted from text to speech using either a platform-supplied, client-side library \(for example, one specific to your operating system\) or a server-side library powered by Azure Cognitive Services.  If your content is converted to speech using a client-side library, no information is sent to Microsoft servers.  If your content is converted to speech using Azure Cognitive Services \(as indicated by the word "Online" in any of the voice names\), the text, along with a randomly generated token, is sent to Microsoft.  Once conversion is complete, the service returns the spoken text in an audio file to your device.  All data is encrypted while being transferred from your device to Microsoft and vice versa.  The text that is sent to Microsoft and the audio file that is generated are both deleted immediately after conversion occurs; no other data about your web content is stored for any period of time.

## Releasing new functionality

To improve Microsoft Edge, the Microsoft Edge team is always learning from users.  As part of the learning, some users may experience new functionality before it is made available to everyone.  To enable new functionality for randomly selected users, Microsoft Edge regularly sends required info about your operating system, channel, version, country or region, and other device configuration data to the Microsoft Edge configuration service.  The data is sent with a resettable identifier unique to your browser.  Data is transmitted to the service over HTTPS.  The data is used for receiving updates to enable new functionality, to keep Microsoft Edge up to date and performing properly, and to improve Microsoft products and services.  Additional controls and configurations are available for organizations.  For more information about additional controls and configurations for organizations, navigate to [Microsoft Edge configurations and experimentation][DeployedgeConfigurationExperiments].

As a user, you are not able to turn off the browser updates controlled or configured by your organization, but to control whether your product usage data is sent to Microsoft, navigate to `edge://settings/privacy` and under **Optional diagnostic data** change the settings.

To understand how new functionality affects Microsoft Edge and Microsoft services, Microsoft Edge sends a resettable identifier unique to your browser and a functionality tag that encodes what new functionality was enabled to Microsoft Edge and Microsoft services.  New functionality helps to build the best experiences and the best browser for everyone.  The functionality tag is not unique to your installation of Microsoft Edge and is shared across all Microsoft Edge installations that share the same set of functionality being enabled.  Microsoft Edge sends the information in HTTPS to Microsoft services.  The browser does not send the information when you browse InPrivate or in Guest mode.  To prevent the data from being sent, navigate to `edge://settings/privacy` and turn off the **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports** setting.  For more information about how to reset the identifier unique to your browser, navigate to the [Diagnostic data about how you use the browser](#diagnostic-data) section.

## Resolve navigation errors

If Microsoft Edge detects SSL connection timeouts, certificate errors, or other network issues that may be caused by a captive portal \(for example, a Wi-Fi network at a hotel or airport\), Microsoft Edge sends a request to `http://edge.microsoft.com/captiveportal/generate_204` and checks the response code.  If the request is redirected to another URL, Microsoft Edge opens the URL in a new tab, assuming that it is a sign-in page.  Requests to the captive portal detection page are a stateless service, requests are not logged, and cookies are not sent or saved.  On Windows platforms, Microsoft Edge uses a Windows captive portal service.  Otherwise, the Microsoft Edge captive portal service is used.  To turn off the service, navigate to `edge://settings/privacy` and turn off the **Use a web service to help resolve navigation errors** setting.

## Secure DNS

To navigate to a website, the browser needs to look up the network address (e.g. 93.184.216.34) for the host name (e.g. example.com) that's used in the website's URL. Secure DNS performs this lookup using a service over an HTTPS connection to the DNS service provider, thus protecting the lookups from modification or eavesdropping by attackers on the network.

By default, your current DNS service provider is used to avoid disruptions to your browsing. Not all service providers offer secure DNS. To avoid any disruption to your browsing, if the secure DNS connection fails, Microsoft Edge will fall back and perform an unencrypted DNS lookup with your current DNS service provider. Microsoft Edge allows you to use a specific secure DNS provider. If a secure DNS provider is chosen, then Microsoft Edge will not fall back to regular DNS lookup if the secure lookup fails. You can choose your secure DNS settings in `edge://setting/privacy`.

Secure DNS is off by default for managed machines that are part of an organization but it can be configured using administrative policies. InPrivate browsing uses the secure DNS setting of the profile from which the InPrivate session was launched. Guest mode will always use your current service provider.

## Shopping

Microsoft Edge helps you find coupons, rebates and better prices while shopping online.  To help you find coupons or the best price while shopping online, Microsoft Edge downloads a list of shopping domains locally to the client from the Microsoft shopping service.  When you navigate a website, or save an item to your Collections, Microsoft Edge locally determines if the website you're on is a shopping domain or product detail webpage.  If the website is identified as a shopping webpage, Microsoft Edge sends the URL with personally identifiable information removed to the Microsoft shopping service.  Microsoft also sends the product price, product image, product name, ratings, and reviews, along with information about Microsoft Edge and your operating system version to the service.  The data is sent over HTTPS with a randomly generated identifier and cookies if cookies are allowed.  The Microsoft Edge shopping feature requires sharing of cookie information with Bing.  For example, the cookies may be used for debugging, fraud detection, and analytics.  The Microsoft shopping service returns prices from other retailers, historical price trends and any available coupons for that website.

When you're applying coupons, cookies are stored on your device to correctly attribute the coupon provider.  Cookies are saved by Microsoft-trusted coupon providers only after a coupon is successfully applied on the cart.  After the coupons are applied, information about the success of the coupons is sent back to the Microsoft shopping service to help understand which coupons succeeded or failed.  Data sent to the Microsoft shopping service is sent over HTTPS with a randomly generated identifier which changes per coupon lookup. Edge partners with Bing Shopping to provide a coupons experience where coupons relevant to the user’s query are displayed. In some instances, Microsoft may receive revenue for use of the coupons, although whether a revenue share payment may be received is not factored into the ranking of coupons shown to users.

:::image type="complex" source="./media/shopping.png" alt-text="Shopping and coupons" lightbox="./media/shopping.png":::
   Shopping and coupons
:::image-end:::

If you visit a shopping domain and you are an existing Bing Rebates user, Microsoft Edge sends the domain along with cookies to the Microsoft shopping service to retrieve your Bing Rebates profile and cash back offers for the domain.  If you choose to activate cash back, Microsoft Edge sends your URL to the Microsoft shopping service to receive an affiliate URL.  Cookies may be stored on your device to correctly attribute the rebates provider.

The shopping service is turned on by default for all users.  To change the shopping setting in Microsoft Edge, complete the following actions.

1.  Navigate to `edge://settings/privacy`.
1.  Turn off the **Save time and money with Shopping in Microsoft Edge** setting.

InPrivate browsing uses the shopping setting of the profile that launched the InPrivate session.

## Sign in and Identity

Signing into Microsoft Edge provides additional features to make the browser more productive for you.  To sign you in seamlessly, when you first launch Microsoft Edge, it attempts to detect your identity from the operating system.  If Microsoft Edge detects your identity from the operating system but you do not want to remain signed into Microsoft Edge, navigate to `edge://settings/profiles` and either sign out or remove your profile.  To sign into Microsoft Edge, your identity in not detected from the operating system, navigate to `edge://settings/profiles`.

If a new identity is added to the operating system and your Microsoft Edge profile does not currently have an identity, Microsoft Edge adds the specific identity to your profile.  If you sign into Microsoft Edge with a Microsoft account or a work or school account and do not have an identity on your Windows 10 profile, the specific account is added to your Windows 10 profile unless you specifically choose to not add it to Windows 10 while signing in.

Your signed-in profile does not begin syncing your data without your explicit permission while either launching Microsoft Edge for the first time or signing into the browser.

Being signed into Microsoft Edge enables single sign-on \(you are automatically signed into certain websites such as Bing\) and other identity-powered experiences such as sync.  If you want to only sign into Microsoft Edge and not other Microsoft sites such as [Bing][BingMain], you may sign out of the specific site.  Microsoft Edge creates a sign-out cookie that tells Microsoft Edge not to sign into the specific site for future visits.  To sign into specific sites again using your user name and password or clear your cookies, navigate to `edge://settings/privacy`.  For more information about clearing browsing data, navigate to [View and delete browser history in Microsoft Edge][MicrosoftSupport10607].

To prevent any identity from being associated with Microsoft Edge, remove your Microsoft Edge profile or sign out of Microsoft Edge.  To delete all data associated with your Microsoft Edge profile from your device, you must remove your Microsoft Edge profile.  Deleting all data does not delete previously synced data associated with the identity.

Your identity in Microsoft Edge on macOS is shared between Microsoft apps.  A shared identity allows you to sign into a Microsoft app without having to separately enter your credentials if you are signed into another Microsoft app on the device.  On macOS, you are not automatically signed into Microsoft Edge based on your authentication state in another Microsoft app.  When you try to sign into Microsoft Edge, it offers to use the credentials from another Microsoft app on the device to sign into Microsoft Edge seamlessly.  Similarly, when you are signed into an account to Microsoft Edge, if you try to sign into other Microsoft apps, your Microsoft Edge credentials may be used to help you sign into the other Microsoft app on the device without requiring you to enter your credentials again.

You are not able to sign into Microsoft Edge when using Guest mode or InPrivate.

## SmartScreen

SmartScreen is designed to help you safely browse the web.  When you go to websites or download files, SmartScreen checks the reputation of the URL or file.  If SmartScreen determines that the site or file is malicious, it blocks you from going to the site or downloading the file.

:::image type="complex" source="./media/smart-screen.png" alt-text="SmartScreen" lightbox="./media/smart-screen.png":::
   SmartScreen
:::image-end:::

As you browse the web, SmartScreen categorizes websites and downloads as top traffic, dangerous, or unknown.  Top traffic is popular sites that SmartScreen has determined are trustworthy.  If you go to a site marked as dangerous, SmartScreen immediately blocks you from accessing the site.  When you go to an unknown site, SmartScreen checks the reputation to determine if you should access the site.

SmartScreen uses three types of reputation checks.  First, SmartScreen checks the URL of sites you visit against a local list to determine if the site is part of top traffic or is a known dangerous site.  When you visit a top traffic site, SmartScreen does not send the URL to the SmartScreen service.  If the URL is on the local list of dangerous sites, SmartScreen blocks it, which prevents any portion of the malicious web content from loading.  Microsoft Edge periodically downloads an updated list of top traffic and dangerous sites to the device.  The second type of URL check is an asynchronous reputation check to the SmartScreen service.  SmartScreen performs the check on all URLs that are not categorized as top traffic.  Microsoft Edge passes the URL, relevant info about the site, an identifier unique to your device, and general location information to the SmartScreen service to determine the safety of the site.  The information provided by Microsoft Edge allows the service to identify new dangerous sites and stay up to date with the latest security threats.  The results of URL checks are stored locally on the device and are automatically cleared at the end of the browser session.  All requests to the SmartScreen service are made with HTTPS encryption.

Third, SmartScreen checks downloaded files to help prevent harm to your device.  SmartScreen performs a binary file reputation check synchronously as your download completes.  Microsoft Edge sends info about the file such as the file hash, file name, download URI, and an identifier unique to your device to SmartScreen to perform the reputation check.  All SmartScreen requests are made with HTTPS encryption.  The SmartScreen service sends back the result of the check, which allows the file to either fully download or not.  The results are stored locally on the device.

The SmartScreen service stores data about the reputation checks and builds a database of known malicious URLs and files.  The data is stored on secure Microsoft servers and is used only for Microsoft security services.  The data is never used to identify or target you in any way.  Clearing your browsing cache clears all locally stored SmartScreen URL data.  Clearing your download history removes any locally stored SmartScreen data about file downloads.

SmartScreen is turned on by default for Microsoft Edge.  To disable SmartScreen, navigate to `edge://settings/privacy` and under **Security** turn off the **Microsoft Defender SmartScreen** setting.  The setting is the same for all profiles associated with the installation of Microsoft Edge on your device.  The setting is not synced across devices.  The setting applies to InPrivate browsing and Guest mode.  If your device is managed with group policies set by your organization, the setting is reflected in Microsoft Edge.  To view the setting, navigate to `edge://settings/privacy`.  For more information about SmartScreen, navigate to [SmartScreen: FAQ][MicrosoftSupport17443].

Optionally, SmartScreen checks the URLs of files you download to see if any are categorized as potentially unwanted apps.  Blocking potentially unwanted apps helps deliver more productive, performant, and delightful Windows experiences.  The setting is turned off by default and is only available on Windows 10 devices.  To enable the feature, navigate to `edge://settings/privacy` and turn on the **Block potentially unwanted apps** setting.  For more information about how potentially unwanted apps are categorized, navigate to [Potentially unwanted application (PUA)][WindowsSecurityThreatProtectionIntelligenceCriteriaPotentiallyUnwanted].  For more information about how to configure the setting, navigate to [Detect and block potentially unwanted applications][WindowsSecurityThreatProtectionWindowsDefender].

## Speech recognition

To convert your speech into text, Microsoft Edge supports the [Web Speech API][GithubW3cIncubatorCommunityGroupSpeechApi].  If a website includes a web feature that requires capture and translation of your speech to text and requests access to your microphone, Microsoft Edge sends the captured audio to a Microsoft service where it is translated into text.  The recorded audio is sent with a randomly generated token over a secure HTTPS connection to the Microsoft Azure Cognitive Services.  The recorded audio content is not stored for any purposes.  The text is sent back to your device and then sent to the website.

To turn off speech translated to text, you may deny microphone access from any site that prompts for permission.  To turn off the Microphone permission for all sites, navigate to `edge://settings/content/microphone`.

## Spellcheck

Microsoft Edge checks your spelling as you type in the browser.  The spellcheck service is completed locally on the device; Microsoft Edge does not send info about your typing to Microsoft for spellcheck.  To turn off the feature, navigate to `edge://settings/languages` and under **Check Spelling** turn off the setting for each language.

When you add a new language to Microsoft Edge, the browser downloads the dictionary for the new language to the device using HTTPS.  The dictionary is used for the built-in spellcheck service.  Deleting the language from your Microsoft Edge settings deletes the dictionary from the device.  Guest mode does not use the custom dictionary from the profile or any added languages.  To add or remove words in your local dictionary, navigate to `edge://settings/languages` and under **Check Spelling** select **Add or delete words**.

## Suggest similar sites

To help resolve URL typos in the address bar that result in a website error, Microsoft Edge may recommend a corrected URL.  When a website navigation error occurs, Microsoft Edge sends the domain of the web address to the Microsoft service to suggest a corrected URL.  Microsoft Edge does not include identifiers or tokens with the domain.  If the service finds a suggestion, it returns the suggested URL.  Microsoft stores the incorrect domain and suggested domain to help improve the service.  To help you navigate to the correct sites, the feature is turned on by default.  To turn off the feature, navigate to `edge://settings/privacy` and under the **Services** turn off the **Suggest similar sites when a website can't be found** setting.

## Sync

Signing into Microsoft Edge with a Microsoft account allows you to sync your browsing data across all your signed-in versions of Microsoft Edge.  You may sync your browsing history, favorites, settings, form fill data \(addresses and more\), passwords, extensions, open tabs and collections.  You must allow permission to turn on sync in Microsoft Edge, and each synced data type may be turned on or off individually.  Favorites includes any tabs you previously set aside in the legacy version of Microsoft Edge, which sync along with the rest of your favorites.  Deleted or modified favorites or other data from one signed-in version of Microsoft Edge sync to all other signed-in versions of Microsoft Edge where sync is turned on.  To manage sync configurations, go to `edge://settings/profiles/sync`.  Your sync settings may be managed by your organization.

:::image type="complex" source="./media/sync.png" alt-text="Image of sync setting being set to on" lightbox="./media/sync.png":::
   Sync setting is on
:::image-end:::

For sync to function, additional device connectivity and configuration data necessary to provide the sync experience, such as the name of your device, make, and model, is sent.  The data may be deleted from the [Microsoft device dashboard][MicrosoftAccountDevices].  To manage your synced favorites, navigate to `edge://favorites`.  To manage all other data types, navigate to `edge://settings/profiles`.

All synced data is encrypted in transit over HTTPS when transferred between the browser and Microsoft servers.  The synced data is also stored in an encrypted state in Microsoft servers.  Sensitive data types such as addresses and passwords are further encrypted on the device before being synced.  If you are using a work or school account, all data types are further encrypted before being synced using Microsoft Information Protection.  All other synced data types are stored until you delete the data, the account is deleted, or the account becomes inactive.  An account ID is attached to all synced data, as the ID is necessary to perform sync across multiple devices.

InPrivate and Guest mode browsing data does not sync to your Microsoft account.  However, favorites created during InPrivate sessions are synced across your signed-in versions of Microsoft Edge where sync is turned on.

## Tips and recommendations

Microsoft Edge wants to provide you with relevant tips and recommendations to get the best experience using the browser.  Microsoft Edge uses available device connectivity and configuration data to provide relevant tips and recommendations.  This data will consist of your operating system, locale, browser settings, and other device connectivity and configuration data.  This data is sent over a secure HTTPS connection with a resettable identifier unique to your browser.  For Windows 10 devices while Microsoft Edge is being set up, we honor tailored experiences in Windows.  [Learn more about tailored experiences in Windows](https://support.microsoft.com/help/4468236/diagnostics-feedback-and-privacy-in-windows-10-microsoft-privacy).

This data is not sent during InPrivate browsing or Guest mode.

## Tracking prevention

Microsoft Edge is designed to detect and block known trackers.  Users may choose from three levels of tracking prevention: Basic, Balanced, and Strict.  To protect user privacy, Balanced is selected by default.  Microsoft Edge detects trackers before any are loaded on the page by using an open-source list of known trackers.  The list is downloaded to the device periodically as the list is updated.  The number of trackers blocked and names of those trackers are stored locally on the device for statistical purposes.  To clear the data, navigate to `edge://settings/privacy/blockedTrackers`.  The detection and blocking of trackers occurs locally on the device.  To disable tracking prevention, navigate to `edge://settings/privacy`.  For more information about Tracking prevention, navigate to [Learn about tracking prevention in Microsoft Edge][MicrosoftAccount4533959].

You may turn off list updates using the following group policy, [Enable component updates in Microsoft Edge][DeployedgePoliciesComponentupdatesenabled].

:::image type="complex" source="./media/tracking-prevention.png" alt-text="Tracking prevention" lightbox="./media/tracking-prevention.png":::
   Tracking prevention
:::image-end:::

## Translate

In Microsoft Edge, you can browse the web and translate webpages into a language of your choice. Microsoft Edge uses [Microsoft Translator][MicrosoftSpeechTranslator] to translate web pages. This feature at first uses a library on your device that samples certain visible portions of a webpage to detect the original language. If the detected language is not one of your preferred languages, Microsoft Edge offers to translate the webpage to your preferred language or another language you choose. You can then translate the page by selecting **Translate**. You can auto-translate all pages in that language by choosing the **Always translate the pages from \<a language\>** checkbox.

Microsoft Edge does not translate a webpage without your permission. If you do decide to translate, Microsoft Edge sends the text of the webpage you want to translate, along with the *to* and *from* language and a service token to Microsoft Translator over a secure HTTPS connection. The service token doesn’t contain any user identifiable information. [Microsoft Translator][MicrosoftSpeechTranslator] then processes the text to remove any identifiers (such as email or phone number) and stores the text for service improvement purposes. The details of this communication are covered under [Microsoft Privacy Statement – Microsoft privacy][MicrosoftPrivacyStatement].

If you want to stop Microsoft Edge from offering to translate webpages, complete the following steps.

1. Navigate to `edge://settings/languages`.
1. Turn off the **Offer to translate pages that are not in a language you read** toggle and close the webpage.

## Web apps and Pinned sites

Microsoft Edge allows you to install web apps made by website developers and pin your favorite sites.

When you pin a site, it is added to your taskbar or dock.  The data is stored locally on your device.  For some sites, info about whether the site has been pinned is shared with the site, so the site knows not to prompt to pin.  You may manage your pinned sites from the taskbar or dock.  Pinned sites open in Microsoft Edge windows and use the same site permissions and diagnostic data settings as the specific version of Microsoft Edge.

## WebView

Microsoft Edge WebViews allow app developers to host web content in native applications on Windows 10 and Windows 7.  The applications hosting the Microsoft Edge WebView may send diagnostic data, such as how you use the Microsoft Edge web platform and sites you visit in the application, to Microsoft.  To enable the diagnostic data collection, navigate to `edge://settings/privacy` and under **Optional diagnostic data** turn on the setting.  To turn off the diagnostic data collection for Microsoft Edge on Windows 10, open **Start** > **Settings** > **Privacy** and select **Diagnostics & feedback**.  To turn off the diagnostic data collection for all other platforms, navigate to `edge://settings/privacy` in a normal browsing session and turn off the **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports** setting.  The applications hosting the Microsoft Edge WebView may collect other data that is governed by the data collection management of the developer and relevant privacy policies.

## Windows Defender Application Guard

Windows Defender Application Guard \(WDAG\) is a feature available for organizations.  When Windows Defender Application Guard is turned on, Microsoft Edge opens untrusted sites inside an isolated container to protect the resources in your organization from malicious sites or phishing attacks.  The feature is only turned on with group policies that are managed by your organization and is only available on recent versions of Windows 10.  WDAG collects product improvement diagnostic data about opening untrusted sites in the isolated container, such as how long it takes to open a new Application Guard window.

With your permission, WDAG also collects info about how you use the browser and information about sites you visit.  To turn off the diagnostic data collection for Microsoft Edge on Windows 10, open **Start** > **Settings** > **Privacy** and select **Diagnostics & feedback**.  To disable diagnostic data collection for all other platforms, navigate to `edge://settings/privacy` in a normal browsing session and turn off the **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports** setting.

## Windows Information Protection

Windows Information Protection \(WIP\) helps prevent the accidental leaking of corporate information.  It is only available for organizations through  group policies that are managed by your organization.  WIP is enabled for those sites that are identified as corporate assets.  Identify which sites are corporate assets from the management icon in the address bar.  WIP enforces features such as the prevention of copying and pasting from the browser or uploading certain files to sites outside your organization.

:::image type="complex" source="./media/w-i-p.png" alt-text="Windows Information Protection" lightbox="./media/w-i-p.png":::
   Windows Information Protection
:::image-end:::

If WIP is turned on for your version of Microsoft Edge, the browser collects event logs and sends them to your organization.  If WIP is turned on, you are not able to opt out of the data collection.  WIP is only available on releases of Windows 10 from August 2016 or later.  For more information about the event logs captured by WIP, navigate to [How to collect Windows Information Protection (WIP) audit event logs][WindowsSecurityInformationProtectionCollectAuditEventLogs].

## Thank you!

Microsoft Edge is made possible by the [Chromium][ChromiumMain] open-source project and other open-source software.  To view all of the software credits, navigate to `edge://credits`.  [Google Chrome Privacy Whitepaper][GoogleChromePrivacyWhitepaper] was used as a source for gathering related information about the Chromium open source project.

<!--Microsoft Edge is committed to protecting and respecting your privacy while giving you the transparency and control you deserve.  Reach out to [@MSEdgeDev][TwitterMsedgedev] on Twitter or submit feedback by opening **Settings and more (...)** > **Help and feedback** and selecting **Send feedback** with questions or comments.  -->


## Getting in touch with the Microsoft Edge team

The Microsoft Edge team is always listening to customers and values your feedback.  To provide feedback in Microsoft Edge, open **Settings and more** > **Help and feedback** and select **Send feedback**.  For Progressive Web Apps \(PWAs\), open **Settings and more (...)** and select **Send feedback to Microsoft**.  You must provide details about the feedback, but all other information is optional.  If an email is detected from your Microsoft Edge profile, it is pre-populated, along with the current URL of the site you are on and relevant diagnostic data.  The diagnostic data may include data about Microsoft Edge features you turned on and your usage of the browser.  A screenshot, files from your device, and recording of your browser may also be optionally included.  The optional screenshot, files, or recording you provide may include personally identifiable information.  The data is only used for diagnostic and product improvement purposes.

User feedback is securely sent to Microsoft using HTTPS and stored on secure Microsoft servers.  If you include your email address and the **Help improve Microsoft products by sending optional diagnostic data about how you use the browser, websites you visit, and crash reports** setting is turned on in your Microsoft Edge privacy settings, an identifier unique to your browser installation on your device is associated with your feedback.  If you're signed into Microsoft Edge with your Microsoft account, your feedback is associated with your account.  All diagnostic data, including diagnostic logs, recordings, and attachments, are stored for up to 30 days.  The remaining feedback data, including an optional screenshot, is stored for up to 15 months.  Make a [request][MicrosoftConcernPrivacy] to delete your feedback if you provided an email with your feedback item.


<!-- ====================================================================== -->
<!-- links -->
[DeployedgeConfigurationExperiments]: /deployedge/edge-configuration-and-experiments "Microsoft Edge configurations and experimentation | Microsoft Docs"
[DeployedgePoliciesComponentupdatesenabled]: /deployedge/microsoft-edge-policies#componentupdatesenabled "ComponentUpdatesEnabled - Microsoft Edge - Policies | Microsoft Docs"
[DeployedgeUpdatePoliciesUpdate]: /deployedge/microsoft-edge-update-policies#update "Update - Microsoft Edge - Update policies | Microsoft Docs"
[DeployedgeEnterprisePrivacySettings]: /deployedge/microsoft-edge-enterprise-privacy-settings "Configure Microsoft Edge policies to support enterprise privacy | Microsoft Docs"
[DeployedgePrivacyOverviewControls]: /deployoffice/privacy/overview-privacy-controls "Overview of privacy controls for Microsoft 365 Apps for enterprise | Microsoft Docs"

[InternetExplorer11DeployGuideCollectDataEnterpriseSiteDiscovery]: /internet-explorer/ie11-deploy-guide/collect-data-using-enterprise-site-discovery "Collect data using Enterprise Site Discovery | Microsoft Docs"

[PlayreadyOverviewSimpleEndSystem]: /playready/overview/simple-end-to-end-system "Simple End to End System | Microsoft Docs"

[WindowsPrivacyConfigureDiagnosticDataOrganization]: /windows/privacy/configure-windows-diagnostic-data-in-your-organization "Configure Windows diagnostic data in your organization | Microsoft Docs"

[WindowsSecurityInformationProtectionCollectAuditEventLogs]: /windows/security/information-protection/windows-information-protection/collect-wip-audit-event-logs "How to collect Windows Information Protection (WIP) audit event logs | Microsoft Docs"
[WindowsSecurityThreatProtectionIntelligenceCriteriaPotentiallyUnwanted]: /windows/security/threat-protection/intelligence/criteria#potentially-unwanted-application-pua "Potentially unwanted application (PUA) - How Microsoft identifies malware and potentially unwanted applications | Microsoft Docs"
[WindowsSecurityThreatProtectionWindowsDefender]: /windows/security/threat-protection/windows-defender-antivirus/detect-block-potentially-unwanted-apps-windows-defender-antivirus "Detect and block potentially unwanted applications | Microsoft Docs"

[WebDriverDoc]: /microsoft-edge/webdriver-chromium "Use WebDriver to automate Microsoft Edge | Microsoft Docs"

[BingMain]: https://bing.com "Bing"

[ChromiumMain]: https://www.chromium.org "The Chromium Projects"

[GithubW3cIncubatorCommunityGroupSpeechApi]: https://wicg.github.io/speech-api "Web Speech API Draft Report | W3C Incubator Community Group"

[GoogleChromePrivacyWhitepaper]: https://www.google.com/chrome/privacy/whitepaper.html "Google Chrome Privacy Whitepaper"

[MicrosoftAccountDevices]: https://account.microsoft.com/devices "Devices | Microsoft Account"
[MicrosoftAccountFamilyMain]: https://account.microsoft.com/family "Family | Microsoft Account"
[MicrosoftAccountPrivacy]:  https://account.microsoft.com/privacy/ "Privacy | Microsoft Account"
[MicrosoftAccountPrivacyAdSettings]: https://account.microsoft.com/privacy/ad-settings "Add settings - Privacy | Microsoft Account"

[MicrosoftConcernPrivacy]: https://www.microsoft.com/concern/privacy "Report a Privacy Concern | Microsoft"
[MicrosoftLicensingProductProducts]: https://www.microsoft.com/licensing/product-licensing/products "Licensing terms | Microsoft Volume Licensing"

[MicrosoftSupport10607]: https://support.microsoft.com/help/10607 "View and delete browser history in Microsoft Edge | Microsoft Edge support"
[MicrosoftSupport12413]: https://support.microsoft.com/help/12413 "What is a Microsoft family group? | Microsoft Account support"
[MicrosoftSupport17443]: https://support.microsoft.com/help/17443 "SmartScreen: FAQ | Microsoft Edge support"
[MicrosoftSupport4468236]: https://support.microsoft.com/help/4468236 "Diagnostics, feedback, and privacy in Windows 10 | Microsoft Privacy support"
[MicrosoftSupport4468240]: https://support.microsoft.com/help/4468240 "Windows 10 location service and privacy | Microsoft Privacy support"
[MicrosoftSupport4532583]: https://support.microsoft.com/help/4532583 "Microsoft Edge browsing history for personalized advertising and experiences | Microsoft Privacy support"
[MicrosoftSupport4533513]: https://support.microsoft.com/help/4533513 "Browse InPrivate in Microsoft Edge | Microsoft Edge support"
[MicrosoftAccount4533959]: https://support.microsoft.com/help/4533959 "Learn about tracking prevention in Microsoft Edge | Microsoft Privacy support"

[OfficeSupport4c83a8d8748642f78e462b0fdf753130]: https://support.office.com/article/4c83a8d8-7486-42f7-8e46-2b0fdf753130 "Download voices for Immersive Reader, Read Mode, and Read Aloud | Office support"

[W3cEncryptedMediaPrivacy]: https://w3.org/TR/encrypted-media#privacy "11. Privacy - Encrypted Media Extensions | W3C"
[W3cGeolocationApiMain]: https://w3.org/TR/geolocation-api "Geolocation API Specification 2nd Edition | W3C"

[WebDriverProtocol]: https://www.w3.org/TR/webdriver2/ "WebDriver | W3C Working Draft 24 August 2020"
[WebDriverProtocolNewSession]: https://www.w3.org/TR/webdriver2/#new-session "8.1 New Session | W3C Working Draft 24 August 2020"

[TwitterMsedgedev]: https://www.twitter.com/MSEdgeDev "Microsoft Edge Dev | Twitter"

[MicrosoftPrivacyStatement]: https://privacy.microsoft.com/privacystatement "Microsoft Privacy Statement – Microsoft privacy"

[MicrosoftSpeechTranslator]: https://azure.microsoft.com/services/cognitive-services/speech-translation/ "Speech Translation | Microsoft Azure"

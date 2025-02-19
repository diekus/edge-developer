---
title: Use Service Workers to manage network requests and push notifications
description: Service Workers are Web Workers that help improve performance, respond to varying network conditions, and increase connectivity with your web application.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: progressive web apps, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
---
# Use Service Workers to manage network requests and push notifications

Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.  Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.

## Registering a Service Worker

Similar to other Web Workers, Service Workers must exist in a separate file. You reference this file when registering the Service Worker, as shown in the following code snippet.

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```

Modern browsers provide different levels of support for Service Workers. As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code. In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site. Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).  In the previous code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain. If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.  As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.

## The Service Worker lifecycle

The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event. You can add listeners to these events to run code to perform an action. The following list presents a high-level view of the lifecycle and related events of service workers.

1.  Register the Service Worker.
1.  The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event. You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.

    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```

1.  The Service Worker is activated, which triggers the `activate` event.  Use this event to clean up outdated caches.

    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```

1.  The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site. If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.

    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```

1.  The Service Worker is now running.

## Using fetch in Service Workers

The main event that you use in a Service Worker is the `fetch` event.  The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker. The following code snippet shows how to add a listener to the fetch event.

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```

Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.  The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.  Here are a few examples of what you may do:

*   If available, return a response from the cache, otherwise fallback to request the resource over the network.
*   Fetch a resource from the network, cache a copy, and return the response.
*   Allow user's to specify a preference to save data.
*   Supply a placeholder image for certain image requests.
*   Generate a response directly in the Service Worker.

## Push Notifications

Service workers can push notifications to users. Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed. For more information, navigate to [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].

## See also

To learn more about Service Workers, navigate to the following list of related topics.

*   [Making PWAs work offline with Service workers][MDNPwasMakingOfflineServiceWorkers]
*   [How to make PWAs re-engageable using Notifications and Push][MDNPwasMakeReengageablesingNotificationsPush]

<!-- links -->

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Web Push Notifications |  Microsoft Edge Demos"

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Making PWAs work offline with Service workers - PWAs | MDN"
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "How to make PWAs re-engageable using Notifications and Push - PWAs | MDN"

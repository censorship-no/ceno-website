---
title: "How CENO Works"
date: 2021-03-03T14:54:43+08:00
featured_image: ""
description: ""
draft: true
---


# How does it work?

![Different ways of retrieving content over CENO](/images/ceno-access.svg "How CENO works")

When you access or *request* a web page using CENO, the application first looks at the browser request to decide whether the page seems *cacheable*, i.e. potentially safe to be saved and publicly shared with other CENO users (requests with authentication tokens, cookies or dynamic connections are not cached). Then it attempts to retrieve the page using several *mechanisms* until one of them succeeds:

  - It first attempts to retrieve the page straight from its **origin** (i.e. web server) as a normal browser would.
  - If that fails, and the page seems cacheable, the application tries to get it from the **distributed cache**, i.e. from other CENO users that may have previously accessed it.  If it succeeds, the application itself starts sharing the page with other users.
  - If retrieving a cacheable page from the distributed cache fails, the application tries to retrieve it via an **injector**, a machine sitting in the uncensored zone which provides the application with the page content.  If the injector deems the *response* amenable to do so, it also provides additional information allowing users to share the page (which the application starts doing immediately).
  - If that fails, or if the page was not cacheable, the application uses the injector as a **proxy** to access content privately.  Neither the injector nor the application share the content publicly (in fact, when accessing secure web content, the injector is not even able to see the request and response themselves).

Users can selectively disable each of these mechanisms so that they are skipped altogether.  In the CENO application menu, just select the *CENO* entry and use the checkboxes corresponding to the different mechanisms.

# Caching

Once a particular piece of content has crossed the boundary to a censored zone, it is further distributed in a BitTorrent-like fashion. This has several advantages:

* Content remains accessible even after the censor shuts down international traffic completely.
* National traffic is often cheaper in censored countries, which may lead to decreased data costs.
* Device to Device communication (currently Wi-Fi only) may suffice in retrieving content.

# On content storage and availability

As you can see, your application will only be sharing *content that you have previously accessed*, and it will do that while it is running.  Conversely, if access to a page's origin or to the injector is not possible, the page will only be available if other users who have previously accessed the same page are still running the application.  The more users actively sharing a page, the more chances for other users to get it.

Content does not stay on your device forever.  After your application has stored more than 10 gigabytes (this is not configurable for the moment), content which has not been accessed for the longest time (either by you or other users via your application) is removed to make space for new content.

If you want to remove all stored pages, you can use the standard procedures to delete the application's data in Android.  Be warned that currently *this will also remove other information* like bookmarks and browsing history, from CENO.  We may later on add a way to remove stored pages without having to delete all application data.

# Help by becoming a bridge!

As mentioned above, because random IP addresses are usually not blocked, CENO relies on users outside of censored zones to act as bridges. Therefore, we ask that people willing to help the CENO project - and most importantly, people behind internet walls - install CENO on an Android device, start it up and let it run for as long as possible.

# Threat model

When the CENO browser is started on a device, a number of internal IO processes are activated. The primary one - one that does not depend on any prior browsing - is that the app shall attempt to determine whether it can communicate with its configured injector servers. This operation is likely to fail in heavily-censored countries, but when it does NOT fail, the application becomes a bridge for others to reach injectors.

Another IO process that starts on app launch is content sharing of the distributed cache. This action depends on whether a user has used this CENO browser in the past to view public websites through the injector. If so, that particular content shall be offered through BitTorrent's DHT network to others for download.

We call the former process "acting as a bridge" and the latter "acting as a seeder". In addition, we call "acting as a user" the process of users browsing internet websites. Please check [the User Manual][user-manual-risks] for a list of risks in playing each of those roles.

[user-manual-risks]: user-manual/en/concepts/risks.md
    "Censorship.no! User Manual — Risks in using CENO/Ouinet"

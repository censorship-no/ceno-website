---
title: "Support"
date: 2021-03-03T14:54:21+08:00
featured_image: ""
description: ""
draft: true
---

# How does it work?

![Different ways of retrieving content over CENO](/images/ceno-access.svg "How CENO works")

When you access or *request* a web page using CENO, the application first looks at the browser request to decide whether the page seems *cacheable*, i.e. potentially safe to be saved and publicly shared with ot>

  - It first attempts to retrieve the page straight from its **origin** (i.e. web server) as a normal browser would.
  - If that fails, and the page seems cacheable, the application tries to get it from the **distributed cache**, i.e. from other CENO users that may have previously accessed it.  If it succeeds, the application>
  - If retrieving a cacheable page from the distributed cache fails, the application tries to retrieve it via an **injector**, a machine sitting in the uncensored zone which provides the application with the pa>
  - If that fails, or if the page was not cacheable, the application uses the injector as a **proxy** to access content privately.  Neither the injector nor the application share the content publicly (in fact, >

Users can selectively disable each of these mechanisms so that they are skipped altogether.  In the CENO application menu, just select the *CENO* entry and use the checkboxes corresponding to the different mech>

# Caching

Once a particular piece of content has crossed the boundary to a censored zone, it is further distributed in a BitTorrent-like fashion. This has several advantages:

* Content remains accessible even after the censor shuts down international traffic completely.
* National traffic is often cheaper in censored countries, which may lead to decreased data costs.
* Device to Device communication (currently Wi-Fi only) may suffice in retrieving content.

# On content storage and availability

As you can see, your application will only be sharing *content that you have previously accessed*, and it will do that while it is running.  Conversely, if access to a page's origin or to the injector is not po>

Content does not stay on your device forever.  After your application has stored more than 10 gigabytes (this is not configurable for the moment), content which has not been accessed for the longest time (eithe>

If you want to remove all stored pages, you can use the standard procedures to delete the application's data in Android.  Be warned that currently *this will also remove other information* like bookmarks and br>

# Help by becoming a bridge!

As mentioned above, because random IP addresses are usually not blocked, CENO relies on users outside of censored zones to act as bridges. Therefore, we ask that people willing to help the CENO project - and mo>

# Threat model

When the CENO browser is started on a device, a number of internal IO processes are activated. The primary one - one that does not depend on any prior browsing - is that the app shall attempt to determine wheth>

Another IO process that starts on app launch is content sharing of the distributed cache. This action depends on whether a user has used this CENO browser in the past to view public websites through the injecto>

We call the former process "acting as a bridge" and the latter "acting as a seeder". In addition, we call "acting as a user" the process of users browsing internet websites. Please check [the User Manual][user->

[user-manual-risks]: user-manual/en/concepts/risks.md
    "Censorship.no! User Manual — Risks in using CENO/Ouinet"

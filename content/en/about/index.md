---
title: "About"
date: 2021-03-03T14:53:57+08:00
featured_image: ""
description: ""
draft: true
type: page
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

# Operational Warnings
## Battery and data usage

To prolong availability of CENO bridges, the CENO browser shall continue working even when it goes to the background. We have not yet put in place functionality which would disable all networking operations when the device switches to cellular internet, nor when it is disconnected from the charger.

Until we implement this functionality, to preserve the device battery and network bandwidth, users need to explicitly disable CENO either by shutting it down from Android's list of running applications, or by tapping the "Tap to stop CENO" button from the notification area.

## CENO is not an anonymity tool

CENO users should also be aware of the fact that CENO is not a network to anonymize users such as Tor or I2P. More akin to BitTorrent, the IP addresses of users sharing particular content are visible to anyone who can understand the internal workings of the BitTorrent DHT protocol.

Information about your browsing might be leaked to other CENO users, as well as the fact that your application is providing particular web content to others. Content accessed with the application may remain in storage in clear text for some time (continue reading for more information on this).  Other security or privacy-affecting issues might exist.

## Censorship circumvention will not always work

At the moment, CENO relies on bridge nodes whose IP addesses are not banned by countries performing network censorship. We rely on people living outside the censored zone (this may be you!) running the CENO client and acting as bridges to people inside the censored zone. Currently, in the event of a complete internet blackout where no data can pass through international boundaries, CENO will cease to work.

The availability of web content (especially under censorship conditions) may vary widely depending on factors like website configuration, network capacity, and the presence, connectivity and browsing behavior of other CENO users. The behavior of the mechanisms currently used to share content between users may be erratic.

In the future we're hoping to address these problems by:

1. Letting users "import" web content by means other than the Internet into a censored zone and disseminate it via decentralized content sharing protocols.
2. Modifying the protocol to find alternative routes to relay the traffic outside of the censored country and back (if one exists).

# Screenshots

Can be found in the [images/screenshots folder](images/screenshots)

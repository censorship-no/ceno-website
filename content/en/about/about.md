---
title: "_About_ceno"
date: 2021-03-03T14:53:57+08:00
featured_image: ""
description: ""
draft: true
type: page
---
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

# Feedback

As mentioned, we're currently in a testing phase and are happy to receive positive and negative feedback as well as questions at <cenoers@equalit.ie>.

# Screenshots

Can be found in the [images/screenshots folder](images/screenshots)

# About eQualitie

![](./images/equalitie-logo.png "eQualitie logo")

[eQualitie][] develops open and reusable systems with a focus on privacy, online security, and information management.  Our goal is to create accessible technology and improve the skill set needed for defending human rights and freedoms in the digital age.

[eQualitie]: https://equalit.ie/

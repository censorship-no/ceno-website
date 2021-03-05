---
title: "Support"
date: 2021-03-03T14:54:21+08:00
featured_image: ""
description: ""
draft: true
---

# Current Status

CENO is currently in BETA release. It is being tested in countries that censor large parts of the Internet from their citizens. We offer it with the best intention that it is useful to you, but due to its highly innovative nature and stage of development, you may expect some issues while using it. We will be submitting the codebase to an independent audit in the near future and will update this entry when that work is completed.

We recommend that you use this tool in controlled environments and **only assume reasonable risks**. eQualitie and its associates decline any legal responsibility derived from the use of this software. See 'Operational Warnings' below for more information on what you need to be aware of in running the beta release.

## What currently works
  - Browse any website with normal speed when Internet access to the resource is not censored.
  - Browse any website (with slightly slower connection time) when it has been selectively censored (via DNS or IP).
  - Retrieve requested website content directly from the distributed cache and naturally browse web pages that other people have previously visited, even when the resource or any existing CENO injectors are not accessible.

When users start the CENO browser, they automatically become part of the CENO network. This means that - when possible - these devices shall act as temporary proxies (bridges) for people who cannot access desired websites due to network censorship.

Provided that there are enough CENO bridges located outside of the censored zone, and that the country has not sealed off international communication completely, CENO users are able to connect to any website and then share its contents with other peers.

## Future functionality
  - Retrieve and naturally browse content inserted off-line (like website captures) under a complete national Internet disconnection.

# How to use CENO

Please refer to the [Censorship.no! User Manual](https://censorship.no/user-manual/en/) for detailed instructions.

## As a user

Using CENO is as easy as downloading the application on an Android device and using it to browse websites as one would with any other mainstream browser.

One caveat at the moment: when accessing dynamic websites such as Twitter, Facebook or Gmail, one has to open an incognito tab in the CENO browser. This is because the non-incognito tab strips down all private data from HTTP requests to ensure they don't get leaked into the distributed cache.

On the other hand, the incognito tab leaves private data (e.g. passwords) intact but the connection stays encrypted - thus only the destination server can see the details of the HTTP transaction (making caching impossible).

## As a bridge

Bridges help route HTTP exchanges to and from censored zones. To become a bridge is again as easy as installing the CENO browser on an Android device and leaving it running for as long as possible. Make sure that your local wifi network supports UPnP.

---
title: "How CENO Browser Works"
date: 2021-03-03T14:54:43+08:00
featured_image: ""
draft: true
type: page
---

Designed for accessing websites in challenging network environments, [censorship.no](https://github.com/censorship-no) (CENO) is a mobile web browser that allows you to browse the Web without restriction, circumventing any network filtering. The underlying architecture offers peer-to-peer routing and distributed caching, using 'darknet' infrastructure to avoid network censorship and bring the Web to your browser.

The CENO project presents a new generation of censorship circumvention possibilities. Our project is built in support of Articles 18, 19 and 20 of the [Universal Declaration of Human Rights](http://www.un.org/en/universal-declaration-human-rights/).

![CENO2 infographic](/images/ceno_infographic.png)

# The CENO Advantage
The majority of internationally-bound traffic in countries that filter content requests are routed through a fixed number of centralized exchanges where surveillance and censorship technology is installed. Traditional circumvention technologies require the user to connect directly to a proxy in the uncensored zone. This design gives the censor an advantage in locating and blocking popular proxies, VPN servers, relays, bridges, etc.

CENO proposes a fundamentally different solution: reduce the requests to externally available proxy servers and enable the storage of retrieved content inside the censored zone. CENOs advantage comes from being both a transport and a storage solution.

Peer-to-peer routing is the ideal solution for the “cat and mouse” scenario that most circumvention providers end up playing with the censor. Clients need not know the location of a proxy to relay censored content, instead using small-world networks to connect to their peers, and thereafter to a bridge in the uncensored zone.

Once a website is accessed by a single user (node), it is stored and continues to propagate inside the country peer-to-peer. Individual nodes are referenced by an identifier which does not give away their physical location. Content remains available inside the censored zone even if external connectivity is cut. Content can be seeded into the network via alternative means as well (e.g. uploaded from a USB drive).

# Learn More:
For a user-level introduction to CENO and Ouinet, the concepts they rely upon, and how to use them, please refer to the [Censorship.no! User Manual][].

[Censorship.no! User Manual]: https://censorship.no/user-manual/en/

For a technical-level, full specification of the Ouinet network, its components and protocols, please refer to the [Ouinet white paper][].

[Ouinet white paper]: https://github.com/equalitie/ouinet/blob/master/doc/ouinet-network-whitepaper.md

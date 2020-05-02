---
template: post
title: Immutable Links in IPFS - IPNS vs DNSLink VS ENS
slug: immutable-ipfs
draft: false
date: 2020-05-04T04:02:37.816Z
description: >-
    How can immutable links be generated for IPFS? What is IPNS, DNS Link and ENS?
category: "General"
socialImage: ./media/FleekOnFleek/socialImage.png
tags:
  - General
  - Informational
---

![](./media/FleekOnFleek/socialImage.png)

We tend to take immutability for granted when navigating the web. For example, if I invited you to visit Fleek's homepage, I'd give you the following link: <https://fleek.co>. This link never changes, that is why I can share it with you.

In this article, we will explain how immutable links, such as the one above, are achieved in IPFS.

# Mutable vs Immutable Links
![](./media/ImmutableLinks/house.jpg)
*Immutable links are like the address of a house*

Content in IPFS is addressed by its content in the form of a hash. This is of great importance for the hosting of IPFS site. 

For example, here is a current hash of the Fleek homepage: `QmZQV5YXKakh7aKqSk3MVARNu8eaxws9KNc6EeStQTYt5w`.

What would happen if we made an update, such as fixing a typo or adding more content? The hash would be totally different!

For example, it could become: `QmRW3V9znzFW9M5FYbitSEvd5dQrPWGvPvgQD6LM22Tv8e`.

If I wanted to share the Fleek homepage with you, it would be impossible to point you to a single link because the hash would change anytime I updated the site. That is because we want an *immutable* link to share my site, even though the website itself is *mutable*.


This mutable vs immutable distinction is comparable to a real-life address and a house. If I wanted to invite you to a party at my house, I would share to you an *immutable link* in the form of the address of the house. However, the content of the house is *mutable*, because we do not know which guest has arrived yet!

So how to we create immutable link to content hosted on IPFS, if a new hash is created everytime an update occurs?

There are three main solutions to this problem.

## 1. IPNS: Immutable Hashes
IPNS links use public-key crytography to produce a hash that links to an IPFS hash.
They can look just like IPFS hashes: `QmSrPmbaUKA3ZodhzPWZnpFgcPMFWF4QsxXbkWfEptTBJd`.

They are hashes of a public key. The owner of that public key can sign a piece of information containing the IPNS hash linking to the most recent version of a website.

That means that if I shared the IPNS hash, I could direct users to same website and it would still allow me to make updates.

The drawback with this solution, however, is that IPNS hashes are not human-readable. 

That's where the second solution comes in.

## 2. DNSLink: Linking DNS and IPFS
DnsLink acts as a sort of bridge between a traditional domain name and the IPFS ecosystem. 

Simply put, it stores a link to an IPFS hash in the DNS records of a domain.

IPFS searches for a DNSLink when a provided IPNS hash is not a valid hash or simply not found. In that case, IPFS will search for the DNS record associated with the domain to see if it contains a DNSLink record.

This is a solution Fleek uses profusely. For example, here's the fleek.co through the DNSLink <https://ipfs.io/ipns/fleek.co/>

This solution, however, relies on centralised DNS servers so it does not fully realize the vision of a fully decentralised web intended by IPFS.

That's where the last solution comes in.

## 3. ENS: The Blockchain Solution
We had IPNS, which was decentralised, but not human-readable.
We had DNSLink, which was human-readable, but not fully decentralised.

ENS is both decentralised AND human-readable.

That's because ENS, short for Ethereum Name Service, is a dentralised name record living on the Ethereum blockchain, the most popular smart contract platform. There we can associate a human-readable link to an IPFS hash.

These domains look just like normal domains, except that they end in `.eth` instead of `.com`.

ENS domains are very cool, but also very new.
In order to access such sites, you will need a browser such as Brave or the Metamask Extension.

Of couse, at Fleek, we fully support ENS for ultimate decentralisation!

Here's our site on ENS: [fleekhq.eth/](https://fleekhq.eth/)!

# Set a Site on Fleek!
Fleek harnesses all theses technologies in an easy-to-use manner.
Host your site on Fleek and join the new decentralised web!

* [Sign up](https://app.fleek.co) to try for yourself
* [Join](https://join.slack.com/t/fleek-public/shared_invite/zt-bxna7y1d-PbVdut4rgHt5jM6Zjg9g9A) our Community Chat
* [Follow](https://twitter.com/FleekHQ) us on Twitter
* [Read](https://docs.fleek.co/) out our Tech Docs
* Contact us at support@fleek.co 
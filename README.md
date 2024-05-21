# mta-sts

MTA-STS policy configuration hosted on [GitHub Pages](https://pages.github.com/).

## Why

We care about cybersecurity: if we expect people to trust us with confidential information, we need to ensure we're handling this securely - and not causing harm while we try to do good in the world.

We expect attacks involving emails to us ("inbound email") to be the most likely way we suffer a serious cybersecurity breach, based on an internal review of our processes and systems.

## What

MTA-STS helps ensure inbound emails are encrypted: this prevents them being intercepted on their way to us. It's a standard defined by [RFC 8461](https://datatracker.ietf.org/doc/html/rfc8461) and recommended by the UK's [National Cyber Security Centre](https://www.ncsc.gov.uk/collection/email-security-and-anti-spoofing/using-mta-sts-to-protect-the-privacy-of-your-emails).

The standard involves hosting a file [`.well-known/mta-sts.txt`](./.well-known/mta-sts.txt) that states we always want inbound email to be encrypted.

**This repository specifically just hosts this file.** It does so with GitHub Pages, which allows us to easily host static files that match the structure of this repository. Because GitHub Pages will serve everything, you can actually also [find this file being served](https://mta-sts.bluedot.org/).

The standard also involves setting up various DNS records, which we do in [Porkbun](https://porkbun.com/) manually at the moment.


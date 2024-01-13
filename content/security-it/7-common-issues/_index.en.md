---
title: "Common Issues"
date: 2024-01-13T12:00:00+05:00
lastmod: 2024-01-13T12:00:00+05:00
weight: 7
draft: false
# search related keywords
keywords: [""]
---

### Multiple Devices & Platform Authenticators

Choosing an approach based entirely on platform authenticators can make using multiple devices harder.

As a user's second factor is tied to the device they registered with, you'll find extra operational toil when users get a new phone or computer.

{{< notice tip >}}
Create a standard process for users to gain access via push notification 2FA whilst registering a new platform authenticator. Automate revoking the ability to authenticate with anything other than WebAuthn
{{</ notice >}}

### Embedded Browsers & Mobile Apps

As WebAuthn is a an API implemented in browsers, apps which use "embedded" browsers as part of their authentication can sometimes not support WebAuthn. Sometimes WebAuthn support can vary between desktop browser & mobile apps for this reason.

When this happens, you'll generally see a response in the sign in window similar to, "the operation is not supported".

{{< notice tip >}}
Pre-create an authentication policy that can be applied to apps that don't support WebAuthn. A slow rollout, with fallback options, should allow you to spot & handle these cases before fully cutting over
{{</ notice >}}

### Refusal to Carry a Cross Platform Authenticator

Some users will refuse to carry their security key, despite the small size & weight. This is fine, just have them register their device as a platform authenticator.

{{< notice info >}}
Your flexibility to allow any kind of WebAuthn authenticator is what will allow you to effectively ban all other kinds of 2FA
{{</ notice >}}

### Resistance to Platform Authenticators

Some users will be cautious about registering their personal devices as platform authenticators for fear of device monitoring, sometimes they will also be the same people who refuse to carry a security key!

{{< notice tip >}}
Educating security teams & your users is critical for a successful rollout. Be sure to separate any discussions about WebAuthn from those about employee tracking, device monitoring or mobile device management. Those technologies have their appropriate time & place, but WebAuthn is nothing to do with them.
{{</ notice >}}
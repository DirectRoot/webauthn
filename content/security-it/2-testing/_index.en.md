---
title: "Testing"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
weight: 2
draft: false
# search related keywords
keywords: [""]
---

### Understand Your Environment

Before you start testing WebAuthn, it's first important to understand the combination of devices and workflows in your environment.

Any modern IdP will log device type, operating system and hopefully browser during authentication. If you don't already have this data in a system for analysis like Splunk or Elastic, now would be a great time to add it!

Use this data to determine the vital combinations of device and application that people use to get work done. Pay attention to; number of sign-ins per app, per device; average sign-ins per day, per app, per device; weekly, monthly or yearly trends of how sign-in patterns change.

{{< notice tip >}}
Whatever the data tells you, test a wide array of devices & apps. Use the most vital combinations of device & app to focus your testing and documentation.
{{</ notice >}}

### Select Your Authenticators

Sign-in patterns should also determine what style and/or brand of authenticators to test.

If you're looking at 200-300 users all with the same hardware and Google Chrome, then maybe you don't need to buy Yubikeys.

If you've got fewer users, but a much more varied landscape of devices & browsers, then cross-platform authenticators have more value (especially if users have multiple devices).

See [Name Your Price](/leaders/5-name-your-price/) for guidelines on authenticators relating to company size.

{{< notice tip >}}
Consider both the organization's size & sign-in habits when selecting authenticators to test.
{{</ notice >}}

### Start Testing

By yourself, or in a small team, methodically test combinations of device, browser & authenticator in the registration and authentication flow for a single app.

Use a sandbox IdP to help you understand how different settings in your IdP affect the ability to use the different authenticators. Experiment with "user verification" options, if they're available.

{{< notice info >}}
It's acceptable for user verification to be set as "optional" because the user's password will act as a verification step beforehand. If set to "required", any authenticator will need to verify the user through a device password, biometric or pin before it can be used.
{{</ notice >}}

{{< notice warning >}}
Browser support for platform authenticators is changing rapidly, so test browser support yourself. Remember to test the same browser across operating systems, the dialogues can be very different!
{{</ notice >}}

Once you've thoroughly tested the registration and authentication flow of a single app, enable your immediate team to use WebAuthn for SSO.

{{< notice tip >}}
Keep this group small and allow them to fall back to an existing second factor if there are any problems. Your aiming to have these trusted users test out WebAuthn in a wide variety of contexts over a few weeks or a month.
{{</ notice >}}

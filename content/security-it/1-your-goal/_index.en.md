---
title: "Your Goal"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
weight: 1
draft: false
# search related keywords
keywords: [""]
---

### Eliminate TOTP & Push

Wherever it is technically possible, you should be removing the use of TOTP & push notification as second factors.

WebAuthn is currently considered the most secure form of second factor available<sup>1</sup>, with push notifications second if WebAuthn isn't possible (more on that later).

{{< notice tip >}}
  Accounts are only as secure as their least secure authentication method. _Enforce_ use of WebAuthn to improve your security. 
{{</ notice >}}

{{< notice warning >}}
  Aim to achieve WebAuthn as a second factor, not a single passwordless authentication mechanism. Single factor WebAuthn is very difficult to make both secure and usable.
{{</ notice >}}

### Stop Yubikey OTP

A Yubikey filling in a random string of characters during authentication **is not WebAuthn, it is an OTP**. A Yubikey OTP is still a phishable credential, it's just a different style of one time password.

{{< notice tip >}}
If you chose to use Yubikeys as part of your WebAuthn rollout, others may initially confuse WebAuthn as Yubikey OTP. You should make it clear that Yubikeys are just one way to "do" WebAuthn.
{{</ notice >}}

### Improve User Experience

Push notifications and retrieving TOTPs is slow, I used to regularly experience ten second delays between a push notification being sent, acknowledging it and being authenticated.

This doesn't sound like much, until you consider that one second is about the limit of time before a user's thought process is interrupted<sup>2</sup>.

Compound the distraction time with having to pick up a _purposefully distracting_ phone to receive the notification, and it's easy to see how authentication flows become annoying for users by distracting them from their work.

{{< notice info >}}
Authenticating using WebAuthn allows users to leave their phone away from where they're working and authenticate with no distractions
{{</ notice >}}


### References

1. [Consumer Authentication Security Maturity Model (Version 6)](https://danielmiessler.com/p/casmm-consumer-authentication-security-maturity-model/), accessed July 2023
2. [Response Times: The 3 Important Limits](https://www.nngroup.com/articles/response-times-3-important-limits/), accessed July 2023
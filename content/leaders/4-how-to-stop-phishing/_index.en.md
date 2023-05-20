---
title: "How to Stop Phishing"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
weight: 4
draft: false
# search related keywords
keywords: [""]
---

### Require WebAuthn

If you're serious about stopping phishing, you need to insist on the use of WebAuthn as a second factor for all human access to your systems, especially SSO.

{{< notice info >}}
  CloudFlare stopped the previously mentioned 0ktapus campaign using the predecessor to WebAuthn called Universal Second Factor (U2F)<sup>1</sup>
{{</ notice >}}

WebAuthn is gaining traction and being touted as the beginning of a passwordless future<sup>2</sup>. In reality, operational challenges & standardization across vendors means WebAuthn is currently best used in combination with a password. If a password is phished, the WebAuthn second factor should stop the attacker gaining access.

{{< notice tip >}}
  Using WebAuthn as a second factor is good enough, you don't need to go full "passwordless" to benefit
{{</ notice >}}

{{< notice info >}}
  Although often used with biometrics, WebAuthn does not **require** their use. You can go completely phishing-resistant without them.
{{</ notice >}}

### References

1. [The Mechanics of a Sophisticated Phishing Scam and How We Stopped It](https://blog.cloudflare.com/2022-07-sms-phishing-attacks/), accessed May 2023
1. [WebAuthn Guide](https://webauthn.guide/), accessed May 2023
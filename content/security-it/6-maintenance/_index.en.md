---
title: "Maintenance"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
weight: 6
draft: false
# search related keywords
keywords: [""]
---

### Enforcement

Now you've reached 100% of users authenticating with WebAuthn as a second factor, you need to maintain that rate.

Ensure changes to processes & authentication policies do not allow for arbitrary exceptions to humans using WebAuthn.

Exceptions can be granted when WebAuthn is not technically possible (some mobile apps & embedded browsers suffer from this). Exceptions may also be required to allow user to register new WebAuthn authenticators. In both cases, enforce the use of non-OTP second factors, generally a push notification.

{{< notice tip >}}
Focus on enforcing the use of WebAuthn, not a particular authenticator. Users will appreciate the flexibility and it gives you options when specific hardware or app combinations don't work.
{{</ notice >}}

{{< notice info >}}
When registering new authenticators, it should be possible to configure your IdP so users can register an authenticator without using WebAuthn, but cannot access an application.
{{</ notice >}}

{{< notice warning >}}
A user registering their first (or replacing their only) authenticator increases their phishing risk. You'll be letting them into your IdP using a less secure second factor, so be sure to fully enforce the use of WebAuthn, once they've registered the authenticator.
{{</ notice >}}

### Replacing Cross Platform Authenticators

Cross platform authenticators have a particular risk of loss, depending on their shape & size they can also be broken with relative ease. Ensure your budget or contract for cross-platform authenticators includes a provision for replacing them, a 15% yearly replacement rate should be plenty.

If you encouraged users to register their devices as platform authenticators during the registration period, someone losing their cross-platform authenticator should not lock them out.

{{< notice tip >}}
Include cross platform authenticators in your IT care policy & encourage users to report their loss like any other IT asset.
{{</ notice >}}

{{< notice info >}}
Losing cross platform authenticators is inevitable, avoiding full "passwordless" gives you extra protection when this happens.
{{</ notice >}}

### Reusing Cross Platform Authenticators

When users leave your organization, it's perfectly safe to reuse their cross platform authenticator with another user. Use your IdP to revoke the WebAuthn registration on the user's last day, then have them return the authenticator with their corporate device(s).

{{< notice info >}}
Once you have the authenticator in your hands, use its management software to reset WebAuthn/FIDO2 credentials. Once you've done this, it's ready for use again.
{{</ notice >}}
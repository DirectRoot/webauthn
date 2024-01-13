---
title: "What You Need To Do"
date: 2024-01-13T12:00:00+05:00
lastmod: 2024-01-13T12:00:00+05:00
weight: 3
draft: false
# search related keywords
keywords: [""]
---

If WebAuthn is being deployed in your organization, there are some terms and processes that you'll need to become familiar with.

### Terminology

* `Authenticator` - The hardware used to help you authenticate
* `Platform authenticator` - An authenticator built into a device like a laptop or phone
* `Cross-platform authenticator` - An authenticator that can be used across different devices, like a Yubikey or Google Titan Key
* `Passkey` - An implementation of WebAuthn meant to make usage easier for consumers. When you're registering a platform authenticator, you might be prompted to save a passkey.

### Registration

Once you know what kind of authenticator(s) your organization is going to use, you'll need to go through a registration process; it's likely that this will happen within your Single Sign-On (SSO) platform.

You'll first need to login using your existing 2FA and start the registration process from your account settings. Once you've completed the registration process, your authenticator can be used when signing in.

{{< notice info >}}
Each new system where you want to use WebAuthn will require you to go through a registration process. But, if your applications are well integrated with SSO then you probably won't need to register anywhere else.
{{</ notice >}}

### Authentication

When authenticating using WebAuthn, your browser might ask you what kind of authenticator you want to use. A cross-platform authenticator might be referred to as a "security key" & using a platform authenticator could be a "passkey".

If you're using a cross-platform authenticator that works over USB (like a Yubikey), it only has to be inserted into your device during authentication. You can remove it once you've signed in.

{{< notice tip >}}
Registering a **platform** authenticator will only allow you sign in from _that device_. A **cross-platform authenticator** can be used on any device that supports it, for example it could be registered via a laptop, removed & used with a phone
{{</ notice >}}
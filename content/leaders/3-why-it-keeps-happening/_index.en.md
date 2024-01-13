---
title: "Why Phishing Keeps Happening"
date: 2024-01-13T12:00:00+05:00
lastmod: 2024-01-13T12:00:00+05:00
weight: 3
draft: false
# search related keywords
keywords: [""]
---

### Weak Second Factors

2FA will remain more secure than using a single factor, but malicious actors have evolved so that the most popular second factors are now relatively easy to circumvent.

#### SMS

It's generally accepted that SMS One Time Passcodes (OTPs) are insecure in both consumer & corporate settings. "Sim swapping" attacks allow a malicious takeover of a phone number, meaning the OTP can be delivered directly to the attacker.

#### Time-based One Time Passcodes (TOTP)

A TOTP from a mobile application is often the most secure second factor available to consumers and is regularly accepted in corporations too.

Whilst the TOTP rotating every thirty seconds seems to make it more secure, the 0ktapus hacking campaign<sup>1</sup> has proven criminals are very capable of phishing employees for password + TOTP _in real time_ to gain access.

{{< notice info >}}
  0ktapus has led to over 130 companies, 10k passwords and 5k TOTPs being compromised
{{</ notice >}}

#### Push Notifications

Whilst removing (T)OTPs means there's no passcode to phish, relying on app push notifications doesn't solve the problem. After phishing or discovering an employees password, a hacker can utilize MFA fatigue to eventually gain access.

MFA fatigue requires bombarding the victim with constant notifications until they relent and approve the sign in. This sounds far-fetched until you imagine receiving multiple notifications at night, whilst driving or during critical meetings. MFA fatigue was successfully used to compromise Uber in 2022<sup>2</sup>.

{{< notice warning >}}
  Push notifications can't be phished, but the human element makes them vulnerable to attack
{{</ notice >}}

### Relying on Education

The approach to stopping phishing in corporations has often relied on educating the user and following up with phishing tests, reports & extra education for those deemed to have "failed". Whilst security education is beneficial, it is not enough to stop a sustained phishing campaign.

Consider vehicle safety, we educate drivers to avoid mistakes but we also accept that they'll happen. Because of this, we use technology to improve the outcomes when they do. Picking a weak second factor and relying on education to stop phishing is equivalent to removing seatbelts and telling drivers, "**don't mess up**".

{{< notice tip >}}
  Using phishing-resistant WebAuthn removes the human error that phishing relies upon
{{</ notice >}}

### References

1. [Roasting 0ktapus: The Phishing Campaign Going After Okta Identity Credentials](https://www.group-ib.com/blog/0ktapus/), accessed May 2023
1. [Multi-Factor Authentication Fatigue Key Factor in Uber Breach](https://www.infoq.com/news/2022/09/Uber-breach-mfa-fatigue/), accessed May 2023
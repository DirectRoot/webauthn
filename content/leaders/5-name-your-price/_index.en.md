---
title: "Name Your Price"
date: 2018-12-29T11:02:05+06:00
lastmod: 2020-01-05T10:42:26+06:00
weight: 5
draft: false
# search related keywords
keywords: [""]
---

### How Much Will This Cost?

With some exceptions for large companies, the answer is often **pay as much as you want**.

{{< tabs >}}

  {{< tab "Less than 100 people" >}}
  Deploy WebAuthn for little to no money, with relative ease
  {{< /tab >}}

  {{< tab "100 to 1000 people" >}}
  Paying for WebAuthn technology is a good idea
  {{< /tab >}}

  {{< tab "Over 1000 people" >}}
  Invest in your WebAuthn deployment, for the sake of your users & technical teams!
  {{< /tab >}}
  
{{< /tabs >}}

### What Do We Need to Buy?

The technology costs for WebAuthn are the **SSO platform** and **hardware authenticators** that enable users to sign in.

{{< notice tip >}}
There are also hidden costs in **operational complexity, user education & support**. Appropriate spending on technology can reduce the hidden costs
{{</ notice >}}

#### The SSO Platform

{{< tabs >}}

  {{< tab "Free" >}}
  If you're already using a SSO platform built for the web, the chances are you've already got WebAuthn support
  {{< /tab >}}  

  {{< tab "Low Cost" >}}
  Good open-source SSO platforms should support WebAuthn, for example <a href=https://www.keycloak.org/>Keycloak</a>. You will incur some extra costs to have your own team install, run & maintain this software
  {{< /tab >}}

  {{< tab "Paid" >}}
  Major Identity as a Service (IDaaS) providers should all support WebAuthn, for example <a href=https://www.okta.com/>Okta</a> or <a href=https://www.onelogin.com/>OneLogin</a>
  {{< /tab >}}
  
{{< /tabs >}}


#### The Hardware Authenticators

{{< tabs >}}

  {{< tab "Free" >}}
  Using Chrome or Safari on relatively modern hardware will enable you to use your devices themselves as <b>platform authenticators</b>, Firefox should be adding support for this in the future. Both mobile & desktop/laptop devices can be used as platform authenticators 
  <br><br>
  You will incur some extra operational complexity when users need to sign into the SSO platform from multiple devices, because the authenticator is tied to each device. This is explained in more detail within the <a href=/security-it>Security & IT section</a>
  {{< /tab >}}  

  {{< tab "Paid" >}}
  <b>Cross platform authenticators</b> are external hardware resembling a USB stick, allowing users to register the authenticator once and use it on multiple devices.
  <br><br>
  Modern versions of <a href=https://www.yubico.com/>Yubico</a>'s well-known Yubikey can act as WebAuthn authenticators. See the <a href=/security-it>Security & IT section</a> for differences between Yubico OTP and WebAuthn.
  <br><br>
  Google also sell a viable authenticator as the <a href=https://cloud.google.com/titan-security-key>Titan Security Key</a>. These can be cheaper per unit than a Yubikey, but larger or more dispersed organizations might prefer to buy Yubikeys and use Yubico's <a href=https://www.yubico.com/products/yubienterprise-delivery/>YubiEnterprise Delivery</a> to handle logistics.

  {{< /tab >}}
  
{{< /tabs >}}

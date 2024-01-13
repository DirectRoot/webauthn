---
title: "Deployment"
date: 2024-01-13T12:00:00+05:00
lastmod: 2024-01-13T12:00:00+05:00
weight: 5
draft: false
# search related keywords
keywords: ["induct", "instate"]
---

### Documentation

With buy-in for a WebAuthn deployment, expand the simple onboarding guide you wrote for the pilot group.

The larger your organization, the higher quality the onboarding documentation needs to be. You be able to help everyone 1-on-1 like you did with the pilot group.

As before, create both text & video onboarding guides to allow people a choice.

{{< notice tip >}}
Re-record videos you made during the pilot stage, it's still common for WebAuthn dialogues in browsers to change. Visual differences in dialogues can put off less technical users.
{{</ notice >}}

### Creative Support & Education

Particularly in larger organizations, you might have to be creative with how you offer support & education to your users.

Consider the following to increase end-user confidence in the project:
* High-level presentations at all-hands or departmental meetings
* Video comparisons of the benefits they'll get from WebAuthn
* Technical, deep-dive presentations for people who want to know how WebAuthn works
* Pre-booked "Office Hours" where users can come for dedicated support or to ask questions

{{< notice tip >}}
This project will affect everyone in your organization, use it to demonstrate that  IT/Security are there to make things better for users - we don't just say "no"
{{</ notice >}}

### Rollout

I highly recommend splitting the rollout of WebAuthn into three phases

#### Authenticator Deployment

Whatever selection of authenticator you're going to use, get them into the hands of your users first. Warn people if you're going to be mailing a cross-platform authenticator to them.

If you're using platform authenticators only, confirm that your fleet of devices has the right hardware for WebAuthn.

{{< notice tip >}}
Encourage users with cross-platform authenticators to add them onto their physical key chain as soon as they arrive. Expect that some users will immediately lose their authenticator, regardless.
{{</ notice >}}

{{< notice warning >}}
Users are anxious to avoid being locked out. Moving onto registration & usage too quickly can be concerning for users who haven't received their authenticator yet.
{{</ notice >}}

#### Registration Period

Once you're at least 80% deployed with authenticators, configure your IdP to allow user registration of WebAuthn authenticators.

Use your documentation and "Registration Office Hours" to allow independent & guided registration.

Make use of WebAuthn _optional_ at this point. Just like you did with the pilot group, allow users to fallback to other authentication methods if required.

The registration period should last a number of weeks, at least four to six weeks with organizations over 1000 users.

{{< notice warning >}}
**Do not** attempt to restrict registration to specific types of authenticator. The functionality in IdP's is still immature and the extra complexity is not currently worth it.
{{</ notice >}}

{{< notice tip >}}
Even if you're using cross-platform authenticators, encourage users to register their corporate devices as authenticators **now**.
{{</ notice >}}

{{< notice tip >}}
Your IdP may remember the last authentication method that a user used. Encourage users to select the WebAuthn method for use once they've registered, whilst reassuring them that the old method will keep working during the registration period.
{{</ notice >}}

#### Cut Over Period

Immediately after the registration period, configure your IdP so that you're able to enforce use of WebAuthn on a specific group of users. You'll still be allowing registration, and will continue to do so.

The cut over period should also last several weeks, but can be shorter than the registration period because the majority of your users should have already taken the action they need to.

Begin placing users **who have already registered** in the enforcement group, starting with a few each day and slowly ramping up to include all registered users towards the end of the period.

There will always be people who leave tasks to the last minute, so increase messaging & the availability of 1-on-1 support in the last week of the period and the first week after.

If you've run the cut over correctly, the final day of the period should pass by unnoticed by almost all of your organization; they're already using WebAuthn, so it won't matter that you're not enforcing its use everywhere.

{{< notice warning >}}
Use a random selection of registered users each time you add more to the enforcement group. Ramping up by department or other grouping risks leaving problems until later & creating a bigger blast radius if something does go wrong.
{{</ notice >}}

{{< notice tip >}}
The slow ramp up of enforcement allows you to test enforced WebAuthn on a growing number of users, whilst giving you time to fix problems before the end of the cut over period.
{{</ notice >}}
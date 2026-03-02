---
title: "Application Controls"
---
# Application Control Reporting in BI for Defender
## 🎉 Application Control for Business: Who's on the Guest List?

Imagine your organization’s Windows devices are exclusive nightclubs. **Application Control** is the sharply dressed bouncer standing outside — sunglasses on, arms crossed, checking IDs. Only apps on the VIP list get in. Everyone else? 👎 Denied at the door.

**Application Control for Business** (powered by [Windows Defender Application Control](https://learn.microsoft.com/en-us/windows/security/application-security/application-control/app-control-for-business/appcontrol)) lets you control exactly which applications, scripts, and installers can run in your environment — based on trust rules like digital signatures, file paths, or publisher info.

It’s one of the most effective ways to stop uninvited guests like malware and rogue apps from crashing your party 🎤.


## 🤔 Why is the Application Controls Page in BI for Defender Blank?
![club wdac](images/club_wdac.png)

If your **Application Controls** page is looking blank — **like the dancefloor before 9 PM** — it’s probably because **Application Control for Business hasn’t been configured yet**.

This report depends on data from devices running WDAC policies. If there's no bouncer at the door, there's no one to report who tried to sneak in.

To get this page dancing:

✅ Deploy one or more WDAC policies via Intune or another management tool
✅ Use supported Windows editions (Enterprise or Education)
✅ Make sure device telemetry is enabled

Once that’s in place, the report will start showing you:

- Which devices are enforcing or auditing policies
- How many apps are being blocked (or trying to get in)
- And other insights that help your security team stay in control


## Need help getting started?

Here's the official [Microsoft Docs for Application Control](https://learn.microsoft.com/en-us/windows/security/application-security/application-control/app-control-for-business/appcontrol)

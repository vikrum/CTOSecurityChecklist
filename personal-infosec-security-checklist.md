---
title: The Personal Infosec & Security Checklist
date: 2021-07-09
description: 'Learn how to protect your personal accounts, settings, and configurations with the Gold Fig personal infosec checklist. Doing the basics goes a long way in keeping your accounts secure.'
image: images/blog/personal-infosec-checklist.jpg
---

Doing the basics goes a long way in keeping your personal accounts secure. This first<sup>1</sup> edition of the Personal Infosec & Security Checklist provides actionable security best practices anyone can use to harden their security posture. This list is far from exhaustive, incomplete by nature since the security you need depends on your risks and threats.

<div onclick="document.body.querySelectorAll('details').forEach((e) => (e.hasAttribute('open')) ? e.removeAttribute('open') : e.setAttribute('open',true))"><center>&#x2766;</center></div>

### ⚙️  Improve account settings beyond defaults

<details><summary>For your high value accounts, turn on the highest vendor provided security settings.</summary>

For example, if you use Google, turn on “Advanced Protection” which mandates the use of hardware MFA keys only among a slew of other security sensitive settings.

##### Read more:
https://landing.google.com/advancedprotection/

https://help.coinbase.com/en/coinbase/privacy-and-security/data-privacy/how-can-i-make-my-account-more-secure


</details>

<details><summary>Use MFA/2FA <b><i>everywhere</i></b> possible. </summary>
Prefer to use a hardware device over an authenticator app. Hardware devices are now supported across a wide variety of services such as Dropbox, GitLab, Epic Games, Coinbase, domain registrars, cloud providers and so on. Only use a reputable authenticator app such as Google Authenticator or Authy. If possible, do not use SMS as an account recovery or for MFA/2FA (see SIM takeover precautions below.) Be sure to enable MFA/2FA everywhere — not just some limited set of accounts or services, this helps prevent lateral account takeovers that might not be immediately obvious. Use multiple devices or methods as a backup in case the primary device is lost or destroyed. Safely keep generated backup codes.

##### Read more:
https://www.yubico.com/works-with-yubikey/catalog/

https://store.google.com/us/product/titan_security_key

https://zapier.com/blog/what-is-a-yubikey/

</details>

<details><summary>Turn off SMS/phone call account recovery and 2FA/MFA if possible. </summary>

Many services require a phone # when signing up which then gets used as an account recovery mechanism. Given how prevalent SIM takeover attacks continue to persist, many services now offer the ability to disable using phone/SMS as an account recovery channel. Be sure to keep recovery codes and linked accounts used for recovery secure as well.

![Turn off phone account recovery](/images/guide/google-phone-account-recovery.png)

##### Read more:
https://myaccount.google.com/phone


</details>

<details><summary>Improve your password hygiene.</summary>

* Use a password manager.
  * https://www.passwordstore.org/
  * https://keepass.info/
  * https://1password.com/
* Never reuse passwords.
  * See above — use a password manager.
* Prefer password length over complexity. When using long passwords (e.g. 32+ characters), double check the password continues to work. Sites will silently truncate input fields, have different restrictions on the password change input fields vs the login fields, etc. After rotating passwords, logout and log back in to ensure the password you intended to set is actually set.
  * https://auth0.com/blog/dont-pass-on-the-new-nist-password-guidelines/
* Assume all of your old passwords are out there in plain text. They are linked to your email and collated across numerous services. Also assume in many cases,  for the same service, if you’ve rotated passwords all of the previous passwords are also out there in plain text.
  * https://haveibeenpwned.com/
  * https://owasp.org/www-community/attacks/Credential_stuffing
  * https://blog.coinbase.com/coinbase-security-now-protecting-your-coinbase-account-in-more-places-d97526ca01e8
  <img src="https://miro.medium.com/max/1400/1*lpVDH4TwJCYFigmPo9GPlw.png">
</details>

<details><summary>Treat account security recovery questions such as “What’s your favorite ice-cream?” as passwords. </summary>

Generate and save responses in your password manager.

</details>

<details><summary>Periodically review and purge unused “connected apps”. </summary>

Review permissions external apps have to your email, calendar, contacts, etc. Similarly, review permissions and apps you have connected to side-projects, code repos, CI systems, domains, etc.

##### Read more:
https://myaccount.google.com/permissions [Google] Apps with access to your account
https://github.com/settings/applications [GitHub] Authorized applications


</details>

<details><summary>Periodically review and purge unused email filters.</summary>

Remove old (or surreptitious) filters and rules that might be automatically hiding or forwarding emails to other accounts. </summary>

##### Read more:
https://support.google.com/mail/answer/10957?hl=en

</details>

<details><summary>Prefer to not login to any of your accounts using someone else’s computer, phone, or device.  </summary>

Change your password from a trusted computer afterward if you login using an untrusted device. Be sure to logout and invalidate all logged in sessions.

</details>

<details><summary>If you use a custom domain for your email, ensure the registrar account is secured with MFA. </summary>

Ensure the billing has a backup credit card to prevent interrupting payment remittance. If the DNS/NS settings point to another provider, ensure that that provider is also secured with MFA. Ensure that billing is uninterrupted there as well. Ensure that privacy settings are enabled on the domain so as to not reveal any information that could be used to socially engineer a transfer. Ensure that domain transfer locks are turned on. Ensure that MX records are not duplicating mail elsewhere.

</details>

<details><summary>Be careful with email auto-replies or vacation auto-responders.  </summary>

Don’t inadvertently leak sensitive information to anyone that emails you.

</details>

### 🌐 Web Browsing
<details><summary>Familiarize yourself with modern phishing, scams, and other social engineering attacks.  </summary>

Stay vigilant and skeptical of all emails, phone calls, letters, and other ways to part you from your data and credentials.


##### Read more:
https://blog.coinbase.com/phishing-attacks-and-how-to-not-fall-victim-42b489d77199

https://www.consumer.ftc.gov/articles/how-recognize-and-avoid-phishing-scams

https://www.hawaii.edu/infosec/phishing/
</details>

<details><summary>Make sure you’re on the site you’re intending to be on.</summary>
Don’t get tricked into sending credentials to the wrong site. Use bookmarks to save known-good URLs and only use those when visiting the sites. Don't click through suspicious text messages, emails, or other alerts.
</details>

<details><summary>Don’t run commands in the terminal or browser console that you don’t fully understand.  </summary>

Commands that someone else is telling you to run at the terminal or console can substantially erode your account and device security.

</details>

<details><summary>Remove unnecessary or unused browser extensions and addons.  </summary>

There is a long and active history of extensions being sold to new owners whose updates might include things you did not initially sign up for.

</details>

<details><summary>Don’t install software from non-trusted sources.  </summary>

##### Read more:
https://its.ucsc.edu/security/download.html

https://support.apple.com/en-us/HT202491
</details>

<details><summary>Be aware of when screen sharing, video call, or screen recording not to reveal passwords, keys, MFA QR codes, etc.  </summary>

Don't inadvertantly reveal your password a character at a time. Modern mobile OSs will turn off the trailing show-character when typing a password if screen recording is turned on, but stay vigilant. If you need to log in to an account while sharing your screen, turn the video feed off if you think a secret or credential might be shown. Be equally alert if an MFA QR code is on the screen.


![Password shown character at a time](/images/guide/IMG_6007.jpg)

</details>


### 📱 Mobile Device
<details><summary>Set up a mobile carrier PIN and port lock out.  </summary>

Prevent your phone number from being transferred out of your control.

##### Read more:
https://about.att.com/pages/cyberaware/ni/blog/porting

https://krebsonsecurity.com/2018/02/how-to-fight-mobile-number-port-out-scams/

https://www.thebalanceeveryday.com/prevent-your-mobile-number-from-being-ported-4160360
</details>

<details><summary>Use a longer passcode on your phone. </summary>

Minimum of 10 digits, prefer over 12 digits. The longer the better.

##### Read more:
https://appleinsider.com/articles/18/04/17/researcher-estimates-graykey-can-unlock-a-6-digit-iphone-passcode-in-11-hours-heres-how-to-protect-yourself

https://www.vice.com/en/article/59jq8a/how-to-make-a-secure-iphone-passcode-6-digits
</details>

<details><summary>Encrypt your device.</summary>

##### Read more:
https://spreadprivacy.com/how-to-encrypt-devices

https://ssd.eff.org/en/module/how-encrypt-your-iphone

https://support.google.com/pixelphone/answer/2844831?hl=en

</details>

<details><summary>Don't show notification payload on lock screen.</summary>

Restrict what someone can see/do with your phone from the lock screen. Don’t show the content of the message on the lock screen if phone is locked. Restrict access to lock screen widgets, notification privacy, Apple Pay/Android Pay/Samsung Pay.

![Hide notification previews](/images/guide/IMG_6037.jpg)

##### Read more:
iPhone: https://www.ikream.com/hide-messages-on-iphone-lock-screen-28039

Android: https://www.digitalcitizen.life/how-hide-contents-sensitive-notifications-android/

</details>

<details><summary>Silence all unknown callers.</summary>

Send all phone calls that aren't in your contacts straight to voicemail. Don’t fall for scam calls. Let them leave a voicemail. Validate the call back number is actually associated with the entity that’s stated.

![Silence unknown callers](/images/guide/IMG_6038.jpg)

##### Read more:
https://support.apple.com/en-us/HT207099#:~:text=To%20turn%20on%20Silence%20Unknown,in%20your%20recent%20calls%20list.

</details>

<details><summary>Consider using throwaway phone numbers.</summary>

You can easily use throwaway numbers for some use cases such as reward points and other low priority sources.  (999) 999-9999, 555-1212, 867-5309, (281) 330-8004

##### Read more:
https://www.reddit.com/r/LifeProTips/comments/1hkq4i/lpt_dont_have_a_particular_stores_reward_card/


</details>

<details><summary>Be careful of phone charging threats.  </summary>

Prefer to use your own charger and cable.

##### Read more:
https://www.fcc.gov/juice-jacking-dangers-public-usb-charging-stations

https://spreadprivacy.com/privacy-risks-usb-charging/

</details>

<details><summary>Enable remote device wipe. </summary>

Enable Find My iPhone or Android Device Manager to use remote wipe if your phone is stolen or lost.

##### Read more:
https://support.google.com/accounts/answer/6160491?hl=en

https://support.apple.com/guide/icloud/erase-a-device-mmfc0ef36f/icloud

</details>

<details><summary>Enable “Erase Data” to delete data after 10 failed passcode attempts.</summary>

##### Read more:
https://support.apple.com/guide/iphone/set-a-passcode-iph14a867ae/ios

</details>

<details><summary>Avoid custom virtual keyboards.  </summary>

##### Read more:
https://zeltser.com/third-party-keyboards-security/

</details>

<details><summary>Be aware of and educate yourself about stalkerware.  </summary>

##### Read more:
https://www.wired.com/story/how-to-check-for-stalkerware/

</details>

<details><summary>Delete old unused apps.</summary>

Be sure to backup any app-specific data you might want to keep.

</details>

<details><summary>Automatically delete old messages. </summary>

Don’t keep sensitive data you no longer need laying around. Delete old text messages, chats, and emails.

![Message history: keep messages for 30 days](/images/guide/IMG_6035.jpg)

</details>

<details><summary>Periodically review SMS/text message forwarding settings. </summary>

Ensure they are up to date and what you expect them to be.

![Text Message Forwarding](/images/guide/IMG_6036.jpg)

##### Read more:
https://support.apple.com/en-us/HT208386

</details>


### 💻 Computer
<details><summary>Encrypt your devices and disks (& power-off instead of hibernate)</summary>

##### Read more:
[FileVault](https://support.apple.com/en-us/HT204837) Mac

[BitLocker](http://www.windowscentral.com/how-use-bitlocker-encryption-windows-10) Windows - Related: [Power off computer, instead of standby](https://docs.microsoft.com/en-us/windows/security/information-protection/bitlocker/bitlocker-security-faq#what-are-the-implications-of-using-the-sleep-or-hibernate-power-management-options-)

[LUKS](http://www.pavelkogan.com/2014/05/23/luks-full-disk-encryption/) Linux

</details>

<details><summary>Keep your system up to date and apply security patches when they become available.</summary>

##### Read more:
https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/keep-windows-up-to-date

https://support.apple.com/guide/mac-help/get-macos-updates-mchlpx1065/mac
</details>

<details><summary>Be careful plugging unknown external devices into your computer.</summary>

##### Read more:
https://us-cert.cisa.gov/ncas/tips/ST08-001

</details>

<details><summary>Activate screen-lock when idle.  </summary>

Require a password when resuming from screensaver.

##### Read more:
https://it.cornell.edu/device-security/set-your-windows-computers-screen-lock-automatically

https://support.apple.com/guide/mac-help/require-a-password-after-waking-your-mac-mchlp2270/11.0/mac/11.0

</details>

<details><summary>Learn the keyboard shortcut to lock your computer.</summary>
* [Windows logo + L](https://support.microsoft.com/en-us/help/12445/windows-keyboard-shortcuts) - Windows
* [control + shift + power/escape](http://www.macworld.co.uk/how-to/mac/how-lock-mac-3639053/) - Mac
* [ctrl + alt + L](https://askubuntu.com/questions/126782/keyboard-shortcut-for-lockscreen-not-working) - Linux
</details>

<details><summary>Review your installed apps and remove old ones.</summary>

Old and unpatched software no longer being used ought to be uninstalled.
</details>


<details><summary>Don't use root/admin account for day to day or non-admin work.</summary>

Avoid using the root or admin account for normal day to day work.
</details>

<details><summary>Disable Undesired Features (Windows) e.g. MS Office Macros.</summary>

##### Read more:
https://www.cyber.gov.au/acsc/view-all-content/publications/hardening-microsoft-office-365-proplus-office-2019-and-office-2016

</details>

<details><summary>Enable and use Secure Boot (Windows).</summary>

##### Read more:
https://itconnect.uw.edu/wares/mws/mgmt/setup-computer/secure-boot/#:~:text=Secure%20Boot%20is%20a%20security,Linux%20and%20variants%20of%20BSD
</details>

<details><summary>Keep multiple backups of your important data.  </summary>

##### Read more:
https://www.tarsnap.com/

https://www.arqbackup.com/

https://www.dropbox.com/

</details>

<details><summary>Delete old sensitive data that you don’t need any more—including from old backups.</summary>

Don’t keep sensitive data you no longer need laying around. Delete old files, archives, and storage devices.
</details>


### ⚔️ Physical security
<details><summary>Never leave a device unattended, in the trunk, or hidden in a car.</summary>

Just bring it with you, no matter how short of a time you’re leaving it there.

##### Read more:
https://observer.com/2019/11/bluetooth-scanner-car-burglary-stealing-laptops/

https://www.wired.com/story/bluetooth-scanner-car-thefts/

</details>

<details><summary>Consolidate external hard drives and USB drives so you have fewer things to keep track of.</summary>

Wipe and destroy unused old computers, phones, tablets, hard drives, etc.
</details>

<details><summary>Consolidate notebooks and papers that could have sensitive info.  </summary>
Shred and destroy the ones you don't need.
</details>

<details><summary>Keep back up Titan/Yubikeys in a safe deposit box or offsite.  </summary>

Backup MFA/2FA devices ought to be kept offsite.
</details>


### 💡 Miscellaneous
<details><summary>Freeze your credit.</summary>

##### Read more:
https://www.nerdwallet.com/article/finance/how-to-freeze-credit


</details>

<details><summary>Delete/archive old projects, domains, DNS records.  </summary>

Dangling records and projects can be used in a variety of ways to compromise your security or rack up charges.  Use your credit card statements to review for recurring charges you might have forgot about to surface dormant projects/domains that are still running.
</details>

<details><summary>Audit your MFA/2FA usage to ensure it’s enabled and up to date.</summary>

* Google/Apple ID
* GitHub/GitLab
* Banking
* Coinbase/crypto wallets
* Amazon (retail)
* Amazon/GCP/Azure/Cloudflare (cloud)
* Domain registrars/DNS/web hosting providers
* Whatsapp/Signal/Telegram
* Dropbox
* Slack - all of your Slack teams!
* Twitter/Facebook/Instagram

</details>

<details><summary>Thoughts on using VPN not improving personal security or privacy.</summary>

##### Read more:
https://gist.github.com/joepie91/5a9909939e6ce7d09e29
</details>



### 📚 Further reading

<details><summary>Read stories of others’ account takeover, hacks, and the lessons they learned.</summary>


* [Getting Hacked, Lessons Learned](https://avc.com/2017/06/getting-hacked-lessons-learned/) - AVC, Fred Wilson
* [How to lose $8k worth of bitcoin in 15 minutes with Verizon and Coinbase.com](https://medium.com/@CodyBrown/how-to-lose-8k-worth-of-bitcoin-in-15-minutes-with-verizon-and-coinbase-com-ba75fb8d0bac) - Cody Brown
* [How I got hacked, lost crypto and what it says about Apple’s security. Part 1](https://ksaitor.medium.com/how-i-got-hacked-lost-crypto-and-what-it-says-about-apples-security-part-1-83c107beae9) - Raman Shalupau

</details>

### 👉 Others in the checklist series
* [The SaaS CTO Security Checklist Redux](https://www.goldfiglabs.com/guide/saas-cto-security-checklist/)
* [The DevOps Security Checklist Redux](https://www.goldfiglabs.com/guide/devops-security-checklist/)


<sup>1</sup> <small>[CCA ShareAlike 4.0 International](https://github.com/vikrum/SecurityChecklists/blob/master/LICENSE.md). This guide is open source via CCA. Your contributions and additions are appreciated!</small>

###### Most recently updated: Fri Jul  9 14:27:48 PDT 2021

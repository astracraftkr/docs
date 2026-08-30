---
title: ScoreCue Privacy Policy
permalink: /ScoreCue/en/privacy/
redirect_from: /en/privacy/
effective: 2026-08-25
updated: 2026-08-25
description: What ScoreCue collects, where it is stored, and how to delete it
lang: en
alt: /ScoreCue/ko/privacy/
---

> This is a translation provided for convenience. The [Korean version]({{ '/ScoreCue/ko/privacy/' | relative_url }})
> is the authoritative text; if the two differ, the Korean version prevails.

ScoreCue (the "App") is a sheet music viewer for band musicians. This policy explains what
information the App collects and uses, where it is stored, and how you can access or delete it.
**The App does not collect personal information beyond what is described below.**

The same policy applies on Android and iOS/iPadOS.

> **In short** — your score files, annotations, and timings stay **on your device** and are never
> uploaded. What goes to the server is your account identity when signed in, your paid entitlement
> status, and your band activity if you use the band features. The App has **no advertising and
> collects no advertising identifiers.**

## 1. What We Collect and Why

### 1-1. Account information (only when signed in)

Viewing scores, annotating, the metronome, and ensemble sessions all work **without signing in**.
When you sign in with a Google or Apple account, the following is processed through Firebase
Authentication.

<div class="table-wrap" markdown="1">

| Item | Purpose |
|---|---|
| User ID (Firebase UID) | Account identification, managing paid entitlements |
| Email address | Account identification, showing sign-in status in the App, support |
| Display name | Showing sign-in status in the App, band roster display |
| Profile photo URL | Showing sign-in status in the App |

</div>

If you choose **Hide My Email** with Apple sign-in, the App receives only the Apple relay address and
cannot see your real email address.

### 1-2. Paid entitlement status (Cloud Firestore)

Paid features can only be unlocked safely if the server can verify your purchase, so entitlement
status is recorded under your own account path (<code>users/{your UID}/entitlements/…</code>).

- Entitlement type (`pro` for on-device features, `community` for band operation) and whether it is active
- Expiry date, the product identifier purchased, the store the purchase was made in, and refresh timestamps

These documents are **written only by the server** (the Developer's cloud functions), are readable only
by you, and are not visible to other users. They contain no payment credentials.

### 1-3. Purchase information (RevenueCat)

RevenueCat is used to process purchases and subscriptions and to validate receipts. Your Firebase UID
(used as the app user ID) and your store purchase/subscription records and receipts are sent to and
stored by RevenueCat.

**Payment credentials such as card numbers are handled by Google Play or the Apple App Store and are
never received by the App or by RevenueCat.**

### 1-4. Community (band) information (Cloud Firestore)

The following is stored only if you create a band or join one with an invite code, and it is
**visible to the other members of that band.**

- Band name and invite code
- Roster: each member's UID, display name, role (owner / co-leader / member), and join and removal times
- Events and attendance responses (RSVPs), availability polls and responses
- Announcement titles, bodies, and attached links
- Shared setlist names and the song titles and order they contain

None of this is created if you do not join a band. **Score PDF files themselves are never uploaded to a
band** — what is shared is list information such as song titles.

### 1-5. Usage statistics and crash reports

- **Firebase Analytics**: basic usage events such as screen views and app launches are collected
  automatically. They are used only for statistical analysis to improve the App, and an app instance ID
  along with device and operating system information may be processed alongside them.
- **Firebase Crashlytics**: if the App terminates abnormally, the error stack, device model, OS version,
  app version, and time of occurrence are sent. Used only to fix defects.

### 1-6. Information stored only on your device

The following stays **on your device** and is never sent to a server.

- Score PDF files and your library list (the App stores only the access path to files you selected)
- Annotations drawn on scores
- Playback timing data (bar and page turns) and analysis results
- App settings and metronome presets
- Backup files you export yourself (you choose where they are saved)

Uninstalling the App deletes the data it stored internally. Backup files you exported elsewhere and your
original PDFs remain where they are.

### 1-7. Ensemble (band sync)

Ensemble sessions communicate **directly between devices over the same local network (Wi-Fi) or via
Bluetooth**, without passing through any external server.

- Devices in a session exchange the session name, participant display names, the current playback
  position, and song change information.
- Over Bluetooth, the host device advertises a fixed service identifier that participant devices scan
  for. No pairing is required.
- On Android, the Bluetooth scanning permission is declared `neverForLocation` — it is **not used to
  derive location**, and the App requests no location permission.

### 1-8. YouTube playback

Playing a YouTube video in the App uses the embedded YouTube player, and YouTube/Google may process
information under their own policies. By using this feature you agree to the
[YouTube Terms of Service](https://www.youtube.com/t/terms); Google's handling of data is described in
the [Google Privacy Policy](https://policies.google.com/privacy).

### 1-9. What we do not collect

- Location, contacts, microphone or camera data
- Advertising identifiers (Android Advertising ID, iOS IDFA) — **the App contains no advertising.**
- Hardware identifiers such as IMEI or serial numbers
- Access to any file you did not select

## 2. Third-Party Services

The App uses the following services, each of which processes data under its own policy.

<div class="table-wrap" markdown="1">

| Service | Purpose | Policy |
|---|---|---|
| Google Firebase (Authentication, Cloud Firestore, Cloud Functions, Analytics, Crashlytics) | Sign-in, entitlement and community data storage, usage statistics, crash reporting | [firebase.google.com/support/privacy](https://firebase.google.com/support/privacy) |
| RevenueCat | Purchase/subscription processing and receipt validation | [revenuecat.com/privacy](https://www.revenuecat.com/privacy) |
| Google Play (Android) | Payment processing | [policies.google.com/privacy](https://policies.google.com/privacy) |
| Apple App Store (iOS/iPadOS) | Payment processing, Apple sign-in | [apple.com/legal/privacy](https://www.apple.com/legal/privacy/) |
| YouTube (Google) | Video playback | [policies.google.com/privacy](https://policies.google.com/privacy) |

</div>

The Developer does not sell personal information or provide it to third parties for purposes other than
the services above.

## 3. International Transfers

The servers of the third-party services above may be located outside the Republic of Korea (primarily
in the United States), and information is transferred to, stored in, and processed in those countries
to the extent necessary to provide the service. The items and purposes transferred are those described
in Sections 1 and 2, and the recipients are the companies listed in the table above. If you do not want
such transfers, you may use the App's basic features without signing in.

## 4. Retention

- **Account information, entitlement status, community data**: retained while the account exists, and
  deleted when the account is deleted.
- **Purchase records (RevenueCat)**: retained under RevenueCat's policy for transaction management such
  as purchase restoration and refunds. Where law requires retention of transaction records, that period
  applies.
- **Usage statistics (Firebase Analytics)**: up to 14 months under Google's default retention setting.
- **Crash reports (Crashlytics)**: retained under Google's policy (typically within 90 days).
- **On-device data**: never stored on a server; removed when the App is uninstalled.

## 5. Your Rights and How to Delete Your Data {#deletion}

You may request access to, correction of, deletion of, or suspension of processing of your personal
information.

- **Sign out**: available at any time from the App's settings screen. Signing out stops server-linked
  features, and the App operates within the free scope.
- **Delete your account in the App**: the account deletion function in settings deletes your account and
  your server-stored data — account information, entitlement status, your member records in every band,
  and the attendance responses and poll votes you authored. **If you own a band, you must first delete it
  or transfer ownership** so that the other members are not left stranded.
- **By email**: write to <a href="mailto:support@astracraft.kr">support@astracraft.kr</a>;
  requests are handled within 30 days of receipt.
- **Device data**: uninstalling the App or clearing its data in your OS settings removes all on-device data.
- **Purchase records**: payment records retained by the stores and by RevenueCat for transaction
  management may persist independently of account deletion. Deleting store purchase history follows each
  store's own policy.

## 6. Security

- All communication between the App and the server uses encrypted connections (TLS).
- Server data is protected by access rules so that you can read only your own data and the data of bands
  you belong to. Entitlement documents are **writable only by the server** and cannot be modified from the App.
- The Developer accesses data only to the minimum extent necessary to operate the service.

## 7. Children's Privacy

The App is not directed at children and does not permit account creation by anyone under the age of 14.
If we learn that personal information of a child under 14 has been collected, we delete it immediately.
Features used without an account send no personal information to a server.

## 8. Changes to This Policy

Changes to this policy are published on this page together with their effective date. Changes that
materially affect users are published at least 30 days before they take effect.

## 9. Contact

Privacy enquiries and access or deletion requests:
<a href="mailto:support@astracraft.kr">support@astracraft.kr</a>

## 10. Privacy Officer

Designated under Article 31 of the Korean Personal Information Protection Act.

| | |
|---|---|
| Name | Park Hyojin (박효진) |
| Title | Representative |
| Phone | <a href="tel:+8250219322092">0502-1932-2092</a> (Korea) |
| Email | <a href="mailto:support@astracraft.kr">support@astracraft.kr</a> |

Enquiries, complaints, and remedy requests regarding the handling of personal data may be sent to
the contact above and will be answered without delay.

### Dispute resolution bodies

Korean users may also apply to the following for mediation or advice.

- Personal Information Dispute Mediation Committee — 1833-6972 / <https://www.kopico.go.kr>
- Privacy Infringement Report Centre — 118 / <https://privacy.kisa.or.kr>
- Supreme Prosecutors' Office, Cybercrime Investigation — 1301 / <https://www.spo.go.kr>
- National Police Agency, Cyber Investigation Bureau — 182 / <https://ecrm.police.go.kr>

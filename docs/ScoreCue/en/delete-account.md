---
title: Delete Your ScoreCue Account and Data
permalink: /ScoreCue/en/delete-account/
effective: 2026-09-02
updated: 2026-09-02
description: How to delete your ScoreCue account and the data stored on our servers — in the app, or by email
lang: en
alt: /ScoreCue/ko/delete-account/
---

> This is a translation provided for convenience. The [Korean version]({{ '/ScoreCue/ko/delete-account/' | relative_url }})
> is the authoritative text; if the two differ, the Korean version prevails.

This page explains how to delete your **ScoreCue** account (Android · iOS/iPadOS, app ID
`kr.astracraft.scorecue`, developer Astra Craft) and the personal data stored on our servers.
The page is public — no sign-in and no app install is required to read it — and you can request
deletion through either route below.

## 1. Delete in the app (immediate)

1. Open the ScoreCue app.
2. Go to **Settings**.
3. Under **Account**, tap **Delete account**.
4. Read the summary of what will be removed, then tap **Continue** → **Delete permanently**.

Confirming removes your account and everything listed in section 3 from our servers **immediately and
permanently**; it cannot be undone. For security, if you have not signed in recently the app may ask you
to sign in again before it proceeds.

> **If you own a band, settle it first.** So that the remaining members are not stranded, delete the
> bands you own or transfer ownership to another member before deleting your account. If you do not, the
> app refuses the deletion and tells you why.

## 2. Request deletion by email (no app needed)

If you have already uninstalled the app or cannot reach it, write to us and we will do it for you.

- **To**: <a href="mailto:support@astracraft.kr?subject=ScoreCue%20account%20deletion%20request">support@astracraft.kr</a>
- **Subject**: `ScoreCue account deletion request`
- **Include**: the email address you signed in with (if you chose Hide My Email with Apple, the relay
  address Apple issued), and whether you want the whole account deleted or only part of your data.

After verifying that the request is yours, we complete it **within 30 days of receipt** and reply with the
result. We use that email address only to reply about this request, and we discard the request record once
it is done.

## 3. What is deleted

| Data | Where it is stored |
|---|---|
| Account identifiers (user ID, email address, display name, profile photo URL) | Firebase Authentication |
| Entitlement status (entitlement type, active flag, expiry, product identifier) | Cloud Firestore |
| Device activation record | Cloud Firestore |
| Purchase-verification token and registered push-notification tokens | Cloud Firestore |
| Your member record and join requests in every band | Cloud Firestore |
| Event attendance responses (RSVPs) and availability votes you authored | Cloud Firestore |

**Data kept only on your device** — sheet-music PDFs, annotations, playback timing, app settings and
metronome presets — never reaches a server, so it is not part of account deletion. It is removed when you
uninstall the app or clear its data in your OS settings. Backup files and original PDFs you exported
yourself stay wherever you put them.

## 4. What is retained after deletion, and for how long

| Data | Retention | Why |
|---|---|---|
| Purchase and payment records at the stores and RevenueCat | Under each company's policy and any statutory retention period for transaction records | Purchase restoration, refunds, accounting |
| Usage statistics (Firebase Analytics) | Deleted automatically after up to 14 months | Statistical analysis to improve the app |
| Crash reports (Firebase Crashlytics) | Deleted automatically under Google's policy, typically within 90 days | Fixing defects |
| Band-wide records such as announcements and shared setlists | While that band exists | Continuity for the remaining members |

Statistics and crash reports are collected against an app-instance identifier separate from your account.
If you want those deleted too, say so in the email described in section 2.

## 5. Delete only some data and keep your account

You can remove any of the following without deleting your account.

- **Band data**: **Leave band** on the band screen deletes your member record, RSVPs and votes in that
  band. Bands you own can be deleted from the band settings.
- **On-device data**: delete individual scores, annotations or timing data inside the app, or clear the
  app's data in your OS settings to remove all of it at once.
- **Usage statistics and crash reports**: request deletion by email as described in section 2.
- **Sign out**: signing out in Settings stops server-linked features and the app runs within the free
  scope. Signing out is not deletion — your account and server data remain.

## 6. Contact

Questions about account or data deletion: <a href="mailto:support@astracraft.kr">support@astracraft.kr</a>

For the full list of what we collect and why, see the
[Privacy Policy]({{ '/ScoreCue/en/privacy/' | relative_url }}).

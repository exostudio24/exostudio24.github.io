# Lingua — Google Play Data Safety Summary

**Updated:** October 3, 2026

This summary describes version 1.1 with ads (AdMob + UMP), Firebase Analytics/Crashlytics/Remote Config, AppMetrica, Meta SDK, and TikTok Business SDK. Re-audit it against the final merged manifest and SDK list of the release AAB before submitting the Play Console form.

## Play Console answers (draft for 1.1)

- Does the app collect or share any required user data types? **Yes**
- Account creation: **No**
- Account deletion URL: **Not applicable; Lingua has no account**
- Data deletion: **Users can reset learning data in Lingua Settings, clear app storage, or uninstall; SDK data deletion requests via hello@exo.ltd**
- Data encrypted in transit: **Yes (HTTPS)**
- Contains ads: **Yes**
- In-app purchases or subscriptions: **No**
- Target audience: **Adults (18 and over)**

| Data type | Collected | Shared | Optional | Purposes |
| --- | --- | --- | --- | --- |
| Device or other IDs (Advertising ID, app-set ID, installation IDs) | Yes | Yes | No | Advertising or marketing, Analytics, Fraud prevention |
| Approximate location (derived from IP by SDKs) | Yes | Yes | No | Advertising or marketing, Analytics, Fraud prevention |
| App interactions | Yes | Yes | No | Analytics, Advertising or marketing, App functionality |
| Other user-generated content / in-app search history | No | No | — | — |
| Crash logs | Yes | No | No | App functionality, Analytics |
| Diagnostics (performance) | Yes | No | No | App functionality, Analytics |
| Other app performance data / other actions (ad impressions and clicks) | Yes | Yes | No | Advertising or marketing, Analytics |
| Personal info (name, email, phone), financial, health, messages, photos, audio, contacts, calendar, precise location | No | No | — | — |

Data is processed ephemerally: **No**. Users can choose whether data is collected: **No** (personalized ads are consent-based via UMP in regions where required).

## Local-only data

Lingua stores interface language, proficiency, daily goal, XP, level, streak, practice dates, onboarding answers, completed lesson identifiers, and identifiers used to prevent duplicate lesson completion in Android's private app storage. Android cloud backup is disabled. The app does not upload this learning data.

## SDKs and providers

- Google AdMob + User Messaging Platform (Google LLC)
- Firebase Analytics, Crashlytics, Remote Config (Google LLC)
- AppMetrica (YANDEX LLC)
- Meta (Facebook) SDK — app events / install measurement
- TikTok Business SDK — app events / install measurement

## Technical evidence (to confirm on the 1.1 AAB)

- Application ID: `exo.learnenglish`
- Target SDK: API 36
- Expected permissions: `INTERNET`, `ACCESS_NETWORK_STATE`, `com.google.android.gms.permission.AD_ID`; no location, camera, microphone, contacts, media, phone, or health permission.
- Privacy policy: https://exostudio24.github.io/lingua/privacy-policy.html

## Release maintenance

Update this summary, the privacy policy, and Play Console declarations (Data safety, Ads, Advertising ID) whenever an SDK, permission, or data flow is added or removed.

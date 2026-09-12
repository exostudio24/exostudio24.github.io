# Lingua — Google Play Data Safety Summary

**Updated:** September 12, 2026

This summary describes version 1.0.0 (version code 1). Re-audit it before adding any SDK, permission, remote service, or new data flow.

## Play Console answers

- Does the app collect or share any required user data types? **No**
- Data collected: **None**
- Data shared with third parties: **None**
- Account creation: **No**
- Account deletion URL: **Not applicable; Lingua has no account**
- Data deletion: **Users can reset all learning data in Lingua Settings, clear Android app storage, or uninstall**
- Data encrypted in transit: **Not applicable; the app does not transmit user data**
- Advertising: **No**
- In-app purchases or subscriptions: **No**
- Analytics or remote crash reporting: **No**
- Sensitive permissions: **None**
- Android Advertising ID: **Not used**
- Target audience: **Adults (18 and over)**

## Local-only data

Lingua stores interface language, proficiency, daily goal, XP, level, streak, practice dates, completed lesson identifiers, and identifiers used to prevent duplicate lesson completion in Android's private app storage. Android cloud backup is disabled. The app does not transmit this data.

## Technical evidence

- Application ID: `exo.learnenglish`
- Target SDK: API 36
- Release manifest includes no `INTERNET`, advertising, location, camera, microphone, contacts, media, phone, or health permission.
- Runtime dependencies are AndroidX, Jetpack Compose, Kotlin serialization, coroutines, and DataStore only.

## Release maintenance

Update this summary, the privacy policy, and Play Console declarations before enabling advertising, analytics, crash reporting, network access, push notifications, accounts, cloud sync, user-generated content, purchases, subscriptions, or sensitive permissions.

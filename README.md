# Slovio for Android

The Slovio phone app for clients, before it reaches Google Play. This repository only holds the
signed app builds (APK files, under [Releases](https://github.com/devcrunchy/slovio-releases/releases))
and `latest.json`, the signed notice the app reads to know a newer build exists. There is no source
code here.

## Install

1. On your Android phone, open the [latest release](https://github.com/devcrunchy/slovio-releases/releases/latest)
   and download the `.apk` file.
2. Open it. Android asks once to allow installs from your browser or file manager; allow it, then tap
   **Install**.
3. Sign in with your Slovio account.

From then on the app updates itself: when a new build is out it shows **New update**. Tap **Update**,
then **Install** on Android's screen. You stay signed in. **Later** asks again after a few hours.

## Check that a download is genuine

Every release lists the APK's SHA-256 below and in its release notes. Compare it with your download:

- Windows: `certutil -hashfile slovio-<version>.apk SHA256`
- macOS / Linux: `shasum -a 256 slovio-<version>.apk`

Every build is signed with the same certificate. Its SHA-256 fingerprint is:

```
(published with the first release)
```

Android refuses to update the app with a file signed by any other certificate, and the app itself
only accepts update notices signed with Slovio's release key.

## Releases

| Version | Build | APK SHA-256 | Published |
|---|---|---|---|
| (first release pending) | | | |

## Security

Found a problem? Write to the Slovio team through the support page in the app. Please do not open a
public issue for security reports.

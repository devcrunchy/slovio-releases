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
443b584795d33ce5adf0c20678c8a8ff51690cdb7fb94d133aa246e6dc9a19d4
```

Android refuses to update the app with a file signed by any other certificate, and the app itself
only accepts update notices signed with Slovio's release key.

## Releases

| Version | Build | APK SHA-256 | Published |
|---|---|---|---|
| 1.1.2 | 7 | `453c9440afb1bf35de2e171bbd8ba6c4c045d78f7ffcf082e5d24f8ffe082e21` | 2026-11-21 |
| 1.1.1 | 5 | `5c96d4a427688fe974410bc81ad6ab1866794fda0578b5b6cf2683cbc9f4a54f` | 2026-11-21 |
| 1.1.0 | 3 | `204bdd20339ad81178b4a29ed93480510082263d0909e361450c89a44b1b10b1` | 2026-11-21 |

## Security

Found a problem? Write to the Slovio team through the support page in the app. Please do not open a
public issue for security reports.

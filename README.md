# SMS → Lark — Android test download

This repository distributes the APK only, plus installation information and its checksum. The source repository is private.

Open **Releases**, select **Android test build 2**, then download **sms-lark-bridge.apk**. Public release downloads do not require a GitHub account.

This is a debug-signed development build for Android 8 and later, tested on an Android 15 emulator. Physical-device SMS reception and Google Sheet/Lark setup require testing on your own phone.

## Install

Download the APK on your phone and open it. If Android prompts, allow installation from the app opening the file. Open **SMS → Lark** and request incoming SMS access.

Android may restrict SMS permission for direct APK installations. If permission is unavailable, install from your own computer using USB or wireless ADB:

```text
adb install -r sms-lark-bridge.apk
```

Then grant SMS permission in the app. Forwarding starts paused. Configure your private rules API and Lark webhook, sync rules, and send a connection test before enabling forwarding. This APK contains no configured account credentials, webhook or API token.

## Verified build

- Android compilation and lint passed.
- 44 platform-independent checks passed.
- Seven Android 15 emulator component tests passed.
- This is not a production or Play Store release. Signing keys can change between development builds; uninstalling to replace a build erases its configuration.

SHA-256: `0c108601f2cc728dbf637de51dbcae551e6fcba5a75243b70007bf1a3fe0f08f`

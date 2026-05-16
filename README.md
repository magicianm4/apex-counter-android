# Apex Counter — Android WebView APK

This Android Studio project wraps **Apex Counter** (built with [CodeWithTrav.AI](https://codewithtrav.ai)) in a native Android WebView, packaged as a `.apk` you can sideload onto any Android device or Android TV box.

## Auto-build via GitHub Actions

Every push to `main` runs `.github/workflows/build-apk.yml`, which:

1. Sets up JDK 17 + Android SDK 34
2. Builds a debug APK
3. Publishes it as a release tagged `latest`

**Download the APK** from the [Releases](../../releases/latest) page.

## Build locally (Android Studio)

1. Install [Android Studio](https://developer.android.com/studio)
2. Open this folder
3. Click ▶︎ Run, or `./gradlew assembleDebug`
4. APK is in `app/build/outputs/apk/debug/app-debug.apk`

## What's inside

- `app/src/main/assets/index.html` — Trav's generated app
- `app/src/main/java/.../MainActivity.java` — Loads the HTML in a WebView
- `app/build.gradle` — AGP 8.2 + AndroidX
- `.github/workflows/build-apk.yml` — Cloud build pipeline

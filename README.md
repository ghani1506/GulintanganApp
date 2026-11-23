# Gulintangan – Android app

A playable gulintangan (C5–C6, caklempong-style sound) that also lets you record your own instrument with the phone's microphone.
Made by Mohammad Ghani bin Awang Ahmad.

## Get the APK without installing anything (GitHub)

1. Sign in to github.com and create a **new repository** (for example `gulintangan-app`). Leave it empty.
2. On the new repository page, click **uploading an existing file**.
3. Unzip `GulintanganApp.zip` on a computer, open the `GulintanganApp` folder, select **everything inside it**
   (including the `.github` folder; turn on "show hidden files" if you can't see it) and drag it into the upload page.
   Click **Commit changes**.
4. Open the **Actions** tab. The "Build APK" job starts by itself (if it asks, click *I understand… enable workflows*,
   then **Run workflow**). It takes about 3–5 minutes.
5. When it shows a green tick, click the run and download **Gulintangan-APK** under *Artifacts*. Unzip it to get `app-debug.apk`.
6. Copy the APK to your Android phone or tablet and open it. Allow "Install unknown apps" when Android asks.

## Or build it in Android Studio

Open this folder in Android Studio, wait for Gradle to sync, then choose **Build ▸ Build App Bundle(s) / APK(s) ▸ Build APK(s)**.

## In the app

- Tap the gongs to play; slide a finger across them for a run.
- **Record one note**: strike any gong within 3 seconds; the app detects the note and builds all the other notes from it.
- **Record** on any row records that exact gong for the most realistic sound.
- The first time you record, Android asks for microphone permission. Tap **Allow**.
- Recordings are kept on the device.

## Updating the app

Replace `app/src/main/assets/index.html` with a newer version, commit, and GitHub builds a new APK.
Raise `versionCode` in `app/build.gradle` so Android installs it as an update.

Note: APK files run on Android only. On iPhone or iPad, use the web version.

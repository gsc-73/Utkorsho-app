# Utkorsho Android App (WebView wrapper)

This wraps https://www.utkorsho.tech in a native Android app shell using Capacitor.
GitHub Actions builds the APK for you — no Android Studio needed.

## Setup (one-time)

1. Create a new **empty** GitHub repo (e.g. `utkorsho-app`).
2. Upload all files in this folder to that repo (keep the folder structure,
   including the hidden `.github` folder).
3. Go to the repo's **Actions** tab. If prompted, click "I understand my
   workflows, go ahead and enable them."
4. The build will run automatically. If it doesn't, click **Build Android APK**
   in the left sidebar → **Run workflow** → **Run workflow** button.
5. Wait 2-4 minutes for it to finish (green checkmark).
6. Click into the finished run → scroll to **Artifacts** → download
   `utkorsho-app-debug` → unzip it → you'll have `app-debug.apk`.
7. Transfer that APK to an Android phone and open it to install
   (you may need to allow "install from unknown sources" in phone settings).

## Notes

- This is a **debug build**, fine for personal use/testing. It is NOT signed
  for the Play Store — that requires a separate signing + release process.
- The app just loads your live website in a WebView. Any changes you make to
  the website show up in the app automatically — no rebuild needed.
- App name/icon are set to defaults. To customize the icon, replace files in
  `android/app/src/main/res/mipmap-*/` after the first build generates them,
  then re-run the workflow.
- iOS builds require a Mac and an Apple Developer account — GitHub Actions
  can do it but it's a heavier setup. Ask me if you want that next.

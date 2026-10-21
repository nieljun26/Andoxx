# Andoxx Android — Floating Quick Expense

This is a native Android Studio project source for an Android overlay companion. It is not the same as the existing Andoxx website yet.

## What it includes
- A draggable ₱ bubble that can appear above other apps after the user grants Android's “Display over other apps” permission.
- A compact expense form opened from the bubble without opening the main screen.
- Local expense records, daily income entry, daily remaining-money calculation, recent entries, delete, and JSON export.
- A persistent notification while the floating button service is running.

## Important limitation
The Android project currently stores data locally on the phone. It does **not** automatically sync with the existing Andoxx website at https://andoxx-bwhm1q.v2.appdeploy.ai/. Avoid treating the two sets of records as shared until a secure sync API is added.

## Build an APK
This environment does not have the Android SDK/Gradle installed, so it cannot produce or verify a compiled APK here. You can build the source using Android Studio:
1. Install Android Studio on a computer.
2. Open this folder as a project.
3. Allow Android Studio to install the requested Android SDK / Gradle components.
4. Select **Build → Build APK(s)**.
5. Install the generated debug APK from `app/build/outputs/apk/debug/app-debug.apk`.

Alternatively, push this project to a GitHub repository. The included GitHub Actions workflow builds a debug APK and makes it available as a workflow artifact.

## First launch
1. Open Andoxx.
2. Tap **Enable floating ₱ button**.
3. Allow **Display over other apps** for Andoxx in Android settings.
4. Return to Andoxx and tap **Enable floating ₱ button** again if needed.
5. The floating ₱ bubble can now be dragged and tapped over other apps.
6. Tap **Hide floating button** in the main app to stop it.

## Privacy
Expense data stays in this app's private local storage unless you explicitly export it. The floating service uses an ongoing notification so Android shows that it is active.

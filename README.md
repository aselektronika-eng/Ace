# Pellet Control — Android project starter

This is a native Android Studio project scaffold for an APK controlling an ESP32 over local Wi-Fi.

## Build APK
1. Open this folder in Android Studio.
2. Allow Gradle sync and install Android SDK Platform 35 if requested.
3. Select Build > Build Bundle(s) / APK(s) > Build APK(s).
4. The debug APK is normally created at `app/build/outputs/apk/debug/app-debug.apk`.

## Network/API
Default ESP32 IP is `192.168.4.1`. The app expects `/api/status` and `/api/command`.
See `firmware/PelletControl_API_Contract.ino.txt`.

## Current limitation
This archive contains the Android source project, not a compiled APK. This execution environment does not have Android SDK/Gradle installed, so it cannot compile or verify the APK here. It also does not yet include the actual ESP32 firmware for a specific stove.

## Safety
Do not use the UI to operate a real pellet stove until the ESP32 firmware, sensors, isolated outputs, original safety interlocks, and safe shutdown behavior have been tested. The UI's displayed values are live only when a compatible ESP32 API is running.

## Автоматско градење на APK (без Android Studio)
1. Направи бесплатен repository на GitHub и качи ги сите фајлови од овој folder (вклучително `.github`).
2. Отвори го табот **Actions** → **Build APK** → почекај ~5 минути.
3. Кликни на завршениот run → долу во **Artifacts** симни `PelletControl-APK` (zip со `app-debug.apk`).
4. Префрли го APK на телефонот и инсталирај го (дозволи „Install unknown apps“).

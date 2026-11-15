# ALTHAF, S TV Launcher (`com.tvlauncher.app`)

A native Kotlin Android TV 11+ (`minSdk 30`, `targetSdk 34`) HOME launcher with an Apple TV 4K-inspired dark interface, automatic installed app detection, horizontal app rows, full D-pad/OK/Back/Menu remote support, gallery wallpaper picker, and customization settings.

## Features
- **Default Android TV HOME Launcher**: Configured with `CATEGORY_HOME`, `CATEGORY_DEFAULT`, and `CATEGORY_LEANBACK_LAUNCHER` in `AndroidManifest.xml`.
- **Apple TV 4K-Inspired Dark UI**: Deep atmospheric themes (Midnight OLED, Apple TV Slate, Obsidian Blue, Cinema Amber) with spring focus animations and glowing focus rings.
- **Automatic App Detection**: Queries Leanback TV apps and optional sideloaded apps, and listens to live package install/uninstall broadcasts.
- **D-Pad Remote Support**: Full `DPAD` navigation, `OK` to launch, `Long-Press OK` or `Menu` for app options (Pin/Unpin, Move Left/Right, Hide, App Info, Uninstall), and `Back` handling.
- **Customization**: Themes, icon/card styles, corner radius, app sorting (Alphabetical, Recently Used, Custom Order), and gallery wallpaper picker with adjustable dimming.

## Building the Installable APK
1. Open the `AlthafTVLauncher` folder in **Android Studio** (or ensure Android SDK 34 & Gradle 8.2+ are installed).
2. Run:
   ```bash
   gradle assembleDebug
   ```
   (or `./gradlew assembleDebug` once Gradle wrapper is generated via `gradle wrapper`).
3. The installable APK will be generated at:
   `app/build/outputs/apk/debug/app-debug.apk`
4. Install on Android TV via ADB:
   ```bash
   adb install -r app/build/outputs/apk/debug/app-debug.apk
   ```

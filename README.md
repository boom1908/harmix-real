# Harmix

A native Android music streaming app built with Kotlin and Jetpack Compose.

## Tech Stack

- **Language**: Kotlin
- **UI**: Jetpack Compose + Material 3
- **Architecture**: MVVM with ViewModels
- **DI**: Hilt (Dagger)
- **Database**: Room (local) + Cloud Firestore (cloud sync)
- **Playback**: Media3 / ExoPlayer
- **Auth**: Google Sign-In via Firebase
- **Streaming**: yt-dlp (via Chaquopy Python bridge)
- **Build**: Gradle with KSP

## Building

### Prerequisites

- JDK 17
- Android SDK
- Python 3.12 (for Chaquopy)

### Build debug APK

```bash
cd android
chmod +x ./gradlew
./gradlew assembleDebug
```

The APK will be at `android/app/build/outputs/apk/debug/`.

### CI

Push to any branch triggers the GitHub Actions workflow (`.github/workflows/android-build.yml`) which builds a debug APK and uploads it as an artifact.

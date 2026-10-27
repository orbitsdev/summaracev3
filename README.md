# SummaRace v3

A reading game: read a story, race through questions, then sum it up. 30 stories (10 sessions x easy/average/hard).

The game is a web app (HTML + JavaScript + three.js) in `app/src/main/assets/www`. A small Android app hosts it in a WebView and gives it a bridge (`window.SummaRaceApp`) for speech, clipboard, sharing, saving records and exit.

This source was recovered from the SummaRace 1.2.0 test APK on 2026-10-16 after the original project folder was lost. Missing from the original: `build-voice.sh`, `CREDITS.md` and the "SummaRace Test" signing key.

## Run in a browser

    cd app/src/main/assets/www
    python -m http.server 8000

Then open http://localhost:8000. Opening index.html straight from disk won't load the scripts.

## Build the APK

Open the folder in Android Studio and build, or run `gradle assembleDebug` with the Android SDK installed. The APK lands in `app/build/outputs/apk/`.

A new signing key means phones with the old 1.2.0 test build must uninstall it first.

# LarpCraft APK (Capacitor wrapper)

Needs: Node 18+, Android Studio (includes JDK 17 + Android SDK).

1. Put Three.js next to the game (one-time download):
   curl -L -o www/three.min.js https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js
2. npm install
3. npx cap add android
4. npx cap sync
5. Build the APK, either:
   - npx cap open android  ->  Build > Build APK(s), or
   - cd android && ./gradlew assembleDebug
   Result: android/app/build/outputs/apk/debug/app-debug.apk
6. Copy the APK to your phone and install it (allow "install unknown apps").

Optional: lock landscape by adding android:screenOrientation="landscape" to the <activity> in
android/app/src/main/AndroidManifest.xml. Change appId in capacitor.config.json before publishing.
Debug APKs are for testing; a Play Store release needs a signed release build.

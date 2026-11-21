# Build Movai APK using only your phone

1. Create a new **private** GitHub repository named `movai`.
2. Upload the contents of this folder to the repository root (including the hidden `.github` folder).
3. In GitHub, open Actions → Build Movai Android APK → Run workflow.
4. Wait for the workflow to finish successfully.
5. Open the completed run and download the `movai-debug-apk` artifact. Extract the ZIP to get `app-debug.apk`.
6. Install the APK on Android. It is a debug build, not a Play Store release-signed APK.

Keep TMDB credentials out of public source files. Add the Read Access Token inside Movai Settings on the device.

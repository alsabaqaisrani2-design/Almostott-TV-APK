AlmostOTT - Android TV app (WebView wrapper for https://almostott.vercel.app/)

BUILD
1. Install Android Studio (free): https://developer.android.com/studio
2. File > Open > select this AlmostOTT folder. Wait for Gradle sync to finish.
3. Build > Build Bundle(s) / APK(s) > Build APK(s).
   APK location: app/build/outputs/apk/debug/app-debug.apk

INSTALL ON TV
- Pen drive: copy app-debug.apk to a USB stick, open it on the TV with a file manager app.
  (Enable "Install unknown apps" for that file manager.)
- Or with adb: TV Settings > About > tap Build 7 times > Developer options > enable
  Network/Wireless debugging, then:
     adb connect <TV-IP>:5555
     adb install app/build/outputs/apk/debug/app-debug.apk

REMOTE CONTROLS
- Arrow keys : move the on-screen cursor
- OK / Enter : click
- Cursor at top/bottom edge + arrow : scroll the page
- Cursor at left/right edge + arrow : scroll carousels horizontally
- Back       : browser back; exits full-screen video; exits app on the home page
- The cursor hides after 5 seconds. Press any arrow to show it again.

CHANGE THE URL: edit homeUrl in app/src/main/java/com/almostott/tv/MainActivity.kt

LOW-DATA OPTION (no Android Studio): build on GitHub for free
1. Create a free account at github.com and make a new repository (e.g. almostott-tv).
2. Click "uploading an existing file", drag in EVERYTHING inside the AlmostOTT folder
   (including the .github folder), and click Commit changes.
3. Open the Actions tab > "Build APK" > wait ~3-5 minutes for the green tick.
   (If it does not start, click "Run workflow".)
4. Open the finished run, download "AlmostOTT-apk" from Artifacts, unzip it -> app-debug.apk.
5. Copy the APK to the TV with a pen drive and install it.

MyTeaPotDemo
============

Proof of Concept getting the [Android NDK](https://developer.android.com/tools/sdk/ndk/index.html) TeaPot sample code working with Gradle based build.

Native Code Compilation
-----------------------
```bash
cd NDK_HOME/samples/Teapot
NDK_HOME/ndk-build
cd libs
cp -Rp * /MyTeaPotDemo/app/src/main/jniLibs
```

Build Android .apk
------------------
```bash
cd /MyTeaPotDemo
./gradlew clean assembleRelease

// Assembled .apk is located here
/MyTeaPotDemo/app/build/outputs/apk/app-release-unsigned.apk
```

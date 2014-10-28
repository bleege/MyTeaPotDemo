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
Contents Of .apk
----------------
```
assets/Shaders/ShaderPlain.fsh
assets/Shaders/VS_ShaderPlain.vsh
res/layout/activity_my.xml
res/layout/widgets.xml
res/menu/my.xml
AndroidManifest.xml
resources.arsc
res/drawable-hdpi-v4/ic_launcher.png
res/drawable-mdpi-v4/ic_launcher.png
res/drawable-xhdpi-v4/ic_launcher.png
res/drawable-xxhdpi-v4/ic_launcher.png
classes.dex
lib/arm64-v8a/libTeapotNativeActivity.so
lib/armeabi/libTeapotNativeActivity.so
lib/armeabi-v7a/libTeapotNativeActivity.so
lib/mips/libTeapotNativeActivity.so
lib/mips64/libTeapotNativeActivity.so
lib/x86/libTeapotNativeActivity.so
lib/x86_64/libTeapotNativeActivity.so
```

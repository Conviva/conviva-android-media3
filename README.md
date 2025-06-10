# conviva-android-media3

This module helps automate data collection from [Media3](https://github.com/androidx/media) player.

## Conviva Media3 module can be included in two ways in any Android app projects.

* Gradle dependency
* Offline library

## Gradle dependency
  Add the following line to app's build.gradle file.
    
    implementation 'com.conviva.sdk:conviva-media3-sdk:<version>'
    
## Offline library
  Place the Conviva library in app's 'lib' folder and add the following line to app's build.gradle file.
    
    implementation fileTree(dir: 'libs',include:['*.aar'])

## Support Conviva Android Core SDK Version
[Conviva Android CoreSDK v4.0.45 (or above)](https://github.com/Conviva/conviva-android-coresdk/releases/tag/v4.0.45)

## Support Android Version (minSdk)
  Android Lollipop (API level 21)

## Support Media3 ExoPlayer SDK Version    
  Media3 ExoPlayer 1.6.1 (or below)

## ProGuard rules
If you are using shrinkResources or minifyEnabled properties in the application to optimize the size of the APK file, then add the following in ProGuard rules:
```
-keep class com.conviva.playerinterface.** { *; }
-keep, allowshrinking class com.conviva.** { *; }
-dontwarn  com.google.android.exoplayer2.ExoPlayer.**, *
```

## Note:  

* Refer https://pulse.conviva.com/learning-center/content/main/main.htm for integration guidelines.
* Applications need to include `android.useFullClasspathForDexingTransform = true` in gradle.properties to avoid "Abstract Method Error" exception.

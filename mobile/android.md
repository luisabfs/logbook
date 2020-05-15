## [ERROR] Could not resolve project: *react-native-camera on Android*

In `android/app/build.gradle`, add: 

```
defaultConfig {
  missingDimensionStrategy 'react-native-camera', 'general'
}
```

[Link 1](https://github.com/react-native-community/react-native-camera/issues/2150#issuecomment-474098081) | [Link 2](https://github.com/react-native-community/react-native-camera/issues/2150#issuecomment-476011915)

## [ERROR] java.io.IOException: *Requested internal only, but not enough space*

Basically, the device I was using didn't have enough storage space for the APK to install.

[Link 1](https://stackoverflow.com/questions/54461288/installation-failed-with-message-error-android-os-parcelableexception-java-io)


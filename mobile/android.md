## [ERROR] cmdline-tools: could not determine SDK root

Since new updates, there are some changes that are not mentioned in the documentation. 

After unzipping the command line tools package, the top-most directory you'll get is `cmdline-tools`. 

Rename the unpacked directory from cmdline-tools to tools, and place it under `$C:/Android/cmdline-tools`, so looks like `$C:/Android/cmdline-tools/tools`

[Link 1](https://stackoverflow.com/a/65262939)

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


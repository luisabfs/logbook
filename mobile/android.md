## [ERROR] Could not resolve project: *react-native-camera on Android*

In `android/app/build.gradle`, add: 

```
defaultConfig {
  missingDimensionStrategy 'react-native-camera', 'general'
}
```

[Link 1](https://github.com/react-native-community/react-native-camera/issues/2150#issuecomment-474098081) | [Link 2](https://github.com/react-native-community/react-native-camera/issues/2150#issuecomment-476011915)

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

[Link](https://stackoverflow.com/questions/54461288/installation-failed-with-message-error-android-os-parcelableexception-java-io)

## [TIP] Change the navigation bar color where 'Home' and 'Back' buttons are

The property is called **navigationBarColor**. You can change it with a few options:

1. For those using `react-navigation v6`: 
    ```
    // in Navigator
    screenOptions={{navigationBarColor: 'gold'}}
    ```
2. For those using `react-native-cli`:
   ```
   // in android/app/src/main/res/values/styles.xml
   <style name="AppTheme" parent="Theme.AppCompat.Light.NoActionBar">
    <item name="android:navigationBarColor">#0D0D0D</item> <!--  ADD THIS LINE TO YOUR styles.xml    -->
    </style>
   ```
3. Add a plugin: https://github.com/thebylito/react-native-navigation-bar-color

[Link](https://stackoverflow.com/a/76516299/9725247)

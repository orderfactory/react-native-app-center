# react-native-app-center

## AppCenter sample of React Native Android application [TypeScript]

This application demonstrates *AppCenter* crash reporting feature for *React Native* Android applications.
Tested with Google API version 28 and Node v16.18.1. To run this application you will need some kind of Android environment, such as *Android Studio*.

If you encounter any issues with emulator, please configure the emulator to run Android 9.0 Google API version 28.

## Steps to Run

1. Go to https://appcenter.ms/ and create a new Android -- React Native application.
2. Edit the [appcenter-config.json](https://github.com/orderfactory/react-native-app-center/blob/main/ReactNativeAppCenter/android/app/src/main/assets/appcenter-config.json) file, and replace the `{APP_SECRET_VALUE}` with GUID from the *step 1* above.
3. Run `npm i`, from the *react-native-app-center/ReactNativeAppCenter* folder, to restore packages.
4. Start Android emulator.
4. Launch the application in RELEASE mode, from the *react-native-app-center/ReactNativeAppCenter* folder, using the following command:
```react-native run-android --mode release```
5. When the app starts, click the "EMULATE CRASH" button. This will cause the application to disappear.
6. Relaunch the application; crash report is sent to AppCenter when application restarts.
7. In a few minutes the crash report will show up in the Diagnostics blade of the app configured in the *step 1*.
8. Open the crash report in the AppCenter and observe that expected [attachment](https://github.com/orderfactory/react-native-app-center/blob/04f30954d29072e6cb7d3e9245d6e4a9a41fc70b/ReactNativeAppCenter/App.tsx#L79) is missing.

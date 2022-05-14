# axyojp-test-firebase-x-device

[Codelab: Firebase Cross Device Codelab](https://firebase.google.com/codelabs/cross-device-controller)

## tejun 
```
gibo dump macOS Dart Android VisualStudioCode Xcode > .gitignore

git submodule add https://github.com/FirebaseExtended/cross-device-controller.git
cp -pr cross-device-controller local_cross-device-controller 

# 不要なディレクトリなどを削除

cd local_cross-device-controller/starter_code
flutter pub get

flutter run -d web-server


iOS の場合でもこれで、先に open -a Simulator しておけば
Xcode とか起動しないでもビルドができるようになっている（前は Xcode からビルドしないとだめだった気がする）。
❯❯❯ flutter run
Multiple devices found:
Android SDK built for x86 (mobile) • emulator-5554                        • android-x86    • Android 8.1.0 (API 27) (emulator)
iPhone 13 Pro (mobile)             • 4C75F54D-1BFC-42F0-8D74-8A2DBE8AB898 • ios            • com.apple.CoreSimulator.SimRuntime.iOS-15-4 (simulator)
Chrome (web)                       • chrome                               • web-javascript • Google Chrome 101.0.4951.64
[1]: Android SDK built for x86 (emulator-5554)
[2]: iPhone 13 Pro (4C75F54D-1BFC-42F0-8D74-8A2DBE8AB898)
[3]: Chrome (chrome)
Please choose one (To quit, press "q/Q"):



flutter pub add firebase_core
firebase login
dart pub global activate flutterfire_cli
flutterfire configure
...
Platform  Firebase App Id
web       1:834729546603:web:59463db17ca382c7ba322e
android   1:834729546603:android:80a6ccad12b6eb80ba322e
ios       1:834729546603:ios:f33f94d9eb0769baba322e

Learn more about using this file and next steps from the documentation:
 > https://firebase.google.com/docs/flutter/setup


 # Add Code
import 'package:firebase_core/firebase_core.dart';
import 'firebase_options.dart';
 
void main() async {
 WidgetsFlutterBinding.ensureInitialized();
 await Firebase.initializeApp(
   options: DefaultFirebaseOptions.currentPlatform,
 );
 runApp(const MyMusicBoxApp());
}



flutter run



# OBJECTIVE: Enable email sign-in for Firebase Authentication
flutter pub add firebase_auth
flutter pub add provider
# コード修正


# OBJECTIVE: Create a sign in flow



```
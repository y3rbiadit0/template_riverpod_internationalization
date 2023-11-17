# Template [`Riverpod`](https://riverpod.dev/) + [`Flutter Internationalization`](https://docs.flutter.dev/ui/accessibility-and-internationalization/internationalization)

Simple Repo to have an easy way to start up a project with Internationalization already there.


## 1. Add Firebase Configuration using [FlutterFire](https://firebase.google.com/docs/flutter/setup?hl=es-419&platform=ios)
Steps:
1. `$firebase login` -- [Firebase CLI](https://firebase.google.com/docs/cli?hl=es-419#setup_update_cli)
2. `$dart pub global activate flutterfire_cli` -- Install FlutterFire CLI Tool
3. `$flutterfire configure` -- Configure your project
   - Will auto-generate files with the Firebase Credentials.
4. Finally add these lines to your `main` function to initialize Firebase with the credentials according the platfom.
```dart
  await Firebase.initializeApp(
    options: DefaultFirebaseOptions.currentPlatform,
  ); 
```
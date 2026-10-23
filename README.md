# 🚀 Connecting Flutter with Supabase

A step-by-step guide to connecting a Flutter application with Supabase.

## 🛠️ Technologies Used

- Flutter
- Dart
- Supabase
- PostgreSQL

---

## Step 1: Sign In to Supabase

Sign in to your Supabase account.

![Sign In to Supabase](https://raw.githubusercontent.com/ihsan7770/Superbase-Setup-Flutter/69c897f42237e145a10a602663a00168138e406e/superbase/signin.png)

---

## Step 2: Create a New Project

Click **New Project** to create a Supabase project.

![Create New Project](https://raw.githubusercontent.com/ihsan7770/Superbase-Setup-Flutter/69c897f42237e145a10a602663a00168138e406e/superbase/start%20new%20project.png)

---

## Step 3: Project Dashboard

After creating the project, the Supabase dashboard will appear.

![Supabase Project Dashboard](https://raw.githubusercontent.com/ihsan7770/Superbase-Setup-Flutter/69c897f42237e145a10a602663a00168138e406e/superbase/project%20created.png)

---

## Step 4: Get Project URL and API Key

Open your Supabase project settings and copy your Project URL and publishable API key.

![Get Project URL and API Key](https://raw.githubusercontent.com/ihsan7770/Superbase-Setup-Flutter/afaa5d28c542e4aa8affd5ab69874abc42230d99/superbase/TAKE2%20urls.png)

---

## Step 5: Install the Supabase Package

Run this command in your Flutter project terminal:

```bash
flutter pub add supabase_flutter


```bash
## Step 6: Initialize Supabase in Flutter

Open `lib/main.dart` in Visual Studio Code and initialize Supabase using your project credentials.

### Flutter Code

```dart
import 'package:flutter/material.dart';
import 'package:supabase_flutter/supabase_flutter.dart';

Future<void> main() async {
  WidgetsFlutterBinding.ensureInitialized();

  await Supabase.initialize(
    url: 'YOUR_SUPABASE_PROJECT_URL',
    anonKey: 'YOUR_SUPABASE_PUBLISHABLE_KEY',
  );

  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        appBar: AppBar(
          title: const Text('Flutter + Supabase'),
        ),
        body: const Center(
          child: Text('Supabase Connected Successfully!'),
        ),
      ),
    );
  }
}






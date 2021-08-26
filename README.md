# flutter_theme

- config/theme.dart
```dart
import 'package:flutter/material.dart';

ThemeData theme() {
  return ThemeData(
    scaffoldBackgroundColor: Colors.white,
    fontFamily: "Avenir",
    textTheme: textTheme(),
  );
}

TextTheme textTheme() {
  return TextTheme(
    headline1: TextStyle(
      color: Colors.black,
      fontSize: 32,
      fontWeight: FontWeight.bold,
    ),
    headline2: TextStyle(
    ),
    headline3: TextStyle(
    ),
    headline4: TextStyle(
    ),
    headline5: TextStyle(
    ),
    headline6: TextStyle(
    ),
    bodyText1: TextStyle(
    ),
    bodyText2: TextStyle(
    ),
  );
}
```

- main.dart
```dart
import 'package:flutter/material.dart';

import 'config/theme.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: theme(),
      onGenerateRoute: AppRouter.onGenerateRoute,
      initialRoute: HomeScreen.routeName,
    );
  }
}
```

- How to use
```dart
Text(
    this.title,
    style: Theme.of(context).textTheme.headline2!.copyWith(color: Colors.white),
)
```

---

```
Copyright 2021 M. Fadli Zein
```
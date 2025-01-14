# Stateless Widget

1. ```runApp()``` function in ```void main()``` for running widget's classes.

2. write ```runApp(const MyApp())``` if the constructor is const and write ```runApp(Mypp());``` when constructor is not const. 

3. when a constructor is const- 
    - both stateless and statefull classes' constructor could be kept constant even if key is passed to them.
    - if class has final or const member and constructor is initializing them than constructor could be const.
    - if we are passing constant variable than constructor could be kept constant.

4. for extending ```StatelessWidget``` class we should -
    - put a constructor with key.
    - override build method.

5. ```build``` methods hold and returns a widget tree which is a part of user interface

6. ```BuildContext context``` provides information of widget in widget tree. use cases of build context are as following:-
    - it allows widgets to access inherited widgets (e.g., ```Theme```, ```MediaQuery```) higher up the widget tree.
    - helpfull in navigation
    - can retrieve screen size or orientation using ```MediaQuery```
    - ```build``` function is called whenever the ```setState``` function is called. 

```dart
import 'package:flutter/material.dart';

void main() {
    runApp(const MyApp(name: "puneet"));
}

class MyApp extends StatelessWidget {
    
    final String name;
    const MyApp({super.key, required this.name});

    @override
    Widget build (BuildContext context) {
        return const MaterialApp();
    }
}
```
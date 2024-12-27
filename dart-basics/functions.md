# 4 Functions in Dart

## 4.1 Named Functions
normal functions
```dart
int add(int a, int b) {
    return a+b;
}
```

## 4.2 Arrows Function
A shorthand for one-line functions.
```dart
int add(int a, int b) => a + b;
```

## 4.3 Parametrized Function

1. **Positional Parameter**
    * variables which are inclosed in ```[]``` are optional and other are necessary
    * All optional parameters must be enclosed within square brackets ```([])``` and placed after all required parameters in a function signature.
    * All optional parameters should either be nullable or should be declared in function signature in case user don't pass any value.

    ```dart
    int add(int a, [int b = 0, int c = 0]) {
        return a + b + c;
    }
    ```

2. **Named Parameters**

    * all parameters in a named parameterized function should be inclosed in ```{}```
    * required parameters written after ```required``` and optional parameters are written as it is.
    * optional parameters must be either nullable or declared within function signature in case user don't pass any value.

    
    ```dart
    void profile({required String name, int rollNo = 0}) {
        print(rollNo);
    }
    ```
# 1 Variables
## 1.1 Data Types
following are the diffferent data types which can be used :-
1. int
2. double
3. String
4. bool
5. List
6. Map
7. Dynamic
8. Null
9. Symbols
10. Records
11. Runes
## 1.2 Non-Nullable and Nullable Variable
a nullable variable is that variable which can take its respectie data type values along with **null value**.
- **Non-Nullable variable**
    1. should be initialized
        ```dart
        int x; // Error : non nullable variable must be initialized.
        ```
   2. can't store null value in its entire life time
        ```dart
        int x = 90;
        x = null; // Error
        int y = null; //Error
        ```
- **Nullable Variable**
    1. need not to be initialized
        ```dart
        int? x;
        ```
    2. can aquire null value at any time
        ```dart
        int ? x = 90;
        x = null;
        ```
## 1.3 **var**, **const** and **final** keywords
- **var Variable**
    1. A var variable can't be given specific data type like int, double, etc.
        ```dart
        var x; // no Error
        var int x; // Error
        ```
    2. If var variable is not initialized while declaration than it could store any data type value in its lifetime
        ```dart
        var x;
        x = 90;
        x = "hehe"
        x = null;
        ```
    3. If var variable is initialized while declaration than it is restricted to store same data type in its entire lifetime.
        ```dart
        var x = 23; // now x can store only int values
        x = 78;
        x = "hello"; // Error
        ```
- **const Variable**
    1. can give specific data type to const variable.
        ```dart
        const int x = 23;
        ```
    2. should be initialized during compile time and then it becomes immutable.
        ```dart
        const int x = DateTime.now(); // Error - its runtime not compile time
        const int y = 89; // no Error
        y = 89; // Error - can't change const variable value
        ```
- **final Variable**
    1. can give specific data type to final variable.
        ```dart
        final int x = 23;
        ```
    2. should be initialized but it could be both compile-time or run-time after which it become immutable.
        ```dart
        final int x = 23; // no Error
        final DateTime y = DateTime.now(); // no Error
        x = 90; // Error
        ```
## 1.4 **dynamic** Variable

can aquire any data type value in its entire lifetime. 
```dart
dynamic x;
x = 90;
x = null;
x = "hello";

dynamic y = 90;
y = "hello";
y = null;
```

## 1.5 **"record"** Variable
there is no specific data type for record in dart 3.0. but this is how it works. 
They are immutable
1. Unnamed record
    ```dart
    var record = (1, 2, "hello");
    print(record.$2); // 2
    ```
2. named record
    ```dart
    var record = (enroll_no : 2726, marks : 20, name : "Puneet");
    print(record.enroll_no);
    ```

## 1.6 **List** Variable

act much like python's list
```dart
List list = ["hehe", 89, {"name": "puneet"}];
list[0] = "hello";
print(list[2]);
```

but we can make it restricted
```dart
List<double> list = [12, 23, 23.34]; //here int is explicitly being converted to double
```

**Operations** -
1. append - add(element)
    ```dart
    List list = [1,2,3];
    list.add(4);
    ```
2. insert - insert(index, element)
    ```dart
    List list = [1,2,3];
    list.insert(0,0);
    ```
3. remove - remove(element)
    ```dart
    List list = [1, 2, 3];
    list.remove(2);
    ```
4. length of list
    ```dart
    List list = [1, 2, 3];
    print(list.length);
    ```
## 1.7 **Map** Variable

non restricted map (similar to python's dictionary)
```dart
Map dict = {"name": "puneet", "enroll": 2726};
dict["name"] = "priyank";
dict["status"] = "good";
print(dict["name"]);
```

restricted map
```dart
Map<String, double> dict1 = {"gpa": 8.3, "cgpa": 8.4};
```

we can also access its keys and values seperatly in form of records :- 
```dart
Map dict = {"name": "puneet", "enroll": 2726};
var dict_keys = dict.keys;
var dict_values = dict.values;
```
## 1.8 **Set** Variable
unrestricted set (just like python) and it is mutable
```dart
Set set = {1, 2, 3, 3, 3, "hehe"};
print(set); //{1,2,3}
```

restricted set
```dart
Set<int> set = {1,2,3};
```
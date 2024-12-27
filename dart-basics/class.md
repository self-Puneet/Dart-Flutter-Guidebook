# 5 Class

## 5.1 Priate Members and Methods
* we don't have any public, protected or private keywords in dart.
* member or method whose name is followed by ```_``` are private. eg - ```_var1```.
* a private member or method could freely be used within its own file but can't be used at all outside the file.

```dart
// custructor with private members
class Class {
    int _name;
    Class(this._name);                                  ✅
    Class({this._name});                                ❌
    Class({required this._name});                       ❌
    Class({required this.name}): this._name = name;     ✅
    Class({this.name}): this._name = name;              ✅
}
```

## 5.2 Constructor
```dart
class CustomClass {
  String name;
  int enroll;
  CustomClass(this.name, this.enroll);
}
```

## 5.3 Getter ad Setter

getter - ```get <return-type> <getter-name> => <return-value>```.

setter - ```set <setter-name> () {}```

setter allows user to set the value of a private member without letting know that it was a private member.
```dart
class CustomClass {
    String name;
    int _enrollNo;
    CustomClass (this.name, this.enrollNo);
    
    // getter
    String get getName => name;
    int get enrollNo => _enrollNo;

    // setter for private member
    set setEnroll (int enroll) {
        _enrollNo = enroll;
    }

    // setter for public member
    set setName (String name) {
        this.name = name;
    }
}


void main() {
    CustomClass obj = CustomClass("Puneet", 2726);
    
    // using setter
    obj.setName = "Yash";
    obj.setEnroll = 2800;

    // using getter
    print("Name - " + obj.getName);
    print("enrollment no - " + obj.getEnroll)
}
```

## 5.4 Static Members and Methods
setter and getter couldn't be set as static.
```dart
class Class {
    static int a = 90;
    static void increment () {
        a++;
    }
}

void main() {
    print(Class.a);
    Class.increment();
    pirnt(Class.a);
    // Class.a      ✅
    // Class().a    ❌
}
```

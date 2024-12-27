# 7 CLass Types

## 7.1 Sealed Class
1. It can neither be implemented nor extended outside the file.
2. If we switch case a obj than all the sub classes should be included into the cases otherwise copile time error will occur.
3. This class can't be instatiated
4. any type of class could be its child class


## 7.2 Final Class
1. It can neither be implemented nor extended outside the file.
2. If we switch case a obj than all the sub classes may or may not be included into the cases.
3. This class can be instatiated.
4. Only a final or base or sealed class could be its child class.

## 7.3 Base Class
1. Can be extended but can't be implemented.
2. All the subclases of a base class should be base or final or sealed.

## 7.4 Interface Class
1. Can't be extended neither in file nor outside it
2. However this is not really a interface like java one because it could still be instantiated. we can even have method implementation within it.
3. **interface abstract class** - It is a true interface from java.


## 7.5 Generic Class
Template class from C++.
```dart
class Class2<T> {
  T? a;
  Class2({required this.a});
}
```

## 7.6 Mixins

1. A mixin is a class-like structure that can be "mixed into" other classes, allowing those classes to inherit its methods and properties without needing to be part of an inheritance hierarchy

2. we can make a mixin class also. but any normal class can't be used as mixin or mixin class i.e. can't be used with ```with``` keyword.

```dart
mixin group1 {
  void hehe() {
    print("hehe");
  }
}

mixin group2 {
  void hehe1() {
    print("jeje");
  }
}

class Class with group1, group2 {
  void hehe2() {
    hehe();
    hehe1();
  }
}

void main() {
  Class obj = Class();
  obj.hehe2();
}
```
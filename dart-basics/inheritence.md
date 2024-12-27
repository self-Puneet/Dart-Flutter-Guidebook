# 6 Inheritence

* inheritence keyword - ```extends```

* If members or methods are defined in the child class and also exist in the parent class, creating an object of the child class will invoke the implementation from the child class, not the parent class

* no multiple inheritence is allowed using simple class but can be done using abstract classes or mixins

* we can use super keyword to get the member and methods of parent class

## 6.1 Referencing
```dart ParentClass obj = ChildClass();```

Here, "obj" is an instance of ChildClass, but it is referenced by a ParentClass type.

**Why is this useful?**
- This approach allows you to store objects of multiple subclasses of the same parent class in a single variable. 
- Instead of creating separate objects for each subclass, you can reference them through the parent class type, enabling polymorphism and more flexible code.

**However,** 
- When using "obj" as a ParentClass reference, you can only access members or methods that are defined in ParentClass. 
- Additional members or methods specific to ChildClass cannot be accessed through this reference, buttt this could be solved by explicitly type casting parentClass object into childClass.

```dart
class ParentClass {
    void walk() {
        print("walk");
    }
}

class ChildClass extends ParentClass{
    void run() {
        print("run");
    }
}

void main() {
    ParentClass obj = ChildClass();
    obj.walk();                     ✅
    obj.run();                      ❌
    (obj as ChildClass).run();      ✅
}
```

## 6.2 Abstraact Class and Interface

* we can implement a class also. but in that case we need to override each and every member and method which are there in parent class.

    ```dart
    class Class {
    int a = 90;
    void hehe() {
        print("hehe");
    }
    }

    class Class1 implements Class {
    @override
    int a = 90;

    @override
    void hehe() {}
    }
    ```

* if a class is abstract than a method may or may not have implementation. but if class is not abstract than method should definitly have implementation.

    ```dart
    abstract class AbstractClass {
    int b = 90;
    void walk();
    }
    ```

* one class can implement multiple abstract or normal classes at a same time.

* same class couldn't be implemented and extended at same time.

* we can't use super keyword when we implements a class inside child class.
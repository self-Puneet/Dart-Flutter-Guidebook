# 2 Conditional Statements

## 2.1 Ternary Operator
(**condition**) ? (**statement if condition is true**) : (**statement if condition is false**)
```dart
bool var1 = (2 > 3) ? true : false;
```

## 2.2 Switch Case

```dart
int var1 = 9;

switch (var1) {
    case (var1 % 2 != 0) :
        print("variable is odd");
        break;
    case (var1 % 2 == 0):
        print("variable is even");
        break;
    default():
        print("number is neither even nor odd");
        break;
}
```

## 2.3 if-else

same as other languages

# 3 Iterative Statements

1. for loop
2. while loop
3. do-while loop
4. for-in loop
5. for-each loop

## 3.1 for-each loop
Calls a function for each element in the collection
```dart
void evenOdd(int a) {
    if (a % 2 != 0) {
        print("even");
        return;
    }
    else {
        print("odd");
        return;
    }
}

void main() {
    List list = [1,2,3,4,5]
    list.forEach((i) {
        evenOdd(i);
    });
}
```

## 3.2 Labeling loops
labels for break and continue - we can assign a name to a perticular loop in a nested system of loop and at any time to break any particular loop. we can write 'break label_of_loop;'
```dart
outerLoop : for (int i = 0; i < 10; i++) {
    innerLoop : for (int j = 0; j < i ; j++) {
        break outerLoop;
    }
}
```

## 3.3 for-in loop
just like in java
```dart
List list = [1, 2, 3, 4];

for (int i in list) {
    print(i);
}
```
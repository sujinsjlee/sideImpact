## Lists

```dart
void main() {
    var numbers1 = [
        1,
        2,
        3,
        4,
    ];
    List<int> numbers2 = [
        1,
        2,
        3,
        4,
    ];
    numbers1.add(1);
}
```

- **collection if**

```dart
void main() {
    bool giveMeFive = true;
    List<int> numbers = [
        1,
        2,
        3,
        4,
        if (giveMeFive) 5,
    ];
    print(numbers)
}
```

## String Interpolation

- **collection for**
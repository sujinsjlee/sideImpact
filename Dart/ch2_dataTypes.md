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

- insert variable inside the text

```dart
void main() {
    var name = 'jay';
    var age = 20;
    var greeting = "Hello everyone, $name, I'm ${age + 5}";
    print(greeting)
}
```

## Collection For

```dart
void main() {
    var oldFriends = ["ace", "bread"];
    var newFriends = [
    "tom",
    "jon",
    for (var friend in oldFriends) "❤️ $friend"
    ];

    print(newFriends); // [tom, jon, ❤️ ace, ❤️ bread]
}
```

## Maps

```dart
 Map <int, bool> player =  {
    1: true,
    2: false,
 }

var player =  {
    1: true,
    2: false,
 }

List<Map<Srting, Object>> players = [
    {
        'name': 'jay',
        'xp': 999,
    },
    {
        'name': 'tom',
        'xp': 8888,
    },
]
```

## Sets
- `Set` make sure all the data are **unique**

```dart
Set<int> numbers = {1,2,3,4};
var numbers = {1,2,3,4};
```

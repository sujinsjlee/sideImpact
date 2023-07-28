## Defining a Function
- in case the function has only one line, we can use **=>**

```dart
String sayHello(String name) => "Hello ${name} nice to meet you.";

num plus(num a, num b) => a + b;

void main() {
    print(sayHello("sugar"));
}
```

## Named Parameters

```dart
String sayHello({
    required String name,
    required int age,
    required String country
}) => return "Hello $name, age: $age, country $country";

void main() {
    print(sayHello({
        age: 40,
        name: "jay", // order doesn't matter
        country: "korea",
    }));
}
```

## Optional Positional Parameters

```dart
String sayHello(
    String name, 
    int age,
    [String? country = "Canada"]) {
    return 'Hello ${name}, You are ${age} from the ${country}';
}

void main() {
    var result = sayHello("jay", 10);
    print(result);
}
```

## QQ Operator

- left `??` right :
    - if left is null, then it will give you the right

```dart
String capitalizeName(String? name) =>return name?.toUpperCase() ?? "JAY";

void main() {
    capitalizeName(null); //JAY
}
```

```dart
void main() {
    String? name;
    name ??= 'jay'; // if name is null assign jay
    name ??= 'another'; // if name is null assign another
    print(name); // jay
}
```


## Typedef

- alias

```dart
typedef ListOfInts = List<int>;

ListOfInts reverseListOfNumbers(ListOfInts list) {
    var reversedList = list.reversed.toList();
    return reversedList;
}
```

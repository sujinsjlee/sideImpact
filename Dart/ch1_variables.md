# Variables

## main

```dart
void main() {
    print('hello world');
}
```

## variable
- `var` : No need to explicitly define type
- Explicitly define type of the variable

```dart
void main() {
    var name1 = 'jay';
    String name2 = 'dale'; 
}
```

## Dynamic Type

- If you don't assign value the type is dynamic
- `dynamic` is the type, `var` is to create a variable.

```dart
void main(){
    dynamic name;
    if(name is String) {
        ////
    }
}
```

## Nullable Variables

- [Null Safety](https://dart.cn/codelabs/null-safety#:~:text=If%20you%20want%20a%20variable,or%20it%20can%20be%20null.)

- If you want a variable of type String to accept any string or the value null, give the variable a nullable type by adding a question mark (?) after the type name. For example, a variable of type String? can contain a string, or it can be null.

```dart
void main(){
    String name = "jay";
    jay = null; // !!!ERROR
}

void main(){
    String? name = "jay";
    jay = null;
    if(jay != null){
        jay.isNotEmpty;
    }
}

void main(){
    String? name = "jay";
    jay = null;

    // The following calls the 'isNotEmpty' only if jay is not null
    jay?.isNotEmpty;

    // The following calls the 'action' method only if nullableObject is not null
    nullableObject?.action();
}

```

## Final Variables

- Just like const, dart has keyword as `final`

```dart
void main() {
    final name = "pizza";
    name = "ham"; // !!!cannot update

    final String username = "tom";
    name = "tom2"; // !!!cannot update
}
```

## Late Variables

- `late` : create data without data, and **later** enter the value

```dart
void main() {
    late final Srting name;
    // do something, go to api
    name = 'jay';
    print(name);
}
```

## Const Variables

- **compile time constant** : If you know the value before the application goes into the appStore(compilation time), it should be defined as `const`

```dart
void main() {
    const API = fetchApi();
}
```

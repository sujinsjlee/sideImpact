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
    String name2 = 'jain'; 
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

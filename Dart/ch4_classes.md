## Constructors

```dart
class Player {
    late final String name; // this variable will get the value later 
    late final int age;

    Player(this.name, this.age); // wOW....
}

void main(){
    var player = Player("jay", 15);
}
```

<!--SO COOOOOOLLLL!!!!!-->

## Named Constructor Parameters


```dart
class Player {
    late final String name; // this variable will get the value later 
    late final int age, xp;
    late String team;

    Player({
        required this.name, 
        required this.age,
        required this.team,
        required this.xp,
    }); 
}

void main(){
    var player = Player(
        name: "jay", 
        age: 15, 
        team: 'RED',
        xp: 1000,
    );
}
```

## Named Constructors

```dart
class Player {
    late final String name; // this variable will get the value later 
    late final int age, xp;
    late String team;

    Player({
        required this.name, 
        required this.age,
        required this.team,
        required this.xp,
    });

    Player.createBluePlayer({
        required String name,
        required int age,
    }) : this.age = age,
         this.name = name,
         this.team = 'blue',
         this.xp = 0;   // name of the constructor is createBluePlayer
}

void main(){
    var player = Player.createBluePlayer(
        name: 'jay',
        age: 21,
    );
}
```


```dart
class Player {
    final String name;
    int xp;
    String team;

    Player.fromJson(Map<String, dynamic> playerJson) 
        : name = playerJson['name'],
          xp = playerJson['xp'],
          team = playerJson['team'];
    void sayHello() => print("Hi my name is $name");
};

int main() {
    var apiData = [
        {
            "name": "jay",
            "team": "RED",
            "xp": 0,
        },
        {
            "name": "anna",
            "team": "BLUE",
            "xp": 0,
        },
    ];

    apiData.forEach((playerJson) {
        var player = Player.fromJson(playerJson);
        player.sayHello();
    })
}
```

## Cascade Notation
<!-- COOOOOOOOOLLLLLLL!!!!!-->

```dart
class Player {
    late final String name; // this variable will get the value later 
    late final int age, xp;
    late String team;

    Player({
        required this.name, 
        required this.age,
        required this.team,
        required this.xp,
    });

    void sayHello() => print("Hi my name is $name");
}

void main(){
    var player = Player(name:'jay', xp:1200, team:'RED', age:29);
    var apple = player
     ..name = 'mi'
     ..xp = 120000
     ..team = 'blue'
     ..sayHello(); // woW..
}
```

<!-- COOOOOOOOOLLLLLLL!!!!!-->
<!-- COOOOOOOOOLLLLLLL!!!!!-->
<!-- COOOOOOOOOLLLLLLL 아 근데 .. 이게 되게 장난치는 것같아 ㅋㅋㅋㅋ!!!!!-->



## Enums


```dart
enum Team {red, blue} // it doesn't have to be "~~", quotation mark is not needed

class Player {
    late final String name;
    late final int age, xp;
    late Team team;

    Player({
        required this.name, 
        required this.age,
        required this.team,
        required this.xp,
    });

    void sayHello() => print("Hi my name is $name");
}

void main(){
    var player = Player(name:'jay', xp:1200, team: Team.red, age:29);
    var apple = player
     ..name = 'mi'
     ..xp = 120000
     ..team = Team.blue
     ..sayHello();
}
```

## Abstract Classes

```dart
abstract class Human {
    void walk();
}

enum Team {red, blue} 

class Player extends Human{
    late final String name;
    late final int age, xp;
    late Team team;

    Player({
        required this.name, 
        required this.age,
        required this.team,
        required this.xp,
    });

    void sayHello() => print("Hi my name is $name");
    void walk() {
        print("I am walking");
    }
}
```

## Inheritance

```dart
enum Team {red, blue} 

class Human {
    final String name;
    Human({required this.name});
    void sayHello(){
        print("Hello! $name");
    }
}

class Player extends Human {
    final Team team;
    Player({
        required this.team,
        required String name,
    }) : super(name: name);

    @override
    void sayHello(){
        super.sayHello();
        print('and I play for ${team}');
    }
}
```


## Mixins

- mixins are normal classes whose method can be used in another class without extending the class. In dart, we can do this by using the keyword `with`

- When you `extends` the class, the class you extend from becomes your parent and you have access to **super**, and the class become an instance of that parent class

- with mixins, all you do is you basically just get their properties and get their method. 
    - **the criteria to be mixins : you should be a class without a Constructor**

```dart
class Tall {
final double tall = "190.00"
}

class Human with Tail {
//..
}
```
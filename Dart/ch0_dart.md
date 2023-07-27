# Dart
- Dart offers sound null safety
<!--
JIT는 개발자가 코드를 디버깅하거나 개발 중간에 빠른 피드백을 받기 위해 사용되며, AOT는 앱이 배포되는 시점에 미리 컴파일하여 빠르게 실행할 수 있도록 합니다.

JIT는 JIT(Just-In-Time)의 약자로 미리 코드가 아닌 런타임에 코드를 기계 코드로 컴파일하는 컴파일러 유형이다. 이를 통해 코드를 보다 효율적으로 실행할 수 있을 뿐만 아니라 최종 실행 파일의 크기도 줄일 수 있다.

JIT 컴파일러는 dart VM을 사용하는데 코드의 결과를 바로 화면에 보여준다.
JIT 컴파일러는 오직 개발중일 때만 사용한다.
따라서 Flutter를 개발할 때 사용하고 있는 hot-reload는 JIT 컴파일러 덕분에 가능하다.

AOT는 실행 전에 코드를 기계 코드로 컴파일하는 컴파일러 유형인 Ahead-Of-Time의 약자이다.
AOT 컴파일러는 일반적으로 해석된 코드에 비해 더 빠르고 더 작은 실행 파일을 생성하지만 변경 사항이 있을 때마다 코드를 다시 컴파일해야 하며 컴파일 프로세스가 더 오래 걸릴 수 있다.

iOS, Android, Widows, Mac 등을 위해 컴파일한다는 건 많은 최적화와 기계어로 변환 작성하는 등 많은 작업이 필요로 하기 때문에 시간이 오래 걸린다.

개발모드에서 변경한 코드에 대한 결과를 보고 싶을때마다 처음부터 모든걸 컴파일한다고 하면 개발 경험이 매우 좋지 않다.
이 상황에서는 JIT 컴파일러를 사용해야한다.
-->
- **JIN** : Just In Time Compiler
    - In the JIT mode, the Dart VM can dynamically import Dart source, parse it, and instantly compile it to native machine code so that it can be executed. Debugging, hot reloading, and other features are available in this mode, which is used when developing a program. JIT only compiles the exact amount of code required. JIT also features incremental recompilation, allowing it to only recompile the compiled code as required.
- **AOT** : Ahead of Time Compiler
    - The dynamic loading, parsing, and assembly of Dart source code are not supported by the Dart VM in the AOT mode. It can only be used to import and run precompiled machine code. The entire source code is compiled into machine code that the platform can handle natively by the ahead-of-time compiler. This is done prior to the platform running the application.
- [dartpad.dev]()dartpad.dev
- [dartpad.dev]()
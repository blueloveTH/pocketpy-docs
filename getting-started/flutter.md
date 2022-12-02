---
icon: package
label: Flutter
order: 4
---

## Installation

```
flutter pub add pocketpy
```

## Usage

```dart
import 'package:pocketpy/pocketpy.dart' as pkpy;

pkpy.VM vm = pkpy.VM();

String code = 'print("Hello World!")';
vm.exec(code);

var _o = vm.readOutput();
print(_o.stdout)
print(_o.stderr)
```
---
icon: code
label: Flutter
order: 4
---

## Installation

```
flutter pub add pocketpy
```

## Example

```dart
import 'package:pocketpy/pocketpy.dart' as pkpy;

pkpy.VM vm = pkpy.VM();

String code = 'print("Hello World!")';
vm.exec(code);

var _o = vm.read_output();
print(_o.stdout)
print(_o.stderr)
```
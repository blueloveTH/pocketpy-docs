---
icon: package
---

# Flutter-API

```dart
import 'package:pocketpy/pocketpy.dart` as pkpy;
```

## pkpy.VM Class

#### `VM()`

Create a virtual machine.

#### `bool exec(String code)`

Run a given source on a virtual machine. Return `true` if there is no error.

#### `PyObject? eval(String code)`

Evaluate a python expression. If there is any error, return `null`.

#### `PyObject? getGlobal(String name)`

Get a global variable of a virtual machine. If not found, return `null`.

#### `PyOutput readOutput()`

Read the standard output and standard error as string of a virtual machine. After this operation, both stream will be cleared.

#### `bool addModule(String name, String code)`

Add a source module into a virtual machine. Return `true` if there is no error. You can use `import` statement to load it later.

#### `void dispose()`

Release the internal pointer.
After this operation, you should not access to this object anymore.

## pkpy.REPL Class

#### `REPL(VM vm)`

Create an interactive console for running python code on a virtual machine.

#### `ReplInputResult input(String code)`

Input a source line to an interactive console.

#### `void dispose()`

Release the internal pointer.
After this operation, you should not access to this object anymore.


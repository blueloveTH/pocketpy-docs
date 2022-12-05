---
icon: code
label: Godot Engine
order: 2
---

## Introduction

PocketPy for Godot is a [Custom C++ module](https://docs.godotengine.org/en/stable/development/cpp/custom_modules_in_cpp.html).

To integrate it, you need to:

1. [Download the source code of Godot](https://docs.godotengine.org/en/stable/development/compiling/index.html)

2. Find a directory named `modules`. It is located in the root path

3. Download `pocketpy.zip` and extract it into `modules` directory

4. Recompile the engine

## Example

```gdscript
def _ready():
    var pkpy = PocketPy.new()

    # Create a virtual machine
    var vm = pkpy.new_vm()

    # Run a script
    pkpy.vm_exec(vm, "print('Hello World!')")

    # Read the output
    var _o = pkpy.vm_read_output(vm)

    # Parse the output
    var res = JSON.parse(_o).result

    # Print the output
    print(res["stdout"])    # "Hello World!\n"
```
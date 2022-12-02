---
icon: package
---

# C-API

## VM

#### `VM* pkpy_new_vm(bool use_stdio)`

Create a virtual machine.
Return its pointer.

+ `use_stdio`, whether to use `std::cout` and `std::cerr` as the standard output and standard error stream.

#### `bool pkpy_exec(VM* vm, const char* source)`

Run a given source on a virtual machine.
Return `true` if there is no error.

+ `vm`, pointer of the virtual machine
+ `source`, the given source

#### `PyObjectDump* pkpy_eval(VM* vm, const char* source)`

Evaluate a python expression. If there is any error, return `nullptr`.

This function returns a struct pointer of `PyObjectDump`.
You need to call `pkpy_delete` to release the memory of the returned `PyObjectDump*`.

+ `vm`, pointer of the virtual machine
+ `source`, the source the expression

#### `PyObjectDump* pkpy_get_global(VM* vm, const char* name)`

Get a global variable of a virtual machine. If not found, return `nullptr`.

This function returns a struct pointer of `PyObjectDump`.
You need to call `pkpy_delete` to release the memory of the returned `PyObjectDump*`.

+ `vm`, pointer of the virtual machine
+ `name`, the variable name

#### `PyOutputDump* pkpy_vm_read_output(VM* vm)`

Read the standard output and standard error as string of a virtual machine. Note the `vm->use_stdio` should be `false`.
After this operation, both stream will be cleared.

This function returns a struct pointer of `PyOutputDump`.
You need to call `pkpy_delete` to release the memory of the returned `PyOutputDump*`.

+ `vm`, pointer of the virtual machine

#### `bool pkpy_add_module(VM* vm, const char* name, const char* source)`

Add a source module into a virtual machine.
Return `true` if there is no error.
You can use `import` statement to load it later.

+ `vm`, pointer of the virtual machine
+ `name`, the name of the module
+ `source`, the source of the module

## REPL

#### `REPL* pkpy_new_repl(VM* vm)`

Create an interactive console for running python code on a virtual machine.
Return its pointer.

+ `vm`, pointer of the virtual machine

#### `int pkpy_repl_input(REPL* r, const char* line)`

Input a source line to an interactive console.
Return `0` if need more lines, `1` if execution happened, `2` if execution skipped (i.e. compile error or empty string).

+ `r`, pointer of the interactive console
+ `line`, the source line

## Others

#### `void pkpy_delete(void* p)`

Delete any resource allocated by `pkpy_xxx_xxx`.
It can be `VM*`, `REPL*` or `PyXXXDump*`, etc.

Deleting a pointer not allocated by `pkpy_xxx_xxx` is not work. But no errors.
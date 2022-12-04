---
label: "Host:arrow_right:Py"
icon: dot
---

Call Python function from host language is easy.
`eval()` is the most powerful way to interact with Python.
You can access any Python object by using `eval()`,
such as getting a variable, calling a function, etc.

For simple cases, you can also try `get_global()`,
it reads a global variable and returns a json representation of it.

### `String? get_global(String)`
Get a global variable of a virtual machine.

Return a json representing the result.
If the variable is not found, return `null`.

### `String? eval(String)`
Evaluate an expression.

Return a json representing the result.
If there is any error, return `null`.

!!!
Though `eval()` is powerful, it may be unsafe in threaded virtual machine.
If you encounter a crash, please report it.
!!!


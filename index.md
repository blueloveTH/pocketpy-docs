---
icon: home
label: Welcome
---

# Welcome to PocketPy

PocketPy is a lightweight Python interpreter for game engines.

![](./static/logo_flat.png)

## Features

| Name            | Example                    | Supported |
| --------------- | -------------------------- | --------- |
| List            | `[1, 2, 'a']`              | YES       |
| ListComp        | `[i for i in range(5)]`    | YES       |
| Dict            | `{'a': 1, 'b': 2}`         | YES       |
| If Else         | `if..else..elif`           | YES       |
| Loop            | `for/while/break/continue` | YES       |
| Import          | `import/from..import`      | YES       |
| F-String        | `f-string`                 | YES       |
| Unpacking       | `a, b = 1, 2`              | YES       |
| Star Unpacking  | `a, *b = [1, 2, 3]`        | NO        |
| Throw Exception | `assert/raise`             | YES       |
| Catch Exception | `try..catch`               | NO        |
| Eval            | `eval()`                   | YES       |
| Function        | `def f(x,*args,y=1):`      | YES       |
| Function KwArgs | `def f(**kwargs):`         | NO        |
| Class           | `class A:`                 | YES       |
| Subclass        | `class A(B):`              | YES       |
| Context Block   | `with <expr> as <id>:`     | YES       |



## Extra Features

For features that are PocketPy specific, see [Extra Features](/extras/goto).

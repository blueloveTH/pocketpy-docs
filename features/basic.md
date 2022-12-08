---
icon: dot
order: 100
---

# Basic Features

The following table shows the basic features of PocketPy with respect to [CPython](https://github.com/python/cpython).
The features marked with `YES` are supported, and the features marked with `NO` are not supported.

| Name            | Example                    | Supported |
| --------------- | -------------------------- | --------- |
| If Else         | `if..else..elif`           | YES       |
| Loop            | `for/while/break/continue` | YES       |
| Function        | `def f(x,*args,y=1):`      | YES       |
| Function `**`   | `def f(**kwargs):`         | NO        |
| Subclass        | `class A(B):`              | YES       |
| List            | `[1, 2, 'a']`              | YES       |
| ListComp        | `[i for i in range(5)]`    | YES       |
| Slice           | `a[1:2], a[:2], a[1:]`     | YES       |
| Tuple           | `(1, 2, 'a')`              | YES       |
| Dict            | `{'a': 1, 'b': 2}`         | YES       |
| F-String        | `f'value is {x}'`          | YES       |
| Unpacking       | `a, b = 1, 2`              | YES       |
| Star Unpacking  | `a, *b = [1, 2, 3]`        | NO        |
| Throw Exception | `assert/raise`             | YES       |
| Catch Exception | `try..catch`               | NO        |
| Eval            | `eval()`                   | YES       |
| Import          | `import/from..import`      | YES       |
| Context Block   | `with <expr> as <id>:`     | YES       |
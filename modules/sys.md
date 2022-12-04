---
icon: package
label: sys
---

### `sys.version`

The version of PocketPy.

### `sys.getrefcount(object)`

Return the reference count of an object. The count returned is generally one higher than you might expect, because it includes the (temporary) reference as an argument to `getrefcount()`.

### `sys.getrecursionlimit()`

Return the current value of the recursion limit, the maximum depth of the Python interpreter stack. This limit prevents infinite recursion from causing an overflow of the C stack and crashing Python. The highest possible limit is platform-dependent.

### `sys.setrecursionlimit(limit)`

Set the maximum depth of the Python interpreter stack to *limit*. This limit prevents infinite recursion from causing an overflow of the C stack and crashing Python. The highest possible limit is platform-dependent.


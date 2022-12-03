---
title: General
icon: code
order: 7
---
#### `void pkpy_delete(void* p)`

Delete a class pointer allocated by `pkpy_xxx_xxx`.
It can be `VM*`, `REPL*`, `ThreadedVM*`, `char*`, etc.

!!!
If the pointer is not allocated by `pkpy_xxx_xxx`, the behavior is undefined.
For char*, you can also use trivial `delete` in your language.
!!!
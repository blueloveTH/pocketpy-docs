---
title: General
icon: code
order: 7
---
#### **`void pkpy_delete(void* p)`**

Delete a pointer allocated by `pkpy_xxx_xxx`.
It can be `VM*`, `REPL*` or `PyXXXDump*`, etc.

!!!
If the pointer not allocated by `pkpy_xxx_xxx`, nothing will happen.
!!!
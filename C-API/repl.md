---
title: REPL
icon: code
order: 8
---
#### **`REPL* pkpy_new_repl(VM* vm)`**

Create a REPL, using the given virtual machine as the backend.

#### **`int pkpy_repl_input(REPL* r, const char* line)`**

Input a source line to an interactive console.

Return `0` if need more lines,
`1` if execution happened,
`2` if execution skipped (compile error or empty input).
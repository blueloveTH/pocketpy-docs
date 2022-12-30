---
title: REPL
icon: dot
order: 8
---
#### `REPL* pkpy_new_repl(VM* vm)`

Create a REPL, using the given virtual machine as the backend.

#### `void pkpy_repl_input(REPL* r, const char* line)`

Input a source line to an interactive console.

#### `int pkpy_repl_last_input_result(REPL* r)`

Check if the REPL needs more lines.
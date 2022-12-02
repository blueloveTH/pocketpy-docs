---
title: ThreadedVM
icon: code
order: 9
---
#### **`ThreadedVM* pkpy_new_tvm(bool use_stdio)`**

Create a virtual machine that supports asynchronous execution.

#### **`bool pkpy_tvm_exec_async(VM* vm, const char* source)`**

Run a given source on a threaded virtual machine.
The excution will be started in a new thread.

Return `true` if there is no compile error.

#### **`int pkpy_tvm_get_state(ThreadedVM* vm)`**

Get the current state of a threaded virtual machine.

Return `0` for `THREAD_READY`,
`1` for `THREAD_RUNNING`,
`2` for `THREAD_SUSPENDED`,
`3` for `THREAD_FINISHED`.

#### **`void pkpy_tvm_keyboard_interrupt(VM* vm)`**

Emit a KeyboardInterrupt signal in order to stop a running threaded virtual machine. 

#### **`PyObjectDump* pkpy_tvm_read_jsonrpc_request(ThreadedVM* vm)`**

Read the current JSONRPC request from shared string buffer.

Return a `PyObjectDump*` representing the string.
You need to call `pkpy_delete` to free the returned `PyObjectDump*` later.
If the buffer is empty, return `nullptr`.

#### **`void pkpy_tvm_reset_state(ThreadedVM* vm)`**

Set the state of a threaded virtual machine to `THREAD_READY`.
The current state should be `THREAD_FINISHED`.

#### **`void pkpy_tvm_resume(ThreadedVM* vm, const char* value)`**

Resume a suspended threaded virtual machine
and put the given string into the shared string buffer.
It is usually used for JSONRPC.
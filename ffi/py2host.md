---
label: "Py:arrow_right:Host"
icon: dot
---

Calling host language function from PocketPy is available for threaded virtual machine.
This process is achieved by [JSONRPC](https://www.jsonrpc.org/specification).
It can be either synchronous or asynchronous.

## Send JSONRPC request

You can use the builtin function `jsonrpc`.

#### `jsonrpc(method, params, raw=False)`
Send a JSONRPC request to host language.

+ `method`: the method name
+ `params`: the parameters, should be a list
+ `raw`: by default it is `False`, you will get an expected Python object. If there is any error, an exception will be raised. If you set `raw=True`, you will get a `dict` object representing the JSONRPC response.

#### Example

```python
a = jsonrpc("add", [1, 2])
print(a)    # 3
```

It will generate a JSONRPC request like this:

```json
{
    "jsonrpc": "2.0",
    "method": "add",
    "params": [1, 2],
}
```

The response will be like this:

```json
{
    "jsonrpc": "2.0",
    "result": 3,
}
```

## Handle JSONRPC request

You can use `JsonRpcServer` to register JSONRPC handlers.

#### `JsonRpcServer.register(String name, Function f)`

Register a JSONRPC handler.

#### `Future<void> JsonRpcServer.attach(ThreadedVM vm)`

Attach the `JsonRpcServer` into a `ThreadedVM`.
Once the `ThreadedVM` encounters JSONRPC request,
it takes care of it automatically.
This process will be stopped when the whole execution is done.

!!!
JSONRPC is expensive. It is not recommended to use it in a loop or frame-based logic.
!!!
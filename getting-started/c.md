---
icon: code
label: 'C/C++'
order: 5
---

For C/C++ developers,
it is possible to generate a single header file `pocketpy.h`
by running the following command on Linux/WSL.

`g++` is required.

```bash
git clone https://github.com/blueloveth/pocketpy.git
cd pocketpy
python amalgamate.py
```

For references, see [C-API](/C-API/vm.md).
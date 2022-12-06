---
icon: code
label: Unity Engine
order: 2
---

## Introduction

PocketPy for Unity can be installed via UPM.

The package source is located in https://github.com/blueloveTH/pocketpy/tree/main/plugins/unity/com.bl.pocketpy

To install it, first clone our repository.

```
git clone https://github.com/blueloveth/pocketpy.git
```

Then:

1. Open the package manager.
2. Click the plus icon on the top left.
3. Select "Add package from disk".
4. Select `plugins/unity/com.bl.pocketpy/package.json`



## Example

```csharp
using UnityEngine;
using UnityEngine.UI;

public class Test : MonoBehaviour
{
    Text text;
    pkpy.VM vm;

    // Start is called before the first frame update
    void Start()
    {
        text = GetComponent<Text>();
        Application.targetFrameRate = 60;
        vm = new pkpy.VM();
        vm.exec("a = 0");
    }

    // Update is called once per frame
    void Update()
    {
        if(vm == null) return;
        vm.exec("a += 1");
        text.text = vm.eval("a");
    }
}
```


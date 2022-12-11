---
icon: code
label: Unity Engine
order: 2
---

## Introduction

PocketPy for Unity can be installed via Unity Asset Store.

https://assetstore.unity.com/packages/slug/241120



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


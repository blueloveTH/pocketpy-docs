---
icon: dot
---

# pointer

PocketPy supports pointers like C.

## `&` operator

You can use `&` operator to get a pointer from a variable.

The operand of `&` must be an *l-value*.

```c
# Correct usage
p = &a
p = &a[0]
p = &obj.a
p = &print

# Wrong usage
p = &1
p = &(a + b)
p = &f(x, y)
```

## `*` operator

You can use `*` operator to access the value where a pointer points to.

```c
a = 1
b = &a
*b = 2

print(a)    # 2
```

The swap function.

```c
def swap(a,b):
    t = *a
    *a = *b
    *b = t

x, y = 1, 2
swap(&x, &y)
print(x, y)     # 2 1
```

## `->` operator

You can use `->` operator to access the class member where a pointer points to. `a->b` is equal to `(*a).b`.

```c
a = [1, 2, 3]
b = &a
b->append(4)

print(a)    # [1, 2, 3, 4]
```

## Pointers are safe

PocketPy ensures all pointer operations are safe.

If you try to access an invalid pointer, a `NullPointerError` will be raised.
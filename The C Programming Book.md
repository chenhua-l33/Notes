
# C Notes (K&R)

## Pointers & Arrays

**Pointer subtraction returns element count, not bytes.**
```c
char *p = s;
while (*p != '\0') p++;
return p - s;   // # of chars (= bytes)
```
- `p++` on `int *` advances `sizeof(int)` bytes → `p - arr` already gives # of ints.
- **Never divide by `sizeof` after pointer subtraction.**
- Only cast to `char *` when you need raw byte distance, then divide:
  ```c
  size_t bytes  = (char *)end - (char *)start;
  size_t nelems = bytes / sizeof(int);
  ```

**Caveats**
- `p - s` requires both pointers into the same array (or one past end).
- No `'\0'` sentinel for `int` arrays unless `0` is guaranteed absent → pass a length or end pointer.

| Pointer type | `p++` advances | `p - s` gives | Divide by `sizeof`? |
|---|---|---|---|
| `char *` | 1 byte | element count | No |
| `int *` | `sizeof(int)` bytes | element count | No |
| `char *` (cast) | 1 byte | byte count | Yes |

---

## Operator Precedence

- `[]` has **higher precedence than `*`** → bracket when combining:
  ```c
  int *a[10];    // array of 10 pointers to int
  int (*a)[10];  // pointer to array of 10 ints
  ```
- `*` binds looser than `[]`, so `*a[10]` means `*(a[10])`, not `(*a)[10]`.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE4MTg2NTAyLDY3NTY2ODA0NV19
-->
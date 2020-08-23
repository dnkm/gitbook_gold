# Range Queries

## Range query

Calculating a value based on a subarray.

* sum in range \[a, b\]
* min in range \[a, b\]
* max in range \[a, b\]

```text
ar = [ 1, 3, 8, 4, 6, 1, 3, 4 ]
sum(3, 6) = 4 + 6 + 1 + 3
```

```cpp
int sum(int a, int b) {
    int s = 0;
    for(int i = a; i <= b; i++)
        s += ar[i];
    return s;
}
```

## Prefix Sum




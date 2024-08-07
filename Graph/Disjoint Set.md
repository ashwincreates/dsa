Disjoint set data structure
```python
def find(A, X):
    p = A[X - 1]
    if p == X:
        return X
    else:
        A[X - 1] = find(A, p)
        return A[X - 1]

def unionSet(A, X, Z):
    pX = find(A, X)
    pZ = find(A, Z)
    A[pX - 1] = pZ
```

> [!todo] Unioun By Rank and Size

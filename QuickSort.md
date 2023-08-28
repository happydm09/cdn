# Quick Sort

### 코드 Code

```python
def partition(arr: list, l: int, r: int):
    pivot, i = arr[r], l - 1
    j = l

    while j <= r - 1:
        if arr[j] <= pivot:
            i += 1
            arr[i], arr[j] = arr[j], arr[i]
        j += 1

    arr[i + 1], arr[r] = arr[r], arr[i + 1]
    return i + 1


def QuickSort(arr: list, l: int, r: int):
    if l < r:
        p = partition(arr, l, r)

        QuickSort(arr, l, p - 1)
        QuickSort(arr, p + 1, r)
    return arr

# 예제
l = [3, 2, 1, 4, 5, 10, 6]
print(QuickSort(l, 0, len(l) - 1)) # [1, 2, 3, 4, 5, 6, 10]
```

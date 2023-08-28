# Bubble Sort

정의: 큰 수 부터 오른쪽 몰아서 정렬하는 알고리즘 <br>
(정렬하는 모습이 거품이 올라오는 것 같아서 '버블소트라 함)

2개 씩 비교하여 왼쪽 수가 더 크면 위치(값)을 바꿈 <br>
(매 루프마다 하나의 값의 위치가 확정되기 때문에 두번째 for 문은 l - i 번 반복임)

시간 복잡도: O(n2)

<br>

###  코드 Code

```python
def BubbleSort(arr : list):
    l = len(arr) - 1
    for i in range(l):
        for j in range(l - i):
            a, b = arr[j], arr[j + 1]
            if a > b: arr[j], arr[j + 1] = b, a
    return arr

# 예제
print(BubbleSort([2,1,10, 4, 5])) # [1, 2, 4, 5, 10]
```

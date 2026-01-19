# 2026/01/20

# 問題概要
正方形の数字列があった場合、その対角線上の和の絶対差を計算する。

# 自分の回答
```python
def diagonalDifference(arr):
    # Write your code here
    left = 0
    right = 0
    n = len(arr)
    for i in range(len(arr)):
        left += arr[i][i]
        right += arr[i][n - i - 1]
    return abs(left - right)
```

# 補足
以下のようにpythonぽくかけるとスマート。
ただ上記の方が読みやすいし簡潔な気もする。
```python
def diagonalDifference(arr):
    n = len(arr)
    left = sum(arr[i][i] for i in range(n))
    right = sum(arr[i][n - 1 - i] for i in range(n))
    return abs(left - right)
```

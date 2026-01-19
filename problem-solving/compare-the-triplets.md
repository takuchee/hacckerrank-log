# 2026/01/16

# 問題概要
2つの同じ長さの配列をインデックスごとに比較し、大きい値を持つ方に1点ずつ加算して最終スコアを返す問題。

# 自分の回答
```python
def compareTriplets(a, b):
    # Write your code here
    alicePoint = 0
    bobPoint = 0
    for i in range(len(a)):
        if a[i] > b[i]:
            alicePoint += 1
        elif b[i] > a[i]:
            bobPoint += 1
    return [alicePoint,bobPoint]
```

# メモ
pythonならzip関数を使用して、各要素を取り出すようにした方がシンプルにできそう
```python
...for a, b in zip(a, b):
        if a > b:
            alicePoint += 1...
```

# 2026/01/25

# 問題概要
配列の中から一番大きい要素の個数を出力

# 自分の回答
```python
def birthdayCakeCandles(candles):
    # Write your code here
    tallestCandle = max(candles)
    return candles.count(tallestCandle)
```

# 補足
計算量: O(n)
べた書きすると以下(上記と違って一回の実行)
mxが更新されたときは以前のcntをリセットする必要があるので、1にするよう注意する
```python
def birthdayCakeCandles(candles):
    # Write your code here
    mx = 0
    cnt = 0
    for i in candles:
        if i > mx:
            mx = i
            cnt = 1
        elif i == mx:
            cnt += 1
    return cnt
``

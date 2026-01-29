# 2026/01/29

# 問題概要
正の整数の配列が与えられ、最初の要素を除き、
前のすべての要素の平均よりも大きい要素の数を返す

# 自分の回答
```python
def countResponseTimeRegressions(responseTimes):
    # Write your code here
    count = 0
    total = 0
    for i in range(len(responseTimes)):
        if i != 0 and responseTimes[i] > total / i:
            count += 1
        total += responseTimes[i]
    return count
```

# 補足
計算量：O(n)
スタックで保存したものを平均した値を比較しようと最初は考えたが、平均を出す度に合計と要素数を算出する必要があるためO(n²)になりうる。
配列を保持しなくても、集約値（合計・個数）だけで十分なケース。

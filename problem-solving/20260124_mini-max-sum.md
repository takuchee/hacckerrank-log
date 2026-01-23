# 2026/01/24

# 問題概要
5つの配列から４つの数字を抜き出し、合計が最小になるもの、最大になるものを出力

# 自分の回答
最初はこれ
```python
def miniMaxSum(arr):
  # Write your code here
  arr.sort()
  print(sum(arr[:4]), sum(arr[1:]))
```
以下の方がsumが一つで済むのでパフォーマンスよさそう
```python
def miniMaxSum(arr):
    # Write your code here
    total = sum(arr)
    print(total - max(arr), total - min(arr))
```
# 補足
TODO：sumの実装内容、処理時間の違いを調べる

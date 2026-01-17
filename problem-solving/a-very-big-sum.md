# 2026/01/18

# 問題概要
大きな整数の時の足し算

# 解法
```python
# input→LONG_INTEGER_ARRAY ex.)[1000000001,1000000002,1000000003,1000000004,1000000005]
def aVeryBigSum(ar):
    # Write your code here
    return sum(ar)
```

# メモ
- pythonのint型はオーバーフローが発生しない。(メモリが許す限り大きな数を使える。)
 →sum関数で一発。
- 愚直にやるならfor文でやってもよし。

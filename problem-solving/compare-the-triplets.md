# 2026/01/16
```
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
pythonならzip関数を使用して、各要素を取り出すようにした方がシンプルにできそう
```
...for a, b in zip(a, b):
        if a > b:
            alicePoint += 1...
```

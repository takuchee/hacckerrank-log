# 2026/01/28
# 問題概要
12時間表記（`hh:mm:ssAM/PM`）の時刻を  
24時間表記（`hh:mm:ss`）に変換する。

# 自分の回答
```python
def timeConversion(s):
    # Write your code here
    hour = int(s[0:2])
    minute = s[2:5]
    sec = s[5:8]
    AMPM = s[8:10]
    
    if hour == 12:
        hour = 0
        
    if AMPM == 'PM':
        resultHour = hour+ 12
    else:
        resultHour = hour
        
    return str(resultHour).zfill(2)+ minute+ sec
```
# 補足
- 文字列処理の問題では、for文よりもスライスで構造をそのまま切り出す方がシンプル
- 12AM / 12PM は境界値なので、先に処理しておくと if を減らせる
　→境界値へのロジックの切り出し方は常に工夫する意識で
- 計算ロジックと表示仕様（0埋め）は分けて考える
- Pythonでは数値の0埋めに zfill が使える
- 時間・分・秒・AM/PM を部品として扱うと処理が整理しやすい

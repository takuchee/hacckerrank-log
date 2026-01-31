# 2026/01/31
# 問題概要
与えられた文字列が、アルファベットのみを対象とした場合に回文（逆から読んでも同じ）であるかを判定する。
- アルファベット以外の文字を無視
- 大文字・小文字を区別しない

# 自分の回答
```python
def isAlphabeticPalindrome(code):
    # Write your code here
    chars = list(filter(lambda x: x.isalpha(), code))
    lowerChars = list(map(lambda y: y.lower(), chars))
    return lowerChars == list(reversed(lowerChars))
```

# 補足
上記だとO(n)の処理が三つある。あと冗長。
Geminiでの助言でTwo Pointersとリストの内包表記を採用し、以下のように修正。
冗長さはかなりなくなった。アーリーリターンも意識。
リストの内包表記を使いこなせてない。
両端からの検索、回文問題などはTwo pointersを使ってみるのがいいかも

```
def isAlphabeticPalindrome(code):
    # Write your code here
    chars = [c.lower() for c in code if c.isalpha()]
    left = 0
    right = len(chars) - 1
    if len(code) <= 1:
        return True
    
    while left < right:
        if chars[left] != chars[right]:
            return False
        left += 1
        right -= 1

    return True
```


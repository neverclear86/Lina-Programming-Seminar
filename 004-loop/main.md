<!-- $theme: gaia -->


## `創好リナ`の
# ==Programming Seminar==
### 3bit 
# Condition
##### 2018.08.19

---

# 条件分岐
- 条件分岐とは
- `if`文
- 条件式
- データ型の変換
- コメント
---

# 条件分岐 ==<u>#とは</u>==

---

# ==条件分岐==
- 条件によって処理を変更する


---


# `if`を使う

---

# `if`の使い方
```lua
if 条件式 then
    条件式が真の時の処理...
end
```

```lua
if 条件式 then
    条件式が真の時の処理...
else
    条件式が偽の時の処理...
end
```

---

# さらに分岐したい時は`elseif`

```lua
if 条件式A then
    条件式Aが真の時の処理...
elseif 条件式B then
    条件式Aが偽、条件式Bが真の時の処理
end
```

```lua
if 条件式A then
    条件式Aが真の時の処理...
elseif 条件式B then
    条件式Aが偽、条件式Bが真の時の処理
else
    条件式AもBも偽の場合の処理
end
```

---

# if文
- `if ~ then`
- `elseif ~ then`
- `else`


---

# ==条件式==

---

# 条件式
- 前回やった`式`です!
  - なんらかの値を返すもの
- 式の返した値が`真値`か`偽値`かで判断される
  - `nil`と`false`以外は全て真値

---

# 条件式 例
- `a` = 1, `b` = 10, `c` = nil
```lua
a == 1            --true
a == 2            --false
a < 0             -- false
a > 0             --true
0 < a and a <10   -- true
a ~= b            -- true
a == 1 or b == 1  --true
c == nil          -- true
not a             -- false
a and c           -- nil -> 偽
b or c            -- 10 -> 真
```

---

# データ型の変換

---

# Luaのデータ型変換
- 型を変換することを`キャスト`とか言う
- Luaでは言語にキャスト機能は無いので、<br>元からある関数(標準関数)を使う
- 型を調べるのは`type()`関数を使う
---

# stringへの変換
- `tostring(e)`
  - 文字列に変換する

```lua
local num = 1
print(type(num)) -- number
num = tostring(num)
print(type(num)) -- string
```

---

# numberへの変換
- `tonumber(e [, base])`
  - 数値型に変換数
  - `base`に基数を入れれば16進数とかもできる

```lua
local str = "123"
print(type(str)) -- string
str = tonumber(str)
print(type(str)) -- number
```

---

# ==コメント==

---

# コメント
- プログラムとして実行されず無視される部分
- 処理のメモなどとして利用
- `--` から行末まで
- `--[[` ~ `]]`まで
- 分かりづらい所をまとめたり、問題を頭に書いたりしとくと便利かもしれない

---

# 今日はここまで

---

# 問題

---

# 3-1
- 2つの数値を入力し、大きい方の数値を出力する
```text
num1
10[enter]
num2
30[enter]
max: 30
```

---

# 3-2
- タートルを前に一つ進ませる。<br>ただし、前にブロック等があり進めない場合は,<br>右を向いて進ませる。

- ヒント: `turtle.forward()`は失敗すると`false`を返す
---

# 3-3
- 西暦を入力し、平年なら`no`/閏年なら`yes`を表示
  - 閏年の条件
    - 4の倍数
    - 100の倍数でないこと
    - ただし400の倍数なら閏年
```text
year -> 2000[enter]
yes
```
```text
year -> 2100[enter]
no
```
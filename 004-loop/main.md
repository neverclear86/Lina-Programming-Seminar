<!-- $theme: gaia -->


## `創好リナ`の
# ==Programming Seminar==
### 4bit 
# Loop
##### 2018.08.26

---

# 繰り返しの処理
- ループ処理とは
- while文
- for文

---

# 繰り返しの処理とは


---

# 繰り返しの処理とは
- 同じような処理を繰り返す時はループを使おう
- 数百回とか自分で書くと地獄&バグの温床
- プログラミングしてるとめっちゃ使うよ!!!

---

# ![](D:\Stream\Slide\Lina-Programming-Seminar\004-loop\img\14f05690bfd503291c32fe4bf6652243.png)

---

# ==While==文2

--- 
# ==While==文
- 一番基本的なループ構文
- 条件式が真値の場合にループする
- 中の処理に入る前に評価される
```lua
while 条件式 do
  処理...
end
```

---

# While 例
```lua
local i = 1
while i < 100 do
  print(i)
  i = i + 1
end
```

---



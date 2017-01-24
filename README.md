# tea_02
TEA Makefile tutorial

*make-example folder: from source to binary*

**Original**
把get_double( )包含實作貼到tip.c
貼好多東西 

**ver1:**
把gd.c獨立出來
geom.c 加入#include "gd.c"
加100次
每次都要全部編譯,當專案大 費時

**ver2-prototype:**
把gd.c事先編成gd.o
geom.c, tip.c上方加funtion prototype

**ver3-empty:**
故意把gd.c變成空的編譯(沒有get_double實作)
發現linking階段出錯

**ver4-header:**
採用ver2
每當新增add.c , minus.c , FFT.c每一個geom.c, tip.c上方都要貼3次function prototype

於是把它包成header gd.h
header裡面只放變數宣告, function prototype

**ver5-Makefile**
以上要在終端機打5次gcc編譯命令, 
用Make自動化

target: dependencies
action
注意格式

**ver6-addHeader**
Make 有記憶特性 不會每次都重新編譯
加入clean, run 當有多個執行檔要編
記得 all: <執行檔1> <執行檔2>

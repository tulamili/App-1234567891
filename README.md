# コマンド 1234567891

## 概要

12345678911234567892... のような、連続する数列である1,2,3.. の各数の最下位を並べる。
ただし、0以外の数で0が最下位の場合は、その数を右から読んで0ではない最も右の文字を与える
(10なら1、200なら2、3000なら3となる)。

このことにより、他の文字列(たとえば15～100文字くらいの記号文字列)と、並べて表示して、
その文字列の長さを、一目瞭然に読み取ることが出来る。

### 機能

ターミナル内に表示された文字列の長さを、簡単に分かる様に、123456789..のような数字を並べる。
連番の数値(1,2,3..)の下位を見て、0が1個以上あれば削除して、1桁を取り出した数字が並ぶ。
引数で、その元の連番の最大値、または最小値と最大値の組合せを指定できる。

その数については、負の値(すなわち0未満の数)も指定できるが、オプションの-と区別をするために
' -3' のようにクオーテーションで囲って、1文字目は半角空白文字にする必要がある。
もしくは、コマンド1234567891 の後に並べたオプションの後ろに '--' (ハイフン2個)を挟んで
その後ろに、その負の数を並べると良い。

### オプション

 -d 桁数 : 未指定だと1と見なされる。2などの桁数を指定することで、1桁でなくその桁数を取り出す。

 -f      : 半角数字の代わりに、全角数字(fullwidth)の数を出力する。全角文字列の長さを知るのに有用。 
 
 --help  : オンラインマニュアルを表示する。(man や perldoc を使っても良い。)  

### コマンド実行例

![image](https://github.com/user-attachments/assets/3f318bbd-5dc4-4b4a-906c-e27ed465206f)

![image](https://github.com/user-attachments/assets/e650bec9-fc5f-4779-bf85-4b61636e8ee2)

## 有用な例

```
> alias 123=1234567891
> 123 80
12345678911234567892123456789312345678941234567895123456789612345678971234567898
> echo 'https://github.com/tulamili/App-1234567891/edit/main/README.md'
https://github.com/tulamili/App-1234567891/edit/main/README.md
> echo 'https://github.com/tulamili/App-1234567891/edit/main/README.md' | wc 
      1       1      63
```

上記で aliasを使ったのは、10文字のコマンドよりも3文字のコマンドにした方が、試行錯誤に便利だからである。
(unalias 123 でエイリアスは解除が可能である。)
URLのような、すぐには何文字か正確に分からない場合、wc で確かめる方法もあるが、コマンド文`1234567891 80`
により、80文字の定規のような文字列を並べて、目で見て比較する方が、上記だと62文字であると、確信しやすい。

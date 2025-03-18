ターミナル内に表示された文字列の長さを、簡単に分かる様に、123456789..のような数字を並べる。
連番の数値(1,2,3..)の下位を見て、0が1個以上あれば削除して、1桁を取り出した数字が並ぶ。
引数で、その元の連番の最大値、または最小値と最大値の組合せを指定できる。

その数については、負の値(すなわち0未満の数)も指定できるが、オプションの-と区別をするために
' -3' のようにクオーテーションで囲って、1文字目は半角空白文字にする必要がある。
もしくは、コマンド1234567891 の後に並べたオプションの後ろに '--' (ハイフン2個)を挟んで
その後ろに、その負の数を並べると良い。

オプションは、下記のものがある。
 -d 桁数 : 未指定だと1と見なされる。2などの桁数を指定することで、1桁でなくその桁数を取り出す。
 -f      : 半角数字の代わりに、全角数字(fullwidth)の数を出力する。全角文字列の長さを知るのに有用。 
 --help  : オンラインマニュアルを表示する。(man や perldoc を使っても良い。)  

![image](https://github.com/user-attachments/assets/3f318bbd-5dc4-4b4a-906c-e27ed465206f)

![image](https://github.com/user-attachments/assets/e650bec9-fc5f-4779-bf85-4b61636e8ee2)

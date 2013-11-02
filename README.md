# レイトン教授

レイトン教授に登場する問題を一部一般化して解くプログラムたち。

## n-気球問題 (kikyu.rb)

サイズ n の気球とは、1~n^2 の数字を n × n の格子状に並べたものである。
以下に サイズ 3 の気球の例を示す。

    1 2 3
    4 5 6
    7 8 9

サイズ n 気球が飛行可能であるためには、気球中の(n-1)×(n-1) の部分格子
の総和がすべて同じ必要がある。例えば上記の例では以下の４つの部分格子の
和が等しくなければならない。

    1 2 *   * 2 3   * * *   * * *
    4 5 *   * 5 6   4 5 *   * 5 6
    * * *   * * *   7 8 *   * 8 9

n-気球問題とは飛行可能な気球の配置を１つもしくはすべて列挙する問題である。



## n-ピラミッド問題 (pyramid.rb)

深さ n のピラミッドとは、d 段目に d 個の数字を配置した三角形である。以
下に深さ 4 のピラミッドの例を示す。

    d
    1 : 1
    2 : 2 3
    3 : 4 5 6
    4 : 7 8 9 10

上図において数字 i の真下の数字、及びその右の数字を i の子と呼ぶ。
今、iの子をj,kとすれば、n-ピラミッド問題とは任意の i について以下を
満たすように数字を配置する問題である。

    i = |j - k|


## 猫の散歩

２匹の猫を同時に操作して、同時に帰宅させる。ただし、猫は隣に魚のあるマ
スがあると、そこに移動してしまう。また、マンホールの上を通過することは
できない。配置をいかに示す。ただし _ は空白、Fは魚、Hはマンホール、Gは
ゴール, U, D, R, L はそれぞれ黒猫がそのマスでどの方向を向いているか、同
様にu, d, r, l は白猫の向きを表す。

      1 2 3 4 5 6 7
    1 _ _ _ F _ _ F
    2 _ D _ _ _ _ _
    3 _ _ F G H r _
    4 F H _ _ _ _ F
    5 _ _ _ _ F H _

なお入力ファイルは以下である。


    1 4 F
    1 7 F
    2 2 D
    3 3 F
    3 4 G
    3 5 H
    3 6 r
    4 1 F
    4 2 H
    4 7 F
    5 5 F
    5 6 H

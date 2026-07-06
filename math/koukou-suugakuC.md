---
layout: default
title: 高校 数学C
parent: 算数・数学
nav_order: 15
---

# 高校 数学C

数学Cは「ベクトル」「平面上の曲線」「複素数平面」の3単元からなる科目です。いずれも、図形や運動を数式で自在に扱うための強力な道具であり、理系の大学入試では最頻出の分野です。ベクトルは向きと大きさをもつ量を、平面上の曲線は2次曲線や媒介変数・極座標を、複素数平面は複素数を平面上の点として幾何学的に扱います。3単元に共通するのは「**図形の問題を計算に、計算の結果を再び図形に翻訳する**」という視点です。抽象的に見えても、必ず図をかきながら、意味を確かめて読み進めてください。

---

## ベクトル

### この単元で学ぶこと

- ベクトルの定義、和・差・実数倍と成分表示
- ベクトルの内積、なす角、大きさ
- 位置ベクトルと分点公式、一直線上・共面条件
- 図形への応用（内分・外分・重心、垂直・平行の証明）
- 空間ベクトルと座標空間、平面・球面の方程式

### 解説

#### ベクトルとその演算

**ベクトル**とは「大きさ」と「向き」をもつ量で、有向線分 $\overrightarrow{AB}$ で表します。位置を問わず、大きさと向きが等しいベクトルは等しいとみなします。ベクトル $\vec{a}, \vec{b}$ と実数 $k$ について、和 $\vec{a}+\vec{b}$、差 $\vec{a}-\vec{b}$、実数倍 $k\vec{a}$ が定義され、次の性質を満たします。

$$
\vec{a}+\vec{b} = \vec{b}+\vec{a}, \qquad (\vec{a}+\vec{b})+\vec{c} = \vec{a}+(\vec{b}+\vec{c})
$$

大きさが $0$ のベクトルを**零ベクトル** $\vec{0}$、大きさが $1$ のベクトルを**単位ベクトル**といいます。$\vec{a} \neq \vec{0}$, $\vec{b} \neq \vec{0}$ のとき、

$$
\vec{a} \parallel \vec{b} \iff \vec{b} = k\vec{a} \ (k \text{ は実数})
$$

（平行条件）。$\vec{a}$, $\vec{b}$ が平行でないとき、平面上の任意のベクトル $\vec{p}$ はただ一通りに $\vec{p} = s\vec{a} + t\vec{b}$（$s, t$ は実数）と表せます。この $\vec{a}, \vec{b}$ を**基本ベクトル**（一次独立な基底）といいます。

#### 成分表示

平面上で $\vec{a} = (a_1, a_2)$, $\vec{b} = (b_1, b_2)$ と成分表示すると

$$
\vec{a} + \vec{b} = (a_1 + b_1,\ a_2 + b_2), \qquad k\vec{a} = (ka_1,\ ka_2)
$$
$$
|\vec{a}| = \sqrt{a_1^2 + a_2^2}
$$

2点 $A(a_1, a_2)$, $B(b_1, b_2)$ について $\overrightarrow{AB} = (b_1 - a_1,\ b_2 - a_2)$（終点 − 始点）。

#### 内積

2つのベクトル $\vec{a}, \vec{b}$ のなす角を $\theta$（$0^\circ \leq \theta \leq 180^\circ$）とするとき、**内積**を

$$
\vec{a} \cdot \vec{b} = |\vec{a}|\,|\vec{b}|\cos\theta
$$

で定義します。内積はベクトルどうしの積ですが、結果は実数（スカラー）です。成分では

$$
\vec{a} \cdot \vec{b} = a_1 b_1 + a_2 b_2
$$

（空間では $a_1b_1 + a_2b_2 + a_3b_3$）。ここから、なす角と垂直条件が得られます。

$$
\cos\theta = \frac{\vec{a}\cdot\vec{b}}{|\vec{a}||\vec{b}|}, \qquad \vec{a} \perp \vec{b} \iff \vec{a}\cdot\vec{b} = 0
$$

内積の主な性質を整理します。

| 性質 | 式 |
|------|-----|
| 交換法則 | $\vec{a}\cdot\vec{b} = \vec{b}\cdot\vec{a}$ |
| 分配法則 | $\vec{a}\cdot(\vec{b}+\vec{c}) = \vec{a}\cdot\vec{b} + \vec{a}\cdot\vec{c}$ |
| 実数倍 | $(k\vec{a})\cdot\vec{b} = k(\vec{a}\cdot\vec{b})$ |
| 大きさとの関係 | $\vec{a}\cdot\vec{a} = |\vec{a}|^2$ |

$|\vec{a}+\vec{b}|^2 = |\vec{a}|^2 + 2\vec{a}\cdot\vec{b} + |\vec{b}|^2$ のように、大きさの2乗は内積を使って展開できます。ここが計算の要です。

#### 位置ベクトルと分点公式

ある定点 $O$ を基準にとり、点 $P$ の位置を $\overrightarrow{OP} = \vec{p}$ で表したものを、$P$ の**位置ベクトル**といいます。2点 $A(\vec{a})$, $B(\vec{b})$ を結ぶ線分 $AB$ を $m:n$ に内分する点 $P$、外分する点 $Q$ の位置ベクトルは

$$
\vec{p} = \frac{n\vec{a} + m\vec{b}}{m+n}, \qquad \vec{q} = \frac{-n\vec{a} + m\vec{b}}{m-n}
$$

特に中点は $\dfrac{\vec{a}+\vec{b}}{2}$。三角形 $ABC$ の**重心** $G$ の位置ベクトルは

$$
\vec{g} = \frac{\vec{a}+\vec{b}+\vec{c}}{3}
$$

#### 一直線上の条件・共面条件

3点 $A, B, C$ が一直線上にある条件は

$$
\overrightarrow{AC} = k\,\overrightarrow{AB} \ (\exists k)
$$

点 $P$ が直線 $AB$ 上にある条件は、$\overrightarrow{OP} = s\overrightarrow{OA} + t\overrightarrow{OB}$ と表したとき $s + t = 1$（係数の和が1）と同値です。空間で4点 $A, B, C, P$ が同一平面上にある（共面）条件は、$\overrightarrow{AP} = s\overrightarrow{AB} + t\overrightarrow{AC}$ となる実数 $s, t$ が存在することです。

#### 空間ベクトルと座標空間

空間では基底が3つ必要で、$\vec{a} = (a_1, a_2, a_3)$ のように3成分で表します。演算・内積・大きさは平面と同じ形で、成分が1つ増えるだけです。

- 2点 $A, B$ 間の距離：$AB = \sqrt{(b_1-a_1)^2 + (b_2-a_2)^2 + (b_3-a_3)^2}$
- **球面の方程式**：中心 $(a, b, c)$、半径 $r$ の球面は $(x-a)^2 + (y-b)^2 + (z-c)^2 = r^2$
- **平面の方程式**：法線ベクトル $\vec{n} = (a, b, c)$ をもち点 $(x_0, y_0, z_0)$ を通る平面は $a(x-x_0) + b(y-y_0) + c(z-z_0) = 0$

#### 三角形の面積とベクトル

$\triangle OAB$ で $\overrightarrow{OA} = \vec{a}$, $\overrightarrow{OB} = \vec{b}$ とするとき、その面積 $S$ は内積を用いて

$$
S = \frac{1}{2}\sqrt{|\vec{a}|^2|\vec{b}|^2 - (\vec{a}\cdot\vec{b})^2}
$$

と表せます。これは $S = \dfrac{1}{2}|\vec{a}||\vec{b}|\sin\theta$ に $\sin^2\theta = 1 - \cos^2\theta$ を代入して整理したものです。特に平面で $\vec{a} = (a_1, a_2)$, $\vec{b} = (b_1, b_2)$ のときは

$$
S = \frac{1}{2}|a_1 b_2 - a_2 b_1|
$$

という簡潔な形になります。

### 例題

**例題1（内積となす角）** $\vec{a} = (2, 1)$, $\vec{b} = (1, 3)$ について、内積 $\vec{a}\cdot\vec{b}$ と、なす角 $\theta$ を求めよ。

**解答** 成分より $\vec{a}\cdot\vec{b} = 2\cdot1 + 1\cdot3 = 5$。また $|\vec{a}| = \sqrt{4+1} = \sqrt5$, $|\vec{b}| = \sqrt{1+9} = \sqrt{10}$。

$$
\cos\theta = \frac{5}{\sqrt5 \cdot \sqrt{10}} = \frac{5}{\sqrt{50}} = \frac{5}{5\sqrt2} = \frac{1}{\sqrt2}
$$

$0^\circ \leq \theta \leq 180^\circ$ より $\theta = 45^\circ$。

---

**例題2（垂直条件）** $\vec{a} = (3, -1)$, $\vec{b} = (1, 2)$ とする。$\vec{a} + t\vec{b}$ が $\vec{a}$ と垂直になるような実数 $t$ を求めよ。

**解答** 垂直条件は内積が $0$。

$$
(\vec{a} + t\vec{b}) \cdot \vec{a} = \vec{a}\cdot\vec{a} + t\,\vec{b}\cdot\vec{a} = |\vec{a}|^2 + t(\vec{a}\cdot\vec{b}) = 0
$$

$|\vec{a}|^2 = 9 + 1 = 10$, $\vec{a}\cdot\vec{b} = 3\cdot1 + (-1)\cdot2 = 1$。よって $10 + t = 0$、$t = -10$。

---

**例題3（分点と一直線上の条件）** $\triangle OAB$ において、辺 $OA$ を $2:1$ に内分する点を $C$、辺 $OB$ の中点を $D$ とする。$\overrightarrow{OA} = \vec{a}$, $\overrightarrow{OB} = \vec{b}$ とおくとき、直線 $CD$ 上の点で、直線 $AB$ 上にもある点 $P$ の位置ベクトル $\overrightarrow{OP}$ を求めよ。

**解答** $\overrightarrow{OC} = \dfrac{2}{3}\vec{a}$, $\overrightarrow{OD} = \dfrac{1}{2}\vec{b}$。$P$ が直線 $CD$ 上にあるので、実数 $s$ を用いて

$$
\overrightarrow{OP} = (1-s)\overrightarrow{OC} + s\,\overrightarrow{OD} = \frac{2(1-s)}{3}\vec{a} + \frac{s}{2}\vec{b}
$$

$P$ が直線 $AB$ 上にある条件は、$\vec{a}, \vec{b}$ の係数の和が $1$。

$$
\frac{2(1-s)}{3} + \frac{s}{2} = 1 \quad\Longrightarrow\quad \frac{4(1-s) + 3s}{6} = 1 \quad\Longrightarrow\quad 4 - s = 6 \quad\Longrightarrow\quad s = -2
$$

代入して

$$
\overrightarrow{OP} = \frac{2(1-(-2))}{3}\vec{a} + \frac{-2}{2}\vec{b} = 2\vec{a} - \vec{b}
$$

---

**例題4（空間ベクトルと垂直）** 空間に $A(1, 0, 2)$, $B(3, 1, 1)$, $C(2, -1, 3)$ がある。$\overrightarrow{AB}$ と $\overrightarrow{AC}$ の両方に垂直なベクトル $\vec{n} = (x, y, 1)$ を求めよ。

**解答** $\overrightarrow{AB} = (2, 1, -1)$, $\overrightarrow{AC} = (1, -1, 1)$。垂直条件より

$$
\vec{n}\cdot\overrightarrow{AB} = 2x + y - 1 = 0, \qquad \vec{n}\cdot\overrightarrow{AC} = x - y + 1 = 0
$$

2式を辺々加えると $3x = 0$ より $x = 0$。$y = x + 1 = 1$。よって $\vec{n} = (0, 1, 1)$。

---

**例題5（ベクトルによる図形の証明）** $\triangle ABC$ の辺 $BC$, $CA$, $AB$ の中点をそれぞれ $L, M, N$ とする。3つの中線 $AL, BM, CN$ が1点で交わり、それが重心であることをベクトルで示せ。

**解答** 基準点 $O$ をとり、$A, B, C$ の位置ベクトルを $\vec{a}, \vec{b}, \vec{c}$ とする。$L$ は $BC$ の中点だから $\overrightarrow{OL} = \dfrac{\vec{b}+\vec{c}}{2}$。中線 $AL$ を $2:1$ に内分する点 $G$ の位置ベクトルは

$$
\overrightarrow{OG} = \frac{1\cdot\vec{a} + 2\cdot\dfrac{\vec{b}+\vec{c}}{2}}{2+1} = \frac{\vec{a}+\vec{b}+\vec{c}}{3}
$$

この式は $A, B, C$ について対称だから、中線 $BM$, $CN$ を $2:1$ に内分する点も同じ位置ベクトル $\dfrac{\vec{a}+\vec{b}+\vec{c}}{3}$ をもつ。したがって3中線は1点 $G$ で交わり、それは重心である。

---

**例題6（三角形の面積）** $\triangle OAB$ で $\overrightarrow{OA} = (3, 1)$, $\overrightarrow{OB} = (1, 4)$ とするとき、$\triangle OAB$ の面積を求めよ。

**解答** 平面の公式 $S = \dfrac{1}{2}|a_1 b_2 - a_2 b_1|$ を用いる。

$$
S = \frac{1}{2}|3\cdot4 - 1\cdot1| = \frac{1}{2}|12 - 1| = \frac{11}{2}
$$

（内積を使う一般公式でも確認できる：$|\vec{a}|^2 = 10$, $|\vec{b}|^2 = 17$, $\vec{a}\cdot\vec{b} = 7$ より $S = \dfrac{1}{2}\sqrt{10\cdot17 - 49} = \dfrac{1}{2}\sqrt{121} = \dfrac{11}{2}$。）

### 練習問題

1. $\vec{a} = (1, -2)$, $\vec{b} = (3, 1)$ とする。 (1) $|\vec{a} + \vec{b}|$ を求めよ。 (2) $\vec{a}$ と $\vec{b}$ のなす角を求めよ。

2. $|\vec{a}| = 2$, $|\vec{b}| = 3$, $\vec{a}\cdot\vec{b} = -3$ のとき、$|2\vec{a} - \vec{b}|$ を求めよ。

3. $\triangle OAB$ で $\overrightarrow{OA} = \vec{a}$, $\overrightarrow{OB} = \vec{b}$ とする。辺 $AB$ を $1:2$ に内分する点を $P$、線分 $OP$ を $3:1$ に内分する点を $Q$ とするとき、$\overrightarrow{OQ}$ を $\vec{a}, \vec{b}$ で表せ。

4. 3点 $A(1, 2)$, $B(4, 3)$, $C(x, 7)$ が一直線上にあるとき、$x$ の値を求めよ。

5. 空間の3点 $A(2, 0, 1)$, $B(0, 3, 2)$, $C(1, 1, 0)$ を通る平面の方程式を求めよ。

6. $\triangle OAB$ において、$OA = 3$, $OB = 4$, $\angle AOB = 60^\circ$ とする。$\angle AOB$ の二等分線と辺 $AB$ の交点を $D$ とするとき、$\overrightarrow{OD}$ を $\overrightarrow{OA} = \vec{a}$, $\overrightarrow{OB} = \vec{b}$ で表せ。

7. 3点 $O(0,0)$, $A(4, 1)$, $B(2, 5)$ を頂点とする $\triangle OAB$ の面積を求めよ。

8. 空間の点 $P(x, y, z)$ が、$A(1, 2, 3)$ から距離 $\sqrt{5}$ の位置にあり、かつ平面 $2x - y + 2z = 6$ 上にある。$A$ からこの平面へ下ろした垂線の足 $H$ の座標を求めよ。

### 解答と解説

**1.**
(1) $\vec{a}+\vec{b} = (4, -1)$ より $|\vec{a}+\vec{b}| = \sqrt{16 + 1} = \sqrt{17}$。
(2) $\vec{a}\cdot\vec{b} = 1\cdot3 + (-2)\cdot1 = 1$。$|\vec{a}| = \sqrt5$, $|\vec{b}| = \sqrt{10}$。

$$
\cos\theta = \frac{1}{\sqrt5\cdot\sqrt{10}} = \frac{1}{\sqrt{50}} = \frac{1}{5\sqrt2} = \frac{\sqrt2}{10}
$$

**2.** 大きさの2乗を内積で展開する。

$$
|2\vec{a}-\vec{b}|^2 = 4|\vec{a}|^2 - 4\vec{a}\cdot\vec{b} + |\vec{b}|^2 = 4\cdot4 - 4\cdot(-3) + 9 = 16 + 12 + 9 = 37
$$

よって $|2\vec{a}-\vec{b}| = \sqrt{37}$。

**3.** $\overrightarrow{OP} = \dfrac{2\vec{a} + 1\cdot\vec{b}}{1+2} = \dfrac{2\vec{a}+\vec{b}}{3}$。$Q$ は $OP$ を $3:1$ に内分するので

$$
\overrightarrow{OQ} = \frac{3}{4}\overrightarrow{OP} = \frac{3}{4}\cdot\frac{2\vec{a}+\vec{b}}{3} = \frac{2\vec{a}+\vec{b}}{4} = \frac{1}{2}\vec{a} + \frac{1}{4}\vec{b}
$$

**4.** $\overrightarrow{AB} = (3, 1)$, $\overrightarrow{AC} = (x-1, 5)$。一直線上にある条件 $\overrightarrow{AC} = k\overrightarrow{AB}$ より $5 = k\cdot1$ から $k = 5$、$x - 1 = 3k = 15$、よって $x = 16$。
（別解：$\overrightarrow{AB}$ と $\overrightarrow{AC}$ が平行なので $3\cdot5 - 1\cdot(x-1) = 0$、$16 - x = 0$、$x = 16$。）

**5.** 平面の方程式を $ax + by + cz = d$ とおく。3点を代入すると

$$
2a + c = d, \quad 3b + 2c = d, \quad a + b = d
$$

$a + b = d$ より $b = d - a$。第1式 $c = d - 2a$。これらを第2式に代入すると $3(d-a) + 2(d-2a) = d$、$5d - 7a = d$、$4d = 7a$、$a = \dfrac{4}{7}d$。$d = 7$ とおくと $a = 4$, $b = 3$, $c = 7 - 8 = -1$。よって平面は

$$
4x + 3y - z = 7
$$

（検算：$A$ で $8 + 0 - 1 = 7$、$B$ で $0 + 9 - 2 = 7$、$C$ で $4 + 3 - 0 = 7$。すべて成立。）

**6.** 角の二等分線と辺の比の性質より $AD:DB = OA:OB = 3:4$。よって

$$
\overrightarrow{OD} = \frac{4\vec{a} + 3\vec{b}}{3+4} = \frac{4}{7}\vec{a} + \frac{3}{7}\vec{b}
$$

**7.** $\overrightarrow{OA} = (4, 1)$, $\overrightarrow{OB} = (2, 5)$ より

$$
S = \frac{1}{2}|4\cdot5 - 1\cdot2| = \frac{1}{2}|20 - 2| = \frac{18}{2} = 9
$$

**8.** 垂線の足 $H$ は、$A$ から平面の法線ベクトル $\vec{n} = (2, -1, 2)$ の方向に進んだ点だから、実数 $t$ を用いて $H = A + t\vec{n} = (1 + 2t,\ 2 - t,\ 3 + 2t)$ とおける。$H$ が平面 $2x - y + 2z = 6$ 上にあるので

$$
2(1 + 2t) - (2 - t) + 2(3 + 2t) = 6 \ \Longrightarrow\ 2 + 4t - 2 + t + 6 + 4t = 6 \ \Longrightarrow\ 9t + 6 = 6
$$

よって $t = 0$。すなわち $A$ 自身が平面上にあり（$2 - 2 + 6 = 6$ で成立）、$H = A = (1, 2, 3)$。垂線の長さは $0$ である。

### つまずきやすいポイント

- **内積はスカラー、和・差はベクトル**：$\vec{a}\cdot\vec{b}$ の結果は実数です。ベクトル量と混同して「$\vec{a}\cdot\vec{b}$ の向き」などと考えないこと。
- **大きさは必ず2乗して展開**：$|\vec{a}+\vec{b}|$ を求めるときは、いきなり大きさを足すのではなく $|\vec{a}+\vec{b}|^2 = |\vec{a}|^2 + 2\vec{a}\cdot\vec{b} + |\vec{b}|^2$ と展開してから平方根をとります。
- **一直線上の条件「係数の和が1」**：$\overrightarrow{OP} = s\vec{a} + t\vec{b}$ で $P$ が直線 $AB$ 上 $\iff s+t=1$。始点 $O$ が直線上にないことが前提です。分点公式との関係を意識しましょう。
- **平行と垂直の条件の混同**：平行は $\vec{b} = k\vec{a}$（成分で $a_1 b_2 - a_2 b_1 = 0$）、垂直は $\vec{a}\cdot\vec{b} = 0$（成分で $a_1 b_1 + a_2 b_2 = 0$）。似ているので式の形をしっかり区別。
- **空間で一次独立な基底は3つ**：平面の感覚のまま2つのベクトルで空間全体を表そうとすると誤ります。共面条件（2ベクトルの一次結合で表せる）と混同しないこと。

---

## 平面上の曲線

### この単元で学ぶこと

- 放物線・楕円・双曲線の定義と方程式（2次曲線）
- 2次曲線の焦点・準線・漸近線・離心率
- 曲線の媒介変数表示（パラメータ表示）
- 極座標と極方程式、直交座標との変換

### 解説

#### 放物線

平面上で、定点 $F$（**焦点**）と、$F$ を通らない定直線 $\ell$（**準線**）からの距離が等しい点の軌跡が**放物線**です。焦点を $(p, 0)$、準線を $x = -p$ とすると、方程式は

$$
y^2 = 4px \qquad (p \neq 0)
$$

$p > 0$ なら右に開き、頂点は原点。焦点が $y$ 軸上のときは $x^2 = 4py$ となります。

#### 楕円

2定点 $F, F'$（**焦点**）からの距離の和が一定である点の軌跡が**楕円**です。距離の和を $2a$、焦点を $(\pm c, 0)$ とすると、$b = \sqrt{a^2 - c^2}$ とおいて

$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 \qquad (a > b > 0)
$$

$a$ を**長半径**、$b$ を**短半径**といい、焦点は $x$ 軸上の $(\pm c, 0)$、$c = \sqrt{a^2 - b^2}$。焦点間距離の和は $2a$ に等しくなります。円は楕円の特別な場合（$a = b$）です。

#### 双曲線

2定点 $F, F'$ からの距離の**差**の絶対値が一定である点の軌跡が**双曲線**です。差を $2a$、焦点を $(\pm c, 0)$ とすると、$b = \sqrt{c^2 - a^2}$ とおいて

$$
\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1
$$

焦点は $(\pm c, 0)$、$c = \sqrt{a^2 + b^2}$。双曲線は2本の**漸近線**

$$
y = \pm \frac{b}{a}x
$$

に限りなく近づきます。

2次曲線の要点を表で整理します。

| 曲線 | 標準形 | 焦点 | 特徴 |
|------|--------|------|------|
| 放物線 | $y^2 = 4px$ | $(p, 0)$ | 準線 $x=-p$、距離が等しい |
| 楕円 | $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1$ | $(\pm\sqrt{a^2-b^2},0)$ | 距離の和が $2a$ |
| 双曲線 | $\dfrac{x^2}{a^2}-\dfrac{y^2}{b^2}=1$ | $(\pm\sqrt{a^2+b^2},0)$ | 距離の差が $2a$、漸近線 $y=\pm\frac{b}{a}x$ |

#### 離心率による統一的な見方

放物線・楕円・双曲線は、実は「1つの焦点 $F$ と1本の準線 $\ell$ からの距離の比が一定」という共通の性質でとらえられます。点 $P$ について

$$
\frac{PF}{(P \text{ から準線 } \ell \text{ までの距離})} = e \ (\text{一定})
$$

が成り立つとき、この $e$ を**離心率**といい、次のように曲線の種類が決まります。

| 離心率 | 曲線 |
|--------|------|
| $0 < e < 1$ | 楕円 |
| $e = 1$ | 放物線 |
| $e > 1$ | 双曲線 |

放物線が「焦点と準線からの距離が等しい（比が $1$）」曲線であったことは、$e = 1$ の場合にほかなりません。このように、3種類の2次曲線を1つの枠組みで見渡せる点が離心率の魅力です。

#### 2次曲線の平行移動

標準形の曲線を $x$ 軸方向に $p$、$y$ 軸方向に $q$ だけ平行移動するには、方程式の $x$ を $x - p$、$y$ を $y - q$ に置き換えます。たとえば楕円 $\dfrac{x^2}{a^2}+\dfrac{y^2}{b^2}=1$ を中心 $(p, q)$ に移すと

$$
\frac{(x-p)^2}{a^2} + \frac{(y-q)^2}{b^2} = 1
$$

となります。一般の2次式で与えられた曲線は、平方完成によって中心（頂点）を求め、標準形に直すのが基本方針です。

#### 媒介変数表示

曲線上の点の座標 $(x, y)$ を、1つの変数 $t$（**媒介変数・パラメータ**）を用いて $x = f(t)$, $y = g(t)$ と表す方法を**媒介変数表示**といいます。代表例は次の通りです。

- 円 $x^2 + y^2 = r^2$：$\ x = r\cos\theta,\ y = r\sin\theta$
- 楕円 $\dfrac{x^2}{a^2} + \dfrac{y^2}{b^2} = 1$：$\ x = a\cos\theta,\ y = b\sin\theta$
- 放物線 $y^2 = 4px$：$\ x = pt^2,\ y = 2pt$

媒介変数を消去すれば、$x, y$ の関係式（直交座標の方程式）に戻せます。$\cos^2\theta + \sin^2\theta = 1$ を利用するのが定石です。**サイクロイド**（半径 $a$ の円が直線上を転がるときの円周上の点の軌跡）$x = a(\theta - \sin\theta)$, $y = a(1 - \cos\theta)$ も重要な例です。

#### 極座標

平面上の点 $P$ を、原点 $O$（**極**）からの距離 $r$ と、始線（$x$ 軸の正の向き）からの角 $\theta$ の組 $(r, \theta)$ で表す方法を**極座標**といいます。直交座標 $(x, y)$ との関係は

$$
x = r\cos\theta, \qquad y = r\sin\theta
$$
$$
r = \sqrt{x^2 + y^2}, \qquad \tan\theta = \frac{y}{x}\ (x\neq0)
$$

$r$ と $\theta$ の関係式 $r = f(\theta)$ を**極方程式**といいます。例えば

- 中心が極、半径 $a$ の円：$r = a$
- 極を通り $x$ 軸と角 $\alpha$ をなす直線：$\theta = \alpha$
- 極を通り中心が $(a, 0)$、半径 $a$ の円：$r = 2a\cos\theta$

円や直線でも、対称性の高い図形は極方程式のほうが簡潔に書けることがあります。

### 例題

**例題1（楕円）** 楕円 $\dfrac{x^2}{25} + \dfrac{y^2}{9} = 1$ について、長半径・短半径・焦点の座標を求めよ。

**解答** $a^2 = 25$, $b^2 = 9$ より $a = 5$（長半径）、$b = 3$（短半径）。焦点は $x$ 軸上にあり $c = \sqrt{a^2 - b^2} = \sqrt{25 - 9} = \sqrt{16} = 4$。よって焦点は $(\pm 4, 0)$。

---

**例題2（双曲線）** 双曲線 $\dfrac{x^2}{9} - \dfrac{y^2}{16} = 1$ の焦点と漸近線を求めよ。

**解答** $a^2 = 9$, $b^2 = 16$ より $a = 3$, $b = 4$。焦点は $c = \sqrt{a^2 + b^2} = \sqrt{9+16} = \sqrt{25} = 5$ で $(\pm 5, 0)$。漸近線は

$$
y = \pm\frac{b}{a}x = \pm\frac{4}{3}x
$$

---

**例題3（放物線の定義）** 焦点が $(2, 0)$、準線が $x = -2$ の放物線の方程式を求めよ。

**解答** 焦点 $(p, 0) = (2, 0)$ より $p = 2$、準線 $x = -p = -2$ と一致する。よって

$$
y^2 = 4px = 4\cdot2\cdot x = 8x
$$

（確認：点 $(x, y)$ から焦点までの距離 $\sqrt{(x-2)^2 + y^2}$ と準線までの距離 $x+2$ が等しいとおいて2乗すると $(x-2)^2 + y^2 = (x+2)^2$、展開して $y^2 = 8x$。）

---

**例題4（媒介変数の消去）** 媒介変数表示 $x = 2\cos\theta + 1$, $y = 3\sin\theta - 2$ で表される曲線の方程式を、$x, y$ の式で表せ。

**解答** $\cos\theta = \dfrac{x-1}{2}$, $\sin\theta = \dfrac{y+2}{3}$。$\cos^2\theta + \sin^2\theta = 1$ に代入して

$$
\left(\frac{x-1}{2}\right)^2 + \left(\frac{y+2}{3}\right)^2 = 1 \quad\Longrightarrow\quad \frac{(x-1)^2}{4} + \frac{(y+2)^2}{9} = 1
$$

これは中心 $(1, -2)$ の楕円である。

---

**例題5（極座標と極方程式）** (1) 極座標 $\left(2, \dfrac{\pi}{3}\right)$ を直交座標に直せ。 (2) 極方程式 $r = 2\cos\theta$ が表す曲線を、直交座標の方程式で表せ。

**解答**
(1) $x = 2\cos\dfrac{\pi}{3} = 2\cdot\dfrac{1}{2} = 1$、$y = 2\sin\dfrac{\pi}{3} = 2\cdot\dfrac{\sqrt3}{2} = \sqrt3$。よって $(1, \sqrt3)$。

(2) 両辺に $r$ を掛けると $r^2 = 2r\cos\theta$。$r^2 = x^2 + y^2$, $r\cos\theta = x$ を代入して

$$
x^2 + y^2 = 2x \quad\Longrightarrow\quad (x-1)^2 + y^2 = 1
$$

これは中心 $(1, 0)$、半径 $1$ の円である。

### 練習問題

1. 楕円 $\dfrac{x^2}{16} + \dfrac{y^2}{4} = 1$ の焦点の座標を求めよ。また、焦点からの距離の和はいくらか。

2. 2点 $(3, 0)$, $(-3, 0)$ を焦点とし、長軸の長さが $10$ の楕円の方程式を求めよ。

3. 双曲線 $\dfrac{x^2}{4} - \dfrac{y^2}{9} = 1$ の焦点と漸近線を求めよ。

4. 焦点が $(0, 3)$、準線が $y = -3$ の放物線の方程式を求めよ。

5. 媒介変数表示 $x = t + \dfrac{1}{t}$, $y = t - \dfrac{1}{t}$（$t \neq 0$）で表される曲線の方程式を $x, y$ で表せ。

6. 極方程式 $r = \dfrac{2}{1 + \cos\theta}$ が表す曲線を、直交座標の方程式で表せ。

7. 2次曲線 $x^2 + 4y^2 - 2x + 8y + 1 = 0$ を平方完成して標準形に直し、中心の座標と曲線の種類を答えよ。

### 解答と解説

**1.** $a^2 = 16$, $b^2 = 4$ より $c = \sqrt{16 - 4} = \sqrt{12} = 2\sqrt3$。焦点は $(\pm 2\sqrt3, 0)$。焦点からの距離の和は $2a = 8$。

**2.** 焦点が $(\pm3, 0)$ より $c = 3$。長軸の長さ $2a = 10$ より $a = 5$。$b^2 = a^2 - c^2 = 25 - 9 = 16$。よって

$$
\frac{x^2}{25} + \frac{y^2}{16} = 1
$$

**3.** $a^2 = 4$, $b^2 = 9$ より $a = 2$, $b = 3$。$c = \sqrt{4 + 9} = \sqrt{13}$。焦点は $(\pm\sqrt{13}, 0)$、漸近線は $y = \pm\dfrac{3}{2}x$。

**4.** 焦点が $y$ 軸上の $(0, p) = (0, 3)$ より $p = 3$、準線 $y = -3$ と整合。$x^2 = 4py$ に代入して

$$
x^2 = 12y
$$

**5.** $x + y = 2t$, $x - y = \dfrac{2}{t}$。両者を掛けると

$$
(x+y)(x-y) = 2t \cdot \frac{2}{t} = 4 \quad\Longrightarrow\quad x^2 - y^2 = 4
$$

これは双曲線 $\dfrac{x^2}{4} - \dfrac{y^2}{4} = 1$ である。

**6.** 分母を払うと $r(1 + \cos\theta) = 2$、すなわち $r + r\cos\theta = 2$。$r\cos\theta = x$ より $r = 2 - x$。両辺を2乗して $r^2 = (2-x)^2$、$r^2 = x^2 + y^2$ を代入すると

$$
x^2 + y^2 = 4 - 4x + x^2 \quad\Longrightarrow\quad y^2 = -4x + 4 = -4(x - 1)
$$

これは放物線 $y^2 = -4(x-1)$ である。（離心率 $1$ の2次曲線が放物線になることの一例。）

**7.** $x$ と $y$ それぞれについて平方完成する。

$$
(x^2 - 2x) + 4(y^2 + 2y) + 1 = (x-1)^2 - 1 + 4\{(y+1)^2 - 1\} + 1 = (x-1)^2 + 4(y+1)^2 - 4
$$

$= 0$ とおくと $(x-1)^2 + 4(y+1)^2 = 4$、両辺を $4$ で割って

$$
\frac{(x-1)^2}{4} + (y+1)^2 = 1
$$

これは中心 $(1, -1)$、長半径 $2$・短半径 $1$ の**楕円**である。

### つまずきやすいポイント

- **楕円と双曲線で $c$ の求め方が逆**：楕円は $c = \sqrt{a^2 - b^2}$（$a > b$）、双曲線は $c = \sqrt{a^2 + b^2}$。符号を取り違えると焦点の位置を誤ります。「楕円は引き算、双曲線は足し算」と覚えましょう。
- **焦点が $x$ 軸上か $y$ 軸上か**：楕円では分母の大きいほうの軸上に焦点があります。$\dfrac{x^2}{4}+\dfrac{y^2}{9}=1$ なら $y$ 軸上です。標準形の丸暗記に頼らず、$a$（大きいほう）を確認しましょう。
- **媒介変数の消去は範囲に注意**：$t = \cos\theta$ などとおいて消去する際、もとのパラメータの動く範囲によって、得られる曲線が一部分に限られることがあります。$-1 \leq \cos\theta \leq 1$ のような値域を確認しましょう。
- **極座標の $\theta$ の不定性**：同じ点でも $(r, \theta)$ の表し方は一通りではありません（$\theta$ に $2\pi$ を足しても同じ、$r < 0$ を許す流儀もある）。極方程式を直交座標に直すときは、$r$ を掛けて $r^2, r\cos\theta$ の形を作るのが安全です。
- **放物線の $4p$ の扱い**：$y^2 = 4px$ の $4p$ を $p$ と混同しないこと。焦点は $(p, 0)$ であって $(4p, 0)$ ではありません。

---

## 複素数平面

### この単元で学ぶこと

- 複素数の図示（複素数平面・ガウス平面）、絶対値と共役
- 極形式と、積・商の図形的意味（回転と拡大）
- ド・モアブルの定理と累乗・n乗根
- 複素数と図形（内分・外分、回転移動、垂直・平行、三角形の形状）

### 解説

#### 複素数平面

複素数 $z = a + bi$（$a, b$ は実数、$i^2 = -1$）を、座標平面上の点 $(a, b)$ に対応させた平面を**複素数平面（ガウス平面）**といいます。$x$ 軸を**実軸**、$y$ 軸を**虚軸**と呼びます。

- **絶対値**：$|z| = \sqrt{a^2 + b^2}$（原点からの距離）
- **共役複素数**：$\bar{z} = a - bi$（実軸に関する対称点）
- 性質：$z\bar{z} = |z|^2$、$|z_1 z_2| = |z_1||z_2|$、$\overline{z_1 z_2} = \bar{z_1}\,\bar{z_2}$

2点 $z_1, z_2$ 間の距離は $|z_2 - z_1|$ で表されます。これは複素数平面の大きな利点で、図形の距離をそのまま複素数の絶対値で扱えます。

#### 極形式

$0$ でない複素数 $z = a + bi$ は、絶対値 $r = |z|$ と偏角 $\theta = \arg z$ を用いて

$$
z = r(\cos\theta + i\sin\theta)
$$

と表せます。これを**極形式**といいます。ここで $a = r\cos\theta$, $b = r\sin\theta$ です。極形式の最大の意義は、**積と商が回転・拡大として解釈できる**点にあります。$z_1 = r_1(\cos\theta_1 + i\sin\theta_1)$, $z_2 = r_2(\cos\theta_2 + i\sin\theta_2)$ とすると

$$
z_1 z_2 = r_1 r_2\{\cos(\theta_1 + \theta_2) + i\sin(\theta_1 + \theta_2)\}
$$
$$
\frac{z_1}{z_2} = \frac{r_1}{r_2}\{\cos(\theta_1 - \theta_2) + i\sin(\theta_1 - \theta_2)\}
$$

すなわち「掛けると絶対値は掛け算、偏角は足し算」。特に $z$ に $\cos\alpha + i\sin\alpha$ を掛けることは、点 $z$ を原点を中心に角 $\alpha$ だけ回転させることを意味します。

#### ド・モアブルの定理

積の偏角が足し算になることを繰り返すと、任意の整数 $n$ について

$$
\{r(\cos\theta + i\sin\theta)\}^n = r^n(\cos n\theta + i\sin n\theta)
$$

が成り立ちます。これが**ド・モアブルの定理**です。複素数の累乗を、偏角の $n$ 倍・絶対値の $n$ 乗として一気に計算できます。

**1の n乗根**：$z^n = 1$ の解は、絶対値が $1$、偏角が $\dfrac{2k\pi}{n}$（$k = 0, 1, \ldots, n-1$）の $n$ 個で

$$
z_k = \cos\frac{2k\pi}{n} + i\sin\frac{2k\pi}{n}
$$

これらは単位円周上に等間隔（正 $n$ 角形の頂点）に並びます。

#### 複素数と図形

複素数平面では、図形の操作が複素数の演算で表せます。

- **内分・外分**：2点 $\alpha, \beta$ を $m:n$ に内分する点は $\dfrac{n\alpha + m\beta}{m+n}$（実数の座標と同じ形）。
- **回転移動**：点 $\alpha$ を中心に、点 $z$ を角 $\theta$ だけ回転した点 $w$ は

$$
w = \alpha + (\cos\theta + i\sin\theta)(z - \alpha)
$$

（中心を原点に移し、回転させ、戻す、という3段階。）

- **平行・垂直・角**：3点 $\alpha, \beta, \gamma$ について、$\dfrac{\gamma - \alpha}{\beta - \alpha}$ の偏角は、$\overrightarrow{\alpha\beta}$ から $\overrightarrow{\alpha\gamma}$ へ測った角 $\angle\beta\alpha\gamma$ を表します。したがって
  - この値が**実数** $\iff$ 3点 $\alpha, \beta, \gamma$ は一直線上（偏角が $0$ または $\pi$）
  - この値が**純虚数** $\iff$ $\overrightarrow{\alpha\beta} \perp \overrightarrow{\alpha\gamma}$（偏角が $\pm\dfrac{\pi}{2}$）

#### 複素数の方程式が表す図形

$z$ が動くとき、$z$ の満たす方程式は複素数平面上の図形（軌跡）を表します。距離が絶対値で表せることを使うのが要点です。

- $|z - \alpha| = r$：中心 $\alpha$、半径 $r$ の**円**。
- $|z - \alpha| = |z - \beta|$：2点 $\alpha, \beta$ から等距離の点、すなわち線分 $\alpha\beta$ の**垂直二等分線**。
- $|z - \alpha| = k|z - \beta|$（$k > 0$, $k \neq 1$）：**アポロニウスの円**（$\alpha, \beta$ からの距離の比が一定の点の軌跡）。

たとえば $|z - \alpha| = r$ の両辺を2乗し、$|w|^2 = w\bar w$ を用いて展開すると、$(z - \alpha)(\bar z - \bar\alpha) = r^2$ となり、$z = x + yi$ を代入すれば通常の円の方程式に一致することが確かめられます。

### 例題

**例題1（極形式）** $z = 1 + \sqrt3 i$ を極形式で表せ。

**解答** $|z| = \sqrt{1^2 + (\sqrt3)^2} = \sqrt{1 + 3} = 2$。$\cos\theta = \dfrac{1}{2}$, $\sin\theta = \dfrac{\sqrt3}{2}$ より $\theta = \dfrac{\pi}{3}$。よって

$$
z = 2\left(\cos\frac{\pi}{3} + i\sin\frac{\pi}{3}\right)
$$

---

**例題2（ド・モアブルの定理）** $(1 + \sqrt3 i)^6$ を計算せよ。

**解答** 例題1より $1 + \sqrt3 i = 2\left(\cos\dfrac{\pi}{3} + i\sin\dfrac{\pi}{3}\right)$。ド・モアブルの定理より

$$
(1+\sqrt3 i)^6 = 2^6\left(\cos\frac{6\pi}{3} + i\sin\frac{6\pi}{3}\right) = 64(\cos 2\pi + i\sin 2\pi) = 64(1 + 0) = 64
$$

---

**例題3（積の図形的意味）** $z = 3 + 2i$ を、原点を中心に $90^\circ$ 回転した点を表す複素数を求めよ。

**解答** $90^\circ$ 回転は $\cos90^\circ + i\sin90^\circ = i$ を掛けることに等しい。

$$
iz = i(3 + 2i) = 3i + 2i^2 = 3i - 2 = -2 + 3i
$$

よって求める点は $-2 + 3i$。

---

**例題4（回転移動）** 点 $\beta = 4 + i$ を、点 $\alpha = 1 + i$ を中心に $60^\circ$ 回転した点 $w$ を求めよ。

**解答** 回転の公式 $w = \alpha + (\cos60^\circ + i\sin60^\circ)(\beta - \alpha)$ を用いる。$\beta - \alpha = 3$、$\cos60^\circ + i\sin60^\circ = \dfrac{1}{2} + \dfrac{\sqrt3}{2}i$。

$$
w = (1 + i) + \left(\frac{1}{2} + \frac{\sqrt3}{2}i\right)\cdot 3 = 1 + i + \frac{3}{2} + \frac{3\sqrt3}{2}i = \frac{5}{2} + \left(1 + \frac{3\sqrt3}{2}\right)i
$$

すなわち $w = \dfrac{5}{2} + \dfrac{2 + 3\sqrt3}{2}i$。

---

**例題5（1の n乗根）** 方程式 $z^3 = 1$ の解をすべて求め、複素数平面上での配置を説明せよ。

**解答** $z = \cos\theta + i\sin\theta$ とおくと $z^3 = \cos3\theta + i\sin3\theta = 1$。よって $3\theta = 2k\pi$（$k$ は整数）、$\theta = \dfrac{2k\pi}{3}$。$k = 0, 1, 2$ に対応して

$$
z_0 = 1, \quad z_1 = \cos\frac{2\pi}{3} + i\sin\frac{2\pi}{3} = -\frac{1}{2} + \frac{\sqrt3}{2}i, \quad z_2 = -\frac{1}{2} - \frac{\sqrt3}{2}i
$$

これら3点は単位円周上に、偏角 $0, \dfrac{2\pi}{3}, \dfrac{4\pi}{3}$ で等間隔に並び、正三角形の頂点をなす。

---

**例題6（回転による正三角形の頂点）** 複素数平面上の2点 $\alpha = 1$, $\beta = 3 + 2i$ を2頂点とする正三角形の、第3の頂点 $\gamma$ を求めよ。

**解答** 正三角形なので、$\gamma$ は $\beta$ を $\alpha$ を中心に $\pm60^\circ$ 回転した点である。$\cos60^\circ + i\sin60^\circ = \dfrac{1}{2} + \dfrac{\sqrt3}{2}i$、$\beta - \alpha = 2 + 2i$ を用いると

$$
\gamma = \alpha + \left(\frac{1}{2} \pm \frac{\sqrt3}{2}i\right)(\beta - \alpha) = 1 + \left(\frac{1}{2} \pm \frac{\sqrt3}{2}i\right)(2 + 2i)
$$

$\left(\dfrac{1}{2} \pm \dfrac{\sqrt3}{2}i\right)(2 + 2i) = (1 \pm \sqrt3 i)(1 + i) = 1 + i \pm \sqrt3 i \pm \sqrt3 i^2 = (1 \mp \sqrt3) + (1 \pm \sqrt3)i$。よって

$$
\gamma = (2 \mp \sqrt3) + (1 \pm \sqrt3)i \qquad (\text{複号同順})
$$

すなわち $\gamma = (2 - \sqrt3) + (1 + \sqrt3)i$ または $\gamma = (2 + \sqrt3) + (1 - \sqrt3)i$ の2点が得られる（回転の向きに応じて2つ存在する）。

### 練習問題

1. $z = -1 + i$ について、絶対値 $|z|$ と偏角 $\arg z$ を求め、極形式で表せ。

2. $z_1 = 2\left(\cos\dfrac{\pi}{4} + i\sin\dfrac{\pi}{4}\right)$, $z_2 = 3\left(\cos\dfrac{\pi}{12} + i\sin\dfrac{\pi}{12}\right)$ について、$z_1 z_2$ と $\dfrac{z_1}{z_2}$ を極形式で求めよ。

3. ド・モアブルの定理を用いて $(\sqrt3 - i)^{5}$ を計算せよ（$a + bi$ の形で答えよ）。

4. 点 $z = 2 + 3i$ を、点 $1 - i$ を中心に $90^\circ$ 回転した点を求めよ。

5. 方程式 $z^4 = -1$ の解をすべて $a + bi$ の形で求めよ。

6. 複素数平面上の3点 $A(2 + i)$, $B(5 + 3i)$, $C(1 + 4i)$ について、$\dfrac{\gamma - \alpha}{\beta - \alpha}$（$\alpha, \beta, \gamma$ はそれぞれ $A, B, C$ を表す複素数）を計算し、$\angle BAC$ が直角かどうかを判定せよ。

7. 方程式 $|z - 2| = 2|z + 1|$ を満たす点 $z$ は、どのような図形を描くか。直交座標の方程式で答えよ。

### 解答と解説

**1.** $|z| = \sqrt{(-1)^2 + 1^2} = \sqrt2$。$\cos\theta = \dfrac{-1}{\sqrt2}$, $\sin\theta = \dfrac{1}{\sqrt2}$ より $\theta = \dfrac{3\pi}{4}$。よって

$$
z = \sqrt2\left(\cos\frac{3\pi}{4} + i\sin\frac{3\pi}{4}\right)
$$

**2.** 積は絶対値を掛け、偏角を足す。

$$
z_1 z_2 = 2\cdot3\left(\cos\left(\frac{\pi}{4}+\frac{\pi}{12}\right) + i\sin\left(\frac{\pi}{4}+\frac{\pi}{12}\right)\right) = 6\left(\cos\frac{\pi}{3} + i\sin\frac{\pi}{3}\right)
$$

（$\dfrac{\pi}{4} + \dfrac{\pi}{12} = \dfrac{3\pi + \pi}{12} = \dfrac{4\pi}{12} = \dfrac{\pi}{3}$。）商は絶対値を割り、偏角を引く。

$$
\frac{z_1}{z_2} = \frac{2}{3}\left(\cos\left(\frac{\pi}{4}-\frac{\pi}{12}\right) + i\sin\left(\frac{\pi}{4}-\frac{\pi}{12}\right)\right) = \frac{2}{3}\left(\cos\frac{\pi}{6} + i\sin\frac{\pi}{6}\right)
$$

**3.** $\sqrt3 - i$ を極形式にする。$|\sqrt3 - i| = \sqrt{3 + 1} = 2$、$\cos\theta = \dfrac{\sqrt3}{2}$, $\sin\theta = -\dfrac{1}{2}$ より $\theta = -\dfrac{\pi}{6}$。ド・モアブルの定理より

$$
(\sqrt3 - i)^5 = 2^5\left(\cos\left(-\frac{5\pi}{6}\right) + i\sin\left(-\frac{5\pi}{6}\right)\right) = 32\left(-\frac{\sqrt3}{2} - \frac{1}{2}i\right) = -16\sqrt3 - 16i
$$

**4.** $90^\circ$ 回転は $i$ を掛けること。中心 $\alpha = 1 - i$、$z = 2 + 3i$ とすると $z - \alpha = (2 + 3i) - (1 - i) = 1 + 4i$。

$$
w = \alpha + i(z - \alpha) = (1 - i) + i(1 + 4i) = 1 - i + i + 4i^2 = 1 - 4 = -3
$$

よって求める点は $-3$（すなわち $-3 + 0i$）。

**5.** $-1 = \cos\pi + i\sin\pi$。$z^4 = -1$ の解は絶対値 $1$、偏角 $\dfrac{\pi + 2k\pi}{4}$（$k = 0,1,2,3$）。

$$
\theta = \frac{\pi}{4},\ \frac{3\pi}{4},\ \frac{5\pi}{4},\ \frac{7\pi}{4}
$$

それぞれ

$$
z = \frac{\sqrt2}{2} + \frac{\sqrt2}{2}i,\quad -\frac{\sqrt2}{2} + \frac{\sqrt2}{2}i,\quad -\frac{\sqrt2}{2} - \frac{\sqrt2}{2}i,\quad \frac{\sqrt2}{2} - \frac{\sqrt2}{2}i
$$

**6.** $\alpha = 2 + i$, $\beta = 5 + 3i$, $\gamma = 1 + 4i$。$\beta - \alpha = 3 + 2i$, $\gamma - \alpha = -1 + 3i$。

$$
\frac{\gamma - \alpha}{\beta - \alpha} = \frac{-1 + 3i}{3 + 2i} = \frac{(-1 + 3i)(3 - 2i)}{(3 + 2i)(3 - 2i)} = \frac{-3 + 2i + 9i - 6i^2}{9 + 4} = \frac{-3 + 11i + 6}{13} = \frac{3 + 11i}{13}
$$

これは純虚数ではない（実部 $\dfrac{3}{13} \neq 0$）ので、$\overrightarrow{AB}$ と $\overrightarrow{AC}$ は垂直ではなく、$\angle BAC$ は直角ではない。

**7.** $z = x + yi$ とおく。$|z - 2| = 2|z + 1|$ の両辺を2乗すると

$$
|z - 2|^2 = 4|z + 1|^2 \ \Longrightarrow\ (x-2)^2 + y^2 = 4\{(x+1)^2 + y^2\}
$$

展開して整理すると

$$
x^2 - 4x + 4 + y^2 = 4x^2 + 8x + 4 + 4y^2
$$
$$
3x^2 + 3y^2 + 12x = 0 \ \Longrightarrow\ x^2 + y^2 + 4x = 0 \ \Longrightarrow\ (x + 2)^2 + y^2 = 4
$$

よって中心 $(-2, 0)$、半径 $2$ の円（アポロニウスの円）を描く。

### つまずきやすいポイント

- **偏角の範囲と象限**：$\arg z$ を求めるとき、$\cos\theta$, $\sin\theta$ の符号から $z$ がどの象限にあるかを確認しないと、$\theta$ を $\pi$ だけ間違えることがあります。図をかいて位置を確かめましょう。
- **積・商での偏角の増減**：積では偏角を足し、商では引きます。「掛け算＝回転を重ねる（角を足す）」というイメージを持つと符号ミスが減ります。
- **ド・モアブルは絶対値の $n$ 乗も忘れずに**：$\{r(\cos\theta+i\sin\theta)\}^n = r^n(\cos n\theta + i\sin n\theta)$。偏角だけ $n$ 倍して $r^n$ を忘れる誤りが頻出です。
- **n乗根は $n$ 個すべて**：$z^n = w$ の解は必ず $n$ 個あり、単位円（正確には半径 $|w|^{1/n}$ の円）上に等間隔で並びます。1つだけ求めて満足しないこと。
- **回転移動は「中心を原点に移してから」**：$\alpha$ を中心とする回転は $w = \alpha + (\cos\theta+i\sin\theta)(z-\alpha)$。いきなり $z$ に回転を掛けると、原点中心の回転になってしまいます。
- **$\dfrac{\gamma-\alpha}{\beta-\alpha}$ の意味**：これは「$\alpha$ から見た $\beta$ と $\gamma$ の関係」を表し、実数なら一直線上、純虚数なら垂直。絶対値は $\dfrac{|\alpha\gamma|}{|\alpha\beta|}$（辺の比）を表します。図形問題での強力な判定法です。

---

## 数学Cの全体を振り返って

数学Cの3単元は、いずれも「**図形と計算の橋渡し**」を担っています。

- **ベクトル**は、向きと大きさをもつ量を成分と内積で扱い、図形の位置関係（平行・垂直・分点・重心）を計算に翻訳します。空間図形もまったく同じ枠組みで扱える点が強みです。
- **平面上の曲線**は、放物線・楕円・双曲線という2次曲線を「焦点からの距離」という統一的な視点でとらえ、媒介変数や極座標という別の言葉でも表現します。同じ曲線を複数の言語で語れるようになることが目標です。
- **複素数平面**は、複素数を平面上の点とみなし、掛け算を「回転と拡大」として幾何学的に解釈します。ド・モアブルの定理と回転移動は、図形問題を鮮やかに解く武器になります。

3単元を貫くのは、「**問題を計算で処理し、結果を図形で解釈する**」という往復運動です。どの分野でも、必ず図をかき、式の一つひとつが図の上で何を意味するかを確かめながら学習を進めてください。そうすれば、抽象的に見えた数学Cが、図形を自在に操るための実践的な道具に変わっていくはずです。

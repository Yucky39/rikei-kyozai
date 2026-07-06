---
layout: default
title: 高校 数学III
parent: 算数・数学
nav_order: 14
---

# 高校 数学III

数学IIIは、理系の数学の集大成となる科目です。数学IIで学んだ微分・積分を、指数関数・対数関数・三角関数・分数関数・無理関数などのあらゆる関数へと拡張し、「極限」という考え方を土台にして解析学の入り口に立ちます。大学入試では最頻出の分野であると同時に、大学以降の数学・物理学・工学のすべての基礎となります。

この教材では、現行学習指導要領に基づき、次の単元を扱います。

| 章 | 単元 | 中心となるテーマ |
|---|---|---|
| 1 | 数列の極限 | 無限数列の収束・発散、無限級数 |
| 2 | 関数の極限 | 関数の極限、連続性、重要な極限公式 |
| 3 | 微分法 | いろいろな関数の導関数、微分の計算技術 |
| 4 | 微分法の応用 | 接線、増減、極値、最大最小、不等式・方程式への応用 |
| 5 | 積分法 | 不定積分・定積分の計算、置換積分・部分積分、区分求積法 |
| 6 | 積分法の応用 | 面積、体積、曲線の長さ、速度と道のり |

---

## 第1章 数列の極限

### この単元で学ぶこと

- 無限数列の収束・発散の意味と、極限値の求め方
- 極限の性質（四則演算との関係）と、はさみうちの原理
- 無限等比数列 $\{r^n\}$ の極限の分類
- 無限級数・無限等比級数の収束条件と和の求め方
- 漸化式で定義された数列の極限（入試頻出）

### 解説

#### 数列の極限の定義

無限数列 $\{a_n\}$ において、$n$ を限りなく大きくするとき、$a_n$ が一定の値 $\alpha$ に限りなく近づくならば、数列 $\{a_n\}$ は $\alpha$ に**収束する**といい、

$$
\lim_{n \to \infty} a_n = \alpha
$$

と書きます。$\alpha$ をこの数列の**極限値**といいます。収束しない数列は**発散する**といい、発散には次の3種類があります。

- $a_n$ が限りなく大きくなる：**正の無限大に発散**（$\lim_{n\to\infty} a_n = \infty$）
- $a_n$ が限りなく小さくなる：**負の無限大に発散**（$\lim_{n\to\infty} a_n = -\infty$）
- どちらでもない：**振動**（例：$a_n = (-1)^n$）

#### 極限の性質

数列 $\{a_n\}$, $\{b_n\}$ が収束して $\lim a_n = \alpha$, $\lim b_n = \beta$ のとき、次が成り立ちます。

| 性質 | 内容 |
|---|---|
| 定数倍 | $\lim_{n\to\infty} k a_n = k\alpha$（$k$ は定数） |
| 和・差 | $\lim_{n\to\infty} (a_n \pm b_n) = \alpha \pm \beta$ |
| 積 | $\lim_{n\to\infty} a_n b_n = \alpha\beta$ |
| 商 | $\lim_{n\to\infty} \dfrac{a_n}{b_n} = \dfrac{\alpha}{\beta}$（$\beta \neq 0$） |

**注意**：これらは「両方の数列が収束する」ときにのみ使えます。$\infty - \infty$ や $\dfrac{\infty}{\infty}$ のような**不定形**は、式変形（有理化、最高次の項でくくる等）で不定形を解消してから極限をとります。

#### はさみうちの原理

すべての $n$ について $a_n \le c_n \le b_n$ であり、$\lim_{n\to\infty} a_n = \lim_{n\to\infty} b_n = \alpha$ ならば、

$$
\lim_{n \to \infty} c_n = \alpha
$$

が成り立ちます。**なぜ成り立つか**：$c_n$ は両側から $\alpha$ に近づく2つの数列に挟まれているため、逃げ場がなく $\alpha$ に近づくしかないからです。$\sin n$ や $(-1)^n$ のように値が確定しない項を含む極限で威力を発揮します。

また、$a_n \le b_n$ かつ $\lim a_n = \infty$ ならば $\lim b_n = \infty$（追い出しの原理）も成り立ちます。

#### 無限等比数列 $\{r^n\}$ の極限

**最重要の分類**です。必ず覚えてください。

| $r$ の範囲 | $\lim_{n\to\infty} r^n$ |
|---|---|
| $r > 1$ | $\infty$（発散） |
| $r = 1$ | $1$（収束） |
| $-1 < r < 1$ | $0$（収束） |
| $r \le -1$ | 振動（発散） |

したがって、**$\{r^n\}$ が収束する条件は $-1 < r \le 1$** です（$r=1$ を含むことに注意）。

**なぜ成り立つか**：$r>1$ のとき $r = 1+h$（$h>0$）とおくと、二項定理より $r^n = (1+h)^n \ge 1 + nh$ となり、右辺は限りなく大きくなるので $r^n \to \infty$（追い出しの原理）。$|r|<1$ のときは $\left|\dfrac{1}{r}\right| > 1$ から $\left|\dfrac{1}{r^n}\right| \to \infty$、よって $|r^n| \to 0$ となります。

#### 無限級数

無限数列 $\{a_n\}$ の各項を順に加えた式 $\displaystyle\sum_{n=1}^{\infty} a_n = a_1 + a_2 + a_3 + \cdots$ を**無限級数**といいます。部分和 $S_n = a_1 + a_2 + \cdots + a_n$ の数列 $\{S_n\}$ が $S$ に収束するとき、この無限級数は $S$ に**収束する**といい、$S$ をその**和**といいます。

**重要な性質**：

- 無限級数 $\sum a_n$ が収束するならば $\lim_{n\to\infty} a_n = 0$
- 対偶：$\lim_{n\to\infty} a_n \neq 0$ ならば $\sum a_n$ は発散する

**なぜ成り立つか**：$a_n = S_n - S_{n-1}$ であり、$S_n \to S$, $S_{n-1} \to S$ なので $a_n \to S - S = 0$ となるからです。逆は成り立ちません（例：$\sum \frac{1}{\sqrt{n}}$ は $a_n \to 0$ だが発散）。

#### 無限等比級数

初項 $a$、公比 $r$ の無限等比級数 $a + ar + ar^2 + \cdots$ について：

$$
\text{収束条件：} a = 0 \ \text{または} \ |r| < 1, \qquad \text{和：} S = \frac{a}{1-r} \ (a \neq 0,\ |r|<1)
$$

**なぜ成り立つか**：$r \neq 1$ のとき部分和は $S_n = \dfrac{a(1-r^n)}{1-r}$ です。$|r|<1$ なら $r^n \to 0$ なので $S_n \to \dfrac{a}{1-r}$。$|r| \ge 1$（かつ $a \ne 0$）なら $r^n$ が収束しない、または $a_n \to 0$ とならないため発散します。

### 例題

**例題1**　次の極限を求めよ。

$$
\lim_{n \to \infty} \left( \sqrt{n^2 + 2n} - n \right)
$$

**解答**　$\infty - \infty$ の不定形なので、分子を有理化する。

$$
\sqrt{n^2+2n} - n = \frac{(\sqrt{n^2+2n}-n)(\sqrt{n^2+2n}+n)}{\sqrt{n^2+2n}+n} = \frac{(n^2+2n) - n^2}{\sqrt{n^2+2n}+n} = \frac{2n}{\sqrt{n^2+2n}+n}
$$

分母・分子を $n$ で割ると（$n > 0$ なので $n = \sqrt{n^2}$ に注意）、

$$
= \frac{2}{\sqrt{1 + \dfrac{2}{n}} + 1} \longrightarrow \frac{2}{\sqrt{1+0}+1} = \frac{2}{2} = 1
$$

よって求める極限値は $1$。

**例題2**　$a_1 = 1$, $a_{n+1} = \dfrac{1}{2}a_n + 1$ で定められる数列 $\{a_n\}$ の極限を求めよ。

**解答**　特性方程式 $\alpha = \dfrac{1}{2}\alpha + 1$ を解くと $\alpha = 2$。漸化式から辺々引くと、

$$
a_{n+1} - 2 = \frac{1}{2}(a_n - 2)
$$

よって数列 $\{a_n - 2\}$ は初項 $a_1 - 2 = -1$、公比 $\dfrac{1}{2}$ の等比数列であり、

$$
a_n - 2 = -\left(\frac{1}{2}\right)^{n-1} \quad \text{すなわち} \quad a_n = 2 - \left(\frac{1}{2}\right)^{n-1}
$$

$\left|\dfrac{1}{2}\right| < 1$ より $\left(\dfrac{1}{2}\right)^{n-1} \to 0$ なので、

$$
\lim_{n \to \infty} a_n = 2
$$

**例題3**　無限級数 $\displaystyle\sum_{n=1}^{\infty} \frac{1}{n(n+1)}$ の和を求めよ。

**解答**　部分分数分解 $\dfrac{1}{n(n+1)} = \dfrac{1}{n} - \dfrac{1}{n+1}$ を用いる。部分和は

$$
S_n = \left(1 - \frac{1}{2}\right) + \left(\frac{1}{2} - \frac{1}{3}\right) + \cdots + \left(\frac{1}{n} - \frac{1}{n+1}\right) = 1 - \frac{1}{n+1}
$$

途中の項が打ち消し合う（望遠鏡和）。よって

$$
\sum_{n=1}^{\infty} \frac{1}{n(n+1)} = \lim_{n\to\infty} S_n = \lim_{n\to\infty}\left(1 - \frac{1}{n+1}\right) = 1
$$

### 練習問題

**問1**　$\displaystyle\lim_{n\to\infty} \frac{3n^2 - 2n + 1}{n^2 + 5}$ を求めよ。

**問2**　$\displaystyle\lim_{n\to\infty} \left( \sqrt{n^2 + 3n} - n \right)$ を求めよ。

**問3**　$\displaystyle\lim_{n\to\infty} \frac{5^n - 3^n}{5^n + 3^n}$ を求めよ。

**問4**　$\displaystyle\lim_{n\to\infty} \frac{\sin n}{n}$ を求めよ。

**問5**　無限級数 $\displaystyle\sum_{n=1}^{\infty} (x-1)^n$ が収束するような実数 $x$ の値の範囲を求め、そのときの和を求めよ。

**問6**　$a_1 = 3$, $a_{n+1} = \dfrac{1}{3}a_n + 2$ で定められる数列 $\{a_n\}$ について、$\displaystyle\lim_{n\to\infty} a_n$ を求めよ。

### 解答と解説

**問1**　分母・分子を $n^2$ で割る。

$$
\frac{3n^2 - 2n + 1}{n^2 + 5} = \frac{3 - \dfrac{2}{n} + \dfrac{1}{n^2}}{1 + \dfrac{5}{n^2}} \longrightarrow \frac{3 - 0 + 0}{1 + 0} = \boldsymbol{3}
$$

**問2**　有理化する。

$$
\sqrt{n^2+3n} - n = \frac{3n}{\sqrt{n^2+3n}+n} = \frac{3}{\sqrt{1+\dfrac{3}{n}}+1} \longrightarrow \frac{3}{1+1} = \boldsymbol{\frac{3}{2}}
$$

**問3**　最も大きい底 $5^n$ で分母・分子を割る。

$$
\frac{5^n - 3^n}{5^n + 3^n} = \frac{1 - \left(\dfrac{3}{5}\right)^n}{1 + \left(\dfrac{3}{5}\right)^n} \longrightarrow \frac{1-0}{1+0} = \boldsymbol{1}
$$

$\left|\dfrac{3}{5}\right| < 1$ より $\left(\dfrac{3}{5}\right)^n \to 0$ を用いた。

**問4**　すべての $n$ について $-1 \le \sin n \le 1$ なので、

$$
-\frac{1}{n} \le \frac{\sin n}{n} \le \frac{1}{n}
$$

$\displaystyle\lim_{n\to\infty}\left(-\frac{1}{n}\right) = \lim_{n\to\infty}\frac{1}{n} = 0$ だから、はさみうちの原理より $\displaystyle\lim_{n\to\infty} \frac{\sin n}{n} = \boldsymbol{0}$。

**問5**　これは初項 $x-1$、公比 $x-1$ の無限等比級数である。

（i）$x - 1 = 0$ すなわち $x = 1$ のとき、すべての項が $0$ なので収束し、和は $0$。

（ii）$x - 1 \neq 0$ のとき、収束条件は $|x-1| < 1$ すなわち $0 < x < 2$（$x \ne 1$）。このとき和は

$$
S = \frac{x-1}{1-(x-1)} = \frac{x-1}{2-x}
$$

（i）（ii）をまとめると、$x=1$ のとき和 $\dfrac{x-1}{2-x} = 0$ とも一致するので、

**収束する範囲は $0 < x < 2$、和は $S = \dfrac{x-1}{2-x}$**

**問6**　特性方程式 $\alpha = \dfrac{1}{3}\alpha + 2$ より $\alpha = 3$。

$$
a_{n+1} - 3 = \frac{1}{3}(a_n - 3)
$$

$a_1 - 3 = 0$ なので、すべての $n$ で $a_n - 3 = 0$、すなわち $a_n = 3$（定数数列）。よって $\displaystyle\lim_{n\to\infty} a_n = \boldsymbol{3}$。

（初項がたまたま特性方程式の解と一致した場合、数列は最初から一定値である。機械的に等比数列の一般項を書く前に初項を確認する習慣をつけよう。）

### つまずきやすいポイント

- **$\{r^n\}$ の収束条件は $-1 < r \le 1$、無限等比級数の収束条件は「$a=0$ または $|r| < 1$」**。この2つを混同するミスが非常に多い。数列は $r=1$ で収束（値1）するが、級数は $r=1$ だと $a+a+a+\cdots$ で発散する。
- $\infty - \infty$、$\dfrac{\infty}{\infty}$ は「不定形」であり、そのままでは値が決まらない。**必ず式変形（有理化・最高次で割る）をしてから**極限をとる。
- 「$\lim a_n = 0$ だから $\sum a_n$ は収束」は**誤り**。矢印の向きは「級数収束 $\Rightarrow$ 項が0に収束」のみ。
- 極限の四則の性質は「収束する数列同士」にしか使えない。発散する数列に対して形式的に使わないこと。
- はさみうちの原理を使うときは、**両側の数列の極限が一致すること**を必ず確認・明記する。

---

## 第2章 関数の極限

### この単元で学ぶこと

- 関数の極限の意味、右側極限・左側極限
- 極限の計算（不定形の処理：因数分解・有理化）
- 三角関数の極限 $\displaystyle\lim_{x\to 0}\frac{\sin x}{x} = 1$ とその応用
- 自然対数の底 $e$ の定義と、指数・対数関数の極限
- 関数の連続性と中間値の定理

### 解説

#### 関数の極限

関数 $f(x)$ において、$x$ が $a$ と異なる値をとりながら $a$ に限りなく近づくとき、$f(x)$ が一定の値 $\alpha$ に限りなく近づくならば、

$$
\lim_{x \to a} f(x) = \alpha
$$

と書きます。ここで重要なのは、**$x = a$ における値 $f(a)$ とは無関係**だということです（$f(a)$ が定義されていなくてもよい）。

#### 右側極限と左側極限

- $x$ が $a$ より大きい側から近づくときの極限：**右側極限** $\displaystyle\lim_{x \to a+0} f(x)$
- $x$ が $a$ より小さい側から近づくときの極限：**左側極限** $\displaystyle\lim_{x \to a-0} f(x)$

$$
\lim_{x \to a} f(x) = \alpha \iff \lim_{x \to a+0} f(x) = \lim_{x \to a-0} f(x) = \alpha
$$

例えば $\displaystyle\lim_{x\to 0+0}\frac{1}{x} = \infty$, $\displaystyle\lim_{x\to 0-0}\frac{1}{x} = -\infty$ なので $\displaystyle\lim_{x\to 0}\frac{1}{x}$ は存在しません。

#### 分数関数の極限で $\frac{0}{0}$ の不定形になる場合

$\displaystyle\lim_{x\to a}\frac{f(x)}{g(x)}$ で分母 $g(x) \to 0$ かつ極限値が存在するならば、**分子も $f(x) \to 0$ でなければならない**（さもないと発散する）。この事実は「極限値から係数を決定する」タイプの入試問題で使う重要な論法です。

#### 三角関数の極限（最重要公式）

$$
\lim_{x \to 0} \frac{\sin x}{x} = 1 \qquad (x \text{ はラジアン})
$$

**なぜ成り立つか（証明の概略）**：$0 < x < \dfrac{\pi}{2}$ のとき、単位円で中心角 $x$ の扇形を考えると、面積の比較から

$$
\triangle OAB < \text{扇形} OAB < \triangle OAT
$$

すなわち $\dfrac{1}{2}\sin x < \dfrac{1}{2}x < \dfrac{1}{2}\tan x$。各辺を $\dfrac{1}{2}\sin x\,(>0)$ で割って逆数をとると、

$$
\cos x < \frac{\sin x}{x} < 1
$$

$x \to +0$ のとき $\cos x \to 1$ なので、はさみうちの原理より $\dfrac{\sin x}{x} \to 1$。$x < 0$ のときは $t = -x$ とおけば同じ結論が得られます。

この公式から次の派生公式も導かれます。

| 公式 | 導き方 |
|---|---|
| $\displaystyle\lim_{x\to 0}\frac{\tan x}{x} = 1$ | $\dfrac{\tan x}{x} = \dfrac{\sin x}{x}\cdot\dfrac{1}{\cos x}$ |
| $\displaystyle\lim_{x\to 0}\frac{1 - \cos x}{x^2} = \frac{1}{2}$ | 分母分子に $1+\cos x$ を掛ける |
| $\displaystyle\lim_{x\to 0}\frac{\sin kx}{x} = k$ | $\dfrac{\sin kx}{kx}\cdot k$ と変形 |

#### 自然対数の底 $e$

$$
e = \lim_{n \to \infty}\left(1 + \frac{1}{n}\right)^n = \lim_{h \to 0}(1+h)^{\frac{1}{h}} = 2.71828\cdots
$$

$e$ は無理数で、微分積分学全体の土台となる定数です。$e$ を底とする対数 $\log_e x$ を**自然対数**といい、単に $\log x$ と書きます。$e$ の定義から次の重要な極限が導かれます。

$$
\lim_{x \to 0} \frac{\log(1+x)}{x} = 1, \qquad \lim_{x \to 0} \frac{e^x - 1}{x} = 1
$$

**なぜ成り立つか**：$\dfrac{\log(1+x)}{x} = \log(1+x)^{\frac{1}{x}} \to \log e = 1$。2つ目は $e^x - 1 = t$ とおくと $x = \log(1+t)$ で、1つ目の逆数の形に帰着します。

#### 関数の連続性

関数 $f(x)$ が $x = a$ で**連続**であるとは、

$$
\lim_{x \to a} f(x) = f(a)
$$

が成り立つことです（極限が存在し、かつその値が関数値に一致する）。区間内のすべての点で連続な関数を、その区間で連続な関数といいます。

#### 中間値の定理

関数 $f(x)$ が閉区間 $[a,\,b]$ で連続で、$f(a) \neq f(b)$ ならば、$f(a)$ と $f(b)$ の間の任意の値 $k$ に対して、

$$
f(c) = k, \quad a < c < b
$$

を満たす $c$ が少なくとも1つ存在します。特に **$f(a)$ と $f(b)$ が異符号ならば、方程式 $f(x) = 0$ は $a < x < b$ に少なくとも1つの実数解をもちます**。これは「解の存在」を示す強力な道具です（連続なグラフは値を飛ばして移動できない、というのが直観的な理由です）。

### 例題

**例題1**　$\displaystyle\lim_{x \to 0} \frac{1 - \cos x}{x^2}$ を求めよ。

**解答**　分母・分子に $1 + \cos x$ を掛ける。

$$
\frac{1-\cos x}{x^2} = \frac{(1-\cos x)(1+\cos x)}{x^2 (1+\cos x)} = \frac{1 - \cos^2 x}{x^2(1+\cos x)} = \frac{\sin^2 x}{x^2(1+\cos x)} = \left(\frac{\sin x}{x}\right)^2 \cdot \frac{1}{1+\cos x}
$$

$x \to 0$ のとき $\dfrac{\sin x}{x} \to 1$, $\cos x \to 1$ なので、

$$
\lim_{x \to 0} \frac{1-\cos x}{x^2} = 1^2 \cdot \frac{1}{1+1} = \frac{1}{2}
$$

**例題2**　等式 $\displaystyle\lim_{x \to 1} \frac{a\sqrt{x} + b}{x - 1} = 2$ が成り立つように、定数 $a,\ b$ の値を定めよ。

**解答**　$x \to 1$ のとき分母 $x - 1 \to 0$ である。極限値が存在する（$2$ に収束する）ためには、分子も $0$ に収束しなければならない。よって

$$
\lim_{x \to 1}(a\sqrt{x} + b) = a + b = 0 \quad \therefore\ b = -a
$$

このとき

$$
\frac{a\sqrt{x} - a}{x-1} = \frac{a(\sqrt{x}-1)}{(\sqrt{x}-1)(\sqrt{x}+1)} = \frac{a}{\sqrt{x}+1} \longrightarrow \frac{a}{2} \quad (x \to 1)
$$

これが $2$ に等しいので $\dfrac{a}{2} = 2$、よって $a = 4$, $b = -4$。

（逆にこのとき与式の極限は確かに $2$ となるので十分性も満たす。）

**例題3**　方程式 $x = \cos x$ は $0 < x < \dfrac{\pi}{2}$ の範囲に実数解をもつことを示せ。

**解答**　$f(x) = x - \cos x$ とおくと、$f(x)$ は連続関数の差なので、閉区間 $\left[0,\ \dfrac{\pi}{2}\right]$ で連続である。

$$
f(0) = 0 - \cos 0 = -1 < 0, \qquad f\!\left(\frac{\pi}{2}\right) = \frac{\pi}{2} - 0 = \frac{\pi}{2} > 0
$$

$f(0)$ と $f\!\left(\dfrac{\pi}{2}\right)$ は異符号なので、中間値の定理より $f(c) = 0$ すなわち $c = \cos c$ を満たす $c$ が $0 < c < \dfrac{\pi}{2}$ に少なくとも1つ存在する。（証明終）

### 練習問題

**問1**　$\displaystyle\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$ を求めよ。

**問2**　$\displaystyle\lim_{x \to 0} \frac{\sqrt{1+x} - 1}{x}$ を求めよ。

**問3**　$\displaystyle\lim_{x \to 0} \frac{\sin 3x}{\sin 5x}$ を求めよ。

**問4**　$\displaystyle\lim_{x \to \infty} \left(1 + \frac{2}{x}\right)^x$ を求めよ。

**問5**　関数 $f(x) = \dfrac{x^2 - 1}{x - 1}$（$x \neq 1$）、$f(1) = a$ が $x = 1$ で連続となるように定数 $a$ の値を定めよ。

**問6**　等式 $\displaystyle\lim_{x \to 0} \frac{a x + b - \cos x}{x^2}$ が有限な値になるように定数 $a, b$ を定め、そのときの極限値を求めよ。

### 解答と解説

**問1**　分子を因数分解する。$x \neq 2$ のもとで

$$
\frac{x^2-4}{x-2} = \frac{(x-2)(x+2)}{x-2} = x+2 \longrightarrow \boldsymbol{4} \quad (x \to 2)
$$

**問2**　分子を有理化する。

$$
\frac{\sqrt{1+x}-1}{x} = \frac{(1+x)-1}{x(\sqrt{1+x}+1)} = \frac{1}{\sqrt{1+x}+1} \longrightarrow \frac{1}{1+1} = \boldsymbol{\frac{1}{2}}
$$

**問3**　$\dfrac{\sin x}{x} \to 1$ の形を作る。

$$
\frac{\sin 3x}{\sin 5x} = \frac{\sin 3x}{3x} \cdot \frac{5x}{\sin 5x} \cdot \frac{3x}{5x} \longrightarrow 1 \cdot 1 \cdot \frac{3}{5} = \boldsymbol{\frac{3}{5}}
$$

**問4**　$\dfrac{x}{2} = t$ とおくと $x = 2t$ で、$x \to \infty$ のとき $t \to \infty$。

$$
\left(1+\frac{2}{x}\right)^x = \left(1+\frac{1}{t}\right)^{2t} = \left\{\left(1+\frac{1}{t}\right)^{t}\right\}^2 \longrightarrow \boldsymbol{e^2}
$$

**問5**　$x \neq 1$ のとき

$$
f(x) = \frac{(x-1)(x+1)}{x-1} = x+1 \quad \therefore \lim_{x\to 1} f(x) = 2
$$

連続となる条件は $\displaystyle\lim_{x\to 1}f(x) = f(1)$ なので $\boldsymbol{a = 2}$。

**問6**　$x \to 0$ で分母 $x^2 \to 0$ なので、有限な極限値をもつためには分子 $\to 0$ が必要。

$$
\lim_{x\to 0}(ax + b - \cos x) = b - 1 = 0 \quad \therefore\ b = 1
$$

このとき

$$
\frac{ax + 1 - \cos x}{x^2} = \frac{a}{x} + \frac{1-\cos x}{x^2}
$$

第2項は $\dfrac{1}{2}$ に収束するので、全体が有限な値をもつためには $\dfrac{a}{x}$ が収束する必要があり、$\boldsymbol{a = 0}$。このとき極限値は

$$
\lim_{x\to 0}\frac{1-\cos x}{x^2} = \boldsymbol{\frac{1}{2}}
$$

### つまずきやすいポイント

- $\displaystyle\lim_{x\to a} f(x)$ は「$x$ が $a$ に近づくときの様子」であり、$f(a)$ の値そのものではない。連続性の定義（両者の一致）と区別する。
- $\dfrac{\sin x}{x} \to 1$ は **$x$ がラジアンのときだけ**成り立つ。度数法では成り立たない（$\lim_{x\to 0}\frac{\sin x°}{x} = \frac{\pi}{180}$ となる）。
- 「分母 $\to 0$ で極限値が存在 $\Rightarrow$ 分子 $\to 0$」の論法を使ったら、**最後に十分性（実際にその値で極限が存在すること）を確認**する答案が望ましい。
- 絶対値やルートを含む極限では、$x \to -\infty$ のとき $\sqrt{x^2} = |x| = -x$ となることに注意。符号ミスの典型的な発生源。
- 中間値の定理を使うときは「閉区間で連続」であることを必ず明記する。連続性が崩れると定理は使えない。

---

## 第3章 微分法

### この単元で学ぶこと

- 微分係数・導関数の定義の再確認と、微分可能性
- 積・商・合成関数の微分法
- 三角関数・指数関数・対数関数の導関数
- 対数微分法、陰関数の微分、媒介変数表示された関数の微分
- 高次導関数

### 解説

#### 導関数の定義と微分可能性

関数 $f(x)$ の $x = a$ における**微分係数**は

$$
f'(a) = \lim_{h \to 0} \frac{f(a+h) - f(a)}{h}
$$

で定義され、この極限が存在するとき $f(x)$ は $x = a$ で**微分可能**といいます。重要な事実として：

> **微分可能ならば連続である。**（逆は成り立たない。例：$f(x) = |x|$ は $x=0$ で連続だが微分可能でない）

**なぜ成り立つか**：$f(a+h) - f(a) = \dfrac{f(a+h)-f(a)}{h} \cdot h \to f'(a) \cdot 0 = 0$ となるからです。

#### 微分法の基本公式

$f, g$ が微分可能なとき：

| 公式名 | 内容 |
|---|---|
| 和・差 | $(f \pm g)' = f' \pm g'$ |
| 定数倍 | $(kf)' = kf'$ |
| **積の微分** | $(fg)' = f'g + fg'$ |
| **商の微分** | $\left(\dfrac{f}{g}\right)' = \dfrac{f'g - fg'}{g^2}$ |
| **合成関数** | $y = f(u),\ u = g(x)$ のとき $\dfrac{dy}{dx} = \dfrac{dy}{du}\cdot\dfrac{du}{dx}$ |
| 逆関数 | $\dfrac{dy}{dx} = \dfrac{1}{\dfrac{dx}{dy}}$ |

**積の微分の証明**：定義に従って

$$
\frac{f(x+h)g(x+h) - f(x)g(x)}{h} = \frac{f(x+h)-f(x)}{h}\,g(x+h) + f(x)\,\frac{g(x+h)-g(x)}{h}
$$

（分子に $-f(x)g(x+h) + f(x)g(x+h)$ を挟んで変形）。$h \to 0$ とすると、$g$ は連続なので $g(x+h) \to g(x)$ であり、右辺は $f'g + fg'$ に収束します。

#### いろいろな関数の導関数（必須公式一覧）

| $f(x)$ | $f'(x)$ | 備考 |
|---|---|---|
| $x^{\alpha}$（$\alpha$ は実数） | $\alpha x^{\alpha - 1}$ | 有理数・無理数の指数でも成立 |
| $\sin x$ | $\cos x$ | |
| $\cos x$ | $-\sin x$ | |
| $\tan x$ | $\dfrac{1}{\cos^2 x}$ | 商の微分から導出 |
| $e^x$ | $e^x$ | 微分しても形が変わらない |
| $a^x$ | $a^x \log a$ | $a^x = e^{x\log a}$ から |
| $\log x$ | $\dfrac{1}{x}$ | $x > 0$ |
| $\log \lvert x \rvert$ | $\dfrac{1}{x}$ | $x \neq 0$ で成立 |
| $\log_a x$ | $\dfrac{1}{x \log a}$ | |

**$(\sin x)' = \cos x$ の導出**：和積の公式（または加法定理）を使い、

$$
\frac{\sin(x+h) - \sin x}{h} = \frac{2\cos\left(x + \frac{h}{2}\right)\sin\frac{h}{2}}{h} = \cos\left(x + \frac{h}{2}\right) \cdot \frac{\sin\frac{h}{2}}{\frac{h}{2}}
$$

$h \to 0$ のとき、第2因子は $\displaystyle\lim_{t\to 0}\frac{\sin t}{t} = 1$ より $1$ に、第1因子は $\cos x$ に収束するので $(\sin x)' = \cos x$。**三角関数の微分の根拠は $\frac{\sin x}{x} \to 1$ にある**ことを押さえてください。

**$(\log x)' = \dfrac{1}{x}$ の導出**：

$$
\frac{\log(x+h) - \log x}{h} = \frac{1}{h}\log\left(1 + \frac{h}{x}\right) = \frac{1}{x} \cdot \frac{x}{h}\log\left(1+\frac{h}{x}\right) = \frac{1}{x}\log\left(1+\frac{h}{x}\right)^{\frac{x}{h}}
$$

$h \to 0$ のとき $\left(1+\frac{h}{x}\right)^{\frac{x}{h}} \to e$ なので、極限は $\dfrac{1}{x}\log e = \dfrac{1}{x}$。**$e$ の定義はここで効いてきます**。さらに $(e^x)' = e^x$ は $y = e^x \iff x = \log y$ と逆関数の微分法から得られます。

#### 対数微分法

累乗・積・商が複雑に絡む関数や、$y = x^x$ のように「底も指数も変数」の関数は、**両辺の（絶対値の）自然対数をとってから微分**します。

$$
y = x^x \ (x>0) \implies \log y = x \log x \implies \frac{y'}{y} = \log x + 1 \implies y' = x^x(\log x + 1)
$$

#### 陰関数の微分・媒介変数表示の微分

- **陰関数**：$x^2 + y^2 = 4$ のような式では、$y$ を $x$ の関数とみて両辺を $x$ で微分します。$\dfrac{d}{dx}y^2 = 2y\dfrac{dy}{dx}$（合成関数の微分）に注意。
- **媒介変数表示**：$x = f(t),\ y = g(t)$ のとき

$$
\frac{dy}{dx} = \frac{\dfrac{dy}{dt}}{\dfrac{dx}{dt}} = \frac{g'(t)}{f'(t)}
$$

#### 高次導関数

$f'(x)$ をさらに微分した $f''(x)$ を第2次導関数、以下 $f'''(x)$, $f^{(n)}(x)$ と続きます。第2次導関数はグラフの凹凸（第4章）や加速度（物理）に対応します。

### 例題

**例題1**　次の関数を微分せよ。

（1）$y = x^2 e^x$　（2）$y = \dfrac{x}{x^2+1}$　（3）$y = \sin^3 2x$

**解答**

（1）積の微分法により、

$$
y' = (x^2)' e^x + x^2 (e^x)' = 2x e^x + x^2 e^x = (x^2 + 2x)e^x
$$

（2）商の微分法により、

$$
y' = \frac{(x)'(x^2+1) - x(x^2+1)'}{(x^2+1)^2} = \frac{(x^2+1) - x \cdot 2x}{(x^2+1)^2} = \frac{1 - x^2}{(x^2+1)^2}
$$

（3）$y = u^3$, $u = \sin v$, $v = 2x$ の三重合成。外側から順に微分して掛ける。

$$
y' = 3\sin^2 2x \cdot (\sin 2x)' = 3\sin^2 2x \cdot \cos 2x \cdot (2x)' = 6\sin^2 2x \cos 2x
$$

**例題2**　曲線 $x = t - \sin t,\ y = 1 - \cos t$（サイクロイド）について、$\dfrac{dy}{dx}$ を $t$ で表せ。

**解答**

$$
\frac{dx}{dt} = 1 - \cos t, \qquad \frac{dy}{dt} = \sin t
$$

よって $1 - \cos t \neq 0$ のとき、

$$
\frac{dy}{dx} = \frac{\sin t}{1 - \cos t}
$$

（半角の公式を使えば $\dfrac{2\sin\frac{t}{2}\cos\frac{t}{2}}{2\sin^2\frac{t}{2}} = \dfrac{\cos\frac{t}{2}}{\sin\frac{t}{2}}$ とも書ける。）

**例題3**　$y = \sqrt[3]{\dfrac{x(x+1)}{x+2}}$（$x>0$）を微分せよ。

**解答**　対数微分法を使う。両辺の自然対数をとると、

$$
\log y = \frac{1}{3}\left\{\log x + \log(x+1) - \log(x+2)\right\}
$$

両辺を $x$ で微分して、

$$
\frac{y'}{y} = \frac{1}{3}\left(\frac{1}{x} + \frac{1}{x+1} - \frac{1}{x+2}\right)
$$

よって

$$
y' = \frac{1}{3}\sqrt[3]{\frac{x(x+1)}{x+2}}\left(\frac{1}{x} + \frac{1}{x+1} - \frac{1}{x+2}\right)
$$

### 練習問題

**問1**　$y = (x^2+1)^3$ を微分せよ。

**問2**　$y = \dfrac{\sin x}{x}$（$x \ne 0$）を微分せよ。

**問3**　$y = \log(x^2+1)$ を微分せよ。

**問4**　$y = x^x$（$x > 0$）を微分せよ。

**問5**　$x^2 + y^2 = 4$ について $\dfrac{dy}{dx}$ を $x,\ y$ で表せ（$y \neq 0$）。

**問6**　定義に従って、$f(x) = \sqrt{x}$（$x>0$）の導関数を求めよ。

### 解答と解説

**問1**　合成関数の微分。$u = x^2+1$ とおくと $y = u^3$。

$$
y' = 3(x^2+1)^2 \cdot (x^2+1)' = 3(x^2+1)^2 \cdot 2x = \boldsymbol{6x(x^2+1)^2}
$$

**問2**　商の微分法。

$$
y' = \frac{(\sin x)' \cdot x - \sin x \cdot (x)'}{x^2} = \boldsymbol{\frac{x\cos x - \sin x}{x^2}}
$$

**問3**　合成関数の微分。

$$
y' = \frac{(x^2+1)'}{x^2+1} = \boldsymbol{\frac{2x}{x^2+1}}
$$

**問4**　両辺の対数をとると $\log y = x \log x$。両辺を微分して、

$$
\frac{y'}{y} = 1 \cdot \log x + x \cdot \frac{1}{x} = \log x + 1
$$

$$
\therefore\ y' = \boldsymbol{x^x(\log x + 1)}
$$

**問5**　両辺を $x$ で微分する。$y$ は $x$ の関数であることに注意して、

$$
2x + 2y\frac{dy}{dx} = 0 \quad \therefore\ \frac{dy}{dx} = \boldsymbol{-\frac{x}{y}}
$$

（円の中心 $(0,0)$ と点 $(x,y)$ を結ぶ半径の傾き $\frac{y}{x}$ と接線の傾きの積が $-1$、という図形的意味とも一致する。）

**問6**　定義に従い、有理化を用いて計算する。

$$
f'(x) = \lim_{h\to 0}\frac{\sqrt{x+h} - \sqrt{x}}{h} = \lim_{h\to 0}\frac{(x+h) - x}{h(\sqrt{x+h}+\sqrt{x})} = \lim_{h\to 0}\frac{1}{\sqrt{x+h}+\sqrt{x}} = \boldsymbol{\frac{1}{2\sqrt{x}}}
$$

（公式 $(x^{1/2})' = \frac{1}{2}x^{-1/2}$ と一致する。）

### つまずきやすいポイント

- **合成関数の微分での「掛け忘れ」**が最頻出ミス。$(\sin 2x)' = \cos 2x$ は誤りで、内側の微分 $2$ を掛けて $2\cos 2x$。「外の微分 × 中の微分」を機械的に徹底する。
- 商の微分の分子は $f'g - fg'$。**順序（引く方向）を逆にしない**こと。「分子の微分×分母 − 分子×分母の微分」と唱えて覚える。
- $(a^x)' = a^x \log a$ の $\log a$ を忘れる。$e^x$ だけが特別（$\log e = 1$）である。
- $\log x$ の微分は $\frac{1}{x}$ だが、積分で使う $\int \frac{1}{x}dx = \log|x| + C$ の絶対値と対応させて、定義域を常に意識する。
- $y = x^x$ を「$x^n$ の公式で $x \cdot x^{x-1}$」とするのは誤り。指数に変数がある場合は対数微分法（または $x^x = e^{x\log x}$ の変形）。

---

## 第4章 微分法の応用

### この単元で学ぶこと

- 接線・法線の方程式
- 平均値の定理とその使い方
- 関数の増減・極値、グラフの凹凸・変曲点、漸近線とグラフの概形
- 最大値・最小値、方程式・不等式への応用
- 速度・加速度、近似式

### 解説

#### 接線と法線

曲線 $y = f(x)$ 上の点 $(a,\ f(a))$ における

- **接線**：$y - f(a) = f'(a)(x - a)$
- **法線**：$y - f(a) = -\dfrac{1}{f'(a)}(x - a)$（$f'(a) \neq 0$）

曲線外の点から引いた接線は、「接点を $(t,\ f(t))$ とおく」のが定石です。

#### 平均値の定理

関数 $f(x)$ が閉区間 $[a,\,b]$ で連続、開区間 $(a,\,b)$ で微分可能ならば、

$$
\frac{f(b) - f(a)}{b - a} = f'(c), \qquad a < c < b
$$

を満たす $c$ が存在します。**図形的意味**：2点 $(a, f(a))$, $(b, f(b))$ を結ぶ直線（平均変化率）と同じ傾きをもつ接線が、区間内のどこかに必ず引ける、ということです。不等式の証明や極限の評価に使われる、理論上も入試上も重要な定理です。

#### 増減と極値

- 区間で $f'(x) > 0$ ならば $f(x)$ はその区間で**単調に増加**、$f'(x) < 0$ ならば**単調に減少**します（平均値の定理から証明できます：任意の2点 $x_1 < x_2$ に対し $f(x_2) - f(x_1) = f'(c)(x_2 - x_1) > 0$）。
- $x = a$ の前後で $f'(x)$ の符号が正から負に変われば $f(a)$ は**極大値**、負から正に変われば**極小値**。
- **注意**：$f'(a) = 0$ は極値をとるための必要条件にすぎない（例：$f(x) = x^3$ の $x=0$）。符号変化の確認が必須。

#### 凹凸と変曲点

- $f''(x) > 0$ の区間でグラフは**下に凸**、$f''(x) < 0$ の区間で**上に凸**。
- 凹凸が入れ替わる点を**変曲点**という。$f''(a) = 0$ かつ前後で $f''$ の符号が変わることが条件。

**なぜ成り立つか**：$f'' > 0$ ならば $f'$ が増加、つまり接線の傾きがだんだん大きくなるので、グラフは接線の上側に反り上がる（下に凸）形になります。

#### グラフの描き方（手順）

1. 定義域を確認する
2. $f'(x)$ を計算し、増減表を作る（極値）
3. 必要なら $f''(x)$ で凹凸・変曲点を調べる
4. 漸近線（$x \to \pm\infty$ の極限、分母 $\to 0$ となる点）を調べる
5. 座標軸との交点・対称性を確認して概形を描く

#### 方程式・不等式への応用

- **不等式 $f(x) > g(x)$ の証明**：$F(x) = f(x) - g(x)$ とおき、増減を調べて（最小値）$> 0$ を示す。
- **方程式 $f(x) = a$ の実数解の個数**：$y = f(x)$ のグラフと直線 $y = a$ の共有点の個数として視覚化する（**定数分離**）。

#### 速度・加速度・近似式

数直線上の点の位置が $x = f(t)$ のとき、速度 $v = \dfrac{dx}{dt}$、加速度 $\alpha = \dfrac{dv}{dt} = \dfrac{d^2x}{dt^2}$。平面上の点 $(x(t),\ y(t))$ では速度ベクトル $\vec{v} = \left(\dfrac{dx}{dt}, \dfrac{dy}{dt}\right)$、速さ $|\vec{v}| = \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}$。

$|h|$ が十分小さいとき、微分係数の定義から次の**1次近似式**が得られます。

$$
f(a+h) \approx f(a) + f'(a)h, \qquad x \approx 0 \text{ のとき } f(x) \approx f(0) + f'(0)x
$$

例：$\sin x \approx x$, $e^x \approx 1 + x$, $(1+x)^{\alpha} \approx 1 + \alpha x$。

### 例題

**例題1**　関数 $f(x) = \dfrac{x}{x^2+1}$ の極値を求め、グラフの概形を述べよ。

**解答**　定義域は実数全体。

$$
f'(x) = \frac{(x^2+1) - x \cdot 2x}{(x^2+1)^2} = \frac{1-x^2}{(x^2+1)^2} = \frac{(1-x)(1+x)}{(x^2+1)^2}
$$

分母は常に正なので、$f'(x)$ の符号は $(1-x)(1+x)$ の符号と一致する。増減表は次の通り。

| $x$ | $\cdots$ | $-1$ | $\cdots$ | $1$ | $\cdots$ |
|---|---|---|---|---|---|
| $f'(x)$ | $-$ | $0$ | $+$ | $0$ | $-$ |
| $f(x)$ | ↘ | 極小 $-\dfrac{1}{2}$ | ↗ | 極大 $\dfrac{1}{2}$ | ↘ |

よって **$x = 1$ で極大値 $\dfrac{1}{2}$、$x = -1$ で極小値 $-\dfrac{1}{2}$**。また $\displaystyle\lim_{x\to\pm\infty} f(x) = 0$ なので $x$ 軸が漸近線であり、$f(-x) = -f(x)$ より原点対称の曲線である。

**例題2**　$x > 0$ のとき、不等式 $e^x > 1 + x$ が成り立つことを証明せよ。

**解答**　$F(x) = e^x - (1 + x)$ とおく。

$$
F'(x) = e^x - 1
$$

$x > 0$ のとき $e^x > e^0 = 1$ なので $F'(x) > 0$。よって $F(x)$ は $x \ge 0$ で単調に増加する。さらに

$$
F(0) = e^0 - 1 = 0
$$

したがって $x > 0$ のとき $F(x) > F(0) = 0$、すなわち $e^x > 1 + x$ が成り立つ。（証明終）

**例題3**　$a$ を正の定数とする。方程式 $e^x = ax$ の異なる実数解の個数を求めよ。

**解答**　$x = 0$ は $e^0 = 1 \neq 0$ より解でない。$x \ne 0$ で両辺を $x$ で割り、定数を分離する。$x<0$ では左辺 $e^x > 0$、右辺 $ax<0$ なので解はなく、解はすべて $x>0$ にある。$x>0$ で

$$
a = \frac{e^x}{x}
$$

$g(x) = \dfrac{e^x}{x}$（$x > 0$）とおくと、

$$
g'(x) = \frac{e^x \cdot x - e^x \cdot 1}{x^2} = \frac{e^x(x-1)}{x^2}
$$

増減表より $g(x)$ は $0 < x < 1$ で減少、$x > 1$ で増加し、$x = 1$ で最小値 $g(1) = e$ をとる。また $x \to +0$ で $g(x) \to \infty$、$x \to \infty$ で $g(x) \to \infty$。

よって直線 $y = a$ とグラフ $y = g(x)$ の共有点の個数を数えて、

- $0 < a < e$ のとき **0個**
- $a = e$ のとき **1個**
- $a > e$ のとき **2個**

### 練習問題

**問1**　曲線 $y = e^x$ 上の点 $(1,\ e)$ における接線の方程式を求めよ。

**問2**　関数 $f(x) = x e^{-x}$（$x \ge 0$）の最大値を求めよ。

**問3**　$x > 0$ のとき、不等式 $x > \sin x$ が成り立つことを証明せよ。

**問4**　$0 < a < b$ のとき、$\dfrac{1}{b} < \dfrac{\log b - \log a}{b - a} < \dfrac{1}{a}$ が成り立つことを、平均値の定理を用いて証明せよ。

**問5**　数直線上を運動する点Pの座標が $x = t^3 - 3t$（$t$ は時刻）で表されるとき、$t = 2$ における速度と加速度を求めよ。

**問6**　関数 $y = \dfrac{x^2 - x + 1}{x - 1}$（$x \ne 1$）の極値を求めよ。

### 解答と解説

**問1**　$y' = e^x$ より、$x = 1$ における接線の傾きは $e$。接線は

$$
y - e = e(x - 1) \quad \therefore\ \boldsymbol{y = ex}
$$

（原点を通る直線になる。$y = e^x$ に原点から引いた接線としても頻出。）

**問2**　$f'(x) = e^{-x} + x(-e^{-x}) = (1 - x)e^{-x}$。$e^{-x} > 0$ なので符号は $1 - x$ で決まり、$0 \le x < 1$ で増加、$x > 1$ で減少。よって $x = 1$ で最大となり、最大値は

$$
f(1) = \boldsymbol{\frac{1}{e}}
$$

**問3**　$F(x) = x - \sin x$ とおくと、$F'(x) = 1 - \cos x \ge 0$ であり、等号は $x = 2n\pi$ の離散的な点でのみ成立する。よって $F(x)$ は $x \ge 0$ で単調に増加し、$F(0) = 0$ だから、$x > 0$ のとき

$$
F(x) > F(0) = 0 \quad \therefore\ x > \sin x \quad \text{（証明終）}
$$

**問4**　$f(x) = \log x$ は $x > 0$ で微分可能で、$f'(x) = \dfrac{1}{x}$。区間 $[a,\ b]$ に平均値の定理を適用すると、

$$
\frac{\log b - \log a}{b - a} = \frac{1}{c}, \qquad a < c < b
$$

を満たす $c$ が存在する。$0 < a < c < b$ より $\dfrac{1}{b} < \dfrac{1}{c} < \dfrac{1}{a}$ なので、

$$
\frac{1}{b} < \frac{\log b - \log a}{b-a} < \frac{1}{a} \quad \text{（証明終）}
$$

**問5**　速度 $v = \dfrac{dx}{dt} = 3t^2 - 3$、加速度 $\alpha = \dfrac{dv}{dt} = 6t$。$t = 2$ を代入して、

$$
v = 3 \cdot 4 - 3 = \boldsymbol{9}, \qquad \alpha = \boldsymbol{12}
$$

**問6**　商の微分法により、

$$
y' = \frac{(2x-1)(x-1) - (x^2 - x + 1)}{(x-1)^2} = \frac{2x^2 - 3x + 1 - x^2 + x - 1}{(x-1)^2} = \frac{x^2 - 2x}{(x-1)^2} = \frac{x(x-2)}{(x-1)^2}
$$

増減表（$x = 1$ は定義域外）：

| $x$ | $\cdots$ | $0$ | $\cdots$ | $1$ | $\cdots$ | $2$ | $\cdots$ |
|---|---|---|---|---|---|---|---|
| $y'$ | $+$ | $0$ | $-$ | × | $-$ | $0$ | $+$ |
| $y$ | ↗ | 極大 | ↘ | × | ↘ | 極小 | ↗ |

$$
x = 0 \text{ のとき } y = \frac{1}{-1} = -1, \qquad x = 2 \text{ のとき } y = \frac{4-2+1}{1} = 3
$$

よって **$x = 0$ で極大値 $-1$、$x = 2$ で極小値 $3$**。（極大値 < 極小値 となるのは、間に漸近線 $x=1$ があるため。分数関数ではよく起こる。）

### つまずきやすいポイント

- **$f'(a) = 0$ だけでは極値と断定できない**。増減表で符号変化を必ず確認する。逆に、$f'(a)$ が存在しない点（尖点）で極値をとることもある。
- 「単調増加だから最小値は左端」など、**定義域の端の扱い**（閉区間か開区間か、端で定義されるか）を確認する。開区間の端の値は「極限」であって最大・最小にならないことがある。
- 定数分離 $a = g(x)$ をするとき、**$x$ で割る前に $x = 0$ が解かどうかを別に確認**する（例題3の冒頭処理）。
- 分数関数のグラフでは**漸近線**（縦・横・斜め）を忘れると概形も解の個数も誤る。
- 不等式の証明では「$F'(x)>0$ かつ $F(0)=0$」のように、**単調性と端点の値の両方**を述べて初めて結論が出る。単調性だけでは不十分。

---

## 第5章 積分法

### この単元で学ぶこと

- いろいろな関数の不定積分（基本公式の拡張）
- 置換積分法・部分積分法
- 定積分の計算（置換積分・部分積分の定積分版）
- 定積分で表された関数の扱い
- 区分求積法と、定積分と不等式（和の評価）

### 解説

#### 不定積分の基本公式

微分の公式を逆向きに読むことで、次の公式が得られます（$C$ は積分定数）。

| 公式 | 条件・備考 |
|---|---|
| $\displaystyle\int x^{\alpha}\,dx = \frac{x^{\alpha+1}}{\alpha+1} + C$ | $\alpha \neq -1$ |
| $\displaystyle\int \frac{1}{x}\,dx = \log \lvert x \rvert + C$ | $\alpha = -1$ の場合はこちら |
| $\displaystyle\int \sin x\,dx = -\cos x + C$ | |
| $\displaystyle\int \cos x\,dx = \sin x + C$ | |
| $\displaystyle\int \frac{1}{\cos^2 x}\,dx = \tan x + C$ | |
| $\displaystyle\int e^x\,dx = e^x + C$ | |
| $\displaystyle\int a^x\,dx = \frac{a^x}{\log a} + C$ | $a>0,\ a\neq 1$ |

また、頻出の形として

$$
\int \frac{f'(x)}{f(x)}\,dx = \log|f(x)| + C, \qquad \int \{f(x)\}^{\alpha} f'(x)\,dx = \frac{\{f(x)\}^{\alpha+1}}{\alpha+1} + C \ (\alpha \ne -1)
$$

を「見た瞬間に反応できる」ようにしておくと計算が速くなります（例：$\int \tan x\,dx = \int \frac{\sin x}{\cos x}dx = -\log|\cos x| + C$）。

#### 置換積分法

$x = g(t)$ とおくと、

$$
\int f(x)\,dx = \int f(g(t))\,g'(t)\,dt
$$

**なぜ成り立つか**：合成関数の微分法 $\dfrac{d}{dt}F(g(t)) = F'(g(t))g'(t) = f(g(t))g'(t)$ を逆に読んだものです。形式的には $\dfrac{dx}{dt} = g'(t)$ から $dx = g'(t)\,dt$ と「置き換える」と覚えられます。

**定積分の置換積分**では、**積分区間も新しい変数のものに変換**します。$x = g(t)$、$a = g(\alpha)$, $b = g(\beta)$ のとき

$$
\int_a^b f(x)\,dx = \int_{\alpha}^{\beta} f(g(t))\,g'(t)\,dt
$$

**代表的な置換**：

- $\sqrt{a^2 - x^2}$ を含む → $x = a\sin\theta$
- $\dfrac{1}{x^2 + a^2}$ を含む → $x = a\tan\theta$
- $\sqrt{\text{1次式}}$ を含む → 根号全体を $t$ とおく

#### 部分積分法

積の微分法 $(fg)' = f'g + fg'$ を移項して積分すると、

$$
\int f(x)g'(x)\,dx = f(x)g(x) - \int f'(x)g(x)\,dx
$$

定積分版：

$$
\int_a^b f(x)g'(x)\,dx = \Big[f(x)g(x)\Big]_a^b - \int_a^b f'(x)g(x)\,dx
$$

「微分すると簡単になる方（多項式、$\log x$ など）を $f$、積分しやすい方（$e^x$, $\sin x$ など）を $g'$」に選ぶのが原則です。$\int \log x\,dx$ は $\log x \cdot (x)'$ とみなして部分積分する有名な例です。

#### 定積分で表された関数

- $\displaystyle\int_a^b f(t)\,dt$（両端が定数）は**定数**。$a$ とおいて方程式に持ち込む。
- $\displaystyle\frac{d}{dx}\int_a^x f(t)\,dt = f(x)$（微分積分学の基本定理）。上端に変数がある場合は微分して情報を取り出す。このとき $x = a$ を代入すると積分が $0$ になることも併用する。

**微分積分学の基本定理のなぜ**：$S(x) = \int_a^x f(t)dt$ とおくと、$S(x+h) - S(x)$ は幅 $h$ の細い部分の面積で、$f$ が連続ならこれは約 $f(x) \cdot h$。よって $\dfrac{S(x+h)-S(x)}{h} \to f(x)$ となります。**「面積の変化率が高さ」**という直観が微分と積分をつなぎます。

#### 区分求積法

区間 $[0,\,1]$ を $n$ 等分してできる長方形の面積の和の極限として、

$$
\lim_{n\to\infty} \frac{1}{n}\sum_{k=1}^{n} f\!\left(\frac{k}{n}\right) = \int_0^1 f(x)\,dx
$$

が成り立ちます（$k$ の範囲が $0$ から $n-1$ でも同じ極限）。「$\dfrac{1}{n}$ をくくり出し、$\dfrac{k}{n}$ を $x$ に読み替える」のが実戦での手順です。

#### 定積分と不等式

区間 $[a,\,b]$ で $f(x) \le g(x)$ ならば $\displaystyle\int_a^b f(x)\,dx \le \int_a^b g(x)\,dx$（等号は $f \equiv g$ のときのみ）。単調な関数の和 $\sum f(k)$ を積分で挟んで評価する手法は入試頻出です。

### 例題

**例題1**　次の不定積分を求めよ。

（1）$\displaystyle\int x\sqrt{x^2+1}\,dx$　（2）$\displaystyle\int x e^x\,dx$　（3）$\displaystyle\int \log x\,dx$

**解答**

（1）$t = x^2 + 1$ とおくと $\dfrac{dt}{dx} = 2x$ すなわち $x\,dx = \dfrac{1}{2}dt$。

$$
\int x\sqrt{x^2+1}\,dx = \int \sqrt{t}\cdot\frac{1}{2}\,dt = \frac{1}{2}\cdot\frac{2}{3}t^{\frac{3}{2}} + C = \frac{1}{3}(x^2+1)\sqrt{x^2+1} + C
$$

（2）部分積分。微分して簡単になる $x$ を $f$、$e^x$ を $g'$ に選ぶ。

$$
\int x e^x\,dx = x e^x - \int 1 \cdot e^x\,dx = x e^x - e^x + C = (x-1)e^x + C
$$

（3）$\log x = \log x \cdot (x)'$ とみて部分積分。

$$
\int \log x\,dx = x\log x - \int \frac{1}{x}\cdot x\,dx = x\log x - \int 1\,dx = x\log x - x + C
$$

**例題2**　定積分 $\displaystyle\int_0^1 \sqrt{1 - x^2}\,dx$ を求めよ。

**解答**　$x = \sin\theta$ とおくと $dx = \cos\theta\,d\theta$。積分区間は $x: 0 \to 1$ が $\theta: 0 \to \dfrac{\pi}{2}$ に対応する。$0 \le \theta \le \dfrac{\pi}{2}$ では $\cos\theta \ge 0$ なので $\sqrt{1-\sin^2\theta} = \cos\theta$。

$$
\int_0^1 \sqrt{1-x^2}\,dx = \int_0^{\frac{\pi}{2}} \cos\theta \cdot \cos\theta\,d\theta = \int_0^{\frac{\pi}{2}} \cos^2\theta\,d\theta
$$

半角の公式 $\cos^2\theta = \dfrac{1+\cos 2\theta}{2}$ を用いて、

$$
= \int_0^{\frac{\pi}{2}} \frac{1+\cos 2\theta}{2}\,d\theta = \left[\frac{\theta}{2} + \frac{\sin 2\theta}{4}\right]_0^{\frac{\pi}{2}} = \frac{\pi}{4} + 0 - 0 = \frac{\pi}{4}
$$

（この値は半径1の四分円の面積に等しい。図形的意味と一致することを確認しよう。）

**例題3**　$\displaystyle\lim_{n\to\infty} \sum_{k=1}^{n} \frac{n}{n^2 + k^2}$ を求めよ。

**解答**　$\dfrac{1}{n}$ をくくり出して区分求積法の形にする。

$$
\sum_{k=1}^{n} \frac{n}{n^2+k^2} = \frac{1}{n}\sum_{k=1}^{n} \frac{n^2}{n^2+k^2} = \frac{1}{n}\sum_{k=1}^{n} \frac{1}{1+\left(\dfrac{k}{n}\right)^2}
$$

よって $f(x) = \dfrac{1}{1+x^2}$ として、

$$
\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^n f\!\left(\frac{k}{n}\right) = \int_0^1 \frac{1}{1+x^2}\,dx
$$

$x = \tan\theta$ とおくと $dx = \dfrac{1}{\cos^2\theta}d\theta$、区間は $\theta: 0 \to \dfrac{\pi}{4}$。

$$
\int_0^1 \frac{dx}{1+x^2} = \int_0^{\frac{\pi}{4}} \frac{1}{1+\tan^2\theta}\cdot\frac{d\theta}{\cos^2\theta} = \int_0^{\frac{\pi}{4}} d\theta = \frac{\pi}{4}
$$

（$1+\tan^2\theta = \dfrac{1}{\cos^2\theta}$ を用いた。）よって求める極限は $\dfrac{\pi}{4}$。

### 練習問題

**問1**　$\displaystyle\int \tan x\,dx$ を求めよ。

**問2**　$\displaystyle\int_0^1 \frac{x}{x^2+1}\,dx$ を求めよ。

**問3**　$\displaystyle\int_0^{\frac{\pi}{2}} \sin^2 x\,dx$ を求めよ。

**問4**　$\displaystyle\int_1^e x\log x\,dx$ を求めよ。

**問5**　等式 $f(x) = x^2 + \displaystyle\int_0^1 x f(t)\,dt$ を満たす関数 $f(x)$ を求めよ。

**問6**　$\displaystyle\lim_{n\to\infty} \frac{1}{n}\left\{\left(\frac{1}{n}\right)^2 + \left(\frac{2}{n}\right)^2 + \cdots + \left(\frac{n}{n}\right)^2\right\}$ を求めよ。

### 解答と解説

**問1**　$\tan x = \dfrac{\sin x}{\cos x}$ で、分子は分母の微分の $(-1)$ 倍。

$$
\int \tan x\,dx = \int \frac{\sin x}{\cos x}\,dx = -\int \frac{(\cos x)'}{\cos x}\,dx = \boldsymbol{-\log|\cos x| + C}
$$

**問2**　分子が分母の微分の $\dfrac{1}{2}$ 倍であることに注目する。

$$
\int_0^1 \frac{x}{x^2+1}\,dx = \frac{1}{2}\int_0^1 \frac{(x^2+1)'}{x^2+1}\,dx = \frac{1}{2}\Big[\log(x^2+1)\Big]_0^1 = \frac{1}{2}(\log 2 - \log 1) = \boldsymbol{\frac{1}{2}\log 2}
$$

**問3**　半角の公式で次数を下げる。

$$
\int_0^{\frac{\pi}{2}} \sin^2 x\,dx = \int_0^{\frac{\pi}{2}} \frac{1 - \cos 2x}{2}\,dx = \left[\frac{x}{2} - \frac{\sin 2x}{4}\right]_0^{\frac{\pi}{2}} = \frac{\pi}{4} - 0 = \boldsymbol{\frac{\pi}{4}}
$$

**問4**　部分積分。$\log x$ を微分する側に選ぶ。

$$
\int_1^e x\log x\,dx = \left[\frac{x^2}{2}\log x\right]_1^e - \int_1^e \frac{x^2}{2}\cdot\frac{1}{x}\,dx = \frac{e^2}{2} - \frac{1}{2}\int_1^e x\,dx
$$

$$
= \frac{e^2}{2} - \frac{1}{2}\left[\frac{x^2}{2}\right]_1^e = \frac{e^2}{2} - \frac{e^2 - 1}{4} = \boldsymbol{\frac{e^2 + 1}{4}}
$$

**問5**　$\displaystyle\int_0^1 f(t)\,dt$ は定数なので $a = \displaystyle\int_0^1 f(t)\,dt$ とおくと、$f(x) = x^2 + ax$。これを $a$ の定義式に代入して、

$$
a = \int_0^1 (t^2 + at)\,dt = \left[\frac{t^3}{3} + \frac{a t^2}{2}\right]_0^1 = \frac{1}{3} + \frac{a}{2}
$$

$$
a - \frac{a}{2} = \frac{1}{3} \quad \therefore\ a = \frac{2}{3}
$$

よって $\boldsymbol{f(x) = x^2 + \dfrac{2}{3}x}$。

**問6**　区分求積法そのものの形である。

$$
\lim_{n\to\infty}\frac{1}{n}\sum_{k=1}^n \left(\frac{k}{n}\right)^2 = \int_0^1 x^2\,dx = \left[\frac{x^3}{3}\right]_0^1 = \boldsymbol{\frac{1}{3}}
$$

### つまずきやすいポイント

- **定積分の置換積分で積分区間の変換を忘れる**のが最も多いミス。「変数を替えたら区間も替える」を徹底する。
- $x = a\sin\theta$ の置換で $\sqrt{a^2 - x^2} = a\cos\theta$ とできるのは、$\theta$ の範囲で $\cos\theta \ge 0$ のとき。**範囲の確認をせずに根号を外さない**。
- 部分積分で $f$ と $g'$ の選び方を誤ると式がかえって複雑になる。「多項式・$\log$ は微分する側、$e^x$・三角関数は積分する側」が原則（$\log$ を含むときは $\log$ を微分する側に）。
- $\int \frac{1}{x}dx = \log|x| + C$ の**絶対値**を忘れない。定積分では区間の符号に応じて外す。
- 区分求積法では $\sum$ の範囲（$k=1$ から $n$ か、$0$ から $n-1$ か）が変わっても極限は同じだが、$\frac{k}{n}$ 以外の形（例：$\frac{k}{2n}$）が現れたら積分区間が $[0, \frac{1}{2}]$ になるなど、**対応する区間を丁寧に確認**する。

---

## 第6章 積分法の応用

### この単元で学ぶこと

- 曲線で囲まれた図形の面積
- 立体の体積（断面積の積分、回転体の体積）
- 曲線の長さ（弧長）
- 直線上・平面上の運動における速度と道のり

### 解説

#### 面積

区間 $[a,\,b]$ で $f(x) \ge g(x)$ のとき、2曲線 $y = f(x)$, $y = g(x)$ と2直線 $x = a$, $x = b$ で囲まれた図形の面積は

$$
S = \int_a^b \{f(x) - g(x)\}\,dx
$$

**上下関係（どちらが上か）を必ず確認**してから立式します。曲線が $x = h(y)$ の形（$y$ の関数）で与えられるときは、$y$ で積分する方が楽な場合が多いです。

$$
S = \int_c^d \{h_1(y) - h_2(y)\}\,dy \quad (h_1 \text{ が右側})
$$

媒介変数表示の曲線では、$S = \displaystyle\int_a^b y\,dx = \int_{\alpha}^{\beta} y(t)\,x'(t)\,dt$ と置換して計算します。

#### 体積（断面積の積分）

$x$ 軸に垂直な平面による立体の断面積が $S(x)$（$a \le x \le b$）のとき、体積は

$$
V = \int_a^b S(x)\,dx
$$

**なぜ成り立つか**：立体を厚さ $dx$ の薄い板の集まりとみなすと、各板の体積は約 $S(x)\,dx$ で、その総和の極限が積分になるからです（区分求積法の考え方）。

#### 回転体の体積

曲線 $y = f(x)$ と $x$ 軸、$x = a$, $x = b$ で囲まれた部分を **$x$ 軸のまわりに1回転**してできる立体の体積は、断面が半径 $|f(x)|$ の円であることから

$$
V = \pi \int_a^b \{f(x)\}^2\,dx
$$

**$y$ 軸のまわりの回転**では、$x = g(y)$ と解いて

$$
V = \pi \int_c^d \{g(y)\}^2\,dy
$$

2曲線間の回転体は「外側の回転体 − 内側の回転体」で求めます（先に2乗の差をとること。$\{f-g\}^2$ ではない！）。

#### 曲線の長さ

| 表し方 | 長さの公式 |
|---|---|
| 媒介変数 $x = f(t),\ y = g(t)$（$\alpha \le t \le \beta$） | $L = \displaystyle\int_{\alpha}^{\beta} \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$ |
| $y = f(x)$（$a \le x \le b$） | $L = \displaystyle\int_a^b \sqrt{1 + \{f'(x)\}^2}\,dx$ |

**なぜ成り立つか**：曲線を細かい折れ線で近似すると、微小部分の長さは三平方の定理より $\sqrt{(\Delta x)^2 + (\Delta y)^2} = \sqrt{\left(\frac{\Delta x}{\Delta t}\right)^2 + \left(\frac{\Delta y}{\Delta t}\right)^2}\,\Delta t$。この総和の極限が上の積分です。

#### 速度と道のり

数直線上を速度 $v(t)$ で動く点について、時刻 $t = a$ から $t = b$ までの

- **位置の変化（変位）**：$\displaystyle\int_a^b v(t)\,dt$
- **道のり（実際に動いた距離）**：$\displaystyle\int_a^b |v(t)|\,dt$

平面運動では、道のりは $\displaystyle\int_a^b \sqrt{\left(\frac{dx}{dt}\right)^2 + \left(\frac{dy}{dt}\right)^2}\,dt$（曲線の長さと同じ式）。

### 例題

**例題1**　曲線 $y = e^x$、直線 $y = e$、$y$ 軸で囲まれた図形の面積を求めよ。

**解答**　$e^x = e$ を解くと $x = 1$。$0 \le x \le 1$ では $e \ge e^x$（$e^x$ は増加関数で $x=1$ で $e$ に達する）なので、

$$
S = \int_0^1 (e - e^x)\,dx = \Big[ex - e^x\Big]_0^1 = (e - e) - (0 - 1) = 1
$$

**例題2**　曲線 $y = \sin x$（$0 \le x \le \pi$）と $x$ 軸で囲まれた図形を、$x$ 軸のまわりに1回転してできる立体の体積を求めよ。

**解答**

$$
V = \pi\int_0^{\pi} \sin^2 x\,dx = \pi\int_0^{\pi} \frac{1 - \cos 2x}{2}\,dx = \pi\left[\frac{x}{2} - \frac{\sin 2x}{4}\right]_0^{\pi} = \pi \cdot \frac{\pi}{2} = \frac{\pi^2}{2}
$$

**例題3**　サイクロイド $x = t - \sin t,\ y = 1 - \cos t$（$0 \le t \le 2\pi$）と $x$ 軸で囲まれた図形の面積を求めよ。

**解答**　$0 \le t \le 2\pi$ で $y \ge 0$ であり、$x$ は $0$ から $2\pi$ まで増加する。面積は

$$
S = \int_0^{2\pi} y\,dx = \int_0^{2\pi} (1-\cos t)\cdot\frac{dx}{dt}\,dt = \int_0^{2\pi} (1-\cos t)^2\,dt
$$

展開して、

$$
= \int_0^{2\pi} (1 - 2\cos t + \cos^2 t)\,dt = \int_0^{2\pi} \left(1 - 2\cos t + \frac{1+\cos 2t}{2}\right) dt
$$

$\cos t$, $\cos 2t$ の1周期分の積分は $0$ なので、

$$
= \int_0^{2\pi} \frac{3}{2}\,dt = \frac{3}{2}\cdot 2\pi = 3\pi
$$

（回転する円の面積 $\pi$ のちょうど3倍になる、という美しい結果。）

### 練習問題

**問1**　放物線 $x = y^2$ と直線 $y = x - 2$ で囲まれた図形の面積を求めよ。

**問2**　曲線 $y = e^x$、$x$ 軸、$x = 0$, $x = 1$ で囲まれた部分を $x$ 軸のまわりに1回転してできる立体の体積を求めよ。

**問3**　曲線 $y = \dfrac{2}{3}x\sqrt{x}$（$0 \le x \le 3$）の長さを求めよ。

**問4**　数直線上を速度 $v(t) = 6t - 3t^2$ で動く点Pについて、$t = 0$ から $t = 3$ までの（1）位置の変化、（2）道のりを求めよ。

**問5**　曲線 $y = \log x$、$x$ 軸、$x = e$ で囲まれた図形の面積を求めよ。

**問6**　曲線 $y = \sqrt{x}$ と直線 $y = x$ で囲まれた図形を $x$ 軸のまわりに1回転してできる立体の体積を求めよ。

### 解答と解説

**問1**　交点を求める。$x = y^2$ を $y = x - 2$ に代入すると $y = y^2 - 2$、すなわち

$$
y^2 - y - 2 = 0 \quad \therefore\ (y-2)(y+1) = 0 \quad \therefore\ y = -1,\ 2
$$

$y$ で積分する（$-1 \le y \le 2$ で直線 $x = y + 2$ が放物線 $x = y^2$ より右側にある）。

$$
S = \int_{-1}^{2} \{(y+2) - y^2\}\,dy = \left[\frac{y^2}{2} + 2y - \frac{y^3}{3}\right]_{-1}^{2}
$$

$$
= \left(2 + 4 - \frac{8}{3}\right) - \left(\frac{1}{2} - 2 + \frac{1}{3}\right) = \frac{10}{3} - \left(-\frac{7}{6}\right) = \boldsymbol{\frac{9}{2}}
$$

**問2**

$$
V = \pi\int_0^1 (e^x)^2\,dx = \pi\int_0^1 e^{2x}\,dx = \pi\left[\frac{e^{2x}}{2}\right]_0^1 = \boldsymbol{\frac{\pi(e^2 - 1)}{2}}
$$

**問3**　$y = \dfrac{2}{3}x^{\frac{3}{2}}$ より $y' = x^{\frac{1}{2}} = \sqrt{x}$。

$$
L = \int_0^3 \sqrt{1 + (\sqrt{x})^2}\,dx = \int_0^3 \sqrt{1+x}\,dx = \left[\frac{2}{3}(1+x)^{\frac{3}{2}}\right]_0^3 = \frac{2}{3}(8 - 1) = \boldsymbol{\frac{14}{3}}
$$

**問4**　（1）位置の変化は

$$
\int_0^3 (6t - 3t^2)\,dt = \Big[3t^2 - t^3\Big]_0^3 = 27 - 27 = \boldsymbol{0}
$$

（2）$v(t) = 3t(2 - t)$ なので、$0 \le t \le 2$ で $v \ge 0$、$2 \le t \le 3$ で $v \le 0$。道のりは

$$
\int_0^3 |v(t)|\,dt = \int_0^2 (6t - 3t^2)\,dt + \int_2^3 (3t^2 - 6t)\,dt
$$

$$
= \Big[3t^2 - t^3\Big]_0^2 + \Big[t^3 - 3t^2\Big]_2^3 = (12 - 8) + \{(27-27) - (8-12)\} = 4 + 4 = \boldsymbol{8}
$$

（出発点に戻ってきたので変位は $0$ だが、往復した距離は $8$。両者の違いを体感できる問題。）

**問5**　$y = \log x$ は $x = 1$ で $x$ 軸と交わる。$1 \le x \le e$ で $\log x \ge 0$ なので、

$$
S = \int_1^e \log x\,dx = \Big[x\log x - x\Big]_1^e = (e - e) - (0 - 1) = \boldsymbol{1}
$$

（部分積分の結果 $\int\log x\,dx = x\log x - x + C$ を用いた。）

**問6**　交点：$\sqrt{x} = x$ より $x = x^2$、$x(x-1) = 0$ で $x = 0,\ 1$。$0 \le x \le 1$ では $\sqrt{x} \ge x$。回転体の体積は「外側 − 内側」で、

$$
V = \pi\int_0^1 (\sqrt{x})^2\,dx - \pi\int_0^1 x^2\,dx = \pi\int_0^1 (x - x^2)\,dx = \pi\left[\frac{x^2}{2} - \frac{x^3}{3}\right]_0^1 = \pi\left(\frac{1}{2} - \frac{1}{3}\right) = \boldsymbol{\frac{\pi}{6}}
$$

### つまずきやすいポイント

- 面積では**上下（左右）関係の確認**が最優先。交点だけ求めて機械的に引き算すると符号を誤る。区間の途中で上下が入れ替わる場合は積分を分割する。
- 2曲線間の回転体は $\pi\int (f^2 - g^2)\,dx$ であり、$\pi\int (f-g)^2\,dx$ **ではない**。断面がドーナツ形（円環）になることをイメージする。
- 回転体では、回転軸をまたぐ図形をそのまま回すと重複が生じる。**軸に関して折り返してから**外側の曲線で立式する。
- 「変位（位置の変化）」と「道のり」の混同。道のりは $|v|$ の積分であり、$v$ の符号が変わる時刻で区間を分ける。
- 曲線の長さの計算は、根号の中が**完全平方の形に変形できるように問題が作られている**ことが多い。$1 + (y')^2$ を計算したら平方完成を疑う。
- 媒介変数表示の面積・長さでは、$t$ の増加にともなって $x$ が増加するか（進行方向）を確認してから置換する。

---

## 学習のまとめと入試へ向けて

数学IIIの学習は「極限 → 微分 → 積分」という一本の流れです。

1. **極限**はすべての土台。$\dfrac{\sin x}{x} \to 1$ と $e$ の定義が、三角関数・指数対数関数の微分公式の根拠になっている。
2. **微分**は計算力が命。合成関数の微分を無意識にできるまで練習し、増減表を正確に速く書けるようにする。
3. **積分**は「微分の逆」＋「区分求積の思想」。置換積分・部分積分の型を体に入れ、面積・体積では図を描いてから立式する習慣をつける。

入試では、極限・微積分の融合問題（例：区分求積と不等式評価、定積分で定義された数列の極限）が頻出です。各章の「つまずきやすいポイント」を定期的に読み返し、自分のミスのパターンを把握することが最短の上達法です。

# 习题5
1. 设$A=\{a,b,c,d,f\}$，构造一对加法和乘法运算，使$\langle A, +, \cdot \rangle$构成一个环。

2. 设$A=\{a+b\sqrt{2}\mid a,b\in\mathbb{Z}\}$，证明：$A$是关于数的加法和乘法构成的环。

3. 设$\langle R, +, \cdot \rangle$是环，证明：$\forall a,b,c\in A$，有
$$(-a)\cdot(-b)=a\cdot b$$
$$a\cdot(b-c)=a\cdot b-a\cdot c$$
$$(b-c)\cdot a=b\cdot a-c\cdot a$$

4. 证明：二项式定理
$$(a+b)^n=\sum_{k=0}^n C_n^k a^k\cdot b^{n-k}$$
在交换环中成立。

5. 找出$\langle \mathbb{Z}_6, \oplus, \otimes \rangle$的全部零因子。

6. 若环$\langle R, +, \cdot \rangle$对于加法构成一个循环群，证明：$\langle R, +, \cdot \rangle$是一个交换环。

7. 证明：若$\langle R, +, \cdot \rangle$是一个除环，则$\langle R, +, \cdot \rangle$中无零因子。

8. 设$S_1$和$S_2$是环$\langle R, +, \cdot \rangle$的子环，证明$S_1\cap S_2$是$\langle R, +, \cdot \rangle$的子环。

9. 设$A=\{a+b\sqrt{3}\mid a,b\in\mathbb{Q}\}$，证明：$A$是关于数的加法和乘法构成的域。

10. 证明：实数集$\mathbb{R}$、复数集$\mathbb{C}$关于普通加法和乘法构成域。

11. 在 S6 中设
$$
\alpha = \begin{pmatrix} 1 & 2 & 3 & 4 & 5 & 6 \\ 5 & 1 & 2 & 3 & 6 & 4 \end{pmatrix},\quad
\beta = \begin{pmatrix} 1 & 2 & 3 & 4 & 5 & 6 \\ 4 & 3 & 1 & 5 & 2 & 6 \end{pmatrix}.
$$

(1) 求解方程 $\alpha x = \beta$；
(2) 写出$\langle x \rangle$的所有子群。

# 第1题解答

取对应关系
$$
a\leftrightarrow 0,\quad b\leftrightarrow 1,\quad c\leftrightarrow 2,\quad d\leftrightarrow 3,\quad f\leftrightarrow 4.
$$

在集合 $A=\{a,b,c,d,f\}$ 上定义加法与乘法，方法是把它们分别对应为模 $5$ 的加法与乘法。也就是说，若元素 $x,y\in A$ 分别对应于 $\overline{m},\overline{n}\in\mathbb{Z}_5$，则
$$
x+y\text{ 对应于 }\overline{m+n},\qquad x\cdot y\text{ 对应于 }\overline{mn}.
$$

具体可写成如下运算表。

加法表：

| $+$ | $a$ | $b$ | $c$ | $d$ | $f$ |
|---|---|---|---|---|---|
| $a$ | $a$ | $b$ | $c$ | $d$ | $f$ |
| $b$ | $b$ | $c$ | $d$ | $f$ | $a$ |
| $c$ | $c$ | $d$ | $f$ | $a$ | $b$ |
| $d$ | $d$ | $f$ | $a$ | $b$ | $c$ |
| $f$ | $f$ | $a$ | $b$ | $c$ | $d$ |

乘法表：

| $\cdot$ | $a$ | $b$ | $c$ | $d$ | $f$ |
|---|---|---|---|---|---|
| $a$ | $a$ | $a$ | $a$ | $a$ | $a$ |
| $b$ | $a$ | $b$ | $c$ | $d$ | $f$ |
| $c$ | $a$ | $c$ | $f$ | $b$ | $d$ |
| $d$ | $a$ | $d$ | $b$ | $f$ | $c$ |
| $f$ | $a$ | $f$ | $d$ | $c$ | $b$ |

这样定义后，$\langle A,+,\cdot\rangle$ 与 $\mathbb{Z}_5$ 在通常加法、乘法下同构。由于 $\mathbb{Z}_5$ 是一个环，所以 $\langle A,+,\cdot\rangle$ 也是一个环。

其中，$a$ 是加法零元，$b$ 是乘法单位元。

# 第2题解答

设
$$
A=\{a+b\sqrt{2}\mid a,b\in\mathbb{Z}\}.
$$

下面证明 $A$ 关于数的普通加法和乘法构成一个环。

任取
$$
x=a+b\sqrt{2},\qquad y=c+d\sqrt{2},
$$
其中 $a,b,c,d\in\mathbb{Z}$。

首先证明 $A$ 对加法构成交换群。因为
$$
x+y=(a+b\sqrt{2})+(c+d\sqrt{2})=(a+c)+(b+d)\sqrt{2}.
$$
由于 $a+c\in\mathbb{Z}$，$b+d\in\mathbb{Z}$，所以 $x+y\in A$，即 $A$ 对加法封闭。

加法零元为
$$
0=0+0\sqrt{2}\in A.
$$

对任意
$$
x=a+b\sqrt{2}\in A,
$$
它的加法逆元为
$$
-x=-a-b\sqrt{2}=(-a)+(-b)\sqrt{2}\in A.
$$

而加法结合律和交换律都由实数加法的结合律和交换律直接得到。因此，$\langle A,+\rangle$ 是交换群。

再证明乘法封闭。任取
$$
x=a+b\sqrt{2},\qquad y=c+d\sqrt{2}\in A,
$$
则
$$
xy=(a+b\sqrt{2})(c+d\sqrt{2})
=ac+ad\sqrt{2}+bc\sqrt{2}+2bd
=(ac+2bd)+(ad+bc)\sqrt{2}.
$$
由于
$$
ac+2bd\in\mathbb{Z},\qquad ad+bc\in\mathbb{Z},
$$
所以
$$
xy\in A.
$$
因此，$A$ 对乘法封闭。

乘法结合律以及乘法对加法的左右分配律，都由实数乘法的结合律和实数乘法对加法的分配律直接得到。

综上，$A$ 对加法构成交换群，对乘法封闭且满足结合律，并且乘法对加法满足分配律，所以 $A$ 关于数的普通加法和乘法构成一个环。

此外，
$$
1=1+0\sqrt{2}\in A,
$$
所以它还是一个含幺交换环。

# 第3题解答

设 $\langle R,+,\cdot\rangle$ 是一个环，任取 $a,b,c\in R$。

先证明一个辅助结论：对任意 $x\in R$，有
$$
0\cdot x=0,\qquad x\cdot 0=0.
$$

事实上，
$$
(0+0)\cdot x=0\cdot x+0\cdot x.
$$
由于 $0+0=0$，所以
$$
0\cdot x=0\cdot x+0\cdot x.
$$
两边同时加上 $-(0\cdot x)$，得
$$
0=0\cdot x.
$$
同理，由
$$
x\cdot(0+0)=x\cdot 0+x\cdot 0
$$
可得
$$
x\cdot 0=0.
$$

下面分别证明题中的三个等式。

1. 证明 $(-a)\cdot(-b)=a\cdot b$

先证
$$
(-a)\cdot b=-(a\cdot b).
$$
因为
$$
(a+(-a))\cdot b=0\cdot b=0,
$$
于是
$$
a\cdot b+(-a)\cdot b=0.
$$
所以 $(-a)\cdot b$ 是 $a\cdot b$ 的加法逆元，即
$$
(-a)\cdot b=-(a\cdot b).
$$

同理可证
$$
a\cdot(-b)=-(a\cdot b).
$$

于是
$$
(-a)\cdot(-b)=-\bigl(a\cdot(-b)\bigr)=-\bigl(-(a\cdot b)\bigr)=a\cdot b.
$$

2. 证明 $a\cdot(b-c)=a\cdot b-a\cdot c$

由于
$$
b-c=b+(-c),
$$
由左分配律得
$$
a\cdot(b-c)=a\cdot(b+(-c))=a\cdot b+a\cdot(-c).
$$
而上面已经证明
$$
a\cdot(-c)=-(a\cdot c),
$$
所以
$$
a\cdot(b-c)=a\cdot b-(a\cdot c)=a\cdot b-a\cdot c.
$$

3. 证明 $(b-c)\cdot a=b\cdot a-c\cdot a$

同样地，
$$
b-c=b+(-c).
$$
由右分配律得
$$
(b-c)\cdot a=(b+(-c))\cdot a=b\cdot a+(-c)\cdot a.
$$
又因为
$$
(-c)\cdot a=-(c\cdot a),
$$
所以
$$
(b-c)\cdot a=b\cdot a-c\cdot a.
$$

综上，
$$
(-a)\cdot(-b)=a\cdot b,\qquad
a\cdot(b-c)=a\cdot b-a\cdot c,\qquad
(b-c)\cdot a=b\cdot a-c\cdot a.
$$
命题得证。

# 第4题解答

设 $R$ 是一个交换环，$a,b\in R$。下面用数学归纳法证明
$$
(a+b)^n=\sum_{k=0}^n C_n^k a^k\cdot b^{n-k}.
$$

以下默认环中有乘法单位元 $1$，因此 $a^0=b^0=1$。

当 $n=1$ 时，
$$
(a+b)^1=a+b=C_1^0a^0b+C_1^1ab^0.
$$
故结论对 $n=1$ 成立。

假设当 $n=m$ 时结论成立，即
$$
(a+b)^m=\sum_{k=0}^m C_m^k a^k\cdot b^{m-k}.
$$

则
$$
\begin{aligned}
(a+b)^{m+1}
&=(a+b)(a+b)^m\\
&=(a+b)\sum_{k=0}^m C_m^k a^k\cdot b^{m-k}\\
&=\sum_{k=0}^m C_m^k a\cdot a^k\cdot b^{m-k}
 +\sum_{k=0}^m C_m^k b\cdot a^k\cdot b^{m-k}.
\end{aligned}
$$

由于环是交换环，所以 $ab=ba$，从而 $a,b$ 与它们的各次幂都可交换，因此
$$
\begin{aligned}
(a+b)^{m+1}
&=\sum_{k=0}^m C_m^k a^{k+1}\cdot b^{m-k}
 +\sum_{k=0}^m C_m^k a^k\cdot b^{m+1-k}.
\end{aligned}
$$

把第一项中的指标换成 $j=k+1$，则
$$
\sum_{k=0}^m C_m^k a^{k+1}\cdot b^{m-k}
=\sum_{j=1}^{m+1} C_m^{j-1} a^j\cdot b^{m+1-j}.
$$

于是
$$
\begin{aligned}
(a+b)^{m+1}
&=\sum_{j=1}^{m+1} C_m^{j-1} a^j\cdot b^{m+1-j}
 +\sum_{j=0}^m C_m^j a^j\cdot b^{m+1-j}\\
&=C_m^0 b^{m+1}
 +\sum_{j=1}^m \left(C_m^{j-1}+C_m^j\right)a^j\cdot b^{m+1-j}
 +C_m^m a^{m+1}.
\end{aligned}
$$

再由组合恒等式
$$
C_m^{j-1}+C_m^j=C_{m+1}^j
$$
可得
$$
\begin{aligned}
(a+b)^{m+1}
&=C_{m+1}^0 a^0\cdot b^{m+1}
 +\sum_{j=1}^m C_{m+1}^j a^j\cdot b^{m+1-j}
 +C_{m+1}^{m+1} a^{m+1}\cdot b^0\\
&=\sum_{j=0}^{m+1} C_{m+1}^j a^j\cdot b^{m+1-j}.
\end{aligned}
$$

所以结论对 $n=m+1$ 也成立。

综上，由数学归纳法知，对任意正整数 $n$，都有
$$
(a+b)^n=\sum_{k=0}^n C_n^k a^k\cdot b^{n-k}.
$$
命题得证。

# 第5题解答

在 $\mathbb{Z}_6=\{0,1,2,3,4,5\}$ 中，零因子是指非零元素 $a$，存在非零元素 $b$，使得
$$
a\otimes b=0.
$$

下面逐个判断 $\mathbb{Z}_6$ 中的非零元素。

$$
1\otimes 1=1,\quad 1\otimes 2=2,\quad 1\otimes 3=3,\quad 1\otimes 4=4,\quad 1\otimes 5=5,
$$
所以 $1$ 不是零因子。

$$
2\otimes 3=6\equiv 0 \pmod 6,
$$
所以 $2$ 是零因子。

$$
3\otimes 2=6\equiv 0 \pmod 6,
$$
所以 $3$ 是零因子。

$$
4\otimes 3=12\equiv 0 \pmod 6,
$$
所以 $4$ 是零因子。

再看 $5$，由于
$$
5\otimes 1=5,\quad 5\otimes 2=10\equiv 4,\quad 5\otimes 3=15\equiv 3,\quad 5\otimes 4=20\equiv 2,\quad 5\otimes 5=25\equiv 1 \pmod 6,
$$
都不等于 $0$，所以 $5$ 不是零因子。

因此，$\langle \mathbb{Z}_6,\oplus,\otimes\rangle$ 的全部零因子是
$$
2,\ 3,\ 4.
$$

# 第6题解答

设环 $\langle R,+,\cdot\rangle$ 对于加法构成一个循环群。则存在某个 $u\in R$，使得
$$
R=\langle u\rangle=\{nu\mid n\in\mathbb{Z}\}.
$$

也就是说，对任意 $x,y\in R$，都存在整数 $m,n$，使得
$$
x=mu,\qquad y=nu.
$$

下面先证明一个结论：对任意 $a,b\in R$ 及任意整数 $k$，有
$$
(ka)\cdot b=k(a\cdot b),\qquad a\cdot(kb)=k(a\cdot b).
$$

当 $k>0$ 时，这由分配律反复使用即可得到；当 $k=0$ 时，等式化为
$$
0\cdot b=0,\qquad a\cdot 0=0,
$$
这在环中成立；当 $k<0$ 时，再结合第 3 题已经证明的
$$
(-a)\cdot b=-(a\cdot b),\qquad a\cdot(-b)=-(a\cdot b)
$$
即可得到上述结论对一切整数 $k$ 都成立。

于是
$$
\begin{aligned}
x\cdot y
&=(mu)\cdot(nu)\\
&=m\bigl(u\cdot(nu)\bigr)\\
&=m\bigl(n(u\cdot u)\bigr)\\
&=(mn)(u\cdot u).
\end{aligned}
$$

同理，
$$
\begin{aligned}
y\cdot x
&=(nu)\cdot(mu)\\
&=(nm)(u\cdot u).
\end{aligned}
$$

由于整数乘法满足交换律，即
$$
mn=nm,
$$
所以
$$
x\cdot y=(mn)(u\cdot u)=(nm)(u\cdot u)=y\cdot x.
$$

因此，对任意 $x,y\in R$，都有
$$
x\cdot y=y\cdot x.
$$

故 $\langle R,+,\cdot\rangle$ 是一个交换环。

# 第7题解答

证明：若 $\langle R,+,\cdot\rangle$ 是一个除环，则 $R$ 中无零因子。

任取 $a,b\in R$，并设
$$
a\cdot b=0.
$$

下面证明必有 $a=0$ 或 $b=0$。

若 $a=0$，则结论显然成立。

若 $a\neq 0$，由于 $R$ 是除环，所以 $a$ 有乘法逆元 $a^{-1}$。于是等式两边左乘 $a^{-1}$，得
$$
a^{-1}(a\cdot b)=a^{-1}\cdot 0.
$$

由结合律以及环中 $x\cdot 0=0$，可得
$$
(a^{-1}a)\cdot b=0,
$$
即
$$
1\cdot b=0.
$$
从而
$$
b=0.
$$

因此，只要 $a\cdot b=0$，就必有 $a=0$ 或 $b=0$。

这说明 $\langle R,+,\cdot\rangle$ 中无零因子。命题得证。

# 第8题解答

设 $S_1$ 和 $S_2$ 是环 $\langle R,+,\cdot\rangle$ 的子环。下面证明
$$
S_1\cap S_2
$$
也是 $R$ 的子环。

先证它非空。因为 $S_1,S_2$ 都是子环，所以它们都含有加法零元 $0$，因此
$$
0\in S_1,\qquad 0\in S_2.
$$
从而
$$
0\in S_1\cap S_2.
$$
所以 $S_1\cap S_2\neq\varnothing$。

再证它对减法和乘法封闭。

任取
$$
a,b\in S_1\cap S_2.
$$
则
$$
a,b\in S_1,\qquad a,b\in S_2.
$$

由于 $S_1$ 是子环，所以
$$
a-b\in S_1,\qquad a\cdot b\in S_1.
$$

由于 $S_2$ 是子环，所以
$$
a-b\in S_2,\qquad a\cdot b\in S_2.
$$

因此
$$
a-b\in S_1\cap S_2,\qquad a\cdot b\in S_1\cap S_2.
$$

所以 $S_1\cap S_2$ 非空，且对减法与乘法封闭。由子环判定法可知，
$$
S_1\cap S_2
$$
是环 $\langle R,+,\cdot\rangle$ 的子环。命题得证。

# 第9题解答

设
$$
A=\{a+b\sqrt{3}\mid a,b\in\mathbb{Q}\}.
$$

下面证明 $A$ 关于数的普通加法和乘法构成一个域。

任取
$$
x=a+b\sqrt{3},\qquad y=c+d\sqrt{3},
$$
其中 $a,b,c,d\in\mathbb{Q}$。

先证明 $A$ 关于加法构成交换群。

因为
$$
x+y=(a+c)+(b+d)\sqrt{3}.
$$
由于 $a+c,b+d\in\mathbb{Q}$，所以
$$
x+y\in A.
$$
因此 $A$ 对加法封闭。

加法零元为
$$
0=0+0\sqrt{3}\in A.
$$

对任意
$$
x=a+b\sqrt{3}\in A,
$$
其加法逆元为
$$
-x=-a-b\sqrt{3}=(-a)+(-b)\sqrt{3}\in A.
$$

加法交换律和结合律都由实数加法直接继承，所以 $\langle A,+\rangle$ 是交换群。

再证明乘法封闭。因为
$$
xy=(a+b\sqrt{3})(c+d\sqrt{3})
=(ac+3bd)+(ad+bc)\sqrt{3}.
$$
由于
$$
ac+3bd\in\mathbb{Q},\qquad ad+bc\in\mathbb{Q},
$$
所以
$$
xy\in A.
$$

而乘法结合律、交换律以及乘法对加法的分配律，都由实数的运算律直接继承。

此外，
$$
1=1+0\sqrt{3}\in A.
$$

最后证明 $A$ 中每个非零元素都有乘法逆元。

任取非零元素
$$
x=a+b\sqrt{3}\in A,\qquad x\neq 0.
$$

考虑
$$
x(a-b\sqrt{3})=(a+b\sqrt{3})(a-b\sqrt{3})=a^2-3b^2.
$$

下面说明
$$
a^2-3b^2\neq 0.
$$

若
$$
a^2-3b^2=0,
$$
则
$$
a^2=3b^2.
$$

若 $b=0$，则 $a=0$，从而 $x=0$，与 $x\neq 0$ 矛盾。

若 $b\neq 0$，则
$$
\left(\frac{a}{b}\right)^2=3.
$$
这就说明
$$
\frac{a}{b}=\pm\sqrt{3},
$$
但 $\dfrac{a}{b}\in\mathbb{Q}$，而 $\sqrt{3}$ 是无理数，矛盾。

因此
$$
a^2-3b^2\neq 0.
$$

于是
$$
x^{-1}=\frac{1}{a+b\sqrt{3}}
=\frac{a-b\sqrt{3}}{a^2-3b^2}
=\frac{a}{a^2-3b^2}+\frac{-b}{a^2-3b^2}\sqrt{3}.
$$

由于
$$
\frac{a}{a^2-3b^2}\in\mathbb{Q},\qquad \frac{-b}{a^2-3b^2}\in\mathbb{Q},
$$
所以
$$
x^{-1}\in A.
$$

综上，$A$ 关于普通加法和乘法构成一个域。命题得证。

# 第10题解答

下面分别证明 $\mathbb{R}$ 和 $\mathbb{C}$ 关于普通加法和乘法都构成域。

## （1）$\mathbb{R}$ 构成域

实数集 $\mathbb{R}$ 对普通加法、乘法都封闭；加法满足交换律、结合律，乘法满足交换律、结合律，且乘法对加法满足分配律，这些都是实数的基本运算律。

加法零元是
$$
0\in\mathbb{R},
$$
乘法单位元是
$$
1\in\mathbb{R},\qquad 1\neq 0.
$$

对任意 $a\in\mathbb{R}$，其加法逆元是 $-a\in\mathbb{R}$。

对任意非零实数 $a\in\mathbb{R}$，其乘法逆元是
$$
\frac{1}{a}\in\mathbb{R}.
$$

因此，$\mathbb{R}$ 关于普通加法构成交换群，$\mathbb{R}\setminus\{0\}$ 关于普通乘法构成交换群，并且乘法对加法满足分配律，所以 $\mathbb{R}$ 构成域。

## （2）$\mathbb{C}$ 构成域

任取
$$
z_1=a+bi,\qquad z_2=c+di,
$$
其中 $a,b,c,d\in\mathbb{R}$。

则
$$
z_1+z_2=(a+c)+(b+d)i\in\mathbb{C},
$$
所以 $\mathbb{C}$ 对加法封闭。

又
$$
z_1z_2=(a+bi)(c+di)=(ac-bd)+(ad+bc)i\in\mathbb{C},
$$
所以 $\mathbb{C}$ 对乘法封闭。

加法零元为
$$
0=0+0i,
$$
乘法单位元为
$$
1=1+0i.
$$

对任意
$$
z=a+bi\in\mathbb{C},
$$
其加法逆元为
$$
-z=-a-bi\in\mathbb{C}.
$$

若
$$
z=a+bi\neq 0,
$$
则 $a,b$ 不同时为 $0$，因此
$$
a^2+b^2>0.
$$

于是
$$
z^{-1}=\frac{1}{a+bi}
=\frac{a-bi}{a^2+b^2}
=\frac{a}{a^2+b^2}-\frac{b}{a^2+b^2}i\in\mathbb{C}.
$$

而加法交换律、结合律，乘法交换律、结合律，以及分配律都由复数的基本运算律成立。

因此，$\mathbb{C}$ 关于普通加法和乘法构成域。

综上，实数集 $\mathbb{R}$、复数集 $\mathbb{C}$ 关于普通加法和乘法都构成域。命题得证。

# 第11题解答

在 $S_6$ 中，置换的乘法是复合运算，并且按“先右后左”计算。方程
$$
\alpha x=\beta
$$
两边左乘 $\alpha^{-1}$，得
$$
x=\alpha^{-1}\beta.
$$

先求 $\alpha^{-1}$。

由
$$
\alpha=\begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6\\
5 & 1 & 2 & 3 & 6 & 4
\end{pmatrix}
$$
可知
$$
\alpha^{-1}=\begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6\\
2 & 3 & 4 & 6 & 1 & 5
\end{pmatrix}.
$$

因此对每个 $i\in\{1,2,3,4,5,6\}$，有
$$
x(i)=\alpha^{-1}(\beta(i)).
$$

逐个计算得
$$
\begin{aligned}
x(1)&=\alpha^{-1}(4)=6,\\
x(2)&=\alpha^{-1}(3)=4,\\
x(3)&=\alpha^{-1}(1)=2,\\
x(4)&=\alpha^{-1}(5)=1,\\
x(5)&=\alpha^{-1}(2)=3,\\
x(6)&=\alpha^{-1}(6)=5.
\end{aligned}
$$

所以
$$
x=\begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6\\
6 & 4 & 2 & 1 & 3 & 5
\end{pmatrix}
=(1\ 6\ 5\ 3\ 2\ 4).
$$

这就解出了方程 $\alpha x=\beta$。

下面写出 $\langle x\rangle$ 的所有子群。

由于
$$
x=(1\ 6\ 5\ 3\ 2\ 4)
$$
是一个 $6$-轮换，所以
$$
|x|=6.
$$

因此 $\langle x\rangle$ 是一个 $6$ 阶循环群。循环群的子群个数与其阶的正因子个数相同，而 $6$ 的正因子为
$$
1,\ 2,\ 3,\ 6.
$$

故 $\langle x\rangle$ 的全部子群为：

1. 阶为 $1$ 的子群
$$
\{e\}.
$$

2. 阶为 $2$ 的子群
$$
\langle x^3\rangle=\{e,x^3\}.
$$
其中
$$
x^3=(1\ 3)(2\ 6)(4\ 5).
$$

3. 阶为 $3$ 的子群
$$
\langle x^2\rangle=\{e,x^2,x^4\}.
$$
其中
$$
x^2=(1\ 5\ 2)(3\ 4\ 6),\qquad
x^4=(1\ 2\ 5)(3\ 6\ 4).
$$

4. 阶为 $6$ 的子群，也就是全群
$$
\langle x\rangle=\{e,x,x^2,x^3,x^4,x^5\}.
$$
其中
$$
x^5=(1\ 4\ 2\ 3\ 5\ 6).
$$

综上，方程的解为
$$
x=\begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6\\
6 & 4 & 2 & 1 & 3 & 5
\end{pmatrix}
=(1\ 6\ 5\ 3\ 2\ 4),
$$
而 $\langle x\rangle$ 的所有子群为
$$
\{e\},\qquad
\langle x^3\rangle,\qquad
\langle x^2\rangle,\qquad
\langle x\rangle.
$$

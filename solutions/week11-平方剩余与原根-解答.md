# 习题 3 解答

## 1.

分别求出模 17 和模 37 的所有平方剩余和平方非剩余。

**模 17**（计算 $1^2$ 至 $8^2 \bmod 17$）：

| $a$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|-----|---|---|---|---|---|---|---|---|
| $a^2\bmod17$ | 1 | 4 | 9 | 16 | 8 | 2 | 15 | 13 |

> **平方剩余**（8 个）：$\{1, 2, 4, 8, 9, 13, 15, 16\}$
> **平方非剩余**（8 个）：$\{3, 5, 6, 7, 10, 11, 12, 14\}$

**模 37**（计算 $1^2$ 至 $18^2 \bmod 37$）：

| $a$ | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
|-----|---|---|---|---|---|---|---|---|---|
| $a^2$ | 1 | 4 | 9 | 16 | 25 | 36 | 12 | 27 | 7 |

| $a$ | 10 | 11 | 12 | 13 | 14 | 15 | 16 | 17 | 18 |
|-----|----|----|----|----|----|----|----|----|----|
| $a^2$ | 26 | 10 | 33 | 21 | 11 | 3 | 34 | 30 | 28 |

> **平方剩余**（18 个）：$\{1, 3, 4, 7, 9, 10, 11, 12, 16, 21, 25, 26, 27, 28, 30, 33, 34, 36\}$
> **平方非剩余**（18 个）：其余 18 个数 $\{2, 5, 6, 8, 13, 14, 15, 17, 18, 19, 20, 22, 23, 24, 29, 31, 32, 35\}$

---

## 2.

求下列同余式的解数。

**(1)** $x^2 \equiv 286 \pmod{563}$。

计算勒让德符号 $\left(\frac{286}{563}\right)$。$286=2\times11\times13$。

- $\left(\frac{2}{563}\right)$：$563\equiv3\pmod{8}$，$=-1$。
- $\left(\frac{11}{563}\right)=-\left(\frac{563}{11}\right)=-\left(\frac{2}{11}\right)=-(-1)=1$。（$563\equiv2\pmod{11}$）
- $\left(\frac{13}{563}\right)=\left(\frac{563}{13}\right)=\left(\frac{4}{13}\right)=1$。（$563\equiv4\pmod{13}$）

$\left(\frac{286}{563}\right)=(-1)\times1\times1=-1$。286 是模 563 的平方非剩余。

> 解数：**0**。

**(2)** $x^2 \equiv 3149 \pmod{5987}$（5987 是素数）。

$3149=47\times67$。计算 $\left(\frac{3149}{5987}\right)=\left(\frac{47}{5987}\right)\left(\frac{67}{5987}\right)$。

- $\left(\frac{47}{5987}\right)=-\left(\frac{5987}{47}\right)=-\left(\frac{18}{47}\right)=-\left(\frac{2}{47}\right)\left(\frac{3}{47}\right)^2=-\left(\frac{2}{47}\right)=-(1)=-1$。（$47\equiv7\pmod{8}$，$(2/47)=1$）

- $\left(\frac{67}{5987}\right)=-\left(\frac{5987}{67}\right)=-\left(\frac{24}{67}\right)=-\left(\frac{2^3\times3}{67}\right)=-\left(\frac{2}{67}\right)^3\left(\frac{3}{67}\right)=-(-1)^3\times(-1)=-1$。
  （$67\equiv3\pmod{8}$，$(2/67)=-1$；$(3/67)=-(67/3)=-(1/3)=-1$）

$\left(\frac{3149}{5987}\right)=(-1)\times(-1)=1$。3149 是模 5987 的平方剩余。

> 解数：**2**。

**(3)** $x^2 \equiv 9 \pmod{35}$。$35=5\times7$。

- 模 5：$x^2\equiv4\pmod{5}$。$x\equiv\pm2$。2 个解。
- 模 7：$x^2\equiv2\pmod{7}$。$(2/7)=1$。2 个解。

> 解数：$2\times2=4$。

**(4)** $x^2 \equiv 2 \pmod{169}$。$169=13^2$。

先求 $x^2\equiv2\pmod{13}$。$\left(\frac{2}{13}\right)=-1$（$13\equiv5\equiv-3\pmod{8}$）。模 13 无解，故模 169 亦无解。

> 解数：**0**。

**(5)** $x^2 \equiv 8 \pmod{75}$。$75=3\times25$。

模 3：$x^2\equiv2\pmod{3}$。枚举 $0^2=0$，$1^2=1$，$2^2=4\equiv1$，无解。

> 解数：**0**。

**(6)** $x^2 \equiv 2 \pmod{45}$。$45=9\times5$。

模 5：$x^2\equiv2\pmod{5}$。$\left(\frac{2}{5}\right)=-1$。无解。

> 解数：**0**。

**(7)** $x^2 \equiv 1 \pmod{75}$。$75=3\times25$。

- 模 3：$x^2\equiv1\pmod{3}$。$x\equiv\pm1$。2 个解。
- 模 25：$x^2\equiv1\pmod{25}$。$x\equiv\pm1$。2 个解。

> 解数：$2\times2=4$。

---

## 3.

求勒让德符号。

**(1)** $\left(\frac{23}{17}\right)=\left(\frac{6}{17}\right)=\left(\frac{2}{17}\right)\left(\frac{3}{17}\right)$。

$\left(\frac{2}{17}\right)=1$（$17\equiv1\pmod{8}$）。
$\left(\frac{3}{17}\right)=\left(\frac{17}{3}\right)=\left(\frac{2}{3}\right)=-1$。

> $\left(\frac{23}{17}\right)=1\times(-1)=-1$。

**(2)** $\left(\frac{21}{29}\right)=\left(\frac{3}{29}\right)\left(\frac{7}{29}\right)$。

$\left(\frac{3}{29}\right)=\left(\frac{29}{3}\right)=\left(\frac{2}{3}\right)=-1$。
$\left(\frac{7}{29}\right)=\left(\frac{29}{7}\right)=\left(\frac{1}{7}\right)=1$。

> $\left(\frac{21}{29}\right)=(-1)\times1=-1$。

**(3)** $\left(\frac{178}{227}\right)=\left(\frac{2}{227}\right)\left(\frac{89}{227}\right)$。

$\left(\frac{2}{227}\right)$：$227\equiv3\pmod{8}$，$=-1$。
$\left(\frac{89}{227}\right)=\left(\frac{227}{89}\right)=\left(\frac{49}{89}\right)=\left(\frac{7}{89}\right)^2=1$。（$227\bmod89=49$）

> $\left(\frac{178}{227}\right)=(-1)\times1=-1$。

**(4)** $\left(\frac{365}{1847}\right)=\left(\frac{5}{1847}\right)\left(\frac{73}{1847}\right)$。

$\left(\frac{5}{1847}\right)$：$1847\equiv2\pmod{5}$，$=-1$。

$\left(\frac{73}{1847}\right)=\left(\frac{1847}{73}\right)=\left(\frac{22}{73}\right)=\left(\frac{2}{73}\right)\left(\frac{11}{73}\right)$。
- $\left(\frac{2}{73}\right)=1$（$73\equiv1\pmod{8}$）。
- $\left(\frac{11}{73}\right)=\left(\frac{73}{11}\right)=\left(\frac{7}{11}\right)=-\left(\frac{11}{7}\right)=-\left(\frac{4}{7}\right)=-1$。

$\left(\frac{22}{73}\right)=-1$，故 $\left(\frac{73}{1847}\right)=-1$。

> $\left(\frac{365}{1847}\right)=(-1)\times(-1)=1$。

---

## 4.

求雅可比符号。

**(1)** $\left(\frac{23}{72}\right)$。$72=2^3\times3^2$。

按 Kronecker 扩充：
- $\left(\frac{23}{2}\right)=(-1)^{(23^2-1)/8}=(-1)^{66}=1$，$\left(\frac{23}{2^3}\right)=1^3=1$。
- $\left(\frac{23}{3}\right)=\left(\frac{2}{3}\right)=-1$，$\left(\frac{23}{3^2}\right)=(-1)^2=1$。

> $\left(\frac{23}{72}\right)=1\times1=1$。

（注：标准 Jacobi 符号要求分母为奇，此处按 Kronecker 符号扩充计算。）

**(2)** $\left(\frac{77}{35}\right)$。$\gcd(77,35)=7\neq1$。

> $\left(\frac{77}{35}\right)=0$。

**(3)** $\left(\frac{21}{39}\right)$。$\gcd(21,39)=3\neq1$。

> $\left(\frac{21}{39}\right)=0$。

**(4)** $\left(\frac{178}{236}\right)$。$\gcd(178,236)=2\neq1$，且分母为偶。

> $\left(\frac{178}{236}\right)=0$。

---

## 5.

求所有的素数 $p$，$(11,p)=1$，且 $x^2\equiv11\pmod{p}$ 有解。

即求使 $\left(\frac{11}{p}\right)=1$ 的奇素数 $p\neq11$。

由二次互反律：
$$\left(\frac{11}{p}\right)=\left(\frac{p}{11}\right)(-1)^{\frac{11-1}{2}\cdot\frac{p-1}{2}}=\left(\frac{p}{11}\right)(-1)^{5\cdot\frac{p-1}{2}}$$

当 $p\equiv1\pmod{4}$ 时，$(-1)^{5\cdot\frac{p-1}{2}}=1$；当 $p\equiv3\pmod{4}$ 时，$=-1$。

$\left(\frac{p}{11}\right)=1$ 当 $p\equiv1,3,4,5,9\pmod{11}$（模 11 的平方剩余）。
$\left(\frac{p}{11}\right)=-1$ 当 $p\equiv2,6,7,8,10\pmod{11}$。

**情况一**：$p\equiv1\pmod{4}$，需 $\left(\frac{p}{11}\right)=1$。即 $p\equiv1\pmod{4}$ 且 $p\equiv1,3,4,5,9\pmod{11}$。

用 CRT 解（$\gcd(4,11)=1$，模 44）：

| $p\bmod11$ | $p\bmod44$（$p\equiv1\bmod4$） |
|------------|------|
| 1 | 1 |
| 3 | 25 |
| 4 | 37 |
| 5 | 5 |
| 9 | 9 |

**情况二**：$p\equiv3\pmod{4}$，需 $\left(\frac{p}{11}\right)=-1$。即 $p\equiv3\pmod{4}$ 且 $p\equiv2,6,7,8,10\pmod{11}$。

| $p\bmod11$ | $p\bmod44$（$p\equiv3\bmod4$） |
| ---------- | ---------------------------- |
| 2          | 35                           |
| 6          | 39                           |
| 7          | 7                            |
| 8          | 19                           |
| 10         | 43                           |

> $p$ 满足 $p \equiv 1,5,7,9,19,25,35,37,39,43 \pmod{44}$（$p\neq11$）。

---

## 6.

求解同余式。

**(1)** $x^2 \equiv 41 \pmod{64}$。$64=2^6$。

$41\equiv1\pmod{8}$，属于 $2^k$（$k\ge3$）下的可解情况（$a\equiv1\pmod{8}$）。

模 8：$x^2\equiv41\equiv1\pmod{8}$。解：$x\equiv1,3,5,7\pmod{8}$（4 个）。

从 $x_0=1$ 提升（其他解可对称得到）：

模 16：$x=1+8t$。$x^2\equiv1+16t\equiv41\equiv9\pmod{16}$。$16t\equiv8\pmod{16}$，即 $t$ 任意。但 $t$ 模 2 给出不同提升...

设 $f(x)=x^2-41$，$f'(x)=2x$。$f(1)=-40\equiv8\pmod{16}$。需 $8+2\cdot1\cdot8t\equiv0\pmod{16}$，即 $8+16t\equiv8\pmod{16}$，自动成立。$t=0,1$ 均可。$x\equiv1,9\pmod{16}$。

模 32：从 $x=1$：$f(1)=-40$。$1+16t$：$f(1+16t)\equiv f(1)+f'(1)\cdot16t\equiv-40+2\cdot16t\equiv24+32t\pmod{32}$。
$24\not\equiv0\pmod{32}$。需要调整... 实际上从 $x=9$：$9^2=81\equiv17\not\equiv41\pmod{32}$。

看来需要系统处理。$x^2\equiv41\equiv9\pmod{16}$，解 $x\equiv3,5\pmod{8}$ 提升：
模 16：$x=3$，$3^2=9\equiv9\not\equiv41\equiv9\pmod{16}$。$9\equiv9$，成立。
$x=5$：$5^2=25\equiv9\pmod{16}$。也成立。
故模 16 的解：$x\equiv3,5\pmod{8}$ 均直接满足 $x\equiv3,5,11,13\pmod{16}$。（因为 $3+8=11$，$5+8=13$）

验证：$3^2=9\equiv41\pmod{16}$ ✓。$11^2=121\equiv9\pmod{16}$ ✓。

现在 $x^2\equiv41\pmod{64}$。41 mod 64 = 41。

已知模 16 的解为 $x\equiv\pm3,\pm5\equiv3,5,11,13\pmod{16}$。

提升到模 32，再提升到模 64。每个解唯一提升（因 $f'(x)=2x$，当 $x$ 为奇数时 $f'(x)\equiv2\pmod{4}\not\equiv0\pmod{2}$ 满足 Hensel 条件）。

从 $x\equiv3\pmod{16}$：$x=3+16t$。$f(3)=9-41=-32\equiv0\pmod{16}$。$-32+2\times3\times16t\equiv-32+96t\pmod{32}$。
$-32\equiv0\pmod{32}$ 且 $96t\equiv0\pmod{32}$。无条件限制，$t$ 任意模 2。
$t=0$：$x=3\pmod{32}$；$t=1$：$x=19\pmod{32}$。都满足模 32。

从 $x\equiv5\pmod{16}$：$x=5+16t$。$f(5)=25-41=-16\equiv16\pmod{32}$。
$16+2\times5\times16t\equiv16+160t\equiv16+0\equiv16\not\equiv0\pmod{32}$。不成立！$t$ 任意都无法成立。

所以只有 $x\equiv3\pmod{16}$ 可以提升到模 32，得到 $x\equiv3,19\pmod{32}$。

现在提升到模 64：
- $x=3+32t$：$f(3)=-32$。$f(3)+f'(3)\cdot32t\equiv-32+2\times3\times32t\equiv-32+192t\pmod{64}$。$-32\equiv32\pmod{64}$。$192t\equiv0\pmod{64}$（$192=3\times64$）。$32\not\equiv0\pmod{64}$，失败。
- $x=19+32t$：$19^2=361\equiv-23\equiv41\pmod{64}$？

$19^2=361$。$64\times5=320$，$361-320=41$。$41=41$ ✓！

所以 $x=19$ 是模 64 的解！提升：$x=19+32t$。$f(19)=0\pmod{64}$（因为 $19^2=361\equiv41$）。
$f'(19)=38$。$f(19+32t)\equiv0+38\times32t\equiv1216t\pmod{64}$。$1216=64\times19\equiv0$。
所以 $t$ 任意。$x\equiv19,51\pmod{64}$。

由对称性，若 $x$ 是解则 $-x$ 也是解。$-19\equiv45$，$-51\equiv13\pmod{64}$。

四个解：$x\equiv13,19,45,51\pmod{64}$。

验证：$13^2=169$，$64\times2=128$，$169-128=41$ ✓。$19^2=361$，$64\times5=320$，$361-320=41$ ✓。

> $x \equiv 13, 19, 45, 51 \pmod{64}$。

**(2)** $x^2 \equiv 11 \pmod{125}$。$125=5^3$。

先解模 5：$x^2\equiv11\equiv1\pmod{5}$。$x\equiv\pm1\pmod{5}$。2 个解。

从 $x_0=1$ 提升（另一个解 $x\equiv-1$ 对称）。$f(x)=x^2-11$，$f'(x)=2x$。

模 25：$x=1+5t$。$f(1)=1-11=-10\equiv15\pmod{25}$。
$f(1+5t)\equiv f(1)+f'(1)\cdot5t\equiv15+2\times5t=15+10t\equiv0\pmod{25}$。
$15+10t\equiv0\pmod{25}\implies3+2t\equiv0\pmod{5}\implies2t\equiv2\pmod{5}\implies t\equiv1$。
$x=1+5=6$。唯一提升。$x\equiv6\pmod{25}$。

模 125：$x=6+25t$。$f(6)=36-11=25$。
$f(6+25t)\equiv f(6)+f'(6)\cdot25t\equiv25+12\times25t=25+300t\pmod{125}$。
$25+300t=25(1+12t)\equiv0\pmod{125}\implies1+12t\equiv0\pmod{5}\implies12t\equiv-1\implies2t\equiv4\implies t\equiv2$。
$x=6+25\times2=56$。

另一个解：$-56\equiv69\pmod{125}$。

验证：$56^2=3136$。$125\times25=3125$，$3136-3125=11$ ✓。

> $x \equiv 56, 69 \pmod{125}$。

---

## 8.

设素数 $p=4m+1$，$a \mid m$，证明 $\left(\frac{a}{p}\right)=1$。

由 $p=4m+1$ 且 $a\mid m$，设 $m=ak$，则 $p=4ak+1$。

需证 $\left(\frac{a}{p}\right)=1$。由二次互反律：
$$\left(\frac{a}{p}\right)=\left(\frac{p}{a}\right)(-1)^{\frac{a-1}{2}\cdot\frac{p-1}{2}}$$

$p=4ak+1\equiv1\pmod{a}$，故 $\left(\frac{p}{a}\right)=\left(\frac{1}{a}\right)=1$。

$\frac{p-1}{2}=2m=2ak$ 为偶数，故 $(-1)^{\frac{a-1}{2}\cdot\frac{p-1}{2}}=(-1)^{\frac{a-1}{2}\cdot(\text{偶})}=1$。

> 因此 $\left(\frac{a}{p}\right)=1\times1=1$。证毕。

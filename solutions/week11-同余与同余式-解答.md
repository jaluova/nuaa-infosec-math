# 习题 2 解答

## 1.

**(1)** 求 $47^{7385} \bmod 19$。

由欧拉定理，$\gcd(47,19)=1$，$\varphi(19)=18$，故 $47^{18} \equiv 1 \pmod{19}$。

$7385 = 410 \times 18 + 5$，所以 $47^{7385} \equiv 47^5 \pmod{19}$。

$47 \equiv 9 \pmod{19}$。计算 $9^5 \bmod 19$：
- $9^2 = 81 \equiv 5 \pmod{19}$
- $9^4 \equiv 5^2 = 25 \equiv 6 \pmod{19}$
- $9^5 \equiv 6 \times 9 = 54 \equiv 16 \pmod{19}$

> 余数为 **16**。

**(2)** 求 $47^{47^{47}}$ 的个位数字，即 $\bmod 10$。

$\varphi(10)=4$，$47 \equiv 7 \pmod{10}$。由欧拉定理 $7^4 \equiv 1 \pmod{10}$。

需计算 $47^{47} \bmod 4$。$47 \equiv 3 \pmod{4}$，$3^{\text{奇}} \equiv 3 \pmod{4}$。

$47$ 是奇数，故 $47^{47}$ 是奇数，$47^{47} \equiv 3 \pmod{4}$。

$7^{47^{47}} \equiv 7^3 \equiv 343 \equiv 3 \pmod{10}$。

> 个位数字为 **3**。

---

## 2.

今天星期一，求 $10^{10}$ 天后是星期几，即计算 $10^{10} \bmod 7$。

$10 \equiv 3 \pmod{7}$，$\varphi(7)=6$。由费马小定理 $3^6 \equiv 1 \pmod{7}$。

$10^{10} \equiv 3^{10} = 3^6 \times 3^4 \equiv 3^4 \pmod{7}$。

$3^2 \equiv 2$，$3^4 \equiv 2^2 = 4 \pmod{7}$。

星期一往后推 4 天 → **星期五**。

---

## 3.

写出模 6 的一组完全剩余系，其中每个数被 4 除都余 3。

需找 6 个整数 $a_0, \dots, a_5$ 满足 $a_i \equiv i \pmod{6}$ 且 $a_i \equiv 3 \pmod{4}$。

即解方程组：
$$\begin{cases} x \equiv i \pmod{6} \\ x \equiv 3 \pmod{4} \end{cases} \quad (i=0,1,\dots,5)$$

对偶数 $i$（$0,2,4$），$x \equiv i \pmod{6}$ 推出 $x \equiv 0 \pmod{2}$；而 $x \equiv 3 \pmod{4}$ 推出 $x \equiv 1 \pmod{2}$，矛盾。

> **不存在这样的完全剩余系。** 因为模 6 的偶数剩余类不能满足 $\equiv 3 \pmod{4}$ 的奇偶条件。

（注：若扩大搜索范围，仍不可能——所有 $\equiv 3 \pmod{4}$ 的数 mod 6 只落在 $\{1,3,5\}$，无法覆盖 $\{0,2,4\}$。）

---

## 4.

写出 12 的一个简化剩余系，要求每项都是 5 的倍数。

$\varphi(12)=4$，简化剩余系有 4 个数，与 12 互素。12 的简化剩余系代表元：$\{1,5,7,11\}$。

用中国剩余定理分别解 $x \equiv a \pmod{12}$，$x \equiv 0 \pmod{5}$（$a \in \{1,5,7,11\}$）：

| $a$ | $x \equiv a \pmod{12}$, $x \equiv 0 \pmod{5}$ | $x$ |
|-----|------|-----|
| 1 | $5k \equiv 1 \pmod{12}$，$k \equiv 5 \pmod{12}$ | 25 |
| 5 | $5k \equiv 5 \pmod{12}$，$k \equiv 1 \pmod{12}$ | 5 |
| 7 | $5k \equiv 7 \pmod{12}$，$k \equiv 11 \pmod{12}$ | 55 |
| 11 | $5k \equiv 11 \pmod{12}$，$k \equiv 7 \pmod{12}$ | 35 |

> 一组满足条件的简化剩余系：**$\{5, 25, 35, 55\}$**。

---

## 7.

设 $a$ 是正整数，$a<100$，且 $a^3+23 \equiv 0 \pmod{24}$，求 $a$。

$a^3 + 23 \equiv 0 \pmod{24} \iff a^3 \equiv 1 \pmod{24}$。

$24=8\times3$，分别解：

**模 8**：枚举 $0$~$7$，仅 $1^3 \equiv 1 \pmod{8}$，故 $a \equiv 1 \pmod{8}$。

**模 3**：由费马小定理 $a^3 \equiv a \pmod{3}$，需 $a \equiv 1 \pmod{3}$。

$\gcd(8,3)=1$，由 CRT 得 $a \equiv 1 \pmod{24}$。

$a<100$：$a = 1, 25, 49, 73, 97$。

> **$a = 1, 25, 49, 73, 97$**。

---

## 8.

证明：若 $p$ 为奇素数，则 $a^p+b^p \equiv (a+b)^p \pmod{p}$。

由二项式定理：
$$(a+b)^p = \sum_{k=0}^{p} \binom{p}{k} a^{p-k} b^k$$

当 $1 \le k \le p-1$ 时，$\binom{p}{k} = \dfrac{p!}{k!(p-k)!}$。$p$ 是素数，$k < p$ 且 $p-k < p$，故分母中不含因子 $p$，分子含因子 $p$，因此 $\binom{p}{k} \equiv 0 \pmod{p}$。

$$\therefore (a+b)^p \equiv \binom{p}{0}a^p + \binom{p}{p}b^p = a^p + b^p \pmod{p}$$

---

## 11.

计算欧拉函数：

- $\varphi(60)$：$60 = 2^2 \times 3 \times 5$，$\varphi(60) = 60 \times \frac{1}{2} \times \frac{2}{3} \times \frac{4}{5} = 16$
- $\varphi(100)$：$100 = 2^2 \times 5^2$，$\varphi(100) = 100 \times \frac{1}{2} \times \frac{4}{5} = 40$
- $\varphi(120)$：$120 = 2^3 \times 3 \times 5$，$\varphi(120) = 120 \times \frac{1}{2} \times \frac{2}{3} \times \frac{4}{5} = 32$
- $\varphi(288)$：$288 = 2^5 \times 3^2$，$\varphi(288) = 288 \times \frac{1}{2} \times \frac{2}{3} = 96$

> $\varphi(60)=16$，$\varphi(100)=40$，$\varphi(120)=32$，$\varphi(288)=96$。

---

## 15.

设 $m,n$ 为正整数，$\gcd(m,n)=1$，证明 $m^{\varphi(n)} + n^{\varphi(m)} \equiv 1 \pmod{mn}$。

由欧拉定理及 $\gcd(m,n)=1$：
$$m^{\varphi(n)} \equiv 1 \pmod{n}$$

又 $n^{\varphi(m)} \equiv 0 \pmod{n}$（显然 $n$ 整除自身），故：
$$m^{\varphi(n)} + n^{\varphi(m)} \equiv 1 + 0 = 1 \pmod{n}$$

同理：
$$m^{\varphi(n)} + n^{\varphi(m)} \equiv 0 + 1 = 1 \pmod{m}$$

由 $\gcd(m,n)=1$ 及中国剩余定理：
$$m^{\varphi(n)} + n^{\varphi(m)} \equiv 1 \pmod{mn}$$

---

## 17.

解下列同余方程组。

**(1)** $x \equiv 3 \pmod{11}$，$x \equiv 2 \pmod{72}$，$x \equiv 1 \pmod{13}$。

$M = 11 \times 72 \times 13 = 10296$。

$M_1 = 936$，$M_1^{-1} \pmod{11} \equiv 936^{-1} \equiv 1^{-1} \equiv 1$。
$M_2 = 143$，$M_2^{-1} \pmod{72} \equiv 143^{-1} \equiv (-1)^{-1} \equiv 71$。
$M_3 = 792$，$M_3^{-1} \pmod{13} \equiv 792^{-1} \equiv (-1)^{-1} \equiv 12$。

$x \equiv 3 \times 936 \times 1 + 2 \times 143 \times 71 + 1 \times 792 \times 12$
$\equiv 2808 + 20306 + 9504 \equiv 32618 \pmod{10296}$

$32618 \bmod 10296 = 1730$。

> $x \equiv 1730 \pmod{10296}$。

**(2)** $x \equiv 1 \pmod{2}$，$x \equiv 2 \pmod{5}$，$x \equiv 3 \pmod{7}$，$x \equiv 4 \pmod{9}$。

逐次代入：
- $x=2k+1$，代入第二个：$2k+1 \equiv 2 \pmod{5} \implies 2k \equiv 1 \implies k \equiv 3 \pmod{5}$。$x=2(5t+3)+1=10t+7$。
- 代入第三个：$10t+7 \equiv 3 \pmod{7} \implies 3t \equiv 3 \implies t \equiv 1 \pmod{7}$。$x=10(7s+1)+7=70s+17$。
- 代入第四个：$70s+17 \equiv 4 \pmod{9} \implies 7s+8 \equiv 4 \implies 7s \equiv 5 \pmod{9}$。$7^{-1} \equiv 4$，$s \equiv 4\times5=20\equiv 2 \pmod{9}$。
$x=70(9u+2)+17=630u+157$。

$M=2\times5\times7\times9=630$。

> $x \equiv 157 \pmod{630}$。

**(3)** $\begin{cases} 5x \equiv 1 \pmod{7} \\ 14x \equiv 2 \pmod{8} \end{cases}$

$5x \equiv 1 \pmod{7}$：$5^{-1}=3$，$x \equiv 3 \pmod{7}$。

$14x \equiv 2 \pmod{8}$：$14\equiv6$，$6x\equiv2 \pmod{8}$。约去 $\gcd(6,8,2)=2$：$3x\equiv1\pmod{4}$，$3^{-1}\equiv3$，$x\equiv3\pmod{4}$。

$x\equiv3\pmod{7}$，$x\equiv3\pmod{4}$，$\gcd(7,4)=1$。

> $x \equiv 3 \pmod{28}$。

**(4)** $\begin{cases} x \equiv 1 \pmod{7} \\ 3x \equiv 4 \pmod{5} \\ 8x \equiv 4 \pmod{9} \end{cases}$

$3x \equiv 4 \pmod{5}$：$3^{-1}=2$，$x \equiv 8 \equiv 3 \pmod{5}$。

$8x \equiv 4 \pmod{9}$：$8\equiv-1$，$-x\equiv4 \implies x\equiv5\pmod{9}$。

$x\equiv1\pmod{7}$，$x\equiv3\pmod{5}$，$x\equiv5\pmod{9}$。

- $x=7k+1$，$7k+1\equiv3\pmod{5}\implies2k\equiv2\implies k\equiv1$。$x=7(5t+1)+1=35t+8$。
- $35t+8\equiv5\pmod{9}\implies (-1)t+8\equiv5\implies t\equiv3\pmod{9}$。
$x=35(9u+3)+8=315u+113$。

> $x \equiv 113 \pmod{315}$。

---

## 18.

求出下列同余式的解数。

**(1)** $6x \equiv 48 \pmod{96}$。$\gcd(6,96)=6$，$6\mid48$。解数 $=6$。

**(2)** $10x \equiv 7 \pmod{65}$。$\gcd(10,65)=5$，$5\nmid7$。解数 $=0$。

**(3)** $9x \equiv 27 \pmod{96}$。$\gcd(9,96)=3$，$3\mid27$。解数 $=3$。

**(4)** $3x \equiv 11 \pmod{56}$。$\gcd(3,56)=1$。解数 $=1$。

**(5)** $21x \equiv 27 \pmod{35}$。$\gcd(21,35)=7$，$7\nmid27$。解数 $=0$。

**(6)** $x^3 + x - 5 \equiv 0 \pmod{15}$。$15=3\times5$。

- 模 3：$f(x)=x^3+x+1\pmod{3}$。$x=1$ 满足（$1+1+1=3\equiv0$）。1 个解。
- 模 5：$f(x)=x^3+x\pmod{5}$。$x=0,2,3$ 满足。3 个解。

总计 $1\times3=3$ 个解。

> (1) 6；(2) 0；(3) 3；(4) 1；(5) 0；(6) 3。

---

## 19.

解下列同余式。

**(1)** $17x \equiv 4 \pmod{19}$。

$\gcd(17,19)=1$。$17^{-1} \equiv 9$（因 $17\times9=153\equiv1\pmod{19}$）。$x \equiv 9\times4=36\equiv17\pmod{19}$。

> $x \equiv 17 \pmod{19}$。

**(2)** $45x \equiv 21 \pmod{132}$。

$\gcd(45,132)=3$，$3\mid21$。约去 3：$15x\equiv7\pmod{44}$。$\gcd(15,44)=1$。

$15^{-1}\equiv3\pmod{44}$。$x\equiv3\times7=21\pmod{44}$。

模 132 的三个解：$x \equiv 21, 65, 109 \pmod{132}$。

> $x \equiv 21, 65, 109 \pmod{132}$。

**(3)** $111x \equiv 75 \pmod{321}$。

$\gcd(111,321)=3$，$3\mid75$。约去 3：$37x\equiv25\pmod{107}$。$\gcd(37,107)=1$。

扩展欧几里得求 $37^{-1}\pmod{107}$：
$$107=2\times37+33,\; 37=1\times33+4,\; 33=8\times4+1$$
$$1=33-8\times4=33-8(37-33)=9\times33-8\times37=9(107-2\times37)-8\times37=9\times107-26\times37$$

$37^{-1}\equiv -26\equiv81\pmod{107}$。$x\equiv81\times25\equiv2025\equiv99\pmod{107}$。

模 321 的三个解：$x\equiv 99, 206, 313 \pmod{321}$。

> $x \equiv 99, 206, 313 \pmod{321}$。

**(4)** $6x^3+27x^2+17x+20\equiv0\pmod{30}$。$30=2\times3\times5$。

- 模 2：$x^2+x=x(x+1)\equiv0\pmod{2}$。解：$x\equiv0,1$（2 个）。
- 模 3：系数约化：$0x^3+0x^2+2x+2=2(x+1)\equiv0\pmod{3}$。解：$x\equiv2$（1 个）。
- 模 5：$x^3+2x^2+2x=x(x^2+2x+2)\equiv0\pmod{5}$。解：$x\equiv0,1,2$（3 个）。

共 $2\times1\times3=6$ 个解。用 CRT：
$x=15x_2+10\times2+6x_5\equiv15x_2+20+6x_5\pmod{30}$。

| $x_2$ | $x_5$ | $x$ |
|-------|-------|-----|
| 0 | 0 | 20 |
| 0 | 1 | 26 |
| 0 | 2 | 2 |
| 1 | 0 | 5 |
| 1 | 1 | 11 |
| 1 | 2 | 17 |

> $x \equiv 2, 5, 11, 17, 20, 26 \pmod{30}$。

**(5)** $x^4+2x^3+8x+9\equiv0\pmod{35}$。$35=5\times7$。

- 模 5：$x^4+2x^3+3x+4\equiv0\pmod{5}$。试 $x=0$~$4$：$x=1,4$ 成立。2 个解。
- 模 7：$x^4+2x^3+x+2\equiv0\pmod{7}$。试 $x=0$~$6$：$x=3,5,6$ 成立。3 个解。

共 6 个解。$M_5^{-1}\equiv3\pmod{5}$（$7\times3\equiv1$），$M_7^{-1}\equiv3\pmod{7}$（$5\times3\equiv1$）。
$x\equiv 7\times3\times x_5 + 5\times3\times x_7\equiv 21x_5+15x_7\pmod{35}$。

| $x_5$ | $x_7$ | $x$ |
|-------|-------|-----|
| 1 | 3 | $21+45\equiv31$ |
| 1 | 5 | $21+75\equiv26$ |
| 1 | 6 | $21+90\equiv6$ |
| 4 | 3 | $84+45\equiv24$ |
| 4 | 5 | $84+75\equiv19$ |
| 4 | 6 | $84+90\equiv34$ |

> $x \equiv 6, 19, 24, 26, 31, 34 \pmod{35}$。

**(6)** $x^4+7x+4\equiv0\pmod{27}$。$27=3^3$，用 Hensel 引理逐次提升。

模 3：$x^4+x+1\equiv0\pmod{3}$。$x\equiv1$（1 个解）。$f'(x)=4x^3+7$，$f'(1)=11\equiv2\not\equiv0\pmod{3}$，可唯一提升。

模 9：$x=1+3t$。$f(1)=12\equiv3\pmod{9}$，$f'(1)\cdot3t\equiv11\times3t=33t\equiv6t\pmod{9}$。
$3+6t\equiv0\pmod{9}\implies2t\equiv2\pmod{3}\implies t\equiv1$。$x=4\pmod{9}$。

模 27：$x=4+9t$。$f(4)=288\equiv18\pmod{27}$。
$f'(4)=263\equiv20\pmod{27}$，$f'(4)\cdot9t\equiv20\times9t=180t\equiv18t\pmod{27}$。
$18+18t\equiv0\pmod{27}\implies18(t+1)\equiv0\pmod{27}\implies t+1\equiv0\pmod{3}$。
$t\equiv2$。$x=4+9\times2=22$。

验证：$22\equiv-5\pmod{27}$，$(-5)^4=625\equiv4$，$7(-5)=-35\equiv19$，$4\equiv4$。$4+19+4=27\equiv0$。✓

> $x \equiv 22 \pmod{27}$。

**(7)** $x^5+5x^2+13x+42\equiv0\pmod{120}$。$120=8\times3\times5$。

- 模 8：$x^5+5x^2+5x+2\pmod{8}$。枚举 $0$~$7$，仅 $x=2$ 满足。1 个解。
- 模 3：$x^5+2x^2+x\pmod{3}$。枚举：$x=0,2$ 满足。2 个解。
- 模 5：$x^5+3x+2\pmod{5}$。由费马 $x^5\equiv x$，得 $4x+2\equiv0\implies4x\equiv3\implies x\equiv2\pmod{5}$。1 个解。

共 $1\times2\times1=2$ 个解。

$M_8=15$，$15^{-1}\equiv7\pmod{8}$；$M_3=40$，$40^{-1}\equiv1\pmod{3}$；$M_5=24$，$24^{-1}\equiv4\pmod{5}$。

$x\equiv15\times7\times2+40\times1\times x_3+24\times4\times2\equiv210+40x_3+192\pmod{120}$。

- $x_3=0$：$x\equiv402\equiv42\pmod{120}$
- $x_3=2$：$x\equiv210+80+192=482\equiv2\pmod{120}$

> $x \equiv 2, 42 \pmod{120}$。

---

## 20.

已知 $3441 = 3 \times 31 \times 37$，解 $71x \equiv 32 \pmod{3441}$。

$\gcd(71,3441)=1$（71 与 3,31,37 均互素），有唯一解。

扩展欧几里得求 $71^{-1}\pmod{3441}$：
$$\begin{aligned}
3441 &= 48 \times 71 + 33 \\
71 &= 2 \times 33 + 5 \\
33 &= 6 \times 5 + 3 \\
5 &= 1 \times 3 + 2 \\
3 &= 1 \times 2 + 1
\end{aligned}$$

回代：
$$\begin{aligned}
1 &= 3-2 = 3-(5-3)=2\times3-5 \\
  &= 2(33-6\times5)-5=2\times33-13\times5 \\
  &= 2\times33-13(71-2\times33)=28\times33-13\times71 \\
  &= 28(3441-48\times71)-13\times71 = 28\times3441-1357\times71
\end{aligned}$$

$71^{-1}\equiv-1357\equiv2084\pmod{3441}$。

$x\equiv2084\times32=66688\equiv1309\pmod{3441}$。

验证：$71\times1309=92939$，$92939\bmod3441=32$。✓

> $x \equiv 1309 \pmod{3441}$。

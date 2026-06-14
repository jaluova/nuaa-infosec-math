# 《信息安全数学基础》期末模拟 C 卷

**结构**：代数 3 题（第 1-3 题）+ 数论 7 题（第 4-10 题），满分 100 分。

---

## 一、代数部分（50 分）

### 1. 环的类型判定（15 分）

设 $A = \{a + bi \mid a, b \in \mathbb{Z}\}$（高斯整数环），在复数加法和乘法下：

(1) 证明 $A$ 构成一个环；
(2) 判断 $A$ 是含幺环、交换环、整环还是域，并给出理由。

---

### 2. 置换群的运算（20 分）

在 $S_6$ 中，设

$$\sigma = (1\ 2\ 3\ 4)(5\ 6),\qquad \tau = (1\ 5)(2\ 6)(3\ 4)$$

求：

(1) $\sigma\tau$ 和 $\tau\sigma$（写成不相交轮换之积）；
(2) $\sigma^{-1}$ 和 $\tau^{-1}$；
(3) $|\sigma|$、$|\tau|$、$|\sigma\tau|$、$|\tau\sigma|$；
(4) 解方程 $\sigma x = \tau$，并求 $|x|$。

---

### 3. 同态关系（15 分）

设 $\mathbb{Z}_6$ 为模 $6$ 加法群，$\mathbb{Z}_{15}$ 为模 $15$ 加法群。找出从 $\mathbb{Z}_6$ 到 $\mathbb{Z}_{15}$ 的**所有**群同态 $f$，写出每个同态的对应规则 $f(k)$ 及其像集 $\operatorname{Im}(f)$。

---

## 二、数论部分（50 分）

### 4. 不定方程（7 分）

求不定方程 $182x + 98y = 28$ 的一切整数解。

---

### 5. 欧拉定理 / 费马定理（7 分）

求 $2^{100}$ 除以 $21$ 的余数。

---

### 6. 剩余系（7 分）

写出模 $12$ 的一组完全剩余系，使得其中每个数被 $5$ 除都余 $3$。

---

### 7. 一次同余式组（7 分）

用孙子定理求解：

$$\begin{cases}
x \equiv 2 \pmod{3} \\[2pt]
x \equiv 3 \pmod{4} \\[2pt]
x \equiv 1 \pmod{5}
\end{cases}$$

---

### 8. 高次同余式（7 分）

解同余式：

$$x^3 + 2x^2 + 2 \equiv 0 \pmod{9}$$

---

### 9. 勒让德符号 / 雅可比符号（8 分）

计算：

$$(1)\ \left(\frac{13}{31}\right);\qquad (2)\ \left(\frac{55}{89}\right);\qquad (3)\ \left(\frac{15}{49}\right)$$

---

### 10. 二次同余式（7 分）

解同余式：

$$x^2 \equiv 3 \pmod{121}$$

---

## 参考答案

### 第 1 题

**(1) 证环**

任取 $x = a + bi$，$y = c + di \in A$。

- **加法封闭**：$x + y = (a + c) + (b + d)i \in A$
- **零元**：$0 = 0 + 0i \in A$
- **负元**：$-x = (-a) + (-b)i \in A$
- 加法结合律、交换律由复数继承，$(A, +)$ 为交换群。
- **乘法封闭**：$xy = (ac - bd) + (ad + bc)i \in A$
- 乘法结合律及分配律由复数继承。

故 $A$ 构成环。

**(2) 判断类型**

- **含幺环**：$1 = 1 + 0i \in A$，$1 \neq 0$。✓
- **交换环**：$xy = yx$，复数乘法交换。✓
- **整环**：若 $xy = 0$，由复数性质，$x = 0$ 或 $y = 0$。无零因子。✓
- **域？**：非零元 $a + bi$ 的逆元 $\dfrac{a - bi}{a^2 + b^2}$。取 $a = 1,\ b = 1$，逆元系数 $\frac{1}{2}, -\frac{1}{2} \notin \mathbb{Z}$。故非域。

> **结论**：$A$（高斯整数环）是**整环**，但不是域。

---

### 第 2 题

$\sigma = (1\ 2\ 3\ 4)(5\ 6)$：$1 \to 2 \to 3 \to 4 \to 1$，$5 \leftrightarrow 6$。
$\tau = (1\ 5)(2\ 6)(3\ 4)$：$1 \leftrightarrow 5$，$2 \leftrightarrow 6$，$3 \leftrightarrow 4$。

**(1) 复合**

$\sigma\tau = \sigma \circ \tau$：

| $x$ | $\tau(x)$ | $\sigma(\tau(x))$ |
|-----|-----------|-------------------|
| 1 | 5 | $\sigma(5) = 6$ |
| 6 | 2 | $\sigma(2) = 3$ |
| 3 | 4 | $\sigma(4) = 1$ |
| 2 | 6 | $\sigma(6) = 5$ |
| 5 | 1 | $\sigma(1) = 2$ |
| 4 | 3 | $\sigma(3) = 4$ |

$\sigma\tau = (1\ 6\ 3)(2\ 5)$

$\tau\sigma = \tau \circ \sigma$：

| $x$ | $\sigma(x)$ | $\tau(\sigma(x))$ |
|-----|-------------|-------------------|
| 1 | 2 | $\tau(2) = 6$ |
| 6 | 5 | $\tau(5) = 1$ |
| 2 | 3 | $\tau(3) = 4$ |
| 4 | 1 | $\tau(1) = 5$ |
| 5 | 6 | $\tau(6) = 2$ |
| 3 | 4 | $\tau(4) = 3$ |

$\tau\sigma = (1\ 6)(2\ 4\ 5)$

**(2) 逆元**

- $\sigma^{-1} = (1\ 2\ 3\ 4)^{-1}(5\ 6)^{-1} = (1\ 4\ 3\ 2)(5\ 6)$
- $\tau^{-1} = \tau = (1\ 5)(2\ 6)(3\ 4)$（对换之积的逆为自身）

**(3) 阶**

- $|\sigma| = \operatorname{lcm}(4, 2) = 4$
- $|\tau| = \operatorname{lcm}(2, 2, 2) = 2$
- $|\sigma\tau| = \operatorname{lcm}(3, 2) = 6$
- $|\tau\sigma| = \operatorname{lcm}(2, 3) = 6$

**(4) 解方程**

$\sigma x = \tau \implies x = \sigma^{-1}\tau$。

计算 $x = \sigma^{-1} \circ \tau$：

| $x$ | $\tau(x)$ | $\sigma^{-1}(\tau(x))$ |
|-----|-----------|------------------------|
| 1 | 5 | $\sigma^{-1}(5) = 6$ |
| 6 | 2 | $\sigma^{-1}(2) = 1$ |
| 2 | 6 | $\sigma^{-1}(6) = 5$ |
| 5 | 1 | $\sigma^{-1}(1) = 4$ |
| 4 | 3 | $\sigma^{-1}(3) = 2$ |
| 3 | 4 | $\sigma^{-1}(4) = 3$ |

$x = (1\ 6)(2\ 5\ 4)$

$|x| = \operatorname{lcm}(2, 3) = 6$。

---

### 第 3 题

$f: \mathbb{Z}_6 \to \mathbb{Z}_{15}$，由 $f(1)$ 完全确定：$f(k) \equiv k \cdot f(1) \pmod{15}$。

约束：$6 \cdot f(1) \equiv 0 \pmod{15}$，即 $15 \mid 6f(1) \iff 5 \mid 2f(1)$。

$\gcd(5, 2) = 1$，故 $5 \mid f(1)$。$f(1) \in \{0, 5, 10\}$。共 3 个同态。

**$f_0$**：$f(1) = 0$

| $k$ | 0 | 1 | 2 | 3 | 4 | 5 |
|-----|---|---|---|---|---|---|
| $f_0(k)$ | 0 | 0 | 0 | 0 | 0 | 0 |

$\operatorname{Im}(f_0) = \{0\}$（平凡同态）

**$f_5$**：$f(1) = 5$

| $k$ | 0 | 1 | 2 | 3 | 4 | 5 |
|-----|---|---|---|---|---|---|
| $f_5(k)$ | 0 | 5 | 10 | 0 | 5 | 10 |

$\operatorname{Im}(f_5) = \{0, 5, 10\} \cong \mathbb{Z}_3$

**$f_{10}$**：$f(1) = 10$

| $k$ | 0 | 1 | 2 | 3 | 4 | 5 |
|-----|---|---|---|---|---|---|
| $f_{10}(k)$ | 0 | 10 | 5 | 0 | 10 | 5 |

$\operatorname{Im}(f_{10}) = \{0, 5, 10\} \cong \mathbb{Z}_3$

---

### 第 4 题

$182x + 98y = 28$

辗转相除：
$$\begin{aligned}
182 &= 1 \times 98 + 84 \\
98 &= 1 \times 84 + 14 \\
84 &= 6 \times 14 + 0
\end{aligned}$$

$\gcd(182, 98) = 14$，且 $14 \mid 28$，有解。

约简：$13x + 7y = 2$。

扩展欧几里得：
$$\begin{aligned}
13 &= 1 \times 7 + 6 \\
7 &= 1 \times 6 + 1
\end{aligned}$$

回溯：$1 = 7 - 6 = 7 - (13 - 7) = 2 \times 7 - 13$。

即 $13 \times (-1) + 7 \times 2 = 1$。乘以 $2$：$13 \times (-2) + 7 \times 4 = 2$。

特解 $(x_0, y_0) = (-2, 4)$。

通解：
$$\boxed{x = -2 + 7t,\quad y = 4 - 13t \qquad (t \in \mathbb{Z})}$$

---

### 第 5 题

求 $2^{100} \bmod 21$。

$\gcd(2, 21) = 1$，$\varphi(21) = \varphi(3) \times \varphi(7) = 2 \times 6 = 12$。

由欧拉定理：$2^{12} \equiv 1 \pmod{21}$。

$100 = 8 \times 12 + 4$，故 $2^{100} \equiv 2^4 = 16 \pmod{21}$。

> **余数为 16**。

---

### 第 6 题

需找 $a_0, a_1, \dots, a_{11}$ 满足 $a_i \equiv i \pmod{12}$ 且 $a_i \equiv 3 \pmod{5}$。

即解 $x \equiv i \pmod{12},\ x \equiv 3 \pmod{5}$（$i = 0, \dots, 11$）。

模 $60$ 下：$M_1 = 5$，$M_2 = 12$。

$5^{-1} \bmod 12 = 5$（$5 \times 5 = 25 \equiv 1$），$12^{-1} \bmod 5 = 3$（$12 \equiv 2$，$2^{-1} = 3$）。

$x \equiv 5 \times 5 \times i + 12 \times 3 \times 3 \equiv 25i + 108 \equiv 25i + 48 \pmod{60}$。

对各 $i$ 取最小正解：

| $i$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 |
|-----|---|---|---|---|---|---|---|---|---|---|----|----|
| $a_i$ | 48 | 13 | 38 | 3 | 28 | 53 | 18 | 43 | 8 | 33 | 58 | 23 |

排序后：
> $\boxed{\{3,\ 8,\ 13,\ 18,\ 23,\ 28,\ 33,\ 38,\ 43,\ 48,\ 53,\ 58\}}$

验证：均为完全剩余系 mod 12，且均 $\equiv 3 \pmod{5}$ ✓。

---

### 第 7 题

$M = 3 \times 4 \times 5 = 60$。

$$\begin{aligned}
M_1 &= 20, & 20^{-1} \bmod 3 &: 20 \equiv 2,\ 2^{-1} = 2 \\
M_2 &= 15, & 15^{-1} \bmod 4 &: 15 \equiv 3,\ 3^{-1} = 3 \\
M_3 &= 12, & 12^{-1} \bmod 5 &: 12 \equiv 2,\ 2^{-1} = 3
\end{aligned}$$

$$\begin{aligned}
x &\equiv 2 \times 20 \times 2 + 3 \times 15 \times 3 + 1 \times 12 \times 3 \\
  &= 80 + 135 + 36 = 251 \\
  &\equiv 251 - 60 \times 4 = 251 - 240 = 11 \pmod{60}
\end{aligned}$$

> $\boxed{x \equiv 11 \pmod{60}}$

验算：$11 \bmod 3 = 2$ ✓；$11 \bmod 4 = 3$ ✓；$11 \bmod 5 = 1$ ✓。

---

### 第 8 题

$x^3 + 2x^2 + 2 \equiv 0 \pmod{9}$。

枚举 $x = 0, 1, \dots, 8$：

| $x$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|-----|---|---|---|---|---|---|---|---|---|
| $x^3+2x^2+2 \bmod 9$ | 2 | 5 | 0 | 2 | 8 | 6 | 2 | 2 | 3 |

仅 $x = 2$ 满足。

验证 $f'(x) = 3x^2 + 4x$，$f'(2) = 12 + 8 = 20 \equiv 2 \pmod{3}$。

$f'(2) \not\equiv 0 \pmod{3}$，由 Hensel 引理，解可唯一提升到模 $3^k$。本题模 $9 = 3^2$，$x = 2$ 即为全部解。

> $\boxed{x \equiv 2 \pmod{9}}$

验算：$2^3 + 2 \times 2^2 + 2 = 8 + 8 + 2 = 18 \equiv 0 \pmod{9}$ ✓。

---

### 第 9 题

**(1)** $\left(\dfrac{13}{31}\right)$

$13 \equiv 1 \pmod{4}$，故 $\left(\dfrac{13}{31}\right) = \left(\dfrac{31}{13}\right) = \left(\dfrac{5}{13}\right)$。

$5 \equiv 1 \pmod{4}$，故 $\left(\dfrac{5}{13}\right) = \left(\dfrac{13}{5}\right) = \left(\dfrac{3}{5}\right)$。

$3 \equiv 3$，$5 \equiv 1 \pmod{4}$，故 $\left(\dfrac{3}{5}\right) = \left(\dfrac{5}{3}\right) = \left(\dfrac{2}{3}\right) = -1$。

> (1) $\boxed{-1}$

**(2)** $\left(\dfrac{55}{89}\right)$

$55 = 5 \times 11$。$\left(\dfrac{55}{89}\right) = \left(\dfrac{5}{89}\right)\left(\dfrac{11}{89}\right)$。

- $\left(\frac{5}{89}\right)$：$5 \equiv 1 \pmod{4}$，$= \left(\frac{89}{5}\right) = \left(\frac{4}{5}\right) = 1$。
- $\left(\frac{11}{89}\right)$：$11 \equiv 3$，$89 \equiv 1 \pmod{4}$，$= \left(\frac{89}{11}\right) = \left(\frac{1}{11}\right) = 1$。

> (2) $\boxed{1}$

**(3)** $\left(\dfrac{15}{49}\right)$（雅可比符号）

$49 = 7^2$，为完全平方数。$\gcd(15, 49) = 1$。

对于雅可比符号，$\left(\dfrac{15}{49}\right) = \left(\dfrac{15}{7}\right)^2 = 1$。

（因为 $\left(\dfrac{a}{p^k}\right) = \left(\dfrac{a}{p}\right)^k$，而 $\left(\dfrac{15}{7}\right) = \left(\dfrac{1}{7}\right) = 1$。）

> (3) $\boxed{1}$

---

### 第 10 题

$x^2 \equiv 3 \pmod{121}$，$121 = 11^2$。

**Step 1** — 先解模 $11$：$x^2 \equiv 3 \pmod{11}$。

$\left(\dfrac{3}{11}\right)$：$3 \equiv 3$，$11 \equiv 3 \pmod{4}$。$= -\left(\dfrac{11}{3}\right) = -\left(\dfrac{2}{3}\right) = -(-1) = 1$。有解。

枚举：$5^2 = 25 \equiv 3$，$6^2 = 36 \equiv 3 \pmod{11}$。$x \equiv 5, 6 \pmod{11}$。2 个解。

**Step 2** — Hensel 提升到模 $121$。

设 $f(x) = x^2 - 3$，$f'(x) = 2x$。

**从 $x_0 = 5$ 提升**：$f(5) = 25 - 3 = 22$。设 $x = 5 + 11t$。

$f(5 + 11t) \equiv f(5) + f'(5) \times 11t \equiv 22 + 10 \times 11t = 11(2 + 10t) \equiv 0 \pmod{121}$。

$2 + 10t \equiv 0 \pmod{11} \implies 10t \equiv 9 \pmod{11}$。

$10^{-1} \bmod 11 = 10$，$t \equiv 10 \times 9 = 90 \equiv 2 \pmod{11}$。

$x = 5 + 11 \times 2 = 27$。

**从 $x_0 = 6$ 提升**：$f(6) = 36 - 3 = 33$。设 $x = 6 + 11t$。

$f(6 + 11t) \equiv 33 + 12 \times 11t = 11(3 + 12t) \equiv 0 \pmod{121}$。

$3 + 12t \equiv 0 \pmod{11} \implies 12t \equiv 8 \pmod{11} \implies t \equiv 8$。

$x = 6 + 11 \times 8 = 94$。

> $\boxed{x \equiv 27,\ 94 \pmod{121}}$

验算：$27^2 = 729 = 121 \times 6 + 3$ ✓；$94^2 = 8836 = 121 \times 73 + 3$ ✓。

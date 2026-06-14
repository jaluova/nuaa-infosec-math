# 《信息安全数学基础》期末模拟 B 卷

**结构**：代数 3 题（第 1-3 题）+ 数论 7 题（第 4-10 题），满分 100 分。

---

## 一、代数部分（50 分）

### 1. 环的类型判定（15 分）

考虑 $\mathbb{Z}_{15}$ 在模 $15$ 加法和模 $15$ 乘法下：

(1) 证明 $\mathbb{Z}_{15}$ 是一个含幺交换环；
(2) 求出 $\mathbb{Z}_{15}$ 中的**所有零因子**；
(3) $\mathbb{Z}_{15}$ 是整环吗？是域吗？说明理由。

---

### 2. 置换群的运算（20 分）

在 $S_4$ 中，设

$$\sigma = (1\ 2\ 3),\qquad \tau = (1\ 4)(2\ 3)$$

求：

(1) $\sigma\tau$ 和 $\tau\sigma$（写成不相交轮换之积）；
(2) $\sigma^{-1}$ 和 $\tau^{-1}$；
(3) $|\sigma|$、$|\tau|$、$|\sigma\tau|$、$|\tau\sigma|$；
(4) 解方程 $\tau x = \sigma$，并求 $|x|$。

---

### 3. 同态关系（15 分）

设 $\mathbb{Z}_4$ 为模 $4$ 加法群，$\mathbb{Z}_{12}$ 为模 $12$ 加法群。找出从 $\mathbb{Z}_4$ 到 $\mathbb{Z}_{12}$ 的**所有**群同态 $f$，写出每个同态的对应规则 $f(k)$ ($k = 0, 1, 2, 3$) 及其像集 $\operatorname{Im}(f)$。

---

## 二、数论部分（50 分）

### 4. 不定方程（7 分）

求不定方程 $196x + 91y = 14$ 的一切整数解。

---

### 5. 欧拉定理（7 分）

求 $3^{3^{3}}$ 除以 $11$ 的余数。

---

### 6. 剩余系（7 分）

写出模 $10$ 的一组**简化剩余系**，使得其中每个数被 $3$ 除都余 $2$。

---

### 7. 一次同余式组（7 分）

用孙子定理求解：

$$\begin{cases}
x \equiv 1 \pmod{4} \\[2pt]
x \equiv 2 \pmod{5} \\[2pt]
x \equiv 3 \pmod{7}
\end{cases}$$

---

### 8. 高次同余式（7 分）

解同余式：

$$x^3 + x + 2 \equiv 0 \pmod{15}$$

---

### 9. 勒让德符号 / 雅可比符号（8 分）

计算：

$$(1)\ \left(\frac{17}{29}\right);\qquad (2)\ \left(\frac{28}{41}\right);\qquad (3)\ \left(\frac{26}{65}\right)$$

---

### 10. 二次同余式（7 分）

解同余式：

$$x^2 \equiv 2 \pmod{49}$$

---

## 参考答案

### 第 1 题

**(1)** $\mathbb{Z}_{15}$ 的加法和乘法继承整数环的性质。加法单位元为 $0$，乘法单位元为 $1$（$1 \neq 0$），乘法和加法均满足交换律。故 $\mathbb{Z}_{15}$ 是**含幺交换环**。

**(2)** $a \neq 0$ 为零因子当且仅当 $\gcd(a, 15) > 1$。与 $15 = 3 \times 5$ 不互素的非零元素：

$$\boxed{3,\ 5,\ 6,\ 9,\ 10,\ 12}$$

验证：$3 \times 5 = 15 \equiv 0$，$6 \times 5 = 30 \equiv 0$，$9 \times 5 = 45 \equiv 0$，$10 \times 3 = 30 \equiv 0$，$12 \times 5 = 60 \equiv 0$。

**(3)** $\mathbb{Z}_{15}$ 有零因子（如 $3 \times 5 = 0$），故**不是整环**。整环都不成立，自然也**不是域**。

> $\mathbb{Z}_n$ 是整环 $\iff$ $\mathbb{Z}_n$ 是域 $\iff$ $n$ 为素数。$15$ 为合数，故 $\mathbb{Z}_{15}$ 仅是一个**含幺交换环**。

---

### 第 2 题

$\sigma = (1\ 2\ 3)$，$\tau = (1\ 4)(2\ 3)$。

**(1) 复合**

$\sigma\tau = \sigma \circ \tau$（先 $\tau$ 后 $\sigma$）：

| $x$ | $\tau(x)$ | $\sigma(\tau(x))$ |
|-----|-----------|-------------------|
| 1 | 4 | $\sigma(4) = 4$ |
| 4 | 1 | $\sigma(1) = 2$ |
| 2 | 3 | $\sigma(3) = 1$ |
| 3 | 2 | $\sigma(2) = 3$ |

$\sigma\tau = (1\ 4\ 2)$

$\tau\sigma = \tau \circ \sigma$（先 $\sigma$ 后 $\tau$）：

| $x$ | $\sigma(x)$ | $\tau(\sigma(x))$ |
|-----|-------------|-------------------|
| 1 | 2 | $\tau(2) = 3$ |
| 3 | 1 | $\tau(1) = 4$ |
| 4 | 4 | $\tau(4) = 1$ |
| 2 | 3 | $\tau(3) = 2$ |

$\tau\sigma = (1\ 3\ 4)$

**(2) 逆元**

- $\sigma^{-1} = (1\ 2\ 3)^{-1} = (1\ 3\ 2)$
- $\tau^{-1} = \tau = (1\ 4)(2\ 3)$（对换之积的逆为自身）

**(3) 阶**

- $|\sigma| = 3$（3-轮换）
- $|\tau| = \operatorname{lcm}(2, 2) = 2$
- $|\sigma\tau| = |(1\ 4\ 2)| = 3$
- $|\tau\sigma| = |(1\ 3\ 4)| = 3$

**(4) 解方程**

$\tau x = \sigma \implies x = \tau^{-1}\sigma = \tau\sigma$（因为 $\tau^{-1} = \tau$）。

故 $x = \tau\sigma = (1\ 3\ 4)$。

$|x| = 3$。

> $\boxed{x = (1\ 3\ 4),\ |x| = 3}$

---

### 第 3 题

设 $f: \mathbb{Z}_4 \to \mathbb{Z}_{12}$ 为群同态，$f$ 由 $f(1)$ 完全确定：$f(k) \equiv k \cdot f(1) \pmod{12}$。

约束条件：$4 \cdot f(1) \equiv 0 \pmod{12}$，即 $12 \mid 4f(1) \iff 3 \mid f(1)$。

故 $f(1) \in \{0, 3, 6, 9\}$，共 4 个同态：

**$f_0$**：$f(1) = 0$

| $k$ | 0 | 1 | 2 | 3 |
|-----|---|---|---|---|
| $f_0(k)$ | 0 | 0 | 0 | 0 |

$\operatorname{Im}(f_0) = \{0\}$（平凡同态）

**$f_3$**：$f(1) = 3$

| $k$ | 0 | 1 | 2 | 3 |
|-----|---|---|---|---|
| $f_3(k)$ | 0 | 3 | 6 | 9 |

$\operatorname{Im}(f_3) = \{0, 3, 6, 9\} \cong \mathbb{Z}_4$

**$f_6$**：$f(1) = 6$

| $k$ | 0 | 1 | 2 | 3 |
|-----|---|---|---|---|
| $f_6(k)$ | 0 | 6 | 0 | 6 |

$\operatorname{Im}(f_6) = \{0, 6\} \cong \mathbb{Z}_2$

**$f_9$**：$f(1) = 9$

| $k$ | 0 | 1 | 2 | 3 |
|-----|---|---|---|---|
| $f_9(k)$ | 0 | 9 | 6 | 3 |

$\operatorname{Im}(f_9) = \{0, 3, 6, 9\} \cong \mathbb{Z}_4$

---

### 第 4 题

$196x + 91y = 14$

辗转相除：
$$\begin{aligned}
196 &= 2 \times 91 + 14 \\
91 &= 6 \times 14 + 7 \\
14 &= 2 \times 7 + 0
\end{aligned}$$

$\gcd(196, 91) = 7$，且 $7 \mid 14$，有解。

约简：$28x + 13y = 2$。

扩展欧几里得：
$$\begin{aligned}
28 &= 2 \times 13 + 2 \\
13 &= 6 \times 2 + 1
\end{aligned}$$

回溯：$1 = 13 - 6 \times 2 = 13 - 6(28 - 2 \times 13) = 13 \times 13 - 6 \times 28$。

乘以 $2$：$2 = 26 \times 13 - 12 \times 28$，即 $28 \times (-12) + 13 \times 26 = 2$。

特解 $(x_0, y_0) = (-12, 26)$。

通解：
$$\boxed{x = -12 + 13t,\quad y = 26 - 28t \qquad (t \in \mathbb{Z})}$$

---

### 第 5 题

求 $3^{3^3} \bmod 11$。

$3^3 = 27$，需求 $3^{27} \bmod 11$。

$\gcd(3, 11) = 1$，$\varphi(11) = 10$。由欧拉定理：$3^{10} \equiv 1 \pmod{11}$。

$27 = 2 \times 10 + 7$，故 $3^{27} \equiv 3^7 \pmod{11}$。

$$\begin{aligned}
3^2 &\equiv 9 \pmod{11} \\
3^4 &\equiv 9^2 = 81 \equiv 4 \pmod{11} \\
3^6 &\equiv 3^4 \times 3^2 \equiv 4 \times 9 = 36 \equiv 3 \pmod{11} \\
3^7 &\equiv 3^6 \times 3 \equiv 3 \times 3 = 9 \pmod{11}
\end{aligned}$$

> **余数为 9**。

---

### 第 6 题

模 $10$ 的标准简化剩余系（与 $10$ 互素）：$\{1, 3, 7, 9\}$。需要 $4$ 个数，每个 $\equiv 2 \pmod{3}$。

分别解 $x \equiv a \pmod{10}$，$x \equiv 2 \pmod{3}$（$a \in \{1, 3, 7, 9\}$）：

- $a = 1$：$x = 10k + 1 \equiv 2 \pmod{3} \implies k + 1 \equiv 2 \implies k \equiv 1$。$x = 11$。
- $a = 3$：$x = 10k + 3 \equiv 2 \pmod{3} \implies k \equiv 2$。$x = 23$。
- $a = 7$：$x = 10k + 7 \equiv 2 \pmod{3} \implies k + 1 \equiv 2 \implies k \equiv 1$。$x = 17$。
- $a = 9$：$x = 10k + 9 \equiv 2 \pmod{3} \implies k \equiv 2$。$x = 29$。

> 简化剩余系：$\boxed{\{11,\ 17,\ 23,\ 29\}}$

验证：均与 $10$ 互素 ✓；$11 \equiv 17 \equiv 23 \equiv 29 \equiv 2 \pmod{3}$ ✓。

---

### 第 7 题

$M = 4 \times 5 \times 7 = 140$。

$$\begin{aligned}
M_1 &= 35, & 35^{-1} \bmod 4 &: 35 \equiv 3,\ 3^{-1} = 3\ (3 \times 3 = 9 \equiv 1) \\
M_2 &= 28, & 28^{-1} \bmod 5 &: 28 \equiv 3,\ 3^{-1} = 2 \\
M_3 &= 20, & 20^{-1} \bmod 7 &: 20 \equiv 6 \equiv -1,\ 6^{-1} = 6
\end{aligned}$$

$$\begin{aligned}
x &\equiv 1 \times 35 \times 3 + 2 \times 28 \times 2 + 3 \times 20 \times 6 \\
  &= 105 + 112 + 360 = 577 \\
  &\equiv 577 - 140 \times 4 = 577 - 560 = 17 \pmod{140}
\end{aligned}$$

> $\boxed{x \equiv 17 \pmod{140}}$

验算：$17 \bmod 4 = 1$ ✓；$17 \bmod 5 = 2$ ✓；$17 \bmod 7 = 3$ ✓。

---

### 第 8 题

$x^3 + x + 2 \equiv 0 \pmod{15}$，$15 = 3 \times 5$。

**模 3**：由费马小定理 $x^3 \equiv x \pmod{3}$，原式化为 $x + x + 2 = 2x + 2 = 2(x+1) \equiv 0 \pmod{3}$，得 $x \equiv 2 \pmod{3}$。1 个解。

**模 5**：枚举：

| $x$ | 0 | 1 | 2 | 3 | 4 |
|-----|---|---|---|---|---|
| $x^3+x+2 \bmod 5$ | 2 | 4 | 2 | 2 | 0 |

$x \equiv 4 \pmod{5}$。1 个解。

共 1 个解。合并：$x = 3k + 2$，$3k + 2 \equiv 4 \pmod{5} \implies 3k \equiv 2 \pmod{5}$。

$3^{-1} \bmod 5 = 2$，$k \equiv 2 \times 2 = 4 \pmod{5}$。

$x = 3(5t + 4) + 2 = 15t + 14$。

> $\boxed{x \equiv 14 \pmod{15}}$

验算：$14^3 = 2744$，$2744 \bmod 15 = 14$，$14 + 14 + 2 = 30 \equiv 0$ ✓。

---

### 第 9 题

**(1)** $\left(\dfrac{17}{29}\right)$

$17 \equiv 1 \pmod{4}$，故 $\left(\dfrac{17}{29}\right) = \left(\dfrac{29}{17}\right) = \left(\dfrac{12}{17}\right) = \left(\dfrac{4}{17}\right)\left(\dfrac{3}{17}\right) = 1 \times \left(\dfrac{3}{17}\right)$。

$3 \equiv 3$，$17 \equiv 1 \pmod{4}$，故 $\left(\dfrac{3}{17}\right) = \left(\dfrac{17}{3}\right) = \left(\dfrac{2}{3}\right) = -1$。

> (1) $\boxed{-1}$

**(2)** $\left(\dfrac{28}{41}\right)$

$28 = 4 \times 7$。$\left(\dfrac{28}{41}\right) = \left(\dfrac{4}{41}\right)\left(\dfrac{7}{41}\right) = 1 \times \left(\dfrac{7}{41}\right)$。

$7 \equiv 3$，$41 \equiv 1 \pmod{4}$，故 $\left(\dfrac{7}{41}\right) = \left(\dfrac{41}{7}\right) = \left(\dfrac{6}{7}\right) = \left(\dfrac{2}{7}\right)\left(\dfrac{3}{7}\right)$。

- $\left(\frac{2}{7}\right)$：$7 \equiv -1 \pmod{8}$，$= 1$。
- $\left(\frac{3}{7}\right)$：$3 \equiv 7 \equiv 3 \pmod{4}$，$= -\left(\frac{7}{3}\right) = -\left(\frac{1}{3}\right) = -1$。

故 $\left(\frac{7}{41}\right) = 1 \times (-1) = -1$。

> (2) $\boxed{-1}$

**(3)** $\left(\dfrac{26}{65}\right)$（雅可比符号）

$\gcd(26, 65) = 13 \neq 1$。

> (3) $\boxed{0}$

---

### 第 10 题

$x^2 \equiv 2 \pmod{49}$，$49 = 7^2$。

**Step 1** — 先解模 $7$：$x^2 \equiv 2 \pmod{7}$。

枚举：$1^2 = 1$，$2^2 = 4$，$3^2 = 9 \equiv 2$，$4^2 \equiv 2$，$5^2 \equiv 4$，$6^2 \equiv 1$。

$x \equiv 3, 4 \pmod{7}$。2 个解。$\left(\frac{2}{7}\right) = 1$ ✓。

**Step 2** — Hensel 提升到模 $49$。

设 $f(x) = x^2 - 2$，$f'(x) = 2x$。

**从 $x_0 = 3$ 提升**：$f(3) = 9 - 2 = 7$。设 $x = 3 + 7t$。

$f(3 + 7t) \equiv f(3) + f'(3) \cdot 7t \equiv 7 + 6 \times 7t = 7(1 + 6t) \equiv 0 \pmod{49}$。

$1 + 6t \equiv 0 \pmod{7} \implies 6t \equiv 6 \pmod{7} \implies t \equiv 1$。

$x = 3 + 7 \times 1 = 10$。

**从 $x_0 = 4$ 提升**：$f(4) = 16 - 2 = 14$。设 $x = 4 + 7t$。

$f(4 + 7t) \equiv 14 + 8 \times 7t = 7(2 + 8t) \equiv 0 \pmod{49}$。

$2 + 8t \equiv 0 \pmod{7} \implies 2 + t \equiv 0 \implies t \equiv 5$。

$x = 4 + 7 \times 5 = 39$。

> $\boxed{x \equiv 10,\ 39 \pmod{49}}$

验算：$10^2 = 100 = 49 \times 2 + 2$ ✓；$39^2 = 1521 = 49 \times 31 + 2$ ✓。

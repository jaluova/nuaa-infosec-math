# 《信息安全数学基础》期末模拟 A 卷

**结构**：代数 3 题（第 1-3 题）+ 数论 7 题（第 4-10 题），满分 100 分。

---

## 一、代数部分（50 分）

### 1. 环的类型判定（15 分）

设 $A = \{a + b\sqrt{5} \mid a, b \in \mathbb{Z}\}$，在通常实数的加法和乘法下：

(1) 证明 $A$ 构成一个环；
(2) 进一步判断 $A$ 是含幺环、交换环、整环还是域，并给出理由。

---

### 2. 置换群的运算（20 分）

在 $S_5$ 中，设

$$\sigma = (1\ 3\ 5)(2\ 4),\qquad \tau = (1\ 2\ 5\ 4\ 3)$$

求：

(1) $\sigma\tau$ 和 $\tau\sigma$（写成不相交轮换之积）；
(2) $\sigma^{-1}$ 和 $\tau^{-1}$；
(3) $|\sigma|$、$|\tau|$、$|\sigma\tau|$、$|\tau\sigma|$；
(4) 解方程 $\sigma x = \tau$，并求 $|x|$。

---

### 3. 同态关系（15 分）

设 $K_4 = \{e, a, b, c\}$ 为 Klein 四元群（$a^2 = b^2 = c^2 = e$，$ab = c = ba$），$\mathbb{Z}_8$ 为模 $8$ 加法群。找出从 $K_4$ 到 $\mathbb{Z}_8$ 的**所有**群同态，写出每个同态映射的完整对应表。

---

## 二、数论部分（50 分）

### 4. 不定方程（7 分）

求不定方程 $231x + 105y = 42$ 的一切整数解。

---

### 5. 欧拉定理（7 分）

求 $5^{2025}$ 除以 $17$ 的余数。

---

### 6. 剩余系（7 分）

写出模 $9$ 的一组完全剩余系，使得其中每个数被 $4$ 除都余 $1$。

---

### 7. 一次同余式组（7 分）

用孙子定理求解：

$$\begin{cases}
x \equiv 2 \pmod{5} \\[2pt]
x \equiv 3 \pmod{7} \\[2pt]
x \equiv 4 \pmod{9}
\end{cases}$$

---

### 8. 高次同余式（7 分）

解同余式：

$$x^3 + 3x + 1 \equiv 0 \pmod{21}$$

---

### 9. 勒让德符号（8 分）

计算下列勒让德符号：

$$(1)\ \left(\frac{19}{23}\right);\qquad (2)\ \left(\frac{39}{17}\right);\qquad (3)\ \left(\frac{105}{59}\right)$$

---

### 10. 二次同余式（7 分）

判断同余式 $x^2 \equiv 4 \pmod{35}$ 解的个数，并求出所有解。

---

## 参考答案

### 第 1 题

**(1) 证环**

任取 $x = a + b\sqrt{5}$，$y = c + d\sqrt{5} \in A$。

- **加法封闭**：$x + y = (a + c) + (b + d)\sqrt{5} \in A$
- **零元**：$0 = 0 + 0\sqrt{5} \in A$
- **负元**：$-x = (-a) + (-b)\sqrt{5} \in A$
- 加法结合律、交换律由实数继承，故 $(A, +)$ 为交换群。
- **乘法封闭**：$xy = (ac + 5bd) + (ad + bc)\sqrt{5} \in A$
- 乘法结合律及分配律由实数继承。

故 $A$ 构成一个环。

**(2) 判断类型**

- **含幺环**：单位元 $1 = 1 + 0\sqrt{5} \in A$，且 $1 \neq 0$。✓
- **交换环**：乘法交换，$xy = yx$。✓
- **整环**：若 $(a+b\sqrt{5})(c+d\sqrt{5}) = 0$，由 $\sqrt{5}$ 为无理数，乘积为零当且仅当 $a=b=0$ 或 $c=d=0$。故无零因子，是整环。✓
- **域？**：非零元 $a + b\sqrt{5}$ 的乘法逆元为 $\dfrac{a-b\sqrt{5}}{a^2-5b^2}$。取 $a=1,\ b=1$，分母 $1-5=-4$，逆元系数为 $\frac{1}{4}, -\frac{1}{4} \notin \mathbb{Z}$。故逆元不一定在 $A$ 中。

> **结论**：$A$ 是**整环**（含幺交换环 + 无零因子），但不是域。

---

### 第 2 题

$\sigma = (1\ 3\ 5)(2\ 4)$，$\tau = (1\ 2\ 5\ 4\ 3)$。

**(1) 复合**

$\sigma\tau = \sigma \circ \tau$（先 $\tau$ 后 $\sigma$）：

| $x$ | $\tau(x)$ | $\sigma(\tau(x))$ |
|-----|-----------|-------------------|
| 1 | 2 | $\sigma(2) = 4$ |
| 2 | 5 | $\sigma(5) = 1$ |
| 3 | 1 | $\sigma(1) = 3$ |
| 4 | 3 | $\sigma(3) = 5$ |
| 5 | 4 | $\sigma(4) = 2$ |

$\sigma\tau = (1\ 4\ 5\ 2)$

$\tau\sigma = \tau \circ \sigma$（先 $\sigma$ 后 $\tau$）：

| $x$ | $\sigma(x)$ | $\tau(\sigma(x))$ |
|-----|-------------|-------------------|
| 1 | 3 | $\tau(3) = 1$ |
| 2 | 4 | $\tau(4) = 3$ |
| 3 | 5 | $\tau(5) = 4$ |
| 4 | 2 | $\tau(2) = 5$ |
| 5 | 1 | $\tau(1) = 2$ |

$\tau\sigma = (2\ 3\ 4\ 5)$

**(2) 逆元**

- $\sigma^{-1} = (1\ 3\ 5)^{-1}(2\ 4)^{-1} = (1\ 5\ 3)(2\ 4)$
- $\tau^{-1}$：将 $\tau = (1\ 2\ 5\ 4\ 3)$ 倒写，得 $\tau^{-1} = (1\ 3\ 4\ 5\ 2)$

**(3) 阶**

- $|\sigma| = \operatorname{lcm}(3, 2) = 6$
- $|\tau| = 5$（5-轮换）
- $|\sigma\tau| = 4$（4-轮换）
- $|\tau\sigma| = 4$（4-轮换）

**(4) 解方程**

$\sigma x = \tau \implies x = \sigma^{-1}\tau$。

计算 $x = \sigma^{-1} \circ \tau$：

| $x$ | $\tau(x)$ | $\sigma^{-1}(\tau(x))$ |
|-----|-----------|------------------------|
| 1 | 2 | $\sigma^{-1}(2) = 4$ |
| 2 | 5 | $\sigma^{-1}(5) = 3$ |
| 3 | 1 | $\sigma^{-1}(1) = 5$ |
| 4 | 3 | $\sigma^{-1}(3) = 1$ |
| 5 | 4 | $\sigma^{-1}(4) = 2$ |

$x = (1\ 4)(2\ 3\ 5)$

$|x| = \operatorname{lcm}(2, 3) = 6$。

---

### 第 3 题

设 $f: K_4 \to \mathbb{Z}_8$ 为群同态。

**约束分析**：
- $f(e) = 0$
- $2f(a) \equiv 0 \pmod{8}$，故 $f(a) \in \{0, 4\}$
- $2f(b) \equiv 0 \pmod{8}$，故 $f(b) \in \{0, 4\}$
- $f(c) = f(ab) = f(a) + f(b) \pmod{8}$

共 4 个同态映射：

| | $f(e)$ | $f(a)$ | $f(b)$ | $f(c)$ |
|---|--------|--------|--------|--------|
| $f_0$ | 0 | 0 | 0 | 0 |
| $f_1$ | 0 | 4 | 0 | 4 |
| $f_2$ | 0 | 0 | 4 | 4 |
| $f_3$ | 0 | 4 | 4 | 0 |

验证：$f_1$ 中 $f(a)=4$，$f(b)=0$，$f(c)=f(ab)=4+0=4$ ✓。其余同理。

---

### 第 4 题

$231x + 105y = 42$

辗转相除：
$$\begin{aligned}
231 &= 2 \times 105 + 21 \\
105 &= 5 \times 21 + 0
\end{aligned}$$

$\gcd(231, 105) = 21$，且 $21 \mid 42$，有解。

约简：$11x + 5y = 2$。

扩展欧几里得：$11 = 2 \times 5 + 1$，故 $1 = 11 - 2 \times 5$。

乘以 $2$：$2 = 11 \times 2 + 5 \times (-4)$。特解 $(x_0, y_0) = (2, -4)$。

通解：
$$\boxed{x = 2 + 5t,\quad y = -4 - 11t \qquad (t \in \mathbb{Z})}$$

---

### 第 5 题

求 $5^{2025} \bmod 17$。

$\gcd(5, 17) = 1$，$\varphi(17) = 16$。由欧拉定理：$5^{16} \equiv 1 \pmod{17}$。

$2025 = 126 \times 16 + 9$，故 $5^{2025} \equiv 5^9 \pmod{17}$。

逐次平方：
$$\begin{aligned}
5^2 &\equiv 25 \equiv 8 \pmod{17} \\
5^4 &\equiv 8^2 = 64 \equiv 13 \pmod{17} \\
5^8 &\equiv 13^2 = 169 \equiv 16 \equiv -1 \pmod{17} \\
5^9 &\equiv 5^8 \times 5 \equiv (-1) \times 5 = -5 \equiv 12 \pmod{17}
\end{aligned}$$

> **余数为 12**。

---

### 第 6 题

需找 $a_0, \dots, a_8$ 满足 $a_i \equiv i \pmod{9}$ 且 $a_i \equiv 1 \pmod{4}$。

即解 $x \equiv i \pmod{9},\ x \equiv 1 \pmod{4}$（$i = 0, 1, \dots, 8$）。

使用 CRT（模 $36$）：$M_1 = 4$，$M_2 = 9$。

$4^{-1} \bmod 9 = 7$（$4 \times 7 = 28 \equiv 1$），$9^{-1} \bmod 4 = 1$。

$x \equiv 4 \times 7 \times i + 9 \times 1 \times 1 \equiv 28i + 9 \pmod{36}$。

对各 $i$ 取最小正解：

| $i$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 |
|-----|---|---|---|---|---|---|---|---|---|
| $a_i$ | 9 | 1 | 29 | 21 | 13 | 5 | 33 | 25 | 17 |

> 完全剩余系：$\boxed{\{1,\ 5,\ 9,\ 13,\ 17,\ 21,\ 25,\ 29,\ 33\}}$

---

### 第 7 题

$M = 5 \times 7 \times 9 = 315$。

$$\begin{aligned}
M_1 &= 63, & 63^{-1} \bmod 5 &: 63 \equiv 3,\ 3^{-1} = 2 \\
M_2 &= 45, & 45^{-1} \bmod 7 &: 45 \equiv 3,\ 3^{-1} = 5 \\
M_3 &= 35, & 35^{-1} \bmod 9 &: 35 \equiv 8 \equiv -1,\ 8^{-1} = 8
\end{aligned}$$

$$\begin{aligned}
x &\equiv 2 \times 63 \times 2 + 3 \times 45 \times 5 + 4 \times 35 \times 8 \\
  &= 252 + 675 + 1120 = 2047 \\
  &\equiv 2047 - 315 \times 6 = 2047 - 1890 = 157 \pmod{315}
\end{aligned}$$

> $\boxed{x \equiv 157 \pmod{315}}$

验算：$157 \bmod 5 = 2$ ✓；$157 \bmod 7 = 3$ ✓；$157 \bmod 9 = 4$ ✓。

---

### 第 8 题

$x^3 + 3x + 1 \equiv 0 \pmod{21}$，$21 = 3 \times 7$。

**模 3**：由费马小定理 $x^3 \equiv x \pmod{3}$，原式化为 $x + 0 + 1 \equiv x + 1 \equiv 0 \pmod{3}$，得 $x \equiv 2 \pmod{3}$。1 个解。

**模 7**：枚举 $x = 0, \dots, 6$：

| $x$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 |
|-----|---|---|---|---|---|---|---|
| $x^3+3x+1 \bmod 7$ | 1 | 5 | 1 | 2 | 0 | 1 | 1 |

得 $x \equiv 4 \pmod{7}$。1 个解。

共 $1 \times 1 = 1$ 个解。用 CRT 合并：

$x = 3k + 2$，$3k + 2 \equiv 4 \pmod{7} \implies 3k \equiv 2 \pmod{7}$。

$3^{-1} \bmod 7 = 5$，$k \equiv 5 \times 2 = 10 \equiv 3 \pmod{7}$。

$x = 3(7t + 3) + 2 = 21t + 11$。

> $\boxed{x \equiv 11 \pmod{21}}$

---

### 第 9 题

**(1)** $\left(\dfrac{19}{23}\right)$

$19 \equiv -4 \pmod{23}$。$$\left(\frac{19}{23}\right) = \left(\frac{-4}{23}\right) = \left(\frac{-1}{23}\right)\left(\frac{4}{23}\right) = (-1)^{\frac{23-1}{2}} \times 1 = (-1)^{11} = -1$$

> (1) $\boxed{-1}$

**(2)** $\left(\dfrac{39}{17}\right)$

$39 \equiv 5 \pmod{17}$。$$\left(\frac{39}{17}\right) = \left(\frac{5}{17}\right)$$

$5 \equiv 1 \pmod{4}$，故 $\left(\frac{5}{17}\right) = \left(\frac{17}{5}\right) = \left(\frac{2}{5}\right)$。

$5 \equiv 5 \pmod{8}$，$(2/5) = -1$。

> (2) $\boxed{-1}$

**(3)** $\left(\dfrac{105}{59}\right)$

$105 = 3 \times 5 \times 7$。$$\left(\frac{105}{59}\right) = \left(\frac{3}{59}\right)\left(\frac{5}{59}\right)\left(\frac{7}{59}\right)$$

- $\left(\frac{3}{59}\right)$：$3 \equiv 59 \equiv 3 \pmod{4}$，$= -\left(\frac{59}{3}\right) = -\left(\frac{2}{3}\right) = -(-1) = 1$
- $\left(\frac{5}{59}\right)$：$5 \equiv 1 \pmod{4}$，$= \left(\frac{59}{5}\right) = \left(\frac{4}{5}\right) = 1$
- $\left(\frac{7}{59}\right)$：$7 \equiv 59 \equiv 3 \pmod{4}$，$= -\left(\frac{59}{7}\right) = -\left(\frac{3}{7}\right) = -(-1) = 1$

> (3) $\boxed{1}$

---

### 第 10 题

$x^2 \equiv 4 \pmod{35}$，$35 = 5 \times 7$。

- **模 5**：$x^2 \equiv 4 \pmod{5}$，$x \equiv \pm 2 \equiv 2, 3 \pmod{5}$。2 个解。
- **模 7**：$x^2 \equiv 4 \pmod{7}$，$x \equiv \pm 2 \equiv 2, 5 \pmod{7}$。2 个解。

共 $2 \times 2 = 4$ 个解。用 CRT 组合：

| $x \bmod 5$ | $x \bmod 7$ | $x \bmod 35$ |
|-------------|-------------|--------------|
| 2 | 2 | 2 |
| 2 | 5 | 12 |
| 3 | 2 | 23 |
| 3 | 5 | 33 |

> 解数：**4**。解为 $\boxed{x \equiv 2,\ 12,\ 23,\ 33 \pmod{35}}$。

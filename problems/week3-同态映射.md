# Week 3 — 同态映射 习题

---

## 简答题：构造从 Klein 群到模 4 加群的所有同态映射并证明

### 1. 群的表示

Klein 四元群 $K_4 = \{e, a, b, c\}$，运算表：

$$
\begin{array}{c|cccc}
\circ & e & a & b & c \\
\hline
e & e & a & b & c \\
a & a & e & c & b \\
b & b & c & e & a \\
c & c & b & a & e
\end{array}
$$

模 4 加群 $\mathbb{Z}_4 = \{0, 1, 2, 3\}$，运算为模 4 加法。

### 2. 同态映射构造

同态需满足：$\forall x,y \in K_4,\ f(x \circ y) = f(x) + f(y) \pmod{4}$，且 $f(e)=0$（单位元映射到单位元）。

由 $a^2 = b^2 = c^2 = e$，得 $2f(a) \equiv 0 \pmod{4}$，$2f(b) \equiv 0 \pmod{4}$，$2f(c) \equiv 0 \pmod{4}$，故 $f(a),f(b),f(c) \in \{0,2\}$。

又 $c = a \circ b$，故 $f(c) = f(a) + f(b) \pmod{4}$。

所有同态映射：

| | $f(e)$ | $f(a)$ | $f(b)$ | $f(c)$ |
|---|--------|--------|--------|--------|
| $f_0$（零同态）| 0 | 0 | 0 | 0 |
| $f_1$ | 0 | 2 | 0 | 2 |
| $f_2$ | 0 | 0 | 2 | 2 |
| $f_3$ | 0 | 2 | 2 | 0 |

### 3. 同态证明

以 $f_1$ 为例：
- $f_1(a \circ a) = f_1(e) = 0$，$f_1(a) + f_1(a) = 2 + 2 = 4 \equiv 0 \pmod{4}$ ✓
- $f_1(a \circ b) = f_1(c) = 2$，$f_1(a) + f_1(b) = 2 + 0 = 2 \pmod{4}$ ✓
- 其余组合同理可验证。

$f_0, f_2, f_3$ 类似验证。

---

## 一、二元运算的性质判定

**1.** 判断下列集合上的二元运算是否满足交换律、结合律、消去律，并给出左右单位元。

(1) 整数集 $\mathbb{Z}$ 上的二元运算：$a \circ b = ab + a + b$

(2) 全体 $n>1$ 阶实可逆矩阵关于矩阵的加法和乘法运算

(3) $S = \left\{ \begin{pmatrix} a & b \\ 0 & 0 \end{pmatrix} \mid a,b \in \mathbb{Q} \right\}$ 关于矩阵的乘法运算

(4) 正整数集 $\mathbb{Z}^+$ 上的二元运算：$a \circ b = a^b$

---

## 二、判断同态映射

**2.** 代数系统 $V_1 = \langle \mathbb{Z}, +, \times \rangle$ 和 $V_2 = \langle \mathbb{Z}_7, \oplus, \otimes \rangle$，映射 $f: V_1 \to V_2$，$f(x) = x \pmod{7}$。判断 $f$ 是否为同态映射。

---

## 三、自同态与自同构

**3.** 设 $A = \{a, b\}$，定义二元运算：

$$
\begin{array}{c|cc}
\circ & a & b \\
\hline
a & a & b \\
b & b & a
\end{array}
$$

列出 $A$ 上所有的映射，并判断哪些是自同态和自同构。

---

## 四、构造自同构 + 验证群结构

**4.** (1) 构造代数系统 $\langle \mathbb{Q}, + \rangle$ 上的一个自同构映射。

(2) 在 $\mathbb{R}^* \times \mathbb{R}$ 上定义二元运算 $\circ$：$(a,b) \circ (c,d) = (ac,\ ad + b)$，验证 $\langle \mathbb{R}^* \times \mathbb{R}, \circ \rangle$ 构成一个群。

---

## 五、构造群 + $x^2=e$ 的群性质

**5.** (1) 设 $A = \{a, b, c, d\}$，设计一个二元运算 $\circ$，使 $\langle A, \circ \rangle$ 是一个群。

(2) 证明：若群 $\langle G, \circ \rangle$ 的每个元素都满足 $x^2 = e$，则 $\langle G, \circ \rangle$ 是交换群。

---

## 六、有限群元素阶的有限性

**6.** 证明：一个有限群的每一个元素的阶都有限。

---

## 七、$\mathbb{Z}_8^*$ 乘法群

**7.** $\mathbb{Z}_8$ 所有非零元关于模乘法运算构成群 $\langle \mathbb{Z}_8^*, \otimes \rangle$，求每个元素的阶和逆。

---

## 参考答案

### 第 1 题

**(1)** $a \circ b = ab + a + b$

- 交换律：$a \circ b = ab+a+b = ba+b+a = b \circ a$ ✓
- 结合律：$(a \circ b) \circ c = (ab+a+b)c + (ab+a+b) + c = abc + ac + bc + ab + a + b + c$，$a \circ (b \circ c) = a(bc+b+c) + a + (bc+b+c) = abc + ab + ac + a + bc + b + c$。两者相等 ✓
- 左单位元：$e \circ a = ea + e + a = a \implies e(a+1) = 0 \implies e = 0$（对所有 $a$ 成立）
- 右单位元同理为 $0$
- 消去律：$a \circ b = a \circ c$ 且 $a \neq -1$ 时 $b=c$（因为 $(a+1)(b-c)=0$），但 $a=-1$ 时消去失效 ✗

**(2)** 全体 $n>1$ 阶实可逆矩阵：

- 加法：封闭性不成立（两个可逆矩阵之和不一定可逆）→ 不构成代数系统
- 乘法：封闭 ✓（可逆矩阵之积可逆），结合律 ✓，单位元 $I$ ✓，消去律 ✓（可逆矩阵可消去），交换律 ✗

**(3)** $S$ 关于矩阵乘法：

- 封闭：$\begin{pmatrix}a&b\\0&0\end{pmatrix}\begin{pmatrix}c&d\\0&0\end{pmatrix} = \begin{pmatrix}ac&ad\\0&0\end{pmatrix} \in S$ ✓
- 结合律 ✓（矩阵乘法），交换律 ✗，无单位元 ✗

**(4)** $a \circ b = a^b$：交换律 ✗（$2^3 \neq 3^2$），结合律 ✗（$(a^b)^c \neq a^{(b^c)}$），无单位元，无消去律。

---

### 第 2 题

$f(x) = x \bmod 7$。

验证加法同态：$f(x+y) = (x+y) \bmod 7 = (x \bmod 7) \oplus (y \bmod 7) = f(x) \oplus f(y)$ ✓

验证乘法同态：$f(x \times y) = (xy) \bmod 7 = (x \bmod 7) \otimes (y \bmod 7) = f(x) \otimes f(y)$ ✓

且 $f(0)=0$，$f(1)=1$。

> $f$ 既是加法群同态，也是乘法半群同态，因此是**环同态**。

---

### 第 3 题

$A=\{a,b\}$ 上共有 $2^2=4$ 个映射：

| 映射 | $f(a)$ | $f(b)$ | 自同态？ | 自同构？ |
|------|--------|--------|----------|----------|
| $f_1$（恒等）| $a$ | $b$ | ✓ | ✓ |
| $f_2$（交换）| $b$ | $a$ | ✓ | ✓ |
| $f_3$（常值 a）| $a$ | $a$ | ✗ | ✗ |
| $f_4$（常值 b）| $b$ | $b$ | ✗ | ✗ |

$f_1$ 和 $f_2$ 都是自同构（该群同构于 $\mathbb{Z}_2$，两个元素互换恰好对应恒等和取负）。

---

### 第 4 题

**(1)** $\langle \mathbb{Q}, + \rangle$ 的自同构：

$f(x) = kx$（$k \in \mathbb{Q}^*$）是自同构。验证：$f(x+y)=k(x+y)=kx+ky=f(x)+f(y)$，双射（$k \neq 0$ 时有逆映射 $f^{-1}(x)=x/k$）。

最简单的非平凡自同构：$\boxed{f(x) = 2x}$ 或 $\boxed{f(x) = -x}$。

**(2)** 验证 $\langle \mathbb{R}^* \times \mathbb{R}, \circ \rangle$ 是群，其中 $(a,b) \circ (c,d) = (ac,\ ad+b)$。

- **封闭**：$a,c \in \mathbb{R}^* \implies ac \in \mathbb{R}^*$，$ad+b \in \mathbb{R}$ ✓
- **结合律**：$((a,b)\circ(c,d))\circ(e,f) = (ac,ad+b)\circ(e,f) = (ace, acf+ad+b)$，$(a,b)\circ((c,d)\circ(e,f)) = (a,b)\circ(ce, cf+d) = (ace, a(cf+d)+b) = (ace, acf+ad+b)$ ✓
- **单位元**：$(1,0)$。$(a,b)\circ(1,0) = (a\cdot1, a\cdot0+b) = (a,b)$，$(1,0)\circ(a,b) = (1\cdot a, 1\cdot b+0) = (a,b)$ ✓
- **逆元**：$(a,b)^{-1} = (\frac{1}{a}, -\frac{b}{a})$。验证 $(a,b)\circ(\frac{1}{a},-\frac{b}{a}) = (1, a(-\frac{b}{a})+b) = (1,0)$ ✓

---

### 第 5 题

**(1)** 构造 4 元群：让 $A$ 对应 $\mathbb{Z}_4$（模 4 加法群），或 $K_4$（Klein 四元群）。

以 $K_4$ 为例，令 $a=e$（单位元），$\circ$ 运算表参见简答题。

**(2)** 证 $x^2=e$（对所有 $x$）$\implies G$ 是交换群。

任取 $a,b \in G$。$(ab)^2 = e \implies abab = e$。

左乘 $a$：$a(abab) = a \implies (a^2)bab = a \implies bab = a$。

再左乘 $b$：$b(bab) = ba \implies (b^2)ab = ba \implies ab = ba$。$\square$

---

### 第 6 题

设 $|G| = n$，$a \in G$。考虑 $a, a^2, a^3, \dots, a^{n+1}$ 这 $n+1$ 个元素，由鸽巢原理必有两个相等：$a^i = a^j$（$i < j$）。则 $a^{j-i} = e$，$j-i \le n$。

> $a$ 的阶 $\le n$，即为有限。$\square$

---

### 第 7 题

$\mathbb{Z}_8^* = \{a \in \mathbb{Z}_8 \mid \gcd(a, 8) = 1\} = \{1, 3, 5, 7\}$，$|\mathbb{Z}_8^*| = \varphi(8) = 4$。

| 元素 | 阶 | 计算 | 逆元 |
|------|-----|------|------|
| $1$ | 1 | $1^1 = 1$ | $1$ |
| $3$ | 2 | $3^2 = 9 \equiv 1$ | $3$ |
| $5$ | 2 | $5^2 = 25 \equiv 1$ | $5$ |
| $7$ | 2 | $7^2 = 49 \equiv 1$ | $7$ |

> 每个非单位元阶均为 2，$\mathbb{Z}_8^* \cong K_4$。

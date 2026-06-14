# Week 11 考试速通

---

## 一、欧拉定理 & 费马小定理

**欧拉定理：** $\gcd(a,m)=1 \;\Longrightarrow\; a^{\varphi(m)} \equiv 1 \pmod m$

**费马小定理：** $p$ 素数，$a^{\varphi(p)} = a^{p-1} \equiv 1 \pmod p$

**解题套路：** 把大指数拆成 $\varphi(m)$ 的倍数 + 余数。
- 例：$47^{7385} \bmod 19$。$\varphi(19)=18$，$7385 = 410 \times 18 + 5$，只算 $47^5 \bmod 19$。

**$\varphi(n)$ 计算公式：** $n = p_1^{e_1}p_2^{e_2}\cdots \;\Longrightarrow\; \varphi(n) = n \cdot \prod\left(1 - \frac{1}{p_i}\right)$

**个位数问题 = 模 10：** $\varphi(10)=4$，只需看指数 $\bmod 4$。

---

## 二、一次同余式 $ax \equiv b \pmod m$

**解数判定：** $d = \gcd(a,m)$
- $d \nmid b$ → 0 个解
- $d \mid b$ → $d$ 个解，形式为 $x \equiv x_0 + \frac{m}{d}t \pmod m$（$t=0,1,\dots,d-1$）

**求解步骤：** 约去 $d$ → 求 $a'$ 的逆元（扩展欧几里得）→ $x_0 \equiv (a')^{-1}b' \pmod{m'}$

---

## 三、同余方程组（CRT）

**逐次代入法（2-3 个方程最实用）：**

$x \equiv a_1 \pmod{m_1}$，$x \equiv a_2 \pmod{m_2}$（且 $\gcd(m_1,m_2)=1$）：

从第一个得 $x = a_1 + m_1k$，代入第二个解出 $k$。

**CRT 公式法（方程多时）：**
$$x \equiv \sum a_i \cdot M_i \cdot M_i^{-1} \pmod M$$
其中 $M = \prod m_i$，$M_i = M/m_i$，$M_i^{-1}$ 是 $M_i$ 模 $m_i$ 的逆。

---

## 四、平方剩余 & 勒让德符号

**定义：** 奇素数 $p$，$(a,p)=1$。若 $x^2 \equiv a \pmod p$ 有解 → $a$ 是平方剩余；无解 → 平方非剩余。

**勒让德符号：**
$$\left(\frac{a}{p}\right) = \begin{cases} 0, & p \mid a \\ 1, & \text{平方剩余} \\ -1, & \text{平方非剩余} \end{cases}$$

**四条运算法则：**

| 规则 | 公式 | 记忆技巧 |
|------|------|----------|
| 乘法 | $\left(\frac{ab}{p}\right)=\left(\frac{a}{p}\right)\left(\frac{b}{p}\right)$ | 随便拆 |
| 平方 | $\left(\frac{a^2}{p}\right)=1$（$p \nmid a$）| 平方数一定是剩余 |
| $-1$ | $\left(\frac{-1}{p}\right)=(-1)^{\frac{p-1}{2}}$ | $p \equiv 1 \pmod 4$ → 1；$p \equiv 3 \pmod 4$ → -1 |
| $2$ | $\left(\frac{2}{p}\right)=(-1)^{\frac{p^2-1}{8}}$ | $p \equiv \pm1 \pmod 8$ → 1；$p \equiv \pm3 \pmod 8$ → -1 |

**二次互反律：**
$$\left(\frac{p}{q}\right)\left(\frac{q}{p}\right) = (-1)^{\frac{p-1}{2} \cdot \frac{q-1}{2}}$$

**翻译：** $p,q$ 都是奇素数。翻分子分母时，只要有一个 $\equiv 1 \pmod 4$ 就不变号；两个都 $\equiv 3 \pmod 4$ 才加负号。

**计算流程：** 分子拆素因子 → 分子模分母化简 → 该互反的互反 → 降到小素数结束。

---

## 五、雅可比符号

**和勒让德唯一区别：** 分母可以是合数（正奇数）。

**运算法则完全一样。** 多一步：分母拆素因子分别算。

**关键坑：** $\left(\frac{a}{n}\right)=1$ **不代表** 有解。$-1$ 才能确认无解。要判断有没有解得拆回勒让德符号看每个分量。

**$\gcd(a,n) \neq 1 \;\Longrightarrow\; \left(\frac{a}{n}\right) = 0$**

---

## 五½、克罗内克符号 (Kronecker Symbol)

**定义：** 勒让德符号（奇素数分母）$\to$ 雅可比符号（奇合数分母）$\to$ **克罗内克符号（任意整数分母）**。

$$\left(\frac{a}{n}\right)$$

其中 $n$ 可以是任意非零整数，包括偶数、负数。

### 基本性质

| 分母 $n$ | $\left(\frac{a}{n}\right)$ | 条件 |
|----------|--------------------------|------|
| 奇素数 $p$ | 同勒让德符号 | — |
| 正奇数 $m$ | 拆素因子乘起来（同雅可比） | — |
| $n = 2$ | $\begin{cases} 0 & a \text{ 偶} \\ 1 & a \equiv \pm1 \pmod 8 \\ -1 & a \equiv \pm3 \pmod 8 \end{cases}$ | — |
| $n = -1$ | $\begin{cases} 1 & a \ge 0 \\ -1 & a < 0 \end{cases}$ | — |

### 完全可乘性

$$\left(\frac{ab}{n}\right) = \left(\frac{a}{n}\right)\left(\frac{b}{n}\right), \quad \left(\frac{a}{mn}\right) = \left(\frac{a}{m}\right)\left(\frac{a}{n}\right)$$

分子分母任意拆，算就完了。

### 与勒让德/雅可比的统一关系

- $n$ 正奇数 $\implies$ 克罗内克 = 雅可比
- $n$ 奇素数 $\implies$ 克罗内克 = 勒让德

### 核心优势

雅可比要求分母是正奇数，克罗内克没这个限制。配合**二次互反律的克罗内克版本**可以处理分母含偶数或负数的情况，尤其在代数数论中作为**狄利克雷特征的推广**使用。

### 零值规则

$\left(\frac{a}{n}\right) = 0 \iff \gcd(a, n) \neq 1$（$n \neq \pm 1$ 时）。

---

## 六、$x^2 \equiv a$ 解数速判

### 奇素数幂 $p^e$（$p$ 奇）：

| 条件 | 解数 |
|------|------|
| $p \nmid a$，且 $\left(\frac{a}{p}\right)=1$ | **2** |
| $p \nmid a$，且 $\left(\frac{a}{p}\right)=-1$ | **0** |
| $p \mid a$ | 看 $a$ 中 $p$ 的指数，偶数可约掉，奇数无解 |

### 模 $2^e$：

| $e$ | 条件 | 解数 |
|-----|------|------|
| 1 | $a$ 奇 | 1 |
| 2 | $a\equiv1\pmod4$ | 2 |
| $\ge 3$ | $a\equiv1\pmod8$ | **4** |
| $\ge 3$ | $a\not\equiv1\pmod8$ | **0** |

### 合数模：

分解模数 → 每部分单独判解数 → **全部相乘**（CRT 保证）。

---

## 七、亨泽尔抬升（$x^2 \equiv a \pmod{p^e}$ 求解）

**适用：** 从模 $p$ 有解开始，逐层抬到 $p^e$。

**核心公式（奇素数 $p$）：**

设 $f(x)=x^2-a$，$f'(x)=2x$。已知模 $p^k$ 的解 $x_k$，抬到 $p^{k+1}$：

$$x_{k+1} = x_k + p^k \cdot t$$

其中 $$t \equiv -\frac{f(x_k)}{p^k} \cdot \big(f'(x_k)\big)^{-1} \pmod p$$

**操作流程：**

1. 解模 $p$，找到种子 $x_0$
2. 算 $f(x_k)$、除 $p^k$、乘 $(f')^{-1}$、取负 → 得 $t$
3. $x_{k+1} = x_k + p^k t$，重复到目标层
4. 另一个解是 $-x$ 对称

**模 $2^k$ 特殊情况：** 导数 $2x$ 是偶数，线性项蒸发。变成看 $f(x_k)/2^k$ 的奇偶：偶则分裂（两个 $t$ 都活），奇则死。$k \ge 3$ 后稳定 4 个解。

---

## 八、扩展欧几里得（求逆元）

求 $a^{-1} \pmod m$：做辗转相除，回代得 $ax + my = 1$，则 $x$ 即逆元。

---

## 九、完全剩余系 & 简化剩余系

- **完全剩余系：** 模 $m$ 每个同余类取一个代表，共 $m$ 个数
- **简化剩余系：** 只取与 $m$ 互素的类，共 $\varphi(m)$ 个数

**带附加条件的题目：** 用 CRT 为每个代表元配满足附加条件的数。

---

## 十、证明题速记

| 题 | 关键 |
|----|------|
| $a^p+b^p \equiv (a+b)^p \pmod p$ | 二项式展开，中间系数含 $p$，模 $p$ 全消失 |
| $m^{\varphi(n)}+n^{\varphi(m)} \equiv 1 \pmod{mn}$ | 第一项模 $n$ 是 1、模 $m$ 是 0；第二项反过来。CRT 组合 |
| $\left(\frac{a}{p}\right)=1$（$p=4m+1, a\mid m$）| 互反律翻，$p\equiv1\pmod a$ 使 $(p/a)=1$，指数部分为偶 |

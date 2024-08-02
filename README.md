# 1. Không gian Metric

## Định nghĩa không gian Metric
Giả sử $E$ là một tập hợp, một hàm số $d: E \times E \to \mathbb{R}$ được gọi là một khoảng cách (distance) trên $E$ nếu nó thoả mãn các tiên đề sau, gọi là các tiên đề của một metric:

1. **Tiên đề về tính đối xứng:** $\forall (x, y) \in E^2$, $d(x, y) = d(y, x)$ và $d(x, x) = 0$.
2. **Tiên đề về bất đẳng thức tam giác:** $\forall (x, y, z) \in E^3$, $d(x, z) \le d(x, y) + d(y, z)$.
3. **Tiên đề về tính đồng nhất:** $\forall (x, y) \in E^2$, $d(x, y) = 0 \iff x = y$.

Cấu trúc $(E, d)$, trong đó $E$ là một không gian vector và $d$ là một khoảng cách, được gọi là một không gian metric.

### Ví dụ 1.1

Tập hợp các số thực và tập hợp các số phức là những không gian metric, với metric $d(x, y) = |x - y|$, với mọi $x, y \in \mathbb{R}$ (hoặc $\mathbb{C}$).

### Ví dụ 1.2

Gọi $C[a, b]$ là tập hợp các hàm số thực liên tục trên khoảng đóng hữu hạn $[a, b]$. Dễ dàng chứng minh được rằng $C[a, b]$ là một không gian metric với metric $d(x, y) = \sup_{t \in [a, b]} |x(t) - y(t)|$ với mọi $x, y \in C[a, b]$.


## Không gian Vector Định Chuẩn

Giả sử $E$ là một không gian vector và $K$ là không gian hệ số của $E$. Một chuẩn (norm) trên $E$, $N: E \to \mathbb{R}^+$, là một hàm số thoả mãn:

1. **Tiên đề về tính đồng nhất của chuẩn:** $\forall (\lambda, x) \in K \times E$, $N(\lambda x) = |\lambda| \cdot N(x)$.
2. **Tiên đề về bất đẳng thức tam giác:** $\forall (x, y) \in E^2$, $N(x + y) \le N(x) + N(y)$.
3. **Tiên đề về tính đồng nhất:** $\forall x \in E$, $N(x) = 0 \iff x = 0$.

Một không gian định chuẩn là mọi không gian vector được trang bị một chuẩn, ký hiệu $(E, N)$.

Khi $N: E \to \mathbb{R}^+$ chỉ thoả mãn tiên đề 1 và 2, ta gọi $N$ là một bán chuẩn (semi-norm).

### Mối liên hệ với không gian metric
Mọi không gian định chuẩn $(E, N)$ là một không gian metric với khoảng cách $d(x, y) = N(x - y)$.

# 2. Tập Đóng và Tập Mở

## Định nghĩa về Tập Mở

Giả sử $(X, d)$ là một không gian metric, $x_0 \in X$ và $r$ là một số dương. Tập hợp $B(x_0, r) = \{ x \in X \mid d(x, x_0) < r \}$ được gọi là quả cầu mở tâm $x_0$ bán kính $r$.


Với $A, B$ là hai tập con khác rỗng trong $X$, khoảng cách giữa hai tập con $A, B$ được định nghĩa là:
$$
d(A, B) = \inf \{ d(a, b) \mid a \in A, b \in B \}.
$$

## Định nghĩa về Điểm Trong và Tập Mở

Giả sử $A$ là một tập con của không gian metric $(X, d)$. Điểm $x_0$ của $X$ được gọi là điểm trong của tập hợp $A$ nếu tồn tại một quả cầu mở $B(x_0, r) \subset A$. Tập tất cả các điểm trong của tập $A$ được gọi là phần trong của $A$ và ký hiệu là $A^\circ$.

Phần trong của một tập hợp có thể là tập hợp rỗng.

Tập hợp $G \subset X$ được gọi là tập mở nếu mọi điểm của $G$ đều là điểm trong của nó.

Hiển nhiên tập $X$ và tập $\emptyset$ đều là những tập mở trong không gian metric $(X, d)$. Mỗi quả cầu mở là tập mở trong $(X, d)$.

## Định lý về Tập Mở

Trong không gian metric $(X, d)$, ta có:

a) Hợp của một họ tuỳ ý những tập mở là một tập mở.

b) Giao của một số hữu hạn những tập mở là một tập mở.

### Chứng minh

a) Giả sử $\{U_t\}_{t \in T}$ là một họ tùy ý những tập con mở trong không gian metric $(X, d)$. Ta chứng minh $U = \bigcup_{t \in T} U_t$ là một tập mở.

Thật vậy, giả sử $x \in U$ tùy ý. Khi đó $x \in U_t$ với $t$ nào đó. Vì $U_t$ mở nên tồn tại một quả cầu $B(x, r) \subset U_t$, do đó $B(x, r) \subset U$. Vậy $U$ là một tập mở.

b) Giả sử $U_1, \ldots, U_n$ là những tập mở. Ta chứng minh $V = \bigcap_{i=1}^n U_i$ là tập mở.

Thật vậy, nếu $x \in V$ thì $x \in U_i$ với mọi $i = 1, \ldots, n$. Vì mỗi $U_i$ mở nên tồn tại một số dương $r_i$ sao cho $B(x, r_i) \subset U_i$, $i = 1, \ldots, n$. Đặt $r = \min \{r_1, \ldots, r_n\}$. Khi đó hiển nhiên $B(x, r) \subset U_i$ với $i = 1, \ldots, n$, do đó $B(x, r) \subset V$. Vậy $V$ là một tập mở.

# Tập Đóng

## Định nghĩa về Tập Đóng

Tập con $A \subset (X, d)$ được gọi là tập đóng nếu phần bù của $A$ trong $X$ (tập $X \setminus A$) là một tập mở.

Hiển nhiên, các tập $X$ và $\emptyset$ là những tập đóng trong không gian metric $(X, d)$. Dễ dàng chứng minh được mọi quả cầu đóng là tập đóng.

## Định lý về Tập Đóng

### Định lý 1.2

Trong không gian metric $(X, d)$ ta có:

a) Giao của một họ tuỳ ý những tập đóng là một tập đóng.

b) Hợp của một họ hữu hạn những tập đóng là một tập đóng.

#### Chứng minh:

a) Giả sử $\{E_t\}_{t \in T}$ là một họ tùy ý những tập đóng trong không gian metric $(X, d)$. Ta chứng minh rằng $F = \bigcap_{t \in T} E_t$ là một tập đóng.

Thật vậy, với mọi $t \in T$, tập $X \setminus E_t$ là mở. Vậy $X \setminus F = \bigcup_{t \in T} (X \setminus E_t)$ là một tập mở, do đó $F$ là một tập đóng.

b) Giả sử $E_1, \ldots, E_n$ là những tập đóng. Ta chứng minh rằng $V = \bigcup_{i=1}^n E_i$ là tập đóng.

Thật vậy, với mỗi $x \in V$ thì $x \in E_i$ với một số hữu hạn các $i$. Vì mỗi $E_i$ là đóng nên $X \setminus E_i$ là mở. Vì vậy, $X \setminus V = \bigcap_{i=1}^n (X \setminus E_i)$ là một tập mở, do đó $V$ là một tập đóng.

### Định lý 1.3

Tập con $F$ của không gian metric $X$ là đóng khi và chỉ khi với dãy bất kỳ $\{x_n\}_{n=1}^\infty$ những phần tử của $F$, nếu $\lim_{n \to \infty} x_n = x_0 \in X$ thì $x_0 \in F$.

#### Chứng minh:

(=>) Cho tập $F$ đóng. Giả sử tồn tại dãy $\{x_n\}_{n=1}^\infty$ trong $F$ thỏa mãn $\lim_{n \to \infty} x_n = x_0$ và $x_0 \notin F$. 

Vì $X \setminus F$ là tập mở nên tồn tại một quả cầu $B(x_0, \epsilon) \subset X \setminus F$. Vì $\lim_{n \to \infty} x_n = x_0$ nên với $n$ đủ lớn, $d(x_n, x_0) < \epsilon$, tức là $x_n \in X \setminus F$ với $n$ đủ lớn. Điều này mâu thuẫn với giả thiết.

(<=) Đảo lại, giả sử với dãy bất kỳ $\{x_n\}_{n=1}^\infty$ những phần tử của $F$, nếu $\lim_{n \to \infty} x_n = x_0 \in X$ thì $x_0 \in F$, và giả sử $X \setminus F$ không phải là một tập mở. Khi đó tồn tại ít nhất một điểm $x_0 \in X \setminus F$ không phải là điểm trong của $X \setminus F$. Khi đó, với mọi số tự nhiên $n$, tồn tại một phần tử $x_n \in F$ thuộc quả cầu $B(x_0, \frac{1}{n})$. Dãy $\{x_n\}_{n=1}^\infty$ là một dãy phần tử của tập $F$ hội tụ đến $x_0 \notin F$ (vì $d(x_0, x_n) < \frac{1}{n}$ với mọi $n$). Điều này mâu thuẫn với giả thiết.

### Định nghĩa về Bao Đóng

Cho $A \subset (X, d)$. Giao của tất cả các tập đóng trong $X$ chứa $A$ được gọi là bao đóng của tập $A$, ký hiệu là $\overline{A}$.

Vì $X$ là một tập đóng chứa $A$ nên bao đóng của tập $A$ luôn tồn tại.

Hiển nhiên ta có:

1) $\overline{A}$ là một tập đóng và đó là tập đóng nhỏ nhất chứa $A$.
2) $A$ là đóng khi và chỉ khi $A = \overline{A}$.
3) Nếu $A \subset B$ thì $\overline{A} \subset \overline{B}$.

### Định lý 1.4

Giả sử $A \subset (X, d)$ và $x \in X$. Điểm $x \in A$ khi và chỉ khi mỗi lân cận $U$ của $x$ đều có điểm chung với $A$.

#### Chứng minh:

(=>) Giả sử $x \in A$, và giả sử tồn tại một lân cận mở $U$ của $x$ thỏa mãn $U \cap A = \emptyset$. Khi đó, $X \setminus U$ là tập đóng chứa $A$ $\implies A \subset X \setminus U \implies A \cap U = \emptyset$, điều này vô lý.

(<=) Nếu $x \notin A$, thì $U = X \setminus A$ là một lân cận của $x$ không có điểm chung với $A$, mâu thuẫn với giả thiết.

### Định lý 1.5

Giả sử $A \subset (X, d)$ và $x \in X$. Điểm $x \in A$ khi và chỉ khi tồn tại một dãy $\{x_n\}_{n=1}^\infty$ những phần tử của $A$ sao cho $\lim_{n \to \infty} x_n = x$.

#### Chứng minh:

(=>) Giả sử $x \notin A$. Theo định lý 1.4, với mỗi số tự nhiên $n$ ta có $B(x, \frac{1}{n}) \cap A \neq \emptyset$. Với mỗi $n$, chọn $x_n \in B(x, \frac{1}{n}) \cap A$. Khi đó $\{x_n\}_{n=1}^\infty$ là một dãy điểm của $A$ thỏa mãn $\lim_{n \to \infty} x_n = x$.

(<=) Nếu $\{x_n\}_{n=1}^\infty \subset A$ thỏa mãn $\lim_{n \to \infty} x_n = x$, thì từ định lý 1.3 suy ra $x \in A$.


## Định nghĩa về Tích của Các Không Gian Metric

Cho $(X_1, d_1)$ và $(X_2, d_2)$ là hai không gian metric. Với bất kỳ $(x_1, x_2), (y_1, y_2) \in X_1 \times X_2$, đặt:

$$
d((x_1, x_2), (y_1, y_2)) = d_1(x_1, y_1) + d_2(x_2, y_2).
$$

Hàm $d$ xác định như trên là một metric trên $X_1 \times X_2$. Tập $X_1 \times X_2$ cùng với metric $d$ được gọi là tích của các không gian metric $(X_1, d_1)$ và $(X_2, d_2)$.

## Giới nội

**Định nghĩa:** Cho một không gian định chuẩn $(E, N)$, một bộ phận $A$ của $E$ được gọi là **giới nội** nếu tồn tại một số thực $M > 0$ sao cho:

$$
\forall x, y \in A, \; d(x, y) \leq M.
$$

**Đường kính của bộ phận giới nội:** Cho $A$ là một bộ phận giới nội của $(E, N)$, đường kính của $A$ được xác định bởi:

$$
\text{diam}(A) = \sup_{(x, y) \in A^2} d(x, y).
$$

Như vậy, nếu $A \subseteq B \subseteq E$ và cả $A$ và $B$ đều giới nội, ta có:

$$
\text{diam}(A) \leq \text{diam}(B).
$$

**Ví dụ:** Xét không gian định chuẩn $(\mathbb{R}, |\cdot|)$ với chuẩn là giá trị tuyệt đối. Tập hợp $A = [0, 1]$ và $B = [-1, 1]$ đều là bộ phận giới nội của $\mathbb{R}$ vì có giới hạn trên cho khoảng cách giữa bất kỳ hai điểm nào trong các tập hợp này. Trong trường hợp này, $\text{diam}(A) = 1$ và $\text{diam}(B) = 2$, và rõ ràng $\text{diam}(A) \leq \text{diam}(B)$.

## Khoảng cách giữa một điểm và một tập hợp

**Định nghĩa:** Khoảng cách giữa một điểm $x \in E$ và một tập con $A \subseteq E$ được xác định bởi:

$$
d(x, A) = \min_{y \in A} d(x, y).
$$


## Lân cận

**Định nghĩa:** Cho $a \in E$ và $V \subseteq E$, ta gọi $V$ là một **lân cận** của $a$ trong $E$ nếu tồn tại một số thực $r > 0$ sao cho:

$$
B(a, r) \subset V,
$$

với $B(a, r) = \{ x \in E \mid d(a, x) < r \}$ là quả cầu mở tâm $a$ và bán kính $r$. Tập hợp tất cả các lân cận của $a$ trong $E$ ký hiệu là $V(a)$.

**Mệnh đề:**

- Nếu $V_1, V_2, \ldots, V_n \in V(a)$ thì $\bigcap_{i=1}^n V_i \in V(a)$.
- Nếu $V_1, V_2, \ldots \in V(a)$ là một tập hợp lân cận thì $\bigcup_{i=1}^\infty V_i \in V(a)$.

**Lưu ý:** Giao của vô hạn lân cận của $a$ không hẳn là một lân cận của $a$, nhưng hợp hữu hạn hoặc vô hạn của các lân cận của $a$ luôn là một lân cận của $a$.


## không gian Hausdorff
### Định nghĩa
Cho $(E, \mathcal{N})$ là một không gian metric. Một không gian metric $(E, \mathcal{N})$ được gọi là một không gian Hausdorff nếu với mọi $a, b \in E$ và $a \neq b$, tồn tại các lân cận $V \in \mathcal{V}_E(a)$ và $W \in \mathcal{V}_E(b)$ sao cho $V \cap W = \emptyset$.

### Tính chất

- Mọi không gian vector định chuẩn đều là không gian Hausdorff.
- Mọi không gian vector định chuẩn đều là không gian phân ly (separable space).

## Không gian Phân ly (Separable Space)

### Định nghĩa

Một không gian metric (hoặc không gian tôpô) được gọi là **không gian phân ly (separable space)** nếu nó chứa một tập con đếm được mà tập này là dày đặc trong không gian đó. Điều này có nghĩa là:

- Một tập con $D$ của không gian $X$ là dày đặc trong $X$ nếu mọi điểm của $X$ hoặc nằm trong $D$, hoặc là một điểm giới hạn của $D$.
- Nói cách khác, không gian $X$ là phân ly nếu có một tập con đếm được $D \subset X$ sao cho mọi điểm trong $X$ đều có một điểm trong $D$ gần kề.

### Ví dụ

- Không gian Euclid $\mathbb{R}^n$ là không gian phân ly vì tập hợp các điểm với tọa độ hữu tỉ là dày đặc trong $\mathbb{R}^n$.
- Không gian các hàm liên tục trên $[0,1]$ với chuẩn tôpô là không gian phân ly vì tập hợp các hàm đa thức với hệ số hữu tỉ là dày đặc trong không gian này.

### Tính chất

- Mọi không gian metric phân ly đều là không gian đếm được trong định nghĩa của không gian tôpô.
- Mọi không gian con của không gian phân ly cũng là không gian phân ly.


# Giới Hạn 

Trong từ đây đến hết nội dung này, ta ký hiệu $(E, \|\cdot\|)$ và $(F, \|\cdot\|_F)$ là hai không gian vector định chuẩn, $d_E$ (tương ứng $d_F$) là khoảng cách liên kết với chuẩn $\|\cdot\|$ (tương ứng, $\|\cdot\|_F$).

## 1. Định nghĩa về giới hạn của hàm số

### 1.1. Giới hạn của hàm số tại một điểm

Cho $X \subseteq E$, $a \in X$, $l \in F$, và hàm số $f: X \to F$. Ta nói rằng $f$ có giới hạn $l$ tại $a$ khi và chỉ khi:

$$
\forall \epsilon > 0, \exists \eta > 0, \forall x \in X, \text{nếu } d_E(x, a) \le \eta \text{ thì } d_F(f(x), l) \le \epsilon.
$$

### 1.2. Giới hạn của hàm số tại vô cùng

#### 1.2.1. Giới hạn tại $+\infty$

- Nếu $f: [a, +\infty) \to F$ ($a \in \mathbb{R}$) và $l \in F$, thì $f$ có giới hạn $l$ tại $+\infty$ khi và chỉ khi:

$$
\forall \epsilon > 0, \exists A > 0, \forall x \ge A \implies d_F(f(x), l) \le \epsilon.
$$

#### 1.2.2. Giới hạn tại $-\infty$

- Nếu $f: (-\infty, a] \to F$ ($a \in \mathbb{R}$) và $l \in F$, thì $f$ có giới hạn $l$ tại $-\infty$ khi và chỉ khi:

$$
\forall \epsilon > 0, \exists A > 0, \forall x \le -A \implies d_F(f(x), l) \le \epsilon.
$$

### 1.3. Giới hạn khi $\|x\|_E$ dần tới vô cùng

- Nếu $f: E \to F$ và $l \in F$, ta nói $f$ có giới hạn $l$ khi $\|x\|_E$ dần tới $+\infty$ khi và chỉ khi:

$$
\forall \epsilon > 0, \exists A > 0, \|x\|_E \ge A \implies d_F(f(x), l) \le \epsilon.
$$

### 1.4. Giới hạn $+\infty$ tại một điểm

- Nếu $a \in X$, $f: X \to \mathbb{R}$, ta nói $f$ có giới hạn $+\infty$ tại $a$ khi và chỉ khi:

$$
\forall A > 0, \exists \eta > 0, \forall x \in X, \text{nếu } d_E(x, a) \le \eta \text{ thì } f(x) \ge A.
$$

### 1.5. Giới hạn $-\infty$ tại một điểm

- Nếu $a \in X$, $f: X \to \mathbb{R}$, ta nói $f$ có giới hạn $-\infty$ tại $a$ khi và chỉ khi:

$$
\forall A < 0, \exists \eta > 0, \forall x \in X, \text{nếu } d_E(x, a) \le \eta \text{ thì } f(x) \le A.
$$

## 2. Các định lý về giới hạn

### 2.1. Tính duy nhất của giới hạn

- **Định lý:** Nếu $f$ có các giới hạn $l$ và $l'$ tại $a$ thì $l = l'$.
- **Chứng minh:** Giả sử $l \ne l'$, thì tồn tại một khoảng cách $\epsilon > 0$ sao cho $d_F(l, l') > \epsilon$. Theo định nghĩa giới hạn, tồn tại $\eta_1 > 0$ và $\eta_2 > 0$ sao cho:

$$
d_F(f(x), l) < \frac{\epsilon}{2} \quad \text{và} \quad d_F(f(x), l') < \frac{\epsilon}{2} \quad \text{khi} \quad d_E(x, a) < \min(\eta_1, \eta_2).
$$

Điều này dẫn đến mâu thuẫn vì $d_F(l, l') \le d_F(l, f(x)) + d_F(f(x), l') < \frac{\epsilon}{2} + \frac{\epsilon}{2} = \epsilon$, không thể đồng thời lớn hơn $\epsilon$. Vậy $l = l'$.

### 2.2. Giới hạn hữu hạn và tính bị chặn

- **Định lý:** Nếu $f$ có giới hạn hữu hạn tại $a$ thì $f$ bị chặn trong lân cận của $a$.
- **Chứng minh:** Giả sử $f$ có giới hạn $l$ tại $a$, thì theo định nghĩa:

$$
\forall \epsilon > 0, \exists \eta > 0, \forall x \in X, d_E(x, a) \le \eta \implies d_F(f(x), l) \le \epsilon.
$$

Chọn $\epsilon = 1$, ta có:

$$
\exists \eta > 0, \forall x \in X, d_E(x, a) \le \eta \implies d_F(f(x), l) \le 1.
$$

Điều này có nghĩa là trong lân cận $V = \{x \in X \mid d_E(x, a) \le \eta\}$, giá trị của $f(x)$ bị chặn bởi $l + 1$ và $l - 1$.

### 2.3. Điều kiện cần và đủ cho giới hạn hữu hạn

- **Định lý:** Để $f: X \to F$ có giới hạn hữu hạn $l \in F$ tại $a \in X$, điều kiện cần và đủ là $f(u_n) \to l$ với mọi dãy $(u_n)$ các phần tử của $X$ thoả mãn $(u_n) \to a$.
- **Chứng minh:** 

  - **Điều kiện cần:** Giả sử $f$ có giới hạn $l$ tại $a$, thì theo định nghĩa:

    $$
    \forall \epsilon > 0, \exists \eta > 0, \forall x \in X, d_E(x, a) \le \eta \implies d_F(f(x), l) \le \epsilon.
    $$

    Với mọi dãy $(u_n)$ sao cho $u_n \to a$, tồn tại $N \in \mathbb{N}$ sao cho $d_E(u_n, a) < \eta$ khi $n \ge N$. Do đó, $d_F(f(u_n), l) < \epsilon$ khi $n \ge N$, hay $f(u_n) \to l$.

  - **Điều kiện đủ:** Giả sử $f(u_n) \to l$ với mọi dãy $(u_n) \to a$, ta cần chứng minh $f$ có giới hạn $l$ tại $a$. Giả sử ngược lại rằng $f$ không có giới hạn $l$ tại $a$, thì tồn tại $\epsilon > 0$ sao cho với mọi $\eta > 0$, tồn tại $x \in X$ với $d_E(x, a) \le \eta$ nhưng $d_F(f(x), l) > \epsilon$. Điều này mâu thuẫn với giả thiết rằng $f(u_n) \to l$ với mọi dãy $(u_n) \to a$. Vậy $f$ phải có giới hạn $l$ tại $a$.

### 2.4. Định lý kẹp đối với các hàm lấy giá trị trên $\mathbb{R}$

- **Định lý:** Cho $a \in X$, $f, g, h: X \to \mathbb{R}$, $l \in \mathbb{R}$. Nếu:
  - $f$ và $h$ có giới hạn $l$ tại $a$.
  - $\exists V \in \mathcal{V}_E(a), \forall x \in V, f(x) \le g(x) \le h(x)$

  thì $g$ có giới hạn $l$ tại $a$.

- **Chứng minh:** Giả sử $f(x) \le g(x) \le h(x)$ trong lân cận $V$ của $a$. Với $\epsilon > 0$, tồn tại $\eta_1$ và $\eta_2$ sao cho:

  $$
  d_E(x, a) < \eta_1 \implies |f(x) - l| < \epsilon,
  $$

  và

  $$
  d_E(x, a) < \eta_2 \implies |h(x) - l| < \epsilon.
  $$

  Chọn $\eta = \min(\eta_1, \eta_2)$, ta có $d_E(x, a) < \eta$ dẫn đến:

  $$
  l - \epsilon < f(x) \le g(x) \le h(x) < l + \epsilon,
  $$

  hay $|g(x) - l| < \epsilon$, do đó $g(x) \to l$ khi $x \to a$.


## Tính Liên Tục Của Hàm Số

### 1. Định nghĩa về tính liên tục

#### 1.1. Liên tục tại một điểm

Cho $X \subseteq E$, $f: X \to F$, $a \in X$, ta nói rằng $f$ liên tục tại $a$ khi và chỉ khi:

$$
\forall \epsilon > 0, \exists \eta > 0, \forall x \in X, d_E(x, a) < \eta \implies d_F(f(x), f(a)) < \epsilon.
$$

Nói cách khác, $f$ liên tục tại $a$ nếu khi $x$ tiến gần đến $a$ thì $f(x)$ tiến gần đến $f(a)$ theo nghĩa của khoảng cách trong không gian $F$. Điều này có nghĩa là với mọi khoảng cách $\epsilon$ tùy ý nhỏ trong $F$, ta có thể tìm được một khoảng cách $\eta$ trong $E$ sao cho nếu $x$ nằm trong khoảng cách $\eta$ từ $a$, thì $f(x)$ sẽ nằm trong khoảng cách $\epsilon$ từ $f(a)$.

#### 1.2. Gián đoạn tại một điểm

- Khi $f$ không liên tục tại $a$, ta nói $f$ bị gián đoạn tại $a$.

#### 1.3. Liên tục trên một tập hợp

- Hàm $f$ được gọi là liên tục trên $X \subseteq E$ khi và chỉ khi $f$ liên tục tại mọi điểm $a \in X$.

- Ký hiệu các hàm liên tục $f: X \to F$ là $C(X, F)$.

### 2. Tính chất của hàm liên tục

#### 2.1. Tính chất mở và đóng của hàm liên tục

Cho $X \subseteq E$, $f: X \to F$, ta có các mệnh đề sau đây đôi một tương đương nhau:

1. **$f$ liên tục.**
2. **$f^{-1}(U)$ là một tập mở của $E$ nếu $U$ là tập mở của $F$.**
3. **$f^{-1}(V)$ là một tập đóng của $E$ nếu $V$ là một tập đóng của $F$.**

#### 2.2. Tính liên tục của hàm hợp

Cho $E, F, G$ là ba không gian vector định chuẩn, $X \subseteq E, Y \subseteq F$, $f: X \to F$, $g: Y \to G$ thỏa mãn $f(X) \subseteq Y$. 

- Nếu:
  - $a \in X$.
  - $f$ liên tục tại $a$.
  - $g$ liên tục tại $f(a)$.
  
  Thì $(g \circ f)(x) = g(f(x))$ liên tục tại $a$.

- Nếu $f$ liên tục trên $X$ và $g$ liên tục trên $Y$ thì $g \circ f$ liên tục trên $X$.

#### 2.3. Một số tính chất khác

- **Bảo toàn tính chất mở:** Hàm liên tục bảo toàn tính chất mở, tức là ảnh ngược của một tập mở dưới hàm liên tục là một tập mở.
- **Bảo toàn tính chất đóng:** Hàm liên tục cũng bảo toàn tính chất đóng, tức là ảnh ngược của một tập đóng dưới hàm liên tục là một tập đóng.
- **Liên tục của phép cộng và nhân:** Nếu $f, g: X \to F$ là hai hàm liên tục, thì hàm tổng $f + g$ và hàm tích $fg$ (nếu định nghĩa được) cũng liên tục trên $X$.
- **Liên tục của hàm hằng:** Mọi hàm hằng đều liên tục trên toàn miền xác định của nó.

#### 2.4. Ví dụ về hàm liên tục và gián đoạn

- **Ví dụ 1:** Hàm số $f(x) = x^2$ liên tục trên $\mathbb{R}$ vì với mọi $\epsilon > 0$, ta có thể tìm được $\eta = \sqrt{\epsilon}$ sao cho $|x - a| < \eta$ dẫn đến $|x^2 - a^2| < \epsilon$.

- **Ví dụ 2:** Hàm số $f(x) = \frac{1}{x}$ không liên tục tại $x = 0$ vì khi $x$ tiến dần đến 0, $f(x)$ không tiến dần đến một giá trị hữu hạn mà tiến đến vô cùng.

## 1. Hàm C-Lipschitz

### 1.1. Định nghĩa

Cho $(E, \|\cdot\|)$ và $(F, \|\cdot\|_F)$ là hai không gian vector định chuẩn, $X \subseteq E$, và $f: X \to F$. Ta gọi $f$ là hàm C-Lipschitz khi và chỉ khi:

$$
\exists C \in \mathbb{R}, \forall (x, y) \in X^2, d_E(x, y) \leq C d_F(f(x), f(y)).
$$

Nói cách khác, có một hằng số $C$ sao cho khoảng cách giữa các giá trị của hàm $f$ luôn bị chặn bởi $C$ nhân với khoảng cách giữa các đối số tương ứng.

## 2. Hàm Liên Tục Đều

### 2.1. Định nghĩa

Cho $(E, \|\cdot\|)$ và $(F, \|\cdot\|_F)$ là hai không gian vector định chuẩn, $X \subseteq E$, và $f: X \to F$. Ta gọi $f$ là liên tục đều (uniformly continuous) khi và chỉ khi:

$$
\forall \epsilon > 0, \exists \alpha > 0, \forall (x, y) \in X^2, d_E(x, y) \leq \alpha \implies d_F(f(x), f(y)) < \epsilon.
$$

Điều này có nghĩa là với mọi $\epsilon > 0$, ta có thể tìm được một $\alpha > 0$ sao cho nếu khoảng cách giữa $x$ và $y$ trong $E$ nhỏ hơn $\alpha$, thì khoảng cách giữa $f(x)$ và $f(y)$ trong $F$ sẽ nhỏ hơn $\epsilon$.

### 2.2. Quan hệ giữa hàm C-Lipschitz và liên tục đều

- Mọi ánh xạ C-Lipschitz đều liên tục đều. Điều này xuất phát từ định nghĩa của hàm C-Lipschitz khi hằng số $C$ đã đảm bảo tính liên tục đều của hàm.

## 3. Độ Mịn của Khoảng Cách

### 3.1. Định nghĩa

Cho $E$ là một không gian vector định chuẩn được trang bị hai chuẩn $N_1$ và $N_2$, $d_1$ và $d_2$ là hai khoảng cách liên kết với hai chuẩn $N_1$ và $N_2$:

- Ta gọi $d_1$ “mịn” hơn (finer than) $d_2$ khi và chỉ khi ánh xạ $Id_E: (E, d_1) \to (E, d_2)$ là hàm Lipschitz, tức là:

$$
\exists C \in \mathbb{R}, d_1 \leq C d_2.
$$

### 3.2. Tính chất

- Nếu $d_1$ mịn hơn $d_2$, thì ta có:

$$
N_1(x_n) \to 0 \implies N_2(x_n) \to 0.
$$

## 4. Tương Đương của Khoảng Cách

### 4.1. Định nghĩa

Cho $E$ là một không gian vector định chuẩn được trang bị hai chuẩn $N_1$ và $N_2$, $d_1$ và $d_2$ là hai khoảng cách liên kết với hai chuẩn $N_1$ và $N_2$:

- Ta gọi $d_1$ và $d_2$ là tương đương nhau khi và chỉ khi $d_1$ mịn hơn $d_2$ và ngược lại, tức là:

$$
\exists (\alpha, \beta) \in \mathbb{R}, \alpha d_1 \leq d_2 \leq \beta d_1.
$$

# Không gian Topo

## Định nghĩa tập mở trong không gian vector định chuẩn

Cho $(E,d)$ là một không gian vector định chuẩn. Một bộ phận $\Omega \in E$ được gọi là mở khi và chỉ khi:

$$\forall x \in E, \Omega \in \mathcal{V}_E(x)$$

Chú thích:
- $E$ là một không gian vector và $d$ là hàm định chuẩn (biểu diễn khoảng cách trong không gian $E$).
- $\mathcal{V}_E(x)$ là tập hợp tất cả các lận cận của $x$ trong không gian vector $E$.

Tính chất:
-  $\emptyset$ và $E$ là những tập mở của $E$.
- Với mọi $I$ và họ các tập mở $`(\Omega_i)_{i \in I}`$ của $E$, $\cup_{i \in I}\Omega_i$ là một tập mở của $E$.
- Với mọi $n \in N^{*}$ và các tập mở $\Omega_{1,2,...,n}$ của $E$, $\cap_{1 \leq i \leq n}\Omega_i$ là tập mở của $E$.

Lưu ý: Giao vô hạn các tập mở trong $E$ có thể không là tập mở trong $E$.

## Định nghĩa cấu trúc Topo

Cho tập hợp $X$, giả sử $\mathcal{T}$ là một họ các tập con của $X$. Họ $\mathcal{T}$ được gọi là một cấu trúc Topo trên tập $X$ (hay $\mathcal{T}$ là một Topo trên $X$) nếu thỏa mãn các điều kiện sau:
1. Tập rỗng $\emptyset$ và tập $X$ là các phần tử của họ $\mathcal{T}$.
2. Hợp của một họ con tùy ý các phần tử của họ $\mathcal{T}$ là phần tử của họ $\mathcal{T}$.
3. Giao của hai phần tử tùy ý của họ $\mathcal{T}$ là phần tử của họ $\mathcal{T}$.

Chú thích:
- Nếu $(X,\mathcal{T})$ được gọi là không gian Topo thì $\mathcal{T}$ là một Topo của $X$. Các phần tử trong $\mathcal{T}$ được gọi là các tập mở trong $X$ đối với Topo $\mathcal{T}$, hay gọi là tập $\mathcal{T}-mở$.
- Ký hiệu $\mathcal{T}$ là họ tất cả các tập mở trong không gian metric $(X,d)$. Ta có $\mathcal{T}$ là một Topo trên $X$ và gọi là Topo metric phù hợp với metric $d$.
- Mọi không gian metric đều là không gian Topo, tuy nhiên điều ngược lại thì không đúng bởi vì vẫn tồn tại một số không gian Topo nhưng không thể metric hóa.

## Định nghĩa lân cận

Cho không gian Topo $(X,\mathcal{T})$, A $\subset X$. Một tập con U của không gian Topo $X$ (U $\subseteq X$) được gọi là lân cận của tập A nếu có một tập mở trong $\mathcal{T}$ chứa A và nằm trong U. Biết rằng, một lân cận của một phần tử x $\in X$ là lận cận của tập con {x}.

Chú ý:
- Lân cận của một điểm không nhất thiết là một tập mở, nhưng mỗi tập mở bất kỳ là lân cận của mọi điểm thuộc nó.
- Nếu lân cận của một điểm là một tập mở thì ta nói đó là lân cận mở của điểm đó.

Ví dụ: Một không gian Topo $(X,\mathcal{T})$, với $X$ = {a,b,c,d} và $\mathcal{T}$ = {$`\emptyset`$, {a,b}, {c}, {a,b,c}, $X$}. Cho A = {a,b} thì lân cận của A có thể là {a,b}, {a,b,c}, {a,b,d} và {a,b,c,d}. Trong đó, {a,b,d} không là lân cận mở.

## Định nghĩa tập đóng

### 1. Không gian vector định chuẩn

Cho $(E,d)$ là một không gian vector định chuẩn. Tập con $F \in E$ là tập đóng khi và chỉ khi $C_E(F) = E\backslash F$ là tập mở.

Tính chất:
-  $\emptyset$ và $E$ là những tập đóng của $E$.
- Với mọi tập $I$ và mọi họ các tập con đóng $`(F_i)_{i \in I}`$ của $E$, $\cap_{i \in I}$$`F_i`$ là một tập đóng của $E$.
- Với mọi $n \in N^*$ và mọi tập đóng $`(F_i)_{1 \leq i \leq n}`$ của $E$, $\cup_{1 \leq i \leq n}F_i$ là tập đóng của $E$.

Lưu ý: Hợp vô hạn các tập đóng trong $E$ có thể không là tập đóng trong $E$.

### 2. Không gian Topo

Tập con A của không gian Topo $(X,\mathcal{T})$ được gọi là tập đóng nếu phần bù của A trong X là tập mở (tập X \ A là $\mathcal{T}$ - mở).

**Định lý đặc trưng họ các tập đóng:** Cho một không gian Topo $(X,\mathcal{T})$. Gọi $\mathcal{F}$ là họ tất cả các tập con đóng trong $X$. Khi đó họ $\mathcal{F}$ thỏa mãn các điều kiện sau:
- Tập $\emptyset$ và tập X thuộc $\mathcal{F}$.
- Giao của một họ con khác rỗng tùy ý các phần tử của $\mathcal{F}$ là phần tử của $\mathcal{F}$.
- Hợp của hai phần tử bất kỳ của $\mathcal{F}$ là phần tử của $\mathcal{F}$.

$$\mathcal{T} = \\{U \subset X | U = X \backslash A, A \in \mathcal{F}\\}$$

## Khái niệm các loại điểm

Trong không gian Topo $(X, \mathcal{T})$. Cho $A$ là một tập con của không gian Topo $X$, đối với mỗi phần tử $a \in X$ :
- $a$ là điểm trong của $A$ nếu tồn tại ít nhất một lân cận của $a$ nằm trong $A$. Tập hợp các điểm trong của $A$ ký hiệu là $Int(A)$.
- $a$ là điểm ngoài của $A$ nếu tồn tại ít nhất một lân cận của $a$ nằm trong $X\backslash A$. Tập hợp các điểm ngoài của $A$ ký hiệu là $Ext(A)$.
- $a$ là điểm dính của $A$ nếu mọi lân cận của $a$ giao với $A$ đều khác rỗng, tức là $\forall V \in \mathcal{V}_X(a), V \cap A \neq \emptyset$. Tập hợp các điểm dính của $A$ ký hiệu là $Adh(A)$.
- $a$ là điểm biên của $A$ nếu $a$ đồng thời không là điểm trong và điểm ngoài của $A$. Hay nói cách khác là mọi lân cận của $a$ đều giao khác rỗng với $A$ và $X \backslash A$. Tập hợp các điểm biên của $A$ ký hiệu là $Fr(A) = Adh(A) \cap Adh(X\backslash A)$ còn được gọi là biên của $A$.
- $a$ là điểm tụ của $A$ nếu mọi lân cận của $a$ giao với $A \backslash \\{a\\}$ đều khác rỗng, tức là $\forall V \in \mathcal{V}_X(a), V \cap A \backslash \\{a\\} \neq \emptyset$. Tập hợp các điểm tụ của $A$ ký hiệu là $Acc(A)$.
- $a$ là điểm cô lập của $A$ nếu $a$ thuộc $A$ và không có điểm nào trong $A$ nằm trong bất kỳ lân cận nào của $a$, tức là $a \in A$ và $a \notin Acc(A)$. Ta gọi $A$ là tập rời rạc của $X$ nếu mọi phần tử trong $A$ đều là điểm cô lập.

**Mệnh đề 1**: $Int(A)$ là tập mở lớn nhất (theo nghĩa bao hàm) có bao hàm $A$.

- **Chứng minh**: Giả sử $U$ là tập mở bất kì trong $A$. Khi đó, $U$ là lân cận của mọi điểm thuộc nó, nghĩa là $\forall x \in U$, ta có $x \in U \subset A$. Suy ra, mọi điểm nằm trong $U$ là điểm trong của $A$. Do đó, $U \subseteq Int(A)$. Vậy $Int(A)$ là tập mở lớn nhất trong $A$.

**Mệnh đề 2**: $Adh(A)$ là tập đóng nhỏ nhất (theo nghĩa bao hàm) có bao hàm $A$.

- **Chứng minh** $Adh(A)$ **là một tập đóng**: Giả sử $x \in X \backslash Adh(A)$, nên $x$ không phải là điểm dính của $A$, nghĩa là không phải mọi lân cận của $x$ đều giao với $A$. Do đó, tồn tại một lân cận mở $U$ của $x$ mà không có điểm chung với $A$, tức là $U \cap A = \emptyset$. Vậy ta sẽ có $\forall x \in U \subseteq X \backslash Adh(A)$. Vậy $Adh(A)$ là tập đóng vì phần bù của nó là tập mở.
- **Chứng minh**: Giả sử $C$ là một tập đóng bất kì sao cho $A \subseteq C$. Khi đó, tất cả các điểm dính của $A$ phải nằm trong $C$ nên $Adh(A) \subseteq C$. Các điểm trong $A$ đều là điểm dính của $A$ vì lân cận của mỗi điểm trong $A$ giao với $A$ khác rỗng. Do đó, $A \subseteq Adh(A)$. Vì $Adh(A)$ là tập đóng và mọi tập đóng chứa $A$ đều phải chứa $Adh(A)$ nên $Adh(A)$ là tập đóng nhỏ nhất chứa $A$.

**Hệ quả**: $A$ là tập đóng khi và chỉ khi $A = Adh(A)$.
- **Chứng minh**:
  - Nếu $A$ là tập đóng thì các điểm trong $A$ đều là điểm dính, do đó $Adh(A) = A$.
  - Nếu $Adh(A) = A$, cần chứng minh $Adh(A)$ là tập đóng để kết luận được $A$ là một tập đóng.

## Định nghĩa trù mật 

Trong một không gian Topo $(X, \mathcal{T})$, giả sử $A \subset B \subset X$. Ta có $A$ là trù mật của $B$ khi và chỉ khi $B \subset Adh(A)$. Ta gọi A là trù mật trong $X$ khi và chỉ khi mọi lân cận của mọi phần tử trong $X$ đều giao với $A$ khác rỗng, ký hiệu là  $X = Adh(A)$. 

**Định lý sự đồng nhất ánh xạ trên tập trù mật**: Cho $E$ và $F$ là hai không gian Topo, $f:E \rightarrow F$ và $g:E \rightarrow F$ là hai ánh xạ trên $E$ và $F$. Giả sử:
- $D \subset E$ là tập con trù mật của $E$.
- $\forall x \in D$, $f(x) = g(x)$.
$\Rightarrow f = g$.

Nếu $D \subset E$ không phải là tập con trù mật của $E$, thì việc $f$ và $g$ đồng nhất trên $D$ không đảm bảo rằng chúng sẽ đồng nhất trên $E$.

# Không gian Compact

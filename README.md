# Không gian Metric

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

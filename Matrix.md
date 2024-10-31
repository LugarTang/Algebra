$$
这里定义了许多我的自定义符号。
\newcommand{\dif}{\mathop{}\!\mathrm{d}}
\newcommand{\matl}{\left(\begin{matrix}}
\newcommand{\matr}{\end{matrix}\right)}
\newcommand{\rank}{\text{rank }}
$$

# Matrix 矩阵

## 记法

$$
\textbf{matrix }A.\\
\text{If }A\left(\begin{matrix}i\\j\end{matrix}\right)=a_{i,j},\\
\text{then set down }A\text{ as }(a_{i,j}).
$$

## 称法

若数域上的n级矩阵A的行列式非零，称为**非退化的**；否则称为**退化的**。

可以写二分之一A不可以写二分之A.

$$
Definition:\\
A\ is\ a\ m\times p\ matrix,\ and\ B\ is\ a\ p\times n\ matrix.\\
C=AB,c_{ij}=a_{ik}*b_{kj}.(i\in[1,m]\cap\mathbb{N},\ j\in[1,n]\cap\mathbb{N},\ k\in[1,p]\cap\mathbb{N}).\\
\left(
\begin{matrix}
\alpha1\\
\alpha2\\
\vdots
\end{matrix}
\right)
*(\beta1,\beta2,\cdots)=i，j元为\alpha_i\beta_j
$$

**两个矩阵相乘的意义是将右边矩阵中的每一列向量** ![[公式]](https://www.zhihu.com/equation?tex=a_i) **变换到左边矩阵中以每一行行向量为基所表示的空间中去。**也就是说一个矩阵可以表示一种线性变换。i,j元即为A的i行乘B的j列.

矩阵乘法可以理解成“一个向量组由另一个向量组表出”的矩阵表示，其实相似之类的关系都是这个的一种形式。

我们知道,行/列初等变换不过是左/右乘elementary matrix的结果啊。

满足结合律。

左

$$
A(B+C)=AB+AC
$$

右分配律

$$
(B+C)A=BA+CA
$$

不满足交换律。

若AB=BA，称它们可交换。这是一个有点复杂的问题，以后可以研究一下。

两边同乘A不可消去。

$$
\text{For matrix }A,\\
\text{if }\exist B,s.t.\ AB=0,\text{then call A a }\textbf{left zero divisor（左零因子）};\\
\text{if }\exist B,s.t.\ BA=0,\text{then call A a }\textbf{right zero divisor（右零因子）}.\\
\text{They are all }\textbf{zero divisors（零因子）}.\\
\textbf{zero matrix}\text{ is called 平凡零因子}，别的都是非平凡的。
$$

A是非零方阵，规定其0次方为单位矩阵。

$$
(A+B)^2=A^2+B^2+AB+BA\\
^t(AB)=^tB\ ^tA
$$

$$
A=
\left(
\begin{matrix}
a_{1,1}&a_{1,2}&\cdots&a_{1,n}\\
a_{2,1}&a_{2,2}&\cdots&a_{2,n}\\
\vdots&\vdots&\ddots&\vdots\\
a_{n,1}&a_{n,2}&\cdots&a_{n,n}\\
\end{matrix}
\right)\\
X=
\left(
\begin{matrix}
x_{1}\\
x_{2}\\
\vdots\\
x_{n}\\
\end{matrix}
\right)\\
\beta=
\left(
\begin{matrix}
b_{1}\\
b_{2}\\
\vdots\\
b_{n}\\
\end{matrix}
\right)\\
AX=\beta\\
$$

$$
\textbf{Fact:}\\
\rank(A^TA)=\rank(AA^T)=\rank(A)\\
\textbf{Proof:}\\
\text{Suppose }(A^TA)X=0,\ AX=0\text{ have same }\textbf{solution}.\Rightarrow\text{They have same }\textbf{solution space}.\\\Rightarrow n-\rank(A^TA)=\dim U=n-\rank(A)\Rightarrow\rank(A^TA)=\rank(A).\\
\text{Then we prove }(A^TA)X=0,\ AX=0\text{ have same }\textbf{solution}.\\
\forall\eta\ s.t.\ A\eta=0,exists\ (A^TA)\eta=A^T(A\eta)=0.\\
\forall\eta\ s.t.\ (A^TA)\eta=0\Rightarrow\eta^TA^TA\eta=0\Leftrightarrow(A\eta)^T(A\eta)=0.\\
\text{Let }A\eta=
\left(
\begin{matrix}
b_{1}\\
b_{2}\\
\vdots\\
b_{n}\\
\end{matrix}
\right),\text{then }\\
\left(
\begin{matrix}
b_{1}&b_{2}&\cdots&b_{n}\\
\end{matrix}
\right)
\left(
\begin{matrix}
b_{1}\\
b_{2}\\
\vdots\\
b_{n}\\
\end{matrix}
\right)
=|a_{i,j}=b_ib_j|=0\\
\Rightarrow b_i^2=0\Leftrightarrow b_i=0\\
\textbf{Extrapolation:}\\
\rank(AA^TA)\leq\rank(A)=\rank(AA^T)=\rank(AA^TAA^T)\leq\rank(AA^TA)\\
\Rightarrow\rank(AA^TA)=\rank(A)
$$

Sylvester & 乘积 rank inequality 秒掉。

注意AI=A这种代换方式。

$$
\forall\ matrix\ whose\ rank=r,\exist列满秩的B_{m\times r}和行满秩的矩阵C_{r\times n},s.t.A=BC.\\
\textbf{Proof:}\\
A的列向量组可由极大无关组表出，故\\
A=(\alpha_{i_1},\cdots,\alpha_{i_r})C\\
r\geq\rank(C)\geq\rank(A)=r
$$

## Binet-Cauchy Formula

$$
\textbf{Binet-Cauchy Formula:}\\
A_{n\times s}B_{s\times n}
\begin{cases}|AB|=0:s<n.\\
A的各级n阶子式与b的对应子式乘积之和:s\geq n.\\
\end{cases}
\\
$$

用分块矩阵的初等行列变换证明的。

Extrapolation：

考虑AB的r阶子式。

r>s 0

$$
r\leq s
$$

$$
(AB)\left(
\begin{matrix}
i_1,i_2,\cdots,i_r\\
j_1,j_2,\cdots,j_r
\end{matrix}
\right)=(A)\left(
\begin{matrix}
i_1,i_2,\cdots,i_r\\
1,2,\cdots,s
\end{matrix}
\right)(B)\left(
\begin{matrix}
1,2,\cdots,s\\
j_1,j_2,\cdots,j_r
\end{matrix}
\right).
$$

对右式使用Binet-Cauchy Formula.

$(右式行列式)
=\sum |A\left(
\begin{matrix}
i_1,i_2,\cdots,i_r\\
v_1,v_2,\cdots,v_r
\end{matrix}
\right)||
B\left(
\begin{matrix}
v_1,v_2,\cdots,v_r\\
j_1,j_2,\cdots,j_r\\
\end{matrix}
\right) |$.

v取遍s的全排列.

推论：

AB皆为方阵时，$|AB|=|A||B|$.

$A\in\mathbb R,AA^T$的r阶主子式均非负，因为那时候 Binet-Cauchy Formula拆出来的两个行列式相等。

### Cauchy Identity 柯西恒等式

When $n\geq2$,$\begin{aligned} &\left(\sum_{i=1}^{n} a_{i} c_{i}\right)\left(\sum_{i=1}^{n} b_{i} d_{i}\right)-\left(\sum_{i=1}^{n} a_{i} d_{i}\right)\left(\sum_{i=1}^{n} b_{i}c_i\right)=\sum_{1 \leq j<k \leq n}\left(a_{j} b_{k}-a_{k} b_{j}\right)\left(c_{j} d_{k}-c_{k} d_{j}\right) \end{aligned}$.

Proof:

$$
\begin{aligned}
&\left(\begin{array}{cc}
\sum_{i=1}^{n} a_{i} c_{i} & \sum_{i=1}^{n} a_{i} d_{i} \\
\sum_{i=1}^{n} b_{i} c_{i} & \sum_{i=1}^{n} b_{i} d_{i}
\end{array}\right)=\left(\begin{array}{lll}
a_{1} & a_{2} & \cdots & a_{n} \\
b_{1} & b_{2} & \cdots & b_{n}
\end{array}\right)\left(\begin{array}{cc}
c_{1} & d_{1} \\
c_{2} & d_{2} \\
\vdots & \vdots\\
c_n&d_n
\end{array}\right)
\end{aligned}
$$

Then Binet-Cauchy Formula.

# 分块矩阵

与数学归纳法结合非常好用。

## 初等行/列变换

出现单位矩阵会比较好使。

将一个分块单位矩阵经过一次分块矩阵的初等行列变换形成的矩阵叫做分块初等矩阵。

分块初等矩阵可以写成很多初等矩阵的乘积。

可以证明，分块矩阵的初等行/列变换相当于用一个对应的分块初等矩阵左/右乘它。

---

1，把一个块行/列的左/右非零K倍加到另一个块行/列上。

若为方阵，行列式不变。两边取行列式即证。

$$
\left(
\begin{matrix}
A&B\\
KA+C&KB+D\\
\end{matrix}
\right)
=
\left(
\begin{matrix}
I&0\\
K&I\\
\end{matrix}
\right)
\left(
\begin{matrix}
A&B\\
C&D\\
\end{matrix}
\right)
两边取行列式即证。(行变多也一样的呐)
$$

---

2，两个块行/列互换位置。

假设行换，要换的两行，内部行数n_1,n_2中间隔着的行内部行数分别为n_3,n_4...n_k

换完后行列式乘

$$
(-1)^{\sum\limits_{1\leq i<j\leq k}n_in_j}
$$

.

---

3，用一个可逆矩阵K（为了不改变rank，要能运算回去）左/右乘某一块行/列。

行列式变为|K|倍，同样，两边取行列式即证。

$$
\left(
\begin{matrix}
KA&KB\\
C&D\\
\end{matrix}
\right)
=
\left(
\begin{matrix}
K&0\\
0&I\\
\end{matrix}
\right)
\left(
\begin{matrix}
A&B\\
C&D\\
\end{matrix}
\right)
两边取行列式即证。
$$

---

如果一个矩阵非常整齐，可以考虑它是不是由两个矩阵乘出来的。

$$
A(i,j)=a_ib_j-1
A=(a一列 1一列)(b一行 -1一行)
$$

$$
\alpha=\matl a_1&a_2&\cdots&a_m\\-1&-1&\cdots&-1\matr,\beta=\matl 1&1&\cdots&1\\b_1&b_2&\cdots&b_n\matr.\\
\alpha^T\beta=A,A\left(\begin{matrix}i\\j\end{matrix}\right)=a_i-b_j.
$$

## 运算

即把矩阵看成**元素为矩阵**的矩阵.

常用变换：

$$
\rank(A)+\rank(B)=n.\Leftrightarrow\rank\left(
\begin{matrix}
A&0\\
0&B\\
\end{matrix}
\right)
=n.
$$

$|A|=\left|\matl A&X\\0&I \matr\right|$.

一个有趣的例题：

$$
一堆n级矩阵\\
\sum\limits_{i=1}^mA_i=I_n,\ \sum\limits_{i=1}^m\rank(A_i)=n.
prove:\ Ai^2=A_i.\\
Let\ m=2\\
\left(
\begin{matrix}
A&0\\
0&B\\
\end{matrix}
\right)
=
\left(
\begin{matrix}
A&0\\
A&B\\
\end{matrix}
\right)
=
\left(
\begin{matrix}
A&0\\
A+B&B\\
\end{matrix}
\right)
=
\left(
\begin{matrix}
A&0\\
I&B\\
\end{matrix}
\right)
=
\left(
\begin{matrix}
0&-AB\\
I&B\\
\end{matrix}
\right)\\
n=\rank\left(
\begin{matrix}
A&0\\
0&B\\
\end{matrix}
\right)=\rank\left(
\begin{matrix}
0&-AB\\
I&B\\
\end{matrix}
\right)=n+\rank(AB)\\
AB=0\\
m>2时，
把后面的全部括起来当成一个矩阵。
n=\rank(\sum\limits_{i=1}^mA_i)\leq\rank(A_1)+\rank(\sum\limits_{i=2}^mA_i)\leq\sum\limits_{i=1}^m\rank(A_i)=n完了。
$$

分块矩阵求转置不仅要把元素转置，而且每个元素自身也得转置。

分块对角矩阵：主对角线上的所有子矩阵都是方阵，别的地方全是0.

记作

$$
diag|A_1,A_2,\cdots,A_s|
$$


同理有分块上三角矩阵。

分块矩阵运算时，把每块小矩阵看成数。加法要求分块的方式相同。做加法时常用的分块：按行/列分块。

乘法：首先要保证大矩阵可乘（A的列分法与B的行分法一样），还要保证每一个元素都可以做乘法。

### A乘B常用的分块方式

1，A看成一块，B按列分块。

$$
A(\beta_1,\beta_2,\cdots) = (A\beta_1,A\beta_2,\cdots)
$$

$$
A_{m\times n}B_{n\times s}=0\Rightarrow r(A)+r(B)\leq n\\
由上知：A\beta_i=0,即\beta_i都为Ax=0的解\\
\rank(B)\leq\dim V=n-\rank(A)\\
要是你里面有一个满秩的，就可以推出来另外一个肯定为0，这个就给了一种可能，实现“方程两边同时消去”。
$$

**这个式子让我们可以引进齐次线性方程组的知识来解决AB=0一类的问题。**

给出一个解矩阵乘法方程的例子：

$$
AX=B\\
A=
\left(
\begin{matrix}
1&-3\\
-2&6
\end{matrix}
\right)
B=
\left(
\begin{matrix}
-1&0&-2\\
2&0&4
\end{matrix}
\right)=(\beta_1\ \beta_2\ \beta_3)\\
\text{Let }X=(X_1,X_2,X_3),\text{ then }AX_i=\beta_i.
就是说直接把（A\ B）化最简阶梯形，我懒得搞了。
$$

2,A按照列分块，B的每个元素自己为一块。

$$
\rank (AB)\leq\rank A\\
\text{for }AB\text{ can be }\textbf{linearly expressed}\text{ by }A.
$$

(AB中的元素都是A中向量的线性组合。)

一个向量可以由向量组线性表出，就可以写成矩阵乘法的形式。

$$
\beta = (\alpha_1,\alpha_2,\cdots)
\left(
\begin{matrix}
k_1\\k_2\\\vdots\\
\end{matrix}
\right)\\
so\ v.g.\{\beta\}\ can\ also\ be\ set\ down\ as\\
(\beta_1,\beta_2,\cdots) = (\alpha_1,\alpha_2,\cdots)
\left(
\begin{matrix}
k_{1,1}&k_{1,2}\cdots\\
k_{2,1}&k_{2,2}\cdots\\
\vdots\\
\end{matrix}
\right)\\
$$

3，A每个元素自己为一块，B按照行分块（其实就是方法二的转置）。则

$$
\rank(AB)\leq\rank(B)
$$

.

综合2，3有：

$$
\rank(AB)<\min\{\rank(A),\ \rank(B)\}
$$

$$
|E_m-BA|=
\left|
\begin{matrix}
E_n&A\\
0&E_m-BA
\end{matrix}
\right|
=
\left|
\begin{matrix}
E_n&A\\
B&E_m
\end{matrix}
\right|
=
\left|
\begin{matrix}
E_n-AB&A\\
0&E_m
\end{matrix}
\right|
=|E_n-AB|
$$

$$
\textbf{Extrapolation}:\\
\lambda\in\mathbb R/\{0\}.\\
|\lambda I_s-AB|=\lambda^{s-n}|\lambda I_n-BA|.\\
\textbf{Proof}:\\
\lambda提出来然后套原来那个。\\
这说明|\lambda I_s-AB|与|\lambda I_n-BA|的特征根顶多相差几个0.
$$

## Diagonalise 对角化

$$
\textbf{Definition}:\\
\text{If }\exist A\ s.t.\ A^{-1}MA\text{ is a }\textbf{diagonal matrix},\\
\text{then say }A\textbf{ diagonalises }M.
$$

$$
\textbf{Property 1}:\\
A=(V_1\ V_2\ \cdots\ V_n)\textbf{ diagonalises }M,\\
\text{where }V_i,\ i=1,2,\cdots n\text{ are }\textbf{eigenvectors}\text{ of }M.\\
\text{Elements remain on the }\textbf{diagonal}\text{ are }\textbf{eigenvalues}\text{ of }M.
$$

对角线上的特征值的下标一定是前面那个特征向量对应的特征值（一一对应）

故可对角化等价于此矩阵有n个（最多也就n个）线性无关（把每一个lambda对应的基础解系放在一起瞅瞅就好了，此性质的证明在下）的特征向量，且与它相似的对角阵的对角元都是它的eigenvalue。

证明，基础解系放在一起依然是无关的，数归前k个线性无关，然后用一下特征关系就好了。

能否对角化，判别过程：求特征值，求出每一个特征值对应的特征子空间（补上0先，不然不好谈基础解系）的基础解系，看看基础解系放在一起是不是n个，是n就可对角化

非零的幂零矩阵不可对角化，因为特征值只能是0。

零矩阵可以对角化。

幂等与对合矩阵一定可以对角化。

你看他们的对应多项式，是可以因式分解的，而且因式互素。

h(x)=f(x)g(x)fg互素，且h(A)=0

$\rank(f(A))+\rank(g(A))=n$

这里好像和最小多项式有点关系.

有n个不同的特征值，必可对角化。

### 实对称矩阵的对角化

命题：

Real对称矩阵的特征多项式的根都是实根，也即必有n个特征值。

证明：

A复矩阵，假设

$$
\lambda=a+ib,s.t.|\lambda I-A|=0
$$

，求证b等于0。

假设

$$
\alpha+i\beta
$$

为其特征向量。

1，代定义，乘开，实虚部对应相等。

2，实部相等式子左乘beta的转置，同理另一式子左乘alpha的转置。

3，然后由数的转置等于自身，则构建等式，消去a为系数的项，得到b=0.

命题：不同特征值对应的特征向量必定正交。

证明：

$$
\lambda(\alpha_1,\alpha_2)=(\lambda\alpha_1,\alpha_2)=(A\alpha_1,\alpha_2)=\alpha_1^TA\alpha_2=(\alpha_1,A\alpha_2)=\lambda'(\alpha_1,\alpha_2).\\
\lambda\neq\lambda'.\\
(\alpha_1,\alpha_2)=0.
$$

命题：

任意实对称矩阵A必定正交相似于对角阵。

证明：数归

将A的某一特征值的单位特征向量扩成一组基etas。

把这组基Schimidt正交化。

A(row etas)=(row rtas)(第一列除了第一个是lambda别的是0，剩下列随便)

则有Q^TAQ=上述方阵，而左式对称，推出上述矩阵右下角是实对称矩阵，左上角是lambda，别的都是0。

对B套用归纳假设。

对实对称矩阵，求正交相似的那个矩阵：

把每组特征向量分别单位正交化。（这样才是互为逆矩阵的）

$$
A\matl\eta_1&\eta_2&\cdots \matr=\matl\eta_1&\eta_2&\cdots \matr diag\{\lambda_1,\lambda_2,\cdots\}.\\
两边右乘\matl\eta_1\\\eta_2\\\vdots\matr .
$$

则这个矩阵就是把这些基排开。

两个矩阵交换，可以同时对角化。先对角化一个再对角化另一个就行了。

AA^T的eigenvalue 非负。这代表它起码是半正定的.

$$
A^TA\alpha=\lambda\alpha.\\
一个向量的模长的平方=\alpha^TA^TA\alpha=\lambda\alpha^T\alpha\\
故非负
$$

# Relations between Matrices 矩阵间的关系

一般地，把一个对于某等价类中的元素都一样的东西叫做不变量，而能完全决定等价类的不变量被称作完全不变量。

## 相似

---

Definition:

称两个F上的方阵A，B相似,If $\exist$ **reversible matrix** $U,s.t.B=U^{-1}AU$.

---

实际上，这样的相似矩阵算出来一个的幂就相当于算出了所有的。

$$
B^m=(U^{-1}AU)^m=(U^{-1}AU)(U^{-1}AU)(U^{-1}AU)\cdots(U^{-1}AU)=U^{-1}A^mU.
$$

这样一来，如果A是对角矩阵，那就很好算了。

而矩阵可以代表线性递推啊，这就是特征根求线性递推数列的理论基础，所谓的特征根就是B的特征值。

---

0矩阵与$kI$所在的相似类只有自己。

如果一个矩阵与对角阵相似，称为**可对角化**的，把此对角阵称为它的**相似标准形**。

实际上，一个矩阵的相似标准形要么是对角形，要么是Jordan形，要么有理标准形。

---

Invariant:

特征多项式,trace,eigenvalue,determinant,rank.

有相同的行列式决定了他们要么都可逆，要么都可以；如果都可逆，逆矩阵也构成相似类。

相似类好像没有完全不变量。

### 正交相似

不可以理解为相似加合同！因为你不能保证那个矩阵一样！

还是得用特征值，不然不是很能说得清。

$$
称两个F上的方阵A，B正交相似，\text{If }\exist\textbf{ reversible matrix }U,s.t.B=U^{-1}AU\text{, where }U\text{ is an }\textbf{orthogonal matrix}.
$$

## 相抵

Definition:

如果A可经有限次初等行列变换化成B，称为AB相抵。

---

complete invariant: rank.

任意m乘n的矩阵等价于左上角为I_r别的全为0的分块矩阵，r为A的秩，称为A的**相抵标准形**.

由此就证明了任意矩阵A可被化为列满秩的矩阵B与行满秩的矩阵C的乘积，满秩矩阵的那一侧维度就是r。

这个I_r是可以挪位置的，再进一步说，只要你保证秩是r中间其实可以随便搞。

$$
A=P^{-1}\left(
\begin{matrix}
I_r&0\\
0&0
\end{matrix}
\right)Q^{-1}=P^{-1}\left(
\begin{matrix}
I_r\\
0
\end{matrix}
\right)(I_r\ 0)Q^{-1}=BC.\\
B列满秩，C行满秩.
$$

## Congruence 合同

Definition:

If $\exist$ **reversible matrix** $C$, s.t. $A=C^TBC$, then we call $A,B$ are **congruent** with each other.

$$
f(\alpha,\beta)=X^TAY,f(\alpha,\beta)=X_1^TBY_1\\
\Rightarrow C^TAC=B\\
对应同一双线性函数的，就叫A、B合同
$$

记作

$$
A\simeq B.
$$

det的正负性不变。

当范围限定在实对称内的时候，相似必定合同（特征值都一样比合同强多了）

### Complete Invariable

When the matrix is **complex**, it's **rank**.

When the matrix is **real**, they are two out of **rank**, **positive index of inertia**, and **negative index of inertia**.

### Invariable:

**Rank**, **positive index of inertia**, and **negative index of inertia**.

# 待整理：

$$
Sherman-Morrison\\
\text{If }A\text{ is }\textbf{reversible},\ \alpha,\beta\text{ are column vectors}\in F^n.\\
(A+\alpha\beta^T（这个东西被称作秩一修正）)^{-1}\\
\text{Consider }A+\alpha\beta^T=AA^{-1}(A+\alpha\beta^T)=A(I+A^{-1}\alpha\beta^T)\\
后面那个展开就完了，它的逆存在的条件是1+\beta^TA^{-1}\alpha\neq0
$$

$$
\text{If }\rank(A^m)=\rank(A^{m+1}),\text{ then }\rank(A^{m+1})=\rank(A^{m+2}).\\
\textbf{Proof}:\\
\dim\ker(A^m)=\dim\ker(A^{m+1})\ and\ \ker(A^m)\subset\ker(A^{m+1})\Rightarrow\ker(A^m)=\ker(A^{m+1}).\\
pick\ x\in\ker(A^{m+2}).
A^{m+2}x=0\Leftrightarrow A^{m+1}(Ax)=0\Leftrightarrow A^mx=0.
$$

$$
\left(
\begin{matrix}
A&0\\
0&A-E
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
A&0\\
A&A-E
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
A&-A\\
A&-E
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
A&A\\
A&E
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
A-A^2&A\\
0&E
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
A-A^2&0\\
0&E
\end{matrix}
\right)\\
\rank(A)+\rank(A-E)=n+\rank(A-A^2)
$$

$$
标正基\eta下
\alpha=\sum\limits_{i=1}^{n}(\alpha,\eta_i)\eta_i.\\
Q=(\eta_1\cdots\eta_n)\\
Q^TQ=I
$$

零映射一定是线性映射。

考虑一个向量空间，有一组基。一个映射：把任何一个向量映射成这组基下的坐标。

这个映射被称作，坐标映射。

任给一个矩阵A_{m\times n}
V_1\subset F^{N_1} n-dimensional
V_2\subset F^{N_2} m-dimensional
各取他们的一组基，
(基向量组)X就是V_1里面的元素，同理(基向量组)Y就是V_2里面的元素
define f:V_1\rightarrow V_2
映射成把那个Y坐标用AX代替掉。

有限维向量空间之间的映射全都是这么定义的。

线性映射一定将0元映成0元

线性映射一定把相关组映成相关组

不一定把无关映成无关，反例：0映射

$$
f((\alpha_1\cdots\alpha_n)X)=f(\alpha)=f(\sum x_i\alpha_i)=\sum\limits_{i=1}^{n}x_if(\alpha_i)=(f(\alpha_1)\cdots f(\alpha_n))X\\
两个X一样
$$

构造线性映射只需要确定基的像

一个线性映射是单射/满射/同构，只考虑这个映射是单射/满射/双射。

单性刻画

$$
f(\alpha_1)=f(\alpha_2),\alpha_1=\alpha_2

如果线性映射，则等价于f(\eta)=0\Rightarrow\eta=0.
$$

坐标映射是个同构映射。

$$
X\rightarrow AX\\
f单 f(x)=AX=\vec 0 \Rightarrow A列满秩\\
f满 AX=Y\forall \beta\in F^{n} AX=\beta有解\\
f同构，当且仅当A是可逆矩阵。\\
$$

若f单，f将无关组映成无关组。
若f同构，f将基映成基。（indicating 维数一定一样）

V_1 V_2之间存在同构映射，则称它们同构，记作V_1全等号 V_2

线性映射产生子空间
f:V_1\rightarrow V_2
\ker f={\alpha\inV_1|f(\alpha)=0_{V_2}}\subset V_1 f的核
\lm f={f(\alpha)|\alpha\in V}\subset V_2 f的像

实际上所有的子空间都是线性映射的kernel,please prove.
f:X\rightarrow AX
\ker f=L(f(\alpha_1)\cdots f(\alpha_n))
\lm f={AX|X\in F^m}

但是子空间和kernel不是一对一的。

$$
\text{Two spaces }V_1,V_2.\\
\text{Set down }Hom(V_1,V_2)为从V_1\rightarrow V_2的全体线性映射。\\
this set is not empty(0映射)\\
f,g:V_1\rightarrow V_2\\
(f+g)(\alpha)=f(\alpha)+g(\alpha)\\
(kf)(\alpha)=k(f(\alpha))\\
Hom(V_1,V_2)是一个向量空间\\
$$

kk可以利用一个数的转置等于本身，来变换形式

找出线性映射对应的矩阵

$$
f:S\longrightarrow S'.\\
S有一组基v.g.\{\alpha\}_1^p.\\
S'有一组基v.g.\{\beta\}_1^q.\\
f(\alpha_i)=\sum\limits_{j=1}^qa_{i,j}\beta_j.\\
可以知道，a_{i,j}的存在唯一确定了这个线性映射。\\
把他们组合成一个p\times q的矩阵，就是这个线性映射在这两组特定的基下对应的矩阵。
$$


可以通过把一个矩阵行列变换成单位矩阵的过程来求矩阵的逆（把每步变换对应的矩阵写出来）

---

$\left|\begin{array}{cc}k I_{n} & A \\ A & k I_{n}\end{array}\right| \geqslant k^{2 n}$, where $A$ is a skew symmetric matrix.

Proof:

$\left|\begin{array}{cc}k I_{n} & A \\ A & k I_{n}\end{array}\right| \geqslant\left|2^{2 n}|. \Leftrightarrow\right| \begin{array}{cc}\operatorname{I_n} & \frac{A}{K} \\ \frac{A}{K} & \operatorname{I_n}\end{array}|\geqslant1. \Leftrightarrow\left|\begin{array}{ll}\operatorname{I_n} & A \\ A & \operatorname{I_n}\end{array}\right| \geqslant 1.$

$\left|\begin{array}{cc}I_{n} & A \\ A & I_{n}\end{array}\right|=\left|\begin{array}{cc}\ I_n & A \\ 0 & I_{n}-A^{2}\end{array}\right|=\left|I_{n}\right|\left|I_{n}-A^{2}\right|=\left|{I_n}-A^{2}\right|=\left|I_{n}+A A^{T}\right|.$

$A A^{T}$ is a positive semi-definite matrix.

$\Rightarrow\left(A A^{T}\right)$'s eigenvalues $\geqslant 0$.

$\Rightarrow\left(I_{n}+A A^T\right)$'s eigenvalues $\geqslant 1$.

$\Rightarrow\left|I_{n}+A A^{T}\right|=\prod \lambda_{i} \geqslant 1 .$

---

# 杂：

合同分类：

V/F
F/F
两个空间V_1,V_2.
各固定一组基。
Hom_F(V_1,V_2)和

$$
M_{n\times m}(F)
$$

差不多

取V_2为F了。

记V*=Hom_F(V,F) 称为V的对偶空间，同构的。

加个星号变线性映射

$$
\alpha_i^*(\alpha_j)=\delta_{i,j}
$$

取星号得到对偶基。

V/F 如果对V的任意两个元素(\alpha,\beta)存在F中的唯一元与其对应，f（\alpha,\beta）就是二元函数。 满足加法与数乘，双线性函数。

$$
f(X,Y)=X^TAY\\
此式子可以表达所有这两个空间之间的线性映射
$$

换基：找到使基变换的矩阵C

$$
\textbf{quadratic（二次） surface equation}\text{ can be written as matrices multiplied together.}\\
e.g.:x^2+4y^2+z^2-4xy-8xz-4yz-1=0.\\
\Leftrightarrow(x,y,z)
\matl
1&-2&-4\\
-2&-4&-2\\
-4&-2&1
\matr
\matl
x\\
y\\
z
\matr=0.
$$

把里面那个矩阵正交相似于一个对角阵，就可以找到一组坐标下，没有交叉项。

12.7的习题课

$$
\text{The scalar product in }\mathbb C^n.\\
x=(x_1\cdots),y=(y_1,\cdots).\\
(x,y)=\sum\limits_{i=1}^nx_iy_i.\\
(\alpha,\beta)=\overline{(\beta,\alpha)}.\\
线性和正定性依然存在。
$$

$$
A可以U对角化\Leftrightarrow AA^H=A^HA（A是正规矩阵）.
先套上面那个分解。\\
TT^H=T^HT,T为上三角，则一定为对角，比较ii元即知。\\
AB=BA，若A为对角阵且对角元互异，则B一定为对角。
$$

**对于一些操作可保持的矩阵间关系，可以不妨加强条件，先从特殊矩阵出发思考，写的时候你先把它变成那种阵。**

各种复杂的情况有时可以用两个极端凑出来，只要你能解决两个极端，里面的就都解决。

除0之外，反对称矩阵与对称矩阵不可能合同。

$$
A=1/2(A+A^T)+1/2(A-A^T)$$前面那个对称，后面那个反对称，且此种分解唯一。



若矩阵（反）对称，则称它对应的双线性函数对称（反对称）。这应该是等价的。



反对称矩阵A均合同于$$\matl0&I_s&0\\-I_s&0&0\\0&0&0\matr,2s=\rank(A)$$。

$$
f=\sum\limits_{i=1}^nx_i^2+\sum\limits_{1\leq i<j\leq n}x_ix_j
$$.

判断正定：

1 配方法

2 顺序主子式法



极分解？

写成把B2分别乘到左右去，会更好看。

$$
C^TAC.\\
P_s^TP_{s-1}^T\cdots P_1^TAP_1\cdots P_{s-1}P_s.\\
从中间开始，做成对的初等变换。
$$

$$
\matl A\\ I\matr 成对初等行列变换\matl D\\ C\matr
$$.

则$$C^TAC=D$$.

这不就是实对称的对角化的一个泛化版本？

拿对角元素十字形打砖块 就出来了

对角元素为0用别的行列加上去就行咯

这个叫“成对初等行列变换法”求标准形

令$X=CY$原来的二次型$X^TAX=(Y^TC^T)A(CY)=Y^TDY$化为标准形。



||a||是a的矩阵范数。



A正定，B半正定。

（先设对角（有合同对角化，相似太强了 这里做不到））

Lemma A正定，B对称，就可以同时合同对角化。

|A+B|\geq |A|+|B|.

$|A+B|^{1/n}\geq|A|^{1/n}+|B|^{1/n}$.

或者

Lemma：

A半正定。

$|A|^{1/n}=\min\{1/n\tr(AA_1)|A_1正定且|A|=1.\}$.

拿trace放均值。







A正定，B实对称，AB特征值全为实数。

$A=CC^T.$

$\Rightarrow C^{-1}(AB)C=C^TBC$.

AB相似于后面那个实对称阵，其特征值显然都是实数。



A半正定，B半正定，AB特征值为非负实数。
$$

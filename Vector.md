# Vector Space 向量空间

$$
Definition:\\
The\ set\ K^n\ comprises\ of\ \textbf{ALL}\ \mathbf{n-ary\ ordered\ array}\ defined\ at\ \mathbb K,\\
along\ with\ \mathbf{addtion},\ \mathbf{scalar\ mulplication},\ and\ the\ 8\ rules\ they\ obey\\
is\ called\ a\ \mathbf{n-dimensional\ vector\ space}\ defined\ at\ \mathbb K.\\
Elements\in K^n\ is\ called\ \mathbf{n-dimensional\ vector}.
$$

$$
Definition:\\
U\subset F^n \\
If\ U\ is\ closed\ with\ \mathbf{addtion},\ \mathbf{scalar\ mulplication},\\
then\ call\ U\ a\ \mathbf{linear\ subspace（线性子空间）}\ of\ F^n.
$$

$$
Definition:\\
Call\ \{\beta|\beta=\sum\limits_{i=1}^nk_i\alpha_i\}\ the\ \mathbf{generating\ subspace（生成子空间）}\ of\ v.g.\{\alpha_i\}_1^n,\\
set\ down\ as\ <\alpha_1,\alpha_2,\cdots,\alpha_n>.
$$

$$
Definition:\\
All\ \mathbf{solutions}\ of\ \mathbf{homogenuous\ linear\ equation}\ make\ up\ a\ \mathbf{solution\ space}.\\
Call\ its\ \mathbf{basis}\ a\ \mathbf{fundamental\ set\ of\ solutions（基础解系）}\ of\ it.\\
Call\ \sum\limits_{\forall \eta_i \in f.s.o.s} k_i\eta_i\ the\ \mathbf{general\ solution（通解）}\ of\ it.
$$

### 空间维数

$$
Definition:\\
Suppose\ U=<\alpha_1,\alpha_2,\cdots,\alpha_n>\ is\ a\ non-zero\ \mathbf{subspace（子空间）}\ of\ K^n,\\
define\ the\ number\ of\ vector\ a\ \mathbf{basis（基）}\ of\ U\ possesses\ the\ \mathbf{dimension（维数）}\ of\ U.\\
Set\ it\ down\ as\ \dim_KU\ or\ \dim U.\\
De\ fecto,\ \dim U = \rank(v.g.\{\alpha_i\}).
$$

零子空间的维数定义为0。
$$
The\ \mathbf{dimension}\ of\ the\ \mathbf{solution\ space}\ of\ the\ \mathbf{n-array\ homogenuous\ linear\ equation}:\\
\dim W=n-\rank(A),\\
where\ A\ is\ the\ \mathbf{coefficient\ matrix}.
$$
来直观理解一下：其实维数就是对于这个向量空间中的向量有多少限制条件，原来是n个自由变量，rank（A）又是限制数，就很显然了。
$$
V_1\cdots V_m是K^n的真子空间。\\
下证V_1\cap V_2\cap\cdots\cap V_m\neq K^n.\\
a_k=(1,k,k^2,\cdots,k^{m-1})\\
A=\{a_k|k\in\mathbb Z\}\\
|V_i\cap A|\leq n-1，不然其中存在n个向量无关。
|(V_1\cap V_2\cap\cdots\cap V_m)\cap A|\leq(n-1)m\neq\infty.\\
$$


## Linear Combination 线性组合

$$
Definition:\\
Call\ \sum\limits_{i=1}^{n}k_i\alpha_i\ (k_i\in \mathbb R)\ a\ \mathbf{linear\ combination（线性组合）}of\ v.g.\{\alpha_i\}_1^n,\\
and\ k_i\ is\ called\ \mathbf{coefficient（系数）}.
$$

### Convex Combination 凸组合

$$
Definition:\\
v.g.\{x_i\}_1^n.\\
If\ \sum\limits_{i=1}^n\lambda_i=1,\ and\ \lambda_i\geq0;\\
Then\ call\ \sum\limits_{i=1}^nx_i\lambda_i\ a\ \mathbf{convex\ combination}\ of\ v.g.\{x_i\}_1^n
$$

$$
and\ \lambda_i\geq0;\\
Then\ call\ \sum\limits_{i=1}^nx_i\lambda_i\ a\ \mathbf{convex\ combination}\ of\ v.g.\{x_i\}_1^n
$$



## Linearly Dependent/Independent 线性相/无关

$$
Definition:\\
If\ \beta=\sum\limits_{i=1}^{n}x_i\alpha_i,\\
then\ call\ \beta\ can\ be\ \mathbf{linearly\ expressed（线性表出）}\ by\ v.g.\{\alpha_i\}_1^n.\\
Extrapolation:\\
If\ \forall \beta \in\ v.g.\{\beta_i\}\ can\ be\ \mathbf{linearly\ expressed}\ by\ v.g.\{\alpha_j\},\\
then\ call\ v.g.\{\beta_i\}\ can\ be\ \mathbf{linearly\ expressed}\ by\ v.g.\{\alpha_j\}.\\
If\ they\ can\ \mathbf{linearly\ express}\ each\ other,\\
then\ they\ are\ \mathbf{equivalent（等价）},\\
set\ down\ as\ v.g.\{\beta_i\}\cong \{\alpha_j\}.
$$

$$
Defition:\\
If\ \exist k_i\;s.t.\sum\limits_{i=1}^{n}k_i\alpha_i=0\;and\;\sum\limits_{i=1}^{n}\abs{k_i}>0\text{（不全为0）},\\
then\ call\ v.g. \{\alpha_i\}\ \mathbf{linearly\ dependent（线性相关）};\\
else,\ k_i\ only\ have\ \mathbf{zero\ solution（零解）},\\
call\ v.g. \{\alpha_i\}\ \mathbf{linearly\ independent（线性无关）}.
$$



### Maximal Linearly Independent System 极大无关组

$$
Definition：\\
If\ \alpha_{i_r}\ in\ \alpha_i\ s.t.\ \forall\alpha_k\in\{\alpha_i\}/\{\alpha_{i_r}\}\ can\ be\ \mathbf{linearly\ expressed}\ by\ \alpha_{i_r},\\
then\ call\  \alpha_{i_r}\ a\ \mathbf{maximal\ linearly\ independent\ system(极大无关组)}\ of\ \alpha_i.\\
$$

极大无关组的向量数目由原向量组唯一决定，称这个数目为原向量组的“秩”。

规定$$\vec{0}$$没有极大无关组。

### Extended v.g. and Shortened v.g. 延伸组和缩短组

给r个n维向量加上或减去k个维度，得到r个n+k或n-k维向量，分别称为原v.g.的e.v.g（延伸组）与s.v.g（缩短组）。

向量组无关，延伸组也无关。向量组相关，缩短组相关。

### Partial v.g. 部分组

从r个n维向量中，取出t个（t<r），构成一个原v.g.的一个p.v.g.。

p.v.g.相关，original v.g.必相关。

## vector normalisation 向量归一化

把每一维的分量都用比例表示，总的加起来是1。

或者让它的长度是1。

## Rank 秩

$$
The\ vector\ number\ of\ \mathbf{maximal\ linearly\ independent\ system}\ is\ only\ decided\ by\ the\ orginal\ v.g.A,\\
call\ this\ number\ the\ \mathbf{rank（秩）}\ of\ v.g.A.\\
Set\ down\ as\ rank(A).
$$

如果秩要在向量范畴内操作就取出最大无关组。

行秩一定等于列秩。

求向量组的秩等价于求其生成子空间的维数。

求极大无关组等价于求生成子空间的一组基。

### Rank Inequality 秩不等式

$$
If\ v.g.A\ \mathbf{linearly\ express}\ v.g.B,\\
then\ \rank(A)\geq \rank(B).
$$

从这里就可以推出“少表多，多相关。”
$$
\rank(A,B)\leq\rank(A)+\rank(B)\\
\\
\max\{\rank(A),\rank(B)\}\leq\rank(A,B)\\
\\
\rank(A\pm B)\leq\rank(A)+\rank(B).\\
\Rightarrow\rank(A-B)\geq|\rank(A)-\rank(B)|.\\
Proof:\\
\rank(A\pm B)\leq\rank(A\pm B,B)=\rank(A,B)\leq\rank(A)+\rank(B)\\
\\
\rank(AB)\leq min\{\rank(A),\rank(B)\}\\
\textbf{Proof:}\\
Binet-Cauchy\ Formula
$$

#### Sylvester's rank inequality

$$
\textbf{Sylvester's rank inequality}:\\
\rank(A_{n\times s}B_{s\times m})\geq\rank(A)+\rank(B)-s.\\
$$

$$
\textbf{Proof}:\\
\text{Mean 1}\\
\left(
\begin{matrix}
E_s&0\\
0&AB
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
E&0\\
A&AB
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
E&B\\
A&0
\end{matrix}
\right)
\rightarrow
\left(
\begin{matrix}
B&E\\
0&A
\end{matrix}
\right)\\
\rank\left(
\begin{matrix}
A&B\\
0&C
\end{matrix}
\right)
\geq
\rank(A)+\rank(C)\\
可以通过这个大矩阵有非零的\rank(A)+\rank(C)阶子式证明（把他们的那两个子式拿出来再拼一个大的）。\\
(B=0可以取等，不一定必要)\\
\text{Mean 2}\\
\exist 列/行满秩矩阵P,Q,\ s.t.A=PQ.\\
P通过再加入列向量可以扩充成一个基的\\
这样他就变成P'=(P\ P_1)一个方阵，同理Q'=\left(
\begin{matrix}
Q\\
Q_1
\end{matrix}
\right).\\
\rank(AB)=\rank((P\ P_1)\left(
\begin{matrix}
Q\\
0
\end{matrix}
\right)B)=\rank(\left(
\begin{matrix}
Q\\
0
\end{matrix}
\right)B)\\
=\rank(\left(
\begin{matrix}
Q\\
Q_1
\end{matrix}
\right)B-\left(
\begin{matrix}
0\\
Q_1
\end{matrix}
\right)B)\geq\rank(\left(
\begin{matrix}
Q\\
Q_1
\end{matrix}
\right)B)-\rank(\left(
\begin{matrix}
0\\
Q_1
\end{matrix}
\right)B)=\\
\rank(B)-\rank(\left(
\begin{matrix}
0\\
Q_1
\end{matrix}
\right)B)\geq\rank(B)-\rank(Q_1)=\rank(B)-(n-\rank(A)).
$$

# Scalar Product 数量积/内积

## Eucilidean Space 欧几里得空间

$$
\alpha,\ \beta\in V.\\
\text{If }(\alpha,\beta)=0,\text{ then call them }\textbf{orthogonal（正交）}.
$$



### Orthogonal vector group 正交向量组

$$
\textbf{Definition}:\\
\text{If}一组向量两两正交，则称为正交向量组。加上长度都是1的条件，称为单位正交向量组。\\
$$

$$
\textbf{Property 1}:\\
正交向量组线性无关。\\
\sum x_i\alpha_i=0\Rightarrow(\sum x_i\alpha_i,\alpha_j)=x_j(\alpha_j,\alpha_j)\Rightarrow x_j=0\\
\text{this vector group definitely are a set of basis of the space, so call it a set of }\textbf{orthogonal basis（正交基）}.
$$

$$
\textbf{Schmidt's orthogonalisation}\\
思想：把非正交的部分用投影算出来减掉。\\
\frac{(\alpha_s,\beta_j)}{(\beta_j,\beta_j)}\beta_j=\frac{(\alpha_s,\beta_j)}{||\beta_j||}\frac{\beta_j}{||\beta_j||}=||\alpha||\cos\theta\frac{\beta_j}{||\beta_j||} 就是把投影算出来了.\\
\textbf{Process}:\\
v.g.\{\alpha\}_1^s\text{ is }\textbf{linearly irrelevant}.\\
\text{Let }\beta_1=\alpha_1,\\
\beta_s=\alpha_s-\sum\limits_{j=1}^{s-1}\frac{(\alpha_s,\beta_j)}{(\beta_j,\beta_j)}\beta_j.\\
$$

$$
\textbf{Property 1}:\\
\beta为正交向量组，数归即证。\\
$$

$$
\textbf{Property 2}:\\
\alpha\cong\beta.\\
\textbf{Proof}:\\
(\beta_1\ \beta_2\ \cdots\ \beta_s)=(\alpha_1\ \alpha_2\ \cdots\ \alpha_s)乘一个
上三角矩阵（一定可逆）\\
$$















$$
U\text{ is a subspace of }R^n.\\
Let Pu:R^n\rightarrow R^n\\
\alpha\rightarrow\alpha_1\\
(\alpha-\alpha_1)\perp U
则称其为R^n到U上的正交投影。\\
prove \alpha_1 唯一存在\\
找一组标正基u_1,u_2\cdots\\
Let\ \alpha_1=\sum(\alpha,u_i)u_i\\
对应的矩阵就是\sum(u_iu_i^T)\\
\alpha_1=Pu(\alpha)\Leftrightarrow|\alpha-\alpha_1|\leq|\alpha-r|\\
套之前证明的勾股定理
$$

$$
A_{m\times n}R阵，m>n\\
x_0=argmin|Ax-\beta|^2\\
call x_0为Ax=\beta的最小二乘解\\
prove\ x_0为最小二乘解\Leftrightarrow A^TAx_0=A^T\beta\\
就是投影的思想\beta投到A的列空间\\
U=\{Ax|x\subset R^n\}
x_0isAx=\beta的最小二乘解
\Leftrightarrow|\beta-Ax_0|\leq|\beta-r|\forall r\in U\\
\Leftrightarrow Ax_0为\beta在U上的正交投影\\
\Leftrightarrow \beta-Ax_0\in U^\perp\Leftrightarrow(\beta-Ax_0,a_i)(a_i是A的列向量组)\Leftrightarrow
a_i^T(Ax_0-\beta)=0完了\\
$$

$$
只要你直接取出一组列向量的基，构成A，一个列满秩矩阵\\
P_A(\beta)=A(A^TA)^{-1}A^T\beta
$$


$$
(f(\alpha_1)\cdots)=(\beta_1\cdots)A\\
A由f唯一决定，称为f在基\{\alpha_i\}_i,\{\beta_j\}_j下的矩阵。
$$

$$
\sigma:Hom(V_1V_2)\rightarrow M_{n\times m}(F)\\
f\rightarrow A\\
\textbf{Property}:\\
\sigma is 同构映射\\
固定一组基的情况下，线性映射和矩阵没差别
$$

$$
作业：刻画基本矩阵对应的线性映射e_{i,j}并用它们表示所有的线性映射。
$$


$$
线性映射f:V\rightarrow V 称为线性变换。\\
(f(\alpha_1)\cdots)=(\alpha_1\cdots)A\\
(f(\beta_1)\cdots)=(\beta_1\cdots)B\\
suppose\ (\beta_1\cdots)=(\alpha_1\cdots)U\\
U\ is\ called\{\alpha_i\}到\{\beta_j\}的过渡矩阵（过渡矩阵一定可逆）\\
(f(\beta_1)\cdots)=(\beta_1\cdots)B=(\alpha_1\cdots)UB\\
((f(\alpha_1)\cdots)X_1\cdots)=(f(\alpha_1)\cdots)U=(\alpha_1\cdots)AU\\
上面两行的首项相等\\
故AU=UB\Rightarrow B=U^{-1}AU
$$






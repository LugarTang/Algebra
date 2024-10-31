# Vector Norm

(向量范数的等价性) 设$\vec x$是任意n维向量，任意两种范数，则存在正常数$c_1,c_2$，使得对于任意的$\vec x$，有

$$
c_1||x||_a\leq||x||_b\leq c_2||x||_a.
$$

即彼此等价.

注： $\mathbb R^n$上一切范数都等价。因此对于范数的极限性质，我们只需针对一种范数进行讨论，其余范数也都具有相似的结论.

converge by coordinates: each component converge to it

converge by norm: some norm tends to 0

converge by coordinate $\to$ converge by all norm

# Matrix Norm

Frobenius Norm

$$
\left(\sum(a_{i,j}^2)\right)^{1/2}.
$$

对于给定的$\R^n$上的一种向量范数$||x||$ 和$\R^{n\times n}$上的一种矩阵范数$||A||$，对于任意的$\vec x$，如果满足

$$
||A\vec x||\leq||A||\cdot||\vec x||
$$

则称矩阵范数与向量范数**相容**

Under the same condition

$$
||A||_n:=\max_{\vec x\neq\vec 0}\frac{||A\vec x||_n}{||\vec x||_n}.
$$

称之为由向量范数导出的矩阵范数，也称为operator norm或从属范数 This norm is definitely 相容

$$
||A||_\infty=\max_i \sum_j|a_{i,j}|\text{ Row Norm}\\
\ \\
||A||_1=\max_j \sum_i|a_{i,j}|\text{ Column Norm}\\
\ \\
||A||_2=\sqrt{\lambda_{
    \max
}(A^TA)}
\text{ Spectrum Norm}\\
$$

the **spectral radius** of a square matrix is the maximum of the absolute values of its eigenvalues, denoted by $\rho(\cdot)$.

$||\cdot||$ for any operator norm, we have

$$
||A\vec x||=||\rho(A)\vec x|| \leq||A||\cdot||\vec x||\\
\ \\
\implies \rho(A)\leq||A||
$$

If $A=A^T$, $||A||_2=\rho(A)$

Banach Lemma

Supposition

1. $A^{-1}\exist.$

Condition

1. $||B||\leq 1/||A^{-1}||$.

Conclusion

1. $$
   (A+B)^{-1}\exist.
   $$
2. $$
   ||(A+B)^{-1}||\leq\frac{||A^{-1}||}{1-||A^{-1}||\cdot||B||}
   $$

Proof

Apply reduction to absurdity.

If $\text{det}(A+B)=0$,$\exist\vec x (A^{-1}B\vec x=-\vec x)$

Then $||A^{-1}||\cdot||B\vec x||\geq ||A^-1B\vec x||=||\vec x||$

$$
\implies ||B\vec x||/||\vec x||\geq 1/||A^{-1}||
$$

Conflict!

Notice that
$$
I=(A+B)(A+B)^{-1}=A(A+B)^{-1}+B(A+B)^{-1}\\
\ \\
\implies (A+B)^{-1}=A^{-1}[I-B(A+B)^{-1}]\\
\ \\
\implies ||(A+B)^{-1}||\leq ||A^{-1}||(1+||B||\cdot||(A+B)^{-1}||)
$$
This guarantees the invertibility of a perturbed operator and gives a bound about the degree to which it is disturbed.

It reminds of the disturbance to invertible! Is there some connection?

Convergence just like vector.
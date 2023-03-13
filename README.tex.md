# Basics
## Vectors, matrices, $\mathbb{R}$ ... Oh my!
Vectors of Real numbers, define an n dimensional vector:
$v=(a,b,c), u=(x,y,z)$

Matrices of real numbers ..
$$\begin{bmatrix}
   a & b \\
   c & d
\end{bmatrix}$$

The interplay of columns and rows is the heart of linear algebra. Four of the central ideas:
* The column space (all combinations of the columns).
* The row space (all combinations of the rows).
* The rank (the number of independent columns) (or rows).
* Elimination (the good way to find the rank of a matrix).
$% TWO VECTORS SUM
\begin{tikzpicture}[line cap=round]
  \coordinate (O) at (0,0);
  \coordinate (A) at ( -3:2.1);
  \coordinate (B) at ( 55:1.4);
  \coordinate (A+B) at ($(A)+(B)$);
  
  \draw[vector,thin arrow,myred!40] (B) -- (A+B) node[midway,above] {$\vb{a}$};
  \draw[vector,thin arrow,myblue!40] (A) -- (A+B) node[midway,below right=-2] {$\vb{b}$};
  
  \draw[vector,myred] (O) -- (A) node[midway,below] {$\vb{a}$};
  \draw[vector,myblue] (O) -- (B) node[midway,above left=-2] {$\vb{b}$};
  \draw[vector,mypurple] (O) -- (A+B) node[above right=-3] {$\vb{a}+\vb{b}$};
\end{tikzpicture}
\end{document}$
## Multiplication 
Matrix multiplication is associative: (AB)C = A(BC)
Matrix operations are distributive: A(B + C) = AB + AC and (B + C)D = BD + CD.
Matrix multiplication is not commutative: Usually FE not equal EF

dot product: 
$$u \cdot v = ||u|| \cdot ||v|| \cdot cos (\phi) = u_x v_x + u_y v_y$$
cross product:
$$u \times v = \left(\begin{array}{c}u_y v_z - u_z v_y\\u_z v_x - u_x v_z\\u_x v_y - u_y v_x\\\end{array}\right)$$
norms:
$$\|x\|_p := \sqrt[p]{\sum_{i=1}^n |x_i|^p}$$
$$\|x\|_1 := \sum_{i=1}^{n} |x_i|$$
$$\|x\|_{\infty} = \max \limits _i |x_i|$$

transpose: $[A^\mathrm{T}]_{ij} = [A]_{ji}$: "mirror over main diagonal"\\
conjungate transpose / adjugate: 
$A^* = (\overline{A})^\mathrm{T} = \overline{A^\mathrm{T}}$\\
"transpose and complex conjugate all entries"\\(same as transpose for real matrices)\\

multiply: $A_{N \times M} * B_{R \times K} = M_{N \times K}$\\
invert: $\begin{bmatrix}
a & b \\ c & d \\ 
\end{bmatrix}^{-1} =
\frac{1}{\det(\mathbf{A})} \begin{bmatrix}
\,\,\,d & \!\!-b \\ -c & \,a \\ 
\end{bmatrix} =
\frac{1}{ad - bc} \begin{bmatrix}
\,\,\,d & \!\!-b \\ -c & \,a \\ 
\end{bmatrix}$\\


$\left \| A \right \| _p = \max \limits _{x \ne 0} \frac{\left \| A x\right \| _p}{\left \| x\right \| _p}\,$, induced by vector p-norm
$\left \| A \right \| _2 = \sqrt{\lambda_\text{max} (A^T A)}$\\
$\left \| A \right \| _1 = \max \limits _j \sum _{i=1} ^m | a_{ij} |, $\\
$\left \| A \right \| _\infty = \max \limits _i \sum _{j=1} ^n | a_{ij} |,$\\
condition:
$\text{cond}(A) = \left \| A \right \| \cdot \left \| A^{-1} \right \|$
$\det(A) = \sum_{\sigma \in S_n} \text{sgn}(\sigma) \prod_{i=1}^n A_{i,\sigma_i}$\\
For 3$\times$3 matrices (Sarrus rule):\\
\includegraphics[scale=0.6]{sarrus}\\

\textbf{arithmetic rules:}\\
$\det (A \cdot B) = \det (A) \cdot \det (B)$\\
$\det (A^{-1}) = \det (A)^{-1}$\\
$\det\left(rA\right) = r^n\det A\,\,$,  for all $A^{n\times n}$ and scalars $r$


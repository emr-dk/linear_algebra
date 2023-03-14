# Basics
## Vectors, matrices, $\mathbb{R}$ ... Oh my!
An $n$ dimensional vector, where the number of elements in the vector is indicated by $n$, is written in the following form:
$$v=(v_1,v_2, \cdots, v_n), u=(u_1,u_2,\cdots, u_n)$$ 

The amount of dimensions spanned by the vector is indicated by $\mathbb{R}^n$, such as $\mathbb{R}^1$,$\mathbb{R}^2$, $\mathbb{R}^3$.

Matrices are arrangements of numbers into rows and columns, used when solving systems of linear equations. The size of the matrix is written as a matrix row $\times$ column vector. Usually $n \times m$. Two $2 \times 2$ vectors are written as:
$$ A =
\begin{bmatrix}
   a & b \\
   c & d
\end{bmatrix}, B= 
\begin{bmatrix}
   x & y \\
   w & z
\end{bmatrix}
$$
Matrices are used in the solving of systems of linear equations, where the following system is written in the indicated form:
$$\begin{matrix}
   3x+2y-z=1 \\
   2x-2y+4z=2 
\end{matrix}
\Rightarrow
\begin{bmatrix}
   3 & 2 & -1 & 1\\
   2 & -2 & 4 & 2
\end{bmatrix}
$$

## Working with vectors and matrices
### Vectors

dot product / inner product: 
$$v \cdot u = ||v|| \cdot ||u|| \cdot cos (\phi) = \sum_{i=1}^n u_1 v_1 + u_2 v_2 + \cdots + u_n v_n$$
cross product results in a vector that is perpendicular to the two vectors:
$$v \times u = ||v|| \cdot ||u|| \cdot sin(\theta) \cdot n =  \left(\begin{array}{c}u_y v_z - u_z v_y\\u_z v_x - u_x v_z\\u_x v_y - u_y v_x\\\end{array}\right)$$
norms:
$$\|x\|_p := \sqrt[p]{\sum_{i=1}^n |x_i|^p}$$
$$\|x\|_1 = L_1 = \ell_1 := \sum_{i=1}^{n} |x_i|$$
$$\|x\|_2 = L_2 = \ell_2 := \sum_{i=1}^{n} |x_i|^2$$
$$\|x\|_{\infty} = \max \limits _i |x_i|$$

### Matrices
* Matrix multiplication is associative: $(AB)C = A(BC)$
* Matrix operations are distributive: $A(B + C) = AB + AC$ and $(B + C)D = BD + CD$.
* Matrix multiplication is not commutative: Usually $AB \ne BA$

Matrices can only be multiplied if there are as many columns of $A$ as there are rows of $B$. I.e. if $A$ is of the size $m \times n$ and $B$ is $n \times k$. 

dot product:
_what is dot product_?

$\begin{bmatrix}
   a & b \\
   c & d
\end{bmatrix} \cdot 
\begin{bmatrix}
   x & y \\
   w & z
\end{bmatrix} = \begin{bmatrix}
   ax + bw & ay + bz \\
   cx + dw & cy + dz
\end{bmatrix}$

cross product:
_what is cross product_?

$\begin{bmatrix}
   a & b \\
   c & d
\end{bmatrix} \times 
\begin{bmatrix}
   x & y \\
   w & z
\end{bmatrix} = \begin{bmatrix}
   ax + bw & ay + bz \\
   cx + dw & cy + dz
\end{bmatrix}$


transpose: $[A^\mathrm{T}]_{ij} = [A]_{ji}$: "mirror over main diagonal"

# Important concepts of Linear Algebra
My own interpretation of linear algebra concepts, from a wide variety of sources including Gilbert Strang, ..., ... and ... .
## Representations
There are a variety of ways of representing the different elements of linear algebra. 
* Scalar, greek letters $\beta, \alpha, \theta$
* Vector, small letters bold: **v**, **u**, **z**
* Matrix, capital letters bold: **A**,**B**,**C**
* Vector space, $V$


## Vectors, matrices, $\mathbb{R}$ ... Oh my!
In linear algebra we will be working with elements that exist in a variety of dimensions. The numbers we will be working with are most commonly though real numbers $\mathbb{R}$.
The dimensions that a matrix or vector exist in are indicated by the superscript $n$ above an indicator for the number space we are working in $\mathbb{R}$. So, a vector in three-dimensional space is defined as $v \in \mathbb{R}^3$. $\mathbb{R}^n$ is also called the euclidean vector space.

For all $n$ of euclidean space we can work with general terms such as distance, length and angle. This is is hard / impossible to conceptualize at $n > 3$ - but all the concepts still apply though. 

**Scalars**: When working with single numbers in linear algebra, these are referred to as scalars. Probably because they as single numbers are used to scale vectors and matrices. So for instance:
$$\beta = 5, \alpha = 0.524, \theta = 19295$$

**Vectors:** A vector consists of a number of components. The amount of components also corresponds to the amount of dimensions it exists in. A vector with two components is a point in a two dimensional space ($x \space y)$, whilst a vector with three components is in a three-dimensional space ($x \space y \space z$) and so on. 

$$\bold{v}=(x_1,x_2, \cdots, x_n) \text{ or } \bold{v}^T =\begin{pmatrix}
   x_1 \\
   x_2 \\
   \vdots \\
   x_n
\end{pmatrix}$$ 
A geometric vector is usually demonstrated with an arrow above the letter $\vec{v}$, but as we are working with a more generalized concpet of vectors we use the boldface indicator.

**Matrix:** A central element of linear algebra is the concept of systems of linear equations. A system of linear equations could be:
$$
\begin{alignat*}{4}
   x_1 & {} + {} x_2 & {} + {} x_3 = 3 \\
   x_1 & {} - {} x_2 & {} + {} 2x_3 = 2 \\
   2x_1 & {} & + {} 3x_3 = 1
\end{alignat*}
$$
To compactly represent these systems matrices are used. These are rectangular schemes that consist of $m$ rows and $n$ columns. There are many forms of matrices, some showing the $y$'s as well. But the most common is to gather all the numbers in front of the varaibles, so that is what we will do here. So the system from before becomes: 
$$
\begin{bmatrix}
   1 & 1 & 1 \\
   1 & -1 & 2 \\
   2 & 0 & 3
\end{bmatrix}
$$
The vector 


A system of linear equations (or linear system) is a collection of one or more linear equations involving the same variables.  

To solve a system of linear equations means to find such values of the variables that all of its equations are simultaneously satisfied. 

A linear system is inconsistent if it has no solution, and otherwise it is said to be consistent. Consistent system can have one or infinite number of solutions

In the elimination method you either add or subtract the equations of the linear system to get an equation with smaller number of variables. If needed, you can also multiply whole equation by non-zero number.

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

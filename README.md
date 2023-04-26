# Important concepts of Linear Algebra
My notes on linear algebra concepts, from a wide variety of sources including Gilbert Strang, the Deep Learning Book, and various online resources.
## Representations
There are a variety of ways of representing the different elements of linear algebra. 
* Scalar, greek letters $\beta, \alpha, \theta$
* Vector, small letters bold: **v**, **u**, **z**
* Matrix, capital letters bold: **A**,**B**,**C**
* Vector space, $V$

## Vectors, matrices, $\mathbb{R}$ ... Oh my!
In linear algebra we will be working with elements that exist in a variety of dimensions. The numbers we will be working with are most commonly real numbers - $\mathbb{R}$.
In a moment we will introduce some important concepts, matrix and vector. These exist in a variety of dimensions which are indicated by the superscript $n$ above an indicator for the number space we are working in $\mathbb{R}$. So, a vector in three-dimensional space is defined as $v \in \mathbb{R}^3$. $\mathbb{R}^n$ is also called the euclidean vector space.

For all $n$ of euclidean space we can work with general terms such as distance, length and angle. This is is hard / impossible to conceptualize at $n > 3$ - but all the concepts still apply though. 

**Scalars**: When working with single numbers in linear algebra, these are referred to as scalars. These numbers can be used to scale vectors and matrices. So for instance the following are examples of scalars:
$$\beta = 5, \alpha = 0.524, \theta = 19295$$

**Vectors:** A vector consists of a number of components. The amount of components also corresponds to the amount of dimensions it exists in. A vector with two components is a point in a two dimensional space ($x \space y)$, whilst a vector with three components is in a three-dimensional space ($x \space y \space z$) and so on. 
$$\bm{v}=(x_1,x_2, \cdots, x_n)$$ 

Even though we formally wont introduce the transpose until later it is so frequently used that we will show a transposed vector below:

$$\bm{v}^T =\begin{pmatrix}
   x_1 \\
   x_2 \\
   \vdots \\
   x_n
\end{pmatrix}$$ 

A geometric vector is usually demonstrated with an arrow above the letter $\vec{v}$, but as we are working with a more generalized concpet of vectors we use the boldface indicator.

**Matrices:** Matrices are arrangements of numbers into rows and columns, used when solving systems of linear equations. The size of the matrix is written as a matrix row $\times$ column vector. Usually $n \times m$. In the example below $A$ is a $2 \times 2$ matrix and $B$ a $2 \times 3$. These are written in the following form:
$$ \bm{A} =
\begin{bmatrix}
   x_{1,1} & x_{1,2} \\
   x_{2,1} & x_{2,2}
\end{bmatrix}, \bm{B}= 
\begin{bmatrix}
   x_{1,1} & x_{1,2} & x_{1,3} \\
   x_{2,1} & x_{2,2} & x_{2,3}
\end{bmatrix}
$$

If $m = n$ the matrix is said to be square of degree $n$.$ 

## Systems of linear equations
A central element of linear algebra is the concept of systems of linear equations. A system of linear equations could be:
$$
\begin{alignat*}{4}
   x_1 & {} + {} x_2 & {} + {} x_3 = 3 \\
   x_1 & {} - {} x_2 & {} + {} 2x_3 = 2 \\
   2x_1 & {} & + {} 3x_3 = 1
\end{alignat*}
$$

As mentioned previously we can represent these systems in matrices. There are many forms of matrices, some showing the $y$'s as well. But the most common is to gather all the numbers in front of the varaibles, so that is what we will do here. So the system from before becomes: 
$$
\begin{bmatrix}
   1 & 1 & 1 \\
   1 & -1 & 2 \\
   2 & 0 & 3
\end{bmatrix}
$$
To solve a system of linear equations means to find such values of the variables that all of its equations are simultaneously satisfied. A linear system is inconsistent if it has no solution, and otherwise it is said to be consistent. Consistent system can have one or infinite number of solutions

**linear dependence** if one vector in a series of vectors can be defined as a linear combination of the others it is said to be linearly dependent.

## Special matrices
**Diagonal matrix** is a square matrix containing zeroes everywhere except non-zero values in the diagonal. This is indicated as $D = diag(d_1, \dots, d_n)$ and can be understood as

$$ D = 
\left(\begin{array}{c}d_1 & 0 & \cdots & 0 \\
0 & \ddots & \ddots & \vdots \\
\vdots & \ddots & \ddots & 0 \\
0 & \cdots & 0 & d_n \end{array}\right)
$$

**Identity Matrix** is a diagonal matrix with 1's in the place of $d_n$. The matrix is denoted as $\bm{I}$ and written as:
$$ D = 
\left(\begin{array}{c}1 & 0 & \cdots & 0 \\
0 & \ddots & \ddots & \vdots \\
\vdots & \ddots & \ddots & 0 \\
0 & \cdots & 0 & 1 \end{array}\right)
$$
The identity matrix is special in the sense that:
$$
\bm{I} \times \bm{A} = \bm{A} \times \bm{I} = \bm{A}
$$

## Matrix manipulations
As a note. Most of these manipulations can only be performed on square matrices, i.e. matrices of the size $m \times m$.

**The inverse of a matrix** is indicated by a superscript, $A^{-1}$, and is defined as follows:  
$$
\bm{A}^{-1}\bm{A} = \bm{A}\bm{A}^{-1} = \bm{I}
$$
If a matrix can be inverted it is said to be non-singular, and otherwise it is singular. To be invertible a matrix must be square, but not all square matrices are invertible.

**Transpose of matrix** It is possible to transform a matrix by "turning" the matrix so that the rows become columns. This is can also be done with vectors (as seen above). 

The transpose of $\bm{A}$ is indicated as $\bm{A}^T$ and is where the $i\text{th}$ column of $\bm{A}$ is the $i\text{th}$ row of $\bm{A}^T$. Thus:
$$
\bm{A}^{(m \times n)} = \bm{A}^{T(n \times m)}  
$$

$$
A = 
\begin{bmatrix}
   x_{1,1} & x_{1,2} \\
   x_{2,1} & x_{2,2}
\end{bmatrix}, A^T = \begin{bmatrix}
   x_{1,1} & x_{2,1} \\
   x_{1,2} & x_{2,2}
\end{bmatrix}
$$

## Math with vectors and matrices
It should be noted that for most intents and purposes a vector is simply a matrix with one column. I.e. it is a 1-dimensional matrix of the form $1 \times n$. Some operations cannot be performed between matrices and vectors though. 

**Algebraic laws** Most algebraic laws hold when working with matrices. Matrices are **not** commutative with multiplication
- Associative
$$
(A + B) + C = A + (B + C)
$$
$$
(AB)C = A(BC)
$$

- Distributive
$$
A(B+C) = AB + AC
$$
- Scalar multiplication
$$
(rA)B = A(rB) = r(AB)
$$

- Commutative addition
$$
A+B = B+A
$$

**Sum of matrices** To add two matrices you simple add the corresponding elements with each other. This means that the two matrices both have to have the same dimensions. 
Thus she sum of matrix $\bm{A}$ and $\bm{B}$ is defined as 
$$
c_{ij} = a_{ij} + b_{ij}
$$
Thus:
$$
A + B = 
$$
 
**Scalar-vector multiplication** Multiplying a scalar into either a vector or a matrix is quite simple. As mentioned previously it simply scales them and thus:
$$
\beta \cdot \bm{v}=(\beta x_1,\beta x_2, \cdots, \beta x_n)
$$
$$
 \beta \cdot \bm{A} =
\begin{bmatrix}
   \beta x_{1,1} & \beta x_{1,2} \\
   \beta x_{2,1} & \beta x_{2,2}
\end{bmatrix}
$$

**Vector-vector multiplication** The inner product returns a scalar and can be obtained by of mutliplying two vectors  is defined as:
$$
v^T \cdot u = \sum_{i=1}^n v_i u_i  
$$

The outer product returns a $m \times n$ matrix defined as 
$$
v \cdot u^T = \begin{bmatrix}
   v_1 u_1 & \cdots & v_1 u_n \\
   \vdots & \ddots & \vdots \\
   v_n u_1 & \cdots & v_n u_n 
\end{bmatrix}
$$

**Matrix multiplication** To multiply vectors and matrices the first element must have the same amount of columns as the other has rows. That means that a $m \times n$ element can be multiplied by a $n \times p$ element. But not the other way around. The formal definition is as follows
$$
c_{ik} = \sum_{j=1}^n a_{ij} b_{jk}
$$

$$ \bm{A} \bm{B} = 
\begin{bmatrix}
   a_{1,1} & a_{1,2} \\
   a_{2,1} & a_{2,2}
\end{bmatrix}
\begin{bmatrix}
   b_{1,1} & b_{1,2} & b_{1,3} \\
   b_{2,1} & b_{2,2} & b_{2,3}
\end{bmatrix}
=
\begin{bmatrix}
   a_{1,1} b_{1,1} + a_{1,2} b_{2,1} & a_{1,1} b_{1,2} + a_{1,2} b_{2,2} \\
   a_{2,1} b_{1,1} + a_{2,2} b{1,2} & a_{2,1} b_{2,1} + a_{2,2} b_{2,2}
\end{bmatrix}
$$

**Span** The span of a set of vectors is the set of all possible linear combinations of those vectors. The concept of span is closely related to linear independence and basis vectors, and is used to define the dimension of a vector space.

**Norm** is best understood as the calculation of different distances from an origin. they are all expressed as some version of $\lvert \lvert x \rvert \rvert_n$ or $L^n$.
- $L^1$, Manhattan:
$$
\sum_{i=1}^n \lvert x_i \rvert
$$   
- $L^2$, Euclidean:
$$
\sqrt{\sum_{i=1}^n x_i^2}
$$
- $L^p$, p-norm:
$$
\left( \sum_{i=1}^n x_i^p\right)^\frac{1}{p}
$$
- $L^\infty$, infinity:
$$
\max_i \lvert x_i \rvert
$$


**Determinant** of a square matrix is the product of a combination of rows and columns as defined by:

$$
\det(\bm{A})= \lvert \bm{A} \rvert = \sum_{j=1}^n(-1)^{i+j} \bm{A}_{i,j} \lvert \bm{A}_{\backslash i,\backslash j}\rvert
$$

This can easier be illustrated by the following image:

The determinant of a matrix is a scalar that can be used to determine whether a matrix is invertible, as well as to calculate the area or volume of a parallelogram or parallelepiped. The determinant is also used to calculate the eigenvalues of a matrix.


**Eigenvalue**


**The trace of a matrix** is the sum of all the elements on the diagonal and is defined as:
$$
\text{tr}(\bm{A})=\sum_{i=1}^n \bm{A}_{i,i}
$$


**Singular non singular** as mentioned in the part about invertibility of a matrix, a matrix is singular if it cannot be inverted.

**Basic operations**

**Symmetric**
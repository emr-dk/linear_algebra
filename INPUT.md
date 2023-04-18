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
$$\bold{v}=(x_1,x_2, \cdots, x_n)$$ 

Even though we formally wont introduce the transpose until later it is so frequently used that we will show a transposed vector below:

$$\bold{v}^T =\begin{pmatrix}
   x_1 \\
   x_2 \\
   \vdots \\
   x_n
\end{pmatrix}$$ 

A geometric vector is usually demonstrated with an arrow above the letter $\vec{v}$, but as we are working with a more generalized concpet of vectors we use the boldface indicator.

**Matrices:** Matrices are arrangements of numbers into rows and columns, used when solving systems of linear equations. The size of the matrix is written as a matrix row $\times$ column vector. Usually $n \times m$. In the example below $A$ is a $2 \times 2$ matrix and $B$ a $2 \times 3$. These are written in the following form:
$$ \bold{A} =
\begin{bmatrix}
   x_{1,1} & x_{1,2} \\
   x_{2,1} & x_{2,2}
\end{bmatrix}, \bold{B}= 
\begin{bmatrix}
   x_{1,1} & x_{1,2} & x_{1,3} \\
   x_{2,1} & x_{2,2} & x_{2,3}
\end{bmatrix}
$$

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

I will not go into how to solve these systems here 
## Math with vectors and matrices

It should be noted that for most intents and purposes a vector is simply a matrix with one column. I.e. it is a 1-dimensional matrix of the form $1 \times n$. 
### Scalar math
**Scalar multiplication** Multiplying a scalar into either a vector or a matrix is quite simple. As mentioned previously it simply scales them and thus:
$$
\beta \cdot \bold{v}=(\beta x_1,\beta x_2, \cdots, \beta x_n)
$$
$$
 \beta \cdot \bold{A} =
\begin{bmatrix}
   \beta x_{1,1} & \beta x_{1,2} \\
   \beta x_{2,1} & \beta x_{2,2}
\end{bmatrix}
$$

### Non-scalar math
From here on things get a bit more hairy. To multiply vectors and matrices the first element must have the same amount of columns as the other has rows. That means that a $m \times n$ element can be multiplied by a $n \times p$ element. But not the other way around. 

### Dot products
All dot products (or scalar products) return a scalar. I.e. a single value.


Geometric definition
$$
\bold{v} \cdot \bold{u} = \lvert \bold{v} \rvert \cdot \lvert \bold{u} \rvert \cos{\theta}
$$
"normal" definition
$$
\bold{v} \cdot \bold{u} = \sum_{i=1}^{n} v_i u_i 
$$

### Cross product
Where a dot product returns a scalar, the cross product always returns a matrix. 

$$
a \times b = \lvert a \rvert \lvert b \rvert \sin(\theta) n
$$ 

$$ \bold{A} \times \bold{B} = 
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
   a_{1,1} b_{1,1} & a_{1,1} b_{1,1} \\
   a_{1,1} b_{1,1} & a_{1,1} b_{1,1}
\end{bmatrix}
$$
$$ \bold{A} =
\begin{bmatrix}
   x_{1,1} & x_{1,2} \\
   x_{2,1} & x_{2,2}
\end{bmatrix}, \bold{B}= 
\begin{bmatrix}
   x_{1,1} & x_{1,2} & x_{1,3} \\
   x_{2,1} & x_{2,2} & x_{2,3}
\end{bmatrix}
$$


**Vector matrix multiplication**

**Matrix multiplication**

**Mathematical properties of matrices** 

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

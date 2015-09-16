---
layout: post
title:  "Linear Algebra Notes to Quiz 1"
date:   2015-09-02
categories: LinearAlgebra
---
#Day 1 notes
What is a Matrix?

- Rectangular array of objects
	- can be real numbers, sometimes complex

A=
$$ \begin{bmatrix} a & b & c & 1 \\\ d & e & f & 2 \\\ g & h & i & 3 \end{bmatrix} $$

A has 3 rows, 4 columns and a<sub>2,3</sub> = \\( f \\) the format is matrix<sub>row, column</sub>

What are they used for?

- System of linear equations
`2x -y + z = 2` and `-x   + 7z = 1`

$$ \begin{pmatrix} 2 & -1 & 1 \\\ -1 & 0 & 7 \end{pmatrix} $$
$$ \begin{pmatrix} 2 \\\ 1 \end{pmatrix} $$

- LCD, OLED are simply represented as matrices
- variance-covariance matrix in stats
- Google matrix represent nodes of internet

easily add operations

A<sub>mxt</sub> = B <sub>mxt</sub> are equal if they have the same values at every index
Sum
(a+b)<sub>i,j</sub> = a<sub>i,j</sub> + b<sub>i,j</sub>

scalar multiplication
each index value is multiplied by a constant value (scalar)

Zero matrix	
a matrix of `m,n` has all index values set to 0
- zero addition property

-----
Transpose of a matrix
transpose of an `m x n`  (matrix A) is defined as \\(A^T\\)

Properties of Transpose (theorem 1.2 on page 7)
\\( \; \\\ (A + B)^T = A^T + B^T \\\
(sA)^T = s A^T\\\
(A^T)^T = A \\)

\\( Exercise: Find (A - 3 B^T)^T + 4B \quad \\\ \\)
\\( A^T - 3B +4B  \quad which \quad simplifies \quad to \quad A^T + B \\)

$$
	A = 
		\begin{pmatrix}
		0 & 1 & 2 & -1 \\\
		0 & 2 & 3 & -1
		\end{pmatrix} \;
		B =
		\begin{pmatrix}
		1 & 2 \\\ 4 & -1 \\\ 1 & 0 \\\ 0 & 7 
		\end{pmatrix} \quad Resultant \quad Matrix \quad = \quad \begin{pmatrix} 	
	1 & 2 \\\
	5 & 1 \\\
	3 & 3 \\\
	-1 & 6
	\end{pmatrix}
$$

Linear Combinations	
Vector: either single row or single column
$$ u = \begin{pmatrix} 1 & 0 & -1 \end{pmatrix} \quad  v = \begin{pmatrix} 1 \\\ -1 \end{pmatrix} $$

usually use lowercase when naming vectors (compared to multi-dimensional matrices)

Example: Any vector in \\(R^3\\) is a linear combination of the standard unit vectors.

can 
$$ \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix} $$
be expressed as a linear combination of 
$$ \begin{pmatrix} 1 \\\ 2 \\\ 3 \end{pmatrix} and \begin{pmatrix} 0 \\\ 1 \\\ 1 \end{pmatrix} $$ ?


$$ c_1  \begin{pmatrix} 1 \\\ 2 \\\ 3 \end{pmatrix} + c_2 \begin{pmatrix} 0 \\\ 1 \\\ 1 \end{pmatrix}  = \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix}\\\$$
$$ \quad \quad \begin{pmatrix} c1 \\\ 2(c1) \\\ 3(c1) \end{pmatrix} +  \begin{pmatrix} 0 \\\ c2 \\\ c2 \end{pmatrix}  = \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix}$$
$$ \quad \quad \begin{pmatrix} c1 \\\ 2c1 + c2 \\\ 3c1 + c2 \end{pmatrix} = \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix} $$

\\( \quad \quad \quad \quad c1 = 2  \quad  c2 = -1 \\) with substation, we can see this evaluates as  a true solution

Standard unit vectors 
$$ e_1 = \begin{pmatrix} 1 \\\ 0 \\\ 0 \end{pmatrix} \quad e_2 = \begin{pmatrix} 0 \\\ 1 \\\ 0 \end{pmatrix} \quad e_3 = \begin{pmatrix} 0 \\\ 0 \\\ 1 \end{pmatrix} \quad
and \quad \begin{pmatrix} a \\\ b \\\ c \end{pmatrix} = ae_1 + be_2 + ce_3 \quad where \begin{pmatrix} a \\\ b \\\ c \end{pmatrix} \; is \; any \; vector \; R^3 $$

-----
Matrix Vector Product
Example: Find the matrix product \\( A \vec v \; where: \\)

$$
A = \begin{pmatrix} 1 & 2 & -1 \\\ 0 & -1 & 1 \end{pmatrix} \; \; and \; \; \vec v = \; \begin{pmatrix} 2 \\\ -3 \\\  7 \end{pmatrix} \quad \; A \vec v = 2 \begin{pmatrix} 1  \\\ 0 \end{pmatrix} + -3 \begin{pmatrix} 2  \\\ -1 \end{pmatrix} + 7 \begin{pmatrix} -1 \\\ 1 \end{pmatrix}  = \begin{pmatrix} -11 \\\ 10 \end{pmatrix} 
$$

----
Identity Matrices
\\( \begin{pmatrix} 1 & 0 & 0 & ... \\\ 0 & 1 & 0 & ... \\\ 0 & 0 & 1 & ... \end{pmatrix} \quad \quad \quad \quad \quad \quad \\) Rotation Matrix \\(  A_{ \theta} = \begin{pmatrix} cos \theta & - sin \theta \\\ sin \theta & cos \theta \end{pmatrix} \\)

given a vector, a user-defined theta offset can be applied using the rotation matrix

{% highlight matlab %}
>> A = [120; 25 - 1; 410 - 1] % Creating a matrix, semicolon separate rows
>> u = [0 2 8] % row vector
>> v = [0; 2; 8] % column vector
>> B = A' % find transpose of A and store in B^T
>> C = A + B
>> w = A * v % Matrix vector product
{% endhighlight %}

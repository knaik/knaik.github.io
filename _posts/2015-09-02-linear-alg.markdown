---
layout: post
title:  "Linear Algebra Notes"
date:   2015-09-02
categories: Linear Algebra
---
#Day 1 notes
$$ \begin{matrix} a & b & c \\\ d & e & f \\\ g & h & i \end{matrix} $$

What is a Matrix?
-Rectangular array of objects
-- can be real numbers, sometimes complex

A=
$$ \begin{matrix} a & b & c & 1 \\\ d & e & f & 2 \\\ g & h & i & 3 \end{matrix} $$

A has 3 rows, 4 colums
a_2,3_ = f

matrix_row, column_

What are they used for?
-System of linear equations
`2x -y + z = 2` and `-x   + 7z = 1`

$$ \begin{pmatrix} 2 & -1 & 1 \\\ -1 & 0 & 7 \end{pmatrix} $$
$$ \begin{pmatrix} 2 \\\ 1 \end{pmatrix} $$

-LCD, OLED are simply represented as matrices
-variance-covariance matrix in stats
-google matrix represent nodes of internet

easily add operations

A<sub>mxt</sub> = B <sub>mxt</sub> are equal if they have the same values at every index
Sum
(a+b)<sub>i,j</sub> = a_i,j + b_i,j

scalar multiplication
each index value is multiplied by a constant value (scalar)

Zero matrix	
a matrix of <sub>m,n</sub> has all index values set to 0
zero addition property

-----
Transpose of a matrix
transpose of an `m x n`  (matrix A) is defined as A^T

Properties of Transpose (theorm 1.2 on page 7)
$$ (A + B)^T = A^T + B^T \\\
(sA)^T = s A^T\\\
(A^T)^T = A$$

\\( Exercise: Find (A - 3 B^T)^T + 4B for\\)
\\( A^T - 3B +4B  which simplies to A^T + B \\)

$$
	A = 
		\begin{pmatrix}
		0 & 1 & 2 & -1 \\\
		0 & 2 & 3 & -1
		\end{pmatrix} \\
		B =
		\begin{pmatrix}
		1 & 2 \\\ 4 & -1 \\\ 1 & 0 \\\ 0 & 7 
		\end{pmatrix}
$$


Resultant Matrix = 
$$	\begin{pmatrix} 	
	1 & 2 \\\
	5 & 1 \\\
	3 & 3 \\\
	-1 & 6
	\end{pmatrix}
$$

Linear Combinations	
Vector: either single row or single column
$$ u = \begin{pmatrix} 1 & 0 & -1 \end{pmatrix}   v = \begin{pmatrix} 1 \\\ -1 \\\ 4 \\\ 0 \end{pmatrix} $$
usually use lowercase when naming vectors (compared to multi-dimensional matrices)

Example: Any vector in \\(R^3\\) is a linear combination of the standard unit vectors.

can 
$$ \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix} $$
be expressed as a linear combination of 
$$ \begin{pmatrix} 1 \\\ 2 \\\ 3 \end{pmatrix} and \begin{pmatrix} 0 \\\ 1 \\\ 1 \end{pmatrix} $$


$$ c_1  \begin{pmatrix} 1 \\\ 2 \\\ 3 \end{pmatrix} + c_2 \begin{pmatrix} 0 \\\ 1 \\\ 1 \end{pmatrix}  = \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix}\\\$$
$$ \begin{pmatrix} c1 \\\ 2(c1) \\\ 3(c1) \end{pmatrix} +  \begin{pmatrix} 0 \\\ c2 \\\ c2 \end{pmatrix}  = \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix}$$
$$ \begin{pmatrix} c1 \\\ 2c1 + c2 \\\ 3c1 + c2 \end{pmatrix} = \begin{pmatrix} 2 \\\ 3 \\\ 5 \end{pmatrix} $$

`c1 = 2   c2 = -1 ` by substation, we can see this evaluates as  a true solution

Standard unit vectors 
$$ e_1 = \begin{pmatrix} 1 \\\ 0 \\\ 0 \end{pmatrix} \\\
\begin{pmatrix} a \\\ b \\\ c \end{pmatrix} = ae_1 + be_2 + ce_3
$$

where a , b is any vector in r^3

-----
Matrix Vector Product
Example: Find the matrix product 
\\(
A \vect{v} where:

A = 
\begin{pmatrix}
1 & 2 & -1 \\\
0 & -1 & 1
\end{pmatrix} 
\vect{v} =
\begin{pmatrix}
2 \\\ -3 \\\  7 
\end{pmatrix} \\\
A \vect{v} = 
2 \begin{pmatrix}
1  \\\ 0 
\end{pmatrix}
+ -3 \begin{pmatrix}
2  \\\ -1 
\end{pmatrix}
+ 7 \begin{pmatrix}
-1 \\\ 1
\end{pmatrix}
 =
\begin{pmatrix}
-11 \\\ 10 
\end{pmatrix}
\\)

----
Identity Matrices
$$ \begin{pmatrix} 1 & 0 & 0 & ... \\\ 0 & 1 & 0 & ... \\\ 0 & 0 & 1 & ... \end{pmatrix} $$

Rotation Matrix
$$ A_\theta = \begin{matrix} cos \theta & - sin \theta \\\ sin \theta & cos \theta \end{pmatrix} $$

given a vector, a user-defined theta offset can be applied using the rotation matrix




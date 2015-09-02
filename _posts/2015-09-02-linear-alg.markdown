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



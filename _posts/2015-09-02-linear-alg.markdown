---
layout: post
title:  "Linear Algebra Notes"
date:   2015-09-08 
categories: Linear Algebra
---
#Day 2

1.1 no 71
Symmetric 
\\( A = A^T \quad a_{i,j} = a_{i,j}^T = a_{j,i} \quad a_{i,j} = a_{j,i} \\)

\\(begin{bmatrix} a & b & c \\\ b & e & f \\\ c & f & i \end{bmatrix} \\)

1.2 no 37
u = [3		, S = { [1		[2		[-2
		8]					2],	3],	 5]}
						c1 * .   c2*..   c3*...
						
				
						
\\( \begin{bmatrix} c_1 + 2c_2 - 2c_3 \\\ 2 c_1 + 3c_2 + 5c_3 \end{bmatrix} \quad \begin{bmatrix} 3 \\\ 8 \end{bmatrix} \\)

System of linear equations:
\\(  a_1x_1+a_2x_2+\cdots +a_nx_n = k \\\
     a_1,\, a_2,\ \dots,\ a_n$ and $k$ are real numbers \\\
 x_1,\, x_2,\ \dots,\ x_n are the variables \\)
 

 An equation is non-lin if any var is raised to a power, multiplied together or involve other functions
 
System oflin eq

\\(	a_{11}x_1 +  a_{12}x_2 + \cdots a_{1n}x_n =  b_1\\\
	a_{21}x_1 +  a_{22}x_2 + \cdots a_{2n}x_n =  b_2\\\
	\vdots  \quad \quad \quad \quad \quad  \vdots\\\
	 a_{m1}x_1 +  a_{m2}x_2 + \cdots a_{mn}x_n =  b_n \\\ \\)

\\( x_1 \begin{bmatrix} a_11 \\\ \vdots \end{bmatrix} +  x_2 \begin{bmatrix} a_21 \\\ \vdots \end{bmatrix} +  x_3 \begin{bmatrix} a_31 \\\ \vdots  \end{bmatrix}   = \begin{bmatrix} b \\\ \vdots  \end{bmatrix} \\
A =  \begin{bmatrix} a_11 \end{bmatrix} , x = \begin{bmatrix} x_1 \\\ x_2 \\\ \vdots \end{bmatrix} ,  b = \begin{bmatrix} b \\\ \vdots \end{bmatrix} \\\
Ax = b \\)

`x + y +z = 1`
`x -4y -z = 7`
`0 + y + 2z = 0`

\\( \begin{bmatrix} 1 &  1  & 1 \\\ 1 & -4 & -1 \\\ 0 & 1 & 2 \end{bmatrix}  \begin{bmatrix} x \\\ y \\\ z \end{bmatrix}  = \begin{bmatrix} 1 \\\ 7 \\\ 0 \end{bmatrix} \\)

Three operations that do not change a system of equations:
- Interchange two equations
- Multiply an equation by a non-zero scaler
- Multiply an equation by a scaler and add to another equation

\\(	A =>  \leftrightarrow r_j B \\\ \\)
	 Multiply a row by a non-zero scaler
	 
\\( A $r_i \rightarrow cr_i$}} \, B$
	\item[] Multiply a row by a scaler and add to another row
	$A \, \xrightarrow{\makebox[2cm]{$r_i \rightarrow cr_j + r_i$}} \, B$ \\)
	
Interchange two equations
\\( \begin{bmatrix}	2&-3&4&1\\\	-1&2&-1&-2\\\	2&3&1&-2	\end{bmatrix}	\xrightarrow{{r_1 \leftrightarrow r_2}} 	\begin{bmatrix}	-1&2&-1&-2\\\ 	2&-3&4&1\\\ 	2&3&1&-2 	\end{bmatrix} \\)
	
Multiply an equation by a non-zero scaler
\\(	\begin{bmatrix}	-1&2&-1&-2\\\
	%
	2&-3&4&1\\\
	%
	2&3&1&-2 	\end{bmatrix}
	%
	\xrightarrow{{$r_2 \rightarrow 2r_1 + r_2$}}
	%
	\begin{bmatrix}
	-1&2&-1&-2\\\
	%
	0&1&2&-3\\\
	%
	2&3&1&-2
	\end{bmatrix} \\)
	
Multiply an equation by a scaler and add to another equation
\\(	\begin{bmatrix}
	-1&2&-1&-2\\\
	%
	0&1&2&-3\\\
	%
	2&3&1&-2
	\end{bmatrix}
	%
	\xrightarrow{{$\begin{subarray}{l} r_3 \rightarrow 2r_1 + r_3 \\ r_1 \rightarrow -1r_1 \end{subarray}$}}
	%
	\begin{bmatrix}
	1&-2&1&2\\\
	%
	0&1&2&-3\\\
	%
	0&7&-1&-6
	\end{bmatrix}
	\\)

---------------------------
Special form of Matrices, goal is to use row ops to get to one of the special forms

The Row-Echelon Form:
 - The zero rows are in the bottom of the matrix
 - Each *leading entry* is in a column to the right of the leading entry in the previous row
 - The entries under leading entries are equal to zero * not real condition, just an implication

 $$ 	\begin{bmatrix} 2&-3&4&1 \\\ 0&0&-1&-2\\\ 0&0&0&0 \end{bmatrix} \quad and \quad \begin{bmatrix}  0&2&-1&-2 \\\ 0&0&4&1\\\ 0&0&0&5	\end{bmatrix}	$$

 Non-examples:
 
 $$	\begin{bmatrix} 	2&-3&4\\\ 0&0&0\\\	0&0&1 	\end{bmatrix} \quad and \quad	\begin{bmatrix} 2&-3&4 \\\ 0&0&5 \\\ 0&0&1	\end{bmatrix} $$
	
Reduced Row Echelon form:
- All conditions of Row-Echelon form
- All leading entries are one (multiply with coefficient --> row operations to make this true)
- Entries above AND below leading entries are all zero
	-identity matrix in reduced row echelon

\\(	\begin{bmatrix} 1&-3&0&1 \\\ 0&0&1&-2\\\  0&0&0&0 	\end{bmatrix} \quad  \begin{bmatrix}	0&1&0&0\\\	0&0&1&0\\\	0&0&0&1	\end{bmatrix} \\\
	Non\; examples \quad \begin{bmatrix}  1&0&4\\\	0&1&0\\\	0&0&2 	\end{bmatrix} \quad \begin{bmatrix} 1&0&0\\\	0&0&1\\\	0&0&1	\end{bmatrix} \\)

augmented matrix 

`x + y +z = 1`
`x -4y -z = 7`
`0 + y + 2z = 0`
\\( \begin{bmatrix} 1 & 1 & 1 & | 1 \\\ 1 & -4 & | -1 \\\ 0 & 1 & 2 & \0 \end{bmatrix} \quad 	\xrightarrow{{row operations}} 	\begin{bmatrix}	1&0&0& \frac{7}{4}\\\	0&1&0 & \frac{-3}{2}\\\	0&0&1 & \frac{3}{4} \end{bmatrix} \\\ 
x_1 = \frac{7}{4}, \quad x_2= -\frac{3}{2}, \quad x_3 = \frac{3}{4} \\)

\\( x = \begin{bmatrix} 2 \\\ 1 - 2x_3 \\\ x_3 \end{bmatrix} = \begin{bmatrix} 2 \\\ 1 \\\ 0 \end{bmatrix} + \begin{bmatrix} 0 \\\ -2x_3 \\\ x_3 \end{bmatrix} \\\
= \begin{bmatrix} 2\\\ 1 \\\ 0 \end{bmatrix} + x_3 \begin{bmatrix} 0 \\\ -2 \\\ 1 \end{bmatrix} \\)

example b
soln 
	x3= 0, x2 = x2, x1 = 5 - 2x2

\\( x = \begin{bmatrix} 5 - 2x_2 \\\ x_2 \\\ 0 \end{bmatrix} = \begin{bmatrix} 5 \\\ 0 \\\ 0 \end{bmatrix} + \begin{bmatrix} -2x2 x2 0...... \\)

example c
no solution because
last row gives self contradictory solution `0 = 4 `

	
	
	
	
	

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

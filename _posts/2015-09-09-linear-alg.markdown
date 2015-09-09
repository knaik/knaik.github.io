---
layout: post
title:  "Linear Algebra Notes"
date:   2015-09-09
categories: LinearAlgebra
---
#Day 3
##Gaussian Elimination 1.4

- Start with the left-most non-zero column
- This is called a pivot column: the pivot position is at the top.
- Select a non-zero entry in the column to be the pivot
- Move the pivot into the pivot position
- Use interchanging rows if necessary
- Change all the values below the pivot to zero
- Use row operations if needed
- Repeat the procedure on the submatrix formed by the remaining rows 
- Go through all the rows
- The matrix will be converted to row echelon form.

$$ \begin{bmatrix} 0 & 0 & 2 & 3 \\\ 0 & -1 & 4 & 5 \\\ 0 & 1 & 2 & 1 \end{bmatrix}\to r_1 <- -> r_2\to \begin{bmatrix} 0 & -1 & 4 & 5 \\\ 0 & 0 & 2 & 3 \\\ 0 & 1 & 2 & 1 \end{bmatrix} $$
$$ r_3 \to r_1+ r_2 \begin{bmatrix} 0 & -1 & 4 & 5 \\\ 0 & 0 & 2 & 3 \\\ 0 & 0 & 6 & 6 \end{bmatrix} \to r_3 \to -3r_2 + r_3 \to \begin{bmatrix} 0 & -1 & 4 & 5 \\\ 0 & 0 & 2 & 3 \\\ 0 & 0 & 0 & -3 \end{bmatrix}$$



$$ \begin{bmatrix} 1& 3 & 5 & 7 & 0 \\\ 3 & 5 & 7 & 9 & 0 \\\ 5& 7 & 9 & 1 & 20 \end{bmatrix} \\\
Solution: \\\
\begin{bmatrix} 1& 3 & 5 & 7 & 0 \\\ 3 & 5 & 7 & 9 & 0 \\\ 5& 7 & 9 & 1 & 20 \end{bmatrix} \xrightarrow{\begin{subarray}{l} r_2 \rightarrow -3r_1 + r_2 \\ r_3 \rightarrow -5r_1 + r_3 \end{subarray}} \begin{bmatrix} 1& 3 & 5 & 7 & 0\\\ 0 & -4 & -8 & -12 & 0 \\\ 0 & -8 & -16 & -34 & 20	\end{bmatrix} \\\
\begin{bmatrix}
1& 3 & 5 & 7 & 0\\\
0 & -4 & -8 & -12 & 0 \\\
0 & -8 & -16 & -34 & 20
\end{bmatrix}
\xrightarrow{r_3 \rightarrow -2r_2 + r_3}
\begin{bmatrix}
1& 3 & 5 & 7 & 0\\\
0 & -4 & -8 & -12 & 0 \\\
0 & 0 & 0 & -10 & 20
\end{bmatrix}
$$

1 3 5 7 0 	r1 //first is already 1
3 5 7 9 0 	r2
5 7 9 1 20 	r3

r2 -> -3r1 +  r2 
1  3  5  7  0 	r1
0 -4 -8 -12 0  r2 
5 7 9 1 20 		r3

r3 -> -5r1 +  r3
1  3  5     7   0 	r1
0 -4 -8   -12  0  r2 
0 -8 -16 -34 20 r3 

r3 -> -2r2 + r3
1  3  5     7   0 	r1
0 -4 -8   -12  0  r2 
0  0  0    -10  20 r3 

Reduced Rowechelon 
zero above leading entries

1  [3]  5     [7]     0 	r1
0 -4   -8   [-12]    0    r2 
0  0    0    -10     20   r3 

Gauss-Jordan Method

- First bring the matrix to the row-echelon form
- Scale pivots to be 1 
- Starting from the bottom pivot use row  operations to change all the values above pivots to be zero  

$$ \begin{bmatrix} 1& 3 & 5 & 7 & 0\\\ 0 & -4 & -8 & -12 & 0 \\\ 0 & 0 & 0 & -10 & 20 \end{bmatrix}
\xrightarrow{\begin{subarray}{l} r_2 \rightarrow \frac{-1}{4} r_2 \\ r_3 \rightarrow \frac{-1}{10} r_3 \end{subarray}}
\begin{bmatrix}
1& 3 & 5 & 7 & 0\\\
0 & 1 & 2 & 3 & 0 \\\
0 & 0 & 0 & 1 & 2 \end{bmatrix} \\\
\begin{bmatrix} 1& 3 & 5 & 7 & 0\\\ 0 & 1 & 2 & 3 & 0 \\\ 0 & 0 & 0 & 1 & 2 \end{bmatrix}
\xrightarrow{\begin{subarray}{l} r_2 \rightarrow -3r_3 + r_2 \\ r_1 \rightarrow -7r_3 + r_1 \end{subarray}}
\begin{bmatrix}
1& 3 & 5 & 0 & -14\\\
0 & 1 & 2 & 0 & -6 \\\
0 & 0 & 0 & 1 & 2
\end{bmatrix} \\\
\begin{bmatrix}
1& 3 & 5 & 0 & -14\\\
0 & 1 & 2 & 0 & -6 \\\
0 & 0 & 0 & 1 & 2
\end{bmatrix}
\xrightarrow{r_1 \rightarrow -3 r_2 + r_1}
\begin{bmatrix} 1& 0 & -1 & 0 & 4\\\ 0 & 1 & 2 & 0 & -6 \\\ 0 & 0 & 0 & 1 & 2 \end{bmatrix} $$









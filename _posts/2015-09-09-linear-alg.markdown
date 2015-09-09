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
\begin{bmatrix} 1& 3 & 5 & 7 & 0 \\\ 3 & 5 & 7 & 9 & 0 \\\ 5& 7 & 9 & 1 & 20 \end{bmatrix} \xrightarrow{\begin{subarray}{l} r_2 \rightarrow -3r_1 + r_2 \\ r_3 \rightarrow -5r_1 + r_3 \end{subarray}} \begin{bmatrix} 1& 3 & 5 & 7 & 0\\\ 0 & -4 & -8 & -12 & 0 \\\ 0 & -8 & -16 & -34 & 20	\end{bmatrix} $$
$$ \begin{bmatrix}
1& 3 & 5 & 7 & 0\\\
0 & -4 & -8 & -12 & 0 \\\
0 & -8 & -16 & -34 & 20
\end{bmatrix}
\xrightarrow{$r_3 \rightarrow -2r_2 + r_3$}
\begin{bmatrix}
1& 3 & 5 & 7 & 0\\\
0 & -4 & -8 & -12 & 0 \\\
0 & 0 & 0 & -10 & 20
\end{bmatrix}
$$
---
layout: post
title:  "Linear Algebra Latex Test"
date:   2015-09-02 11:23:32
categories: Linear Algebra
---
#A trial of copy paste Latex code

\def\d#1#2{ \frac{d #1}{d #2}}
\def\dn#1#2#3{\frac{d^{#3}{#1}}{d #2^{#3}}}
\def\dd#1#2{\dn{#1}{#2}{2}}
\def\L{{\mathcal{L}}}

\newcommand{\vect}[1]{\boldsymbol{#1}}​

\frame{\titlepage}

\section{Matrices}

\frame{
\frametitle{What is a Matrix?}

\begin{itemize}[<+-| alert@+>]
	\item  A rectangular array of "objects" or entries
	\vspace{0.1in}
	\item[] The entries are usually real numbers (in this course). Can be complex numbers, vectors, functions,...
	\item[] Organized in rows and columns and enclosed inside brackets
	\item[] We usually denote matrices using uppercase letters. 
	\item[] The corresponding lowercase letter, indexed by the row and column numbers is used to refer to the entries.
	\vspace{0.1in}
	\item Examples: 
	\begin{equation*}
	A = 
	\begin{pmatrix}
	0 & 1 & 2 & -1 \\
	1 & 0 & 1 & 1 \\
	0 & 2 & 3 & -1
	\end{pmatrix} \,,
	\qquad B =
	\begin{pmatrix}
	1 & \pi \\ 4 & \sqrt{2} \\ 0 & 7 
	\end{pmatrix}
	\end{equation*}
	\item[] $A$ has $3$ rows and $4$ columns. $B$ has $3$ rows and $2$ columns
	\vspace{0.1in} 
	\item[]  $a_{2,3} =1, \, a_{3,1} = 0, \, b_{2,2}=\sqrt{2}$  
	\item[\ ]
\end{itemize}
}

\frame{	
	\frametitle{The Where and the Why of Matrices}
	\pause
	Where?
	\vspace{0.1in} 
	\begin{itemize}
		\item Systems of linear equations: The coefficients form a matrix
		\item A computer monitor consists of rows (and columns) of pixels: each has an associated vector of intensities.
		\item A variance-covariance matrix (in statistics) contains the measures of association between variables. 
		\item A Google matrix represents a graph with edges representing links between web pages. About 30 billion rows and columns!
	\end{itemize}
	\pause 
	\vspace{0.1in} 
	Why?	
	\begin{itemize}
		\item Abstract the rectangular array. Add math operations:
		\item[] analyze it mathematically
		\item[] find hidden patterns and structures
	\end{itemize}
}

\frame{	
	\frametitle{Matrix Arithmatic}

	\vspace{0.1in}
	\begin{itemize}[<+-| alert@+>]
		\item  Equality: Two matrices are the same if they have the same size and if the corresponding entries are the same.
		\item[] $A_{mxn} = B_{mxn} \iff a_{i,j} = b_{i,j} \, \mathrm{for \, all} \, i,j$
		\vspace{0.1in}
		\item Sum: Two matrices of the same size can be added by adding the individual entries. 
		\item[] $(a + b)_{i,j} = a_{i,j} + b_{i,j}$
		\vspace{0.1in}
		\item Scaler Multiplication: Multiply each entry by the scaler
		\item[] $(cA)_{i,j} = c a_{i,j}$
		\vspace{0.1in}
		\item The zero matrix $0_{m\times n}$ has all entries equal to $0$.
		\item[] For any matrix $A_{m\times n}$, $A_{m\times n} + 0_{m\times n} = A_{m\times n}$
		\vspace{0.2in}
		\item Study example 1 on page 5
		\item Go over Theorem 1.1 on page 6
	\end{itemize}
}

\frame{	
	\frametitle{Transpose of a Matrix}
	\begin{definition}
		The transpose of an $n\times m$ matrix $A$ is the $m \times n$ matrix $A^T$ defined by $a^T_{i,j} = a_{j,i} \,$.
	\end{definition}
	\vspace{0.1in}
	\begin{itemize}[<+-| alert@+>]
		\item  Properties of the transpose (see theorem 1.2 on page 7).
		\item[] $(A+B)^T = A^T + B^T$
		\item[] $(sA)^T = sA^T$
		\item[] $(A^T)^T = A$
		\vspace{0.1in}
		\item Exercise: Find $(A - 3 B^T)^T + 4B$ for
		\begin{equation*}
		A = 
		\begin{pmatrix}
		0 & 1 & 2 & -1 \\
		0 & 2 & 3 & -1
		\end{pmatrix} \,,
		\qquad B =
		\begin{pmatrix}
		1 & 2 \\ 4 & -1 \\ 1 & 0 \\ 0 & 7 
		\end{pmatrix}
		\end{equation*}
	\end{itemize}	
}

%\frame{
%	\frametitle{Plot of the Direction Field for Free Fall Example}
%	\includegraphics{l1ex1}	
%}


\section{Linear Combinations, Matrix Vector Product, Special Matrices  - 1.2}
\frame{

\frametitle{Linear Combinations}

\begin{itemize}[<+-| alert@+>]
\item A matrix with exactly one column (or row) is called a vector. 
\item[] Example: 
		\begin{equation*}
		\vect{u}= \begin{pmatrix}
			1  \\ 4  \\ 1 \\ 0  
		\end{pmatrix}
		, \quad \vect{v} = \begin{pmatrix}
		1  $ -2  $ 0  
		\end{pmatrix}
		\end{equation*}
\vspace{0.1in}
\item A \emph{linear combination} of $k$ vectors $\vect{u_1}, \vect{u_2}, ... \vect{u_k}$ is a vector of the form $c_1\vect{u_1} + c_2\vect{u_2} + \cdots + c_k\vect{u_k}$ where $c_1, c_2, ... c_k$ are scalers.
\item[] Go over example 1 on page 14.
\vspace{0.1in}
\item Example: Any vector in $R^3$ is a linear combination of the standard unit vectors.
\end{itemize}
}

\frame{
\frametitle{Matrix Vector Products}
\begin{itemize}[<+-| alert@+>]
\item Definition (page 19): Let $A$ be an $m \times n$ matrix and $\vect{v}$ an $n \times 1$ vector. The \emph{matrix vector product} $A \vect{v}$ is defined as the linear combination $ v_1 \vect{a_1} + v_2 \vect{a_2} + \cdots + v_n \vect{a_n}$ formed by the components of $\vect{v}$ and column vectors of $A$.
\vspace{0.1in}
\item[] Example: Find the matrix product $A \vect{v}$ where:
		\begin{equation*}
		A = 
		\begin{pmatrix}
		1 & 2 & -1 \\
		0 & -1 & 1
		\end{pmatrix} \,,
		\qquad \vect{v} =
		\begin{pmatrix}
		2 \\ -3 \\  7 
		\end{pmatrix}
		\end{equation*}
\item[] 		\begin{equation*}
A \vect{v} = 
2 \begin{pmatrix}
1  \\ 0 
\end{pmatrix}
+ -3 \begin{pmatrix}
2  \\ -1 
\end{pmatrix}
+ 7 \begin{pmatrix}
-1 \\ 1
\end{pmatrix}
 =
\begin{pmatrix}
-11 \\ 10 
\end{pmatrix}
\end{equation*}

\item Can to do this using the rows of $A$ too. Read pages 20-21.
\item Read and understand theorem 1.3 on page 24.
\end{itemize}	
}

\frame{
	\frametitle{Special Matrices: The Identity Matrix $I_n$}
	\begin{itemize}[<+-| alert@+>]
		\item Definition (page 22): For each positive integer $n$, the $n \times n$ identity matrix $I_n$ is the $n \times n$ matrix whose columns are the standard vectors $\vect{e_1}, \vect{e_2}, ... \vect{e_n}$ of $R^n$.
		\vspace{0.1in}
		\item[] Examples: 
		\begin{equation*}
		I_3= \begin{pmatrix}
		1 & 0 & 0 \\
		0 & 1 & 0 \\
		0 & 0 & 1
		\end{pmatrix}
		, \quad I_2 = \begin{pmatrix}
		1 & 0 \\
		0 & 1 
		\end{pmatrix}
		\end{equation*}
		\vspace{0.1in}
		\item Exercise: Write down any $3 \times 1$ column vector $\vect{v}$ and  Calculate $I_3 \vect{v}$.
		\vspace{0.1in}
		\item General Property: If $\vect{v}$ is \emph{any} $n \times 1$ column vector, then $I_n \vect{v} = \vect{v}$
	\end{itemize}
}

\frame{
	\frametitle{Special Matrices: The Rotation Matrices $A_\theta$}
	\begin{itemize}[<+-| alert@+>]
		\item Definition (page 23): The rotation matrix $A_\theta$ is defined by
		\begin{equation*}
		A_\theta = \begin{pmatrix}
		\cos \theta & -\sin \theta\\
		\sin \theta & \cos \theta
		\end{pmatrix}
		\end{equation*}
		\item Multiplying a vector by a $A_\theta$  rotates the vector counterclockwise by the angle $\theta$.
		\vspace{0.1in}
		\item What is $A_{45^{\circ}}$ ? Apply it to $\vect{e_1}$ once, and twice and check the result.
		\vspace{0.1in}
		\item Show that $A_{0^{\circ}}$ is the same as $I_2$.
		 
	\end{itemize}
}

\section{MATLAB}

\frame{
	\frametitle{Matrices in MATLAB}
	
	\begin{itemize}[<+-| alert@+>]
		\item Creating a matrix:\\
		$>> A = [1\, 2\, 0; 2\, 5\, -1; 4\, 10\, -1]$
		\item[] The semicolons separate the rows. 
		\item Create a row vector:\\
		$>> u = [0\, 2\, 8]$	
		\item Create a column vector:\\
		$>> v = [0;2;8]$	
		\item Find the transpose:\\
		$>>  B = A'$\\
		\item Add two matrices:\\
		$>> C = A + B$
		\item Matrix vector product:\\
		$>> w = A*v$ 
	\end{itemize}
}
 </script>
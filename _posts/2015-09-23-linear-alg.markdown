Lesson 6 
---
layout: post
title:  "Lesson 6"
date:   2015-09-23
categories: LinearAlgebra
---
#Lesson 6
An nxn matrix A is invertible if there exists and nxn matrix B such athat
AB = BA = I<sub>n</sub>. In this case B is the inverse 
1, 1; 1, 2]; 2, -1; -1, 1];

2+ -1, -1+ 1; 2 -2, -1+ 2]; = 1,0; 0,1];

2-1, 1-1; -1 + 1, -1 + 2]; = 1,0; 0,1];

General form, prove
A = a, b; c, d]; , A^-1 = 1 / ad - bc [d, -b; -c, a];

multiply A and A^-1 times scalar coefficient ..
[ad - bc, a(-b) + ba; cd - dc, -bc + da] * coeff = [ad-bc / ad-bc, 0; 0, ad - bc/ad-bc];

The matrix is not invertible when ad - bc (the sum of the product of the diagonals0 = 0; since 1/ad - bc != 1/0 (undef);
1/ad-bc = the determinant of a 2x2 matrix.

Theorem, let A and B be `nxn`
I. if A is invertible then the inverse of A has to be, (A^-1)^-1 = A
II. if A and B are invertible, then AB is invertible and (AB)^-1 = B^-1 *A^-1
III. if A is invertible, then so is it's transponse, and (A^T)-1 = (A^-1)^T

aka,
I. the inverse of the inverse of A is itself. AA^-1 = I, A^-1A = I =>A^-1 A = I and AA&-1 = I;
II. The inverse of the product of two matrices is equal to the product of the inverse of the second times the product of the inverse of the first
AB(B^-1A^-1) =I and B-1A-1(AB) = I, = ABB-1A-1, AB B-1A-1, A In A-1 = AA-1 = A; and the same for the other side
III. A*A-1 = In, now we take transpose of left and right, AA-1^T - I^T, then by property of transpose (AB^T = B^T*A^T),
A-1^T A^T = In^T ( = In), . then prove the same by starting with A-1A = In, .. A^T(A-1)^T = I => A^T^-1 = (A^-1)^T.

HW #9 #11 #15,

(B^T)^-1 = (B^-1)^T = [2, 0, 3; -1, 0, -2; 3, 4, 1].
(BA) ^-1 = A^-1 B^-1, = [2+0+9, -1 + 0 + -6, 3 + 8 + 3; 4 + 0 + 3, -2 + 0 + -2, 6 + 0 + 1; 2 + 0 - 3, -1 + 0 + 2, 3 + 4 -1];= 11, -7, 14; 7, -4, 7; -1, 1, 6];
[11, -7, 14; 7, -4, 7; -1, 1, 6];


Elementary row ops
multiplying Amxn by Em(the elementary matrix obtained by doin ght row op on Im), has the same effect od oing the row ops

replace row ops by matrix op.

Review questions:
True or false? If the only solution of Ax = 0 is the trivial solution, then the columns are linearly independant.

we have u_1, u_2, u_3, u_4... u_k;
if c1u1 + c2i2.. must allci's be zero - yes linear indie. no linear dependent.

Therefor true, since each.

[1; -1], [-1; 1]; = [0;0];
dependent

c1[1;0] + c2[0;1]; = [0,0];
indiependt

if u and v are linealry indie, and if {u, v, w} is linearly depen, then w is in Span{u, v}
true, if a set has redundancy, then there is a linear part that we don't need.

we know u and v are indie, but u, v, w is not.
c1u + c2v + c3w = 0

we can not have c3 = 0 and c1,c2 != 0,  because
if then we would have u v dependent but since we know that is not true, C3 != 0;

now we can write u and v in terms of c3w.

(c1u + c2v) * (1/c3) = w;

since w can be written as a linear combinaitn of u and v, we can therefor say w is in the Span{u,v};

{u1, u2, 0} is linearly dependent.
true 
c1u1 + c2u2 + c3*0 = 0;

by picking c3 to be non-zero and c1 and c2 = 0.
and therefore it is dependent.

ANY SET involving 0 vector is linearly Dependent.	

if u1, u2, u3, u4 is linearly indie, then so is u1, u2, u3?

if u1, u2, u3, is lin dep, then c1u1, cu2, cu3, = 0 and at least one ci is!=0;
we do not lose generality (in this case) by picking c ranodmly.

Let's say c1 != 0, and then
c1u1 + cu2 + cu3 + 0*u4 = 0;
therefore u1,u2,u3,u4 is lin dep,.. cutting down does not make indie into dependent.. not true for dependt. 

S is linearly dep, then each vector is a linear combin of the other vectors in S

any 5 x 8 are linearly dependent.

------------------------------------------------------

Lesson 6:
Let A[] be m x r, and B[] be r x n. The product AB is defined as the matrix m x n whose ABij = is the product of the Aith row x Bjth column

number of columns in A have to be the same number as rows in B.

we learned dot product in calc?

[ 2 0 -1; 			[1 0;
  1 0 0; 			 2 -1;
  0 1 1] (3x3) *  0 1]; (3x2)

we get a resulting 3x2:
[2*1 + 0*2 + -1*0, -1;
1 (+0 +0), 0;
2, 0]

Which products are possible?
A[1, 0, -1; 2, 2, 0]; B[1, 1, -1; 4, 0, 1; 1, 0 , 0]; C[1, 1; 0, -2];

Valid?
AB, CA, BB, CC

Invalid:
BA, AC, CA, BC, CB, AA

When multiplying by itself, possible only with square M[](mxn) when m  = n.

Properties of matrices, Theorem 2.1 p100; Given A(kxm) B(kxm), C(mxn), P(nxp), Q(nxp);
s(AC) = sA(C) = A(sC) for any scalar
A(CP) = AC(P) for each b which exists in R^n (
!!note we can not change order and multiply A and P and then C
(A+B)C = AC + BC; distributive property (and reverse C(P+Q) = CP + CQ;)
Ik (identity matrix, square m x m with  diagonal 1s [1, 0, 0; 0, 1, 0; 0, 0, 1]; .. 
IkA = A = AIm where A[](kxm) (dimensions based on order. for I x A, I should be kxk; for A x I, I should be m x m;)
(AC)^T = C^T * A^T

A[1, 4; 0, 3]; B[9, 0; 14, 2]; AB= [9 + 4*14, 8; 42, 6]; BA = [..

{% highlight matlab%}
A = fix(10*rand(2,3)); % entries would be -1, 1; fix rounds the numbers.. so generates a 2x3 from -10, 10?
{% endhighlight %}
 

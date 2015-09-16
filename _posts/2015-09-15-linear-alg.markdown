---
layout: post
title:  "Linear Algebra Notes"
date:   2015-09-15
categories: LinearAlgebra
---
#Day 5

Context, from last class:

Span(V_1) = Span (V_1, 2V_1)

Here, the addition of a vector to itself, does not change the span.

Theorem: If v in a linear combination of u1 u2, ... ,uk, then, span(u1,u2, ... ,uk) = span(u1, u2, ... ,uk,v)

eg
\\( v = 3 u_1 + 2u_2 + 0u_3 - u4, v \; would \; not \; add \; to \; the \; span \\\
but \quad u_4 = 3u_1 + 2u_2 + 0u_3 - v \\)

We do not base definition on a single vector, we make general statements porperty statements. 

All we can say is \\( 3U_1 + 2u_2 + 0u_3 - u_4 - v = 0 \\)

The 0u3 can not be thrown out, 

A set of k vectors { \\(u_1, u_2, ... , u_k\\) } in R^n is called linealry dependent if there exists
scalers \\(c_1 + c_2 + ... + c_k \quad c_1 u_1 + c_2  u_2+ ... + c_k u_k = 0 \\) and not all c1, c2 are all zero.

Suppose c1 != zero, ((\  c_2  u_2+ ... + c_k u_k = c_1 u_1 \quad ( 1/ {c_1 u_1} )(c_2  u_2+ ... + c_k u_k = u_1) \\)

In order to ensure not dependent, you need to solve

((\ \vect{u}_1, \vect{u}_2, \cdots \vect{u}_k \\) is linear independent if and only if the only solution of \\( A \vect{x} =\vect{0} \; \; , \; where \; \;  A = \vect{u}_1, \vect{u}_2, \cdots \vect{u}_k \\) is the zero solution

1 1 1 1 = 0 ((\ r_2 -> -2r_1 + r_2 \\)

2 4 0 2 = 0 ((\r_3 -> -r_1 + r_3 \\)
1 1 1 3 = 0

 1  1  1  1  
 0  2 -2  0  
 0  0  0  2  

1 1  1 1 
0 1 -1 0
0 0  0 2

1 1 1 1
0 1 -1 0
0 0 0 1

1 0  2 0
0 1 -1 0
0 0  0 1

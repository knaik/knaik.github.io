Lesson 5 
---
layout: post
title:  "Lesson 5+"
date:   2015-09-21
categories: LinearAlgebra
---
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

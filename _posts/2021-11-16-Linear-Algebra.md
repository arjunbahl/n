---
id: "DJUMDaKBAgnYUX9K5PIel"
title: "Linear Algebra"
desc: ''
updated: "1643035548170"
created: "1637049329055"
date: "2021-11-16"
categories: 
  - "research"
---
<!-- Solutions https://linearalgebras.com/2a.html 
Sheldon Axler - "Linear Algebra" Done Right-Springer (1997).-->
# Vector space
## Span
- Linear combination of $(v_1,v_2,v_3..v_n)$ makes a Vector Space
- If $span(v_1,...,v_m)$ equals V, we say that $(v_1,...,v_m)$ spans V

- Polynomial form: "$a_0+a_1z+..a_mz^m$"
- [ ] Figure out infinite dimensional vector spaces
## Linear Dependence
1. Suppose $v=a_1v_1+a_2v_2+..a_nv_n$ st. $a\in F$
2. $v=0$ if and only if $a_1=a_2=a_n=0$ then we say that 
    * $(v_1,v_2..,v_n)$ are _"linearly independent"_
3. Which means if all coefficients are 0 $\text{such that } v=0*v_1+0*v_2+..0*v_n = 0 \Longrightarrow v_1,v_2,v_3...,v_n\text{ are orthogonal to each other (kinda like 2dim cartesian plane)}$


## Basis
- List of Vectors $V (v_1,v_2..,v_n)$ 
    1. Linearly independent
    2. Spans V
forms **Basis**






## Eigenvectors & Eigenvalues
$Av=\lambda v$<br>
$\longrightarrow Av-\lambda v=0 \Longrightarrow(A-\lambda I)v=0$<br>
$(A-\lambda I)$ must not be invertible, because if it is then:<br>
$(A-\lambda I)^{-1}(A-\lambda I)v=(A-\lambda I)^{-1}\Longrightarrow v=0$ but $v$ is non-zero vector 





---
id: "QnW8suSOlL3cpXeeIcpoo"
title: "Portfolio Optimisation"
desc: ''
updated: "1637614430206"
created: "1637056501259"
date: "2021-11-16"
categories: 
  - "research"
---
# Portfolio construction
## Portfolio weights
$w= \begin{bmatrix}w_1 \\w_2\\..\\w_n \end{bmatrix}$
## Expected returns
$\mu =\begin{bmatrix}\mu_1\\\mu_2\\..\\\mu_n \end{bmatrix}$
## Covariance Matrix
$\Sigma = \begin{bmatrix}
cov(\mu_1,\mu_1)& cov(\mu_1,\mu_2)&cov(u_1,\mu_3)..&cov(\mu_1,\mu_n)
\\.\\.\\
(\mu_n,\mu_1)&cov(u_n,\mu_2)&cov(u_n,\mu_3)..&cov(\mu_n,\mu_n)
\end{bmatrix}$


## Portfolio
1. Portolio return: 
    * $\mu=w_1\mu_1 + w_2\mu_2 +.. w_n\mu_n$
     $=\mu.w^T$
2. Portfolio variance:
    * $\sigma = \sigma_1^2w_1^2 +\sigma_2^2w_2^2... +\sigma_n^2w_n^2  +2\sigma_{12}w_1w_2 +2\sigma_{23}w_3w_3 + ....2\sigma_{nn-1}w_nw_{n-1}$ =$w.\Sigma.w^T$


## Optimisation
### Minimum variance portfolio
* $\argmin w.\Sigma.w^T$
    * s.t. $w^{T}1=1$

$\Longrightarrow L(w,\lambda)= w.\Sigma.w^T + \lambda(w^{T}1-1)$
<br><br>
$\Longrightarrow \frac{\partial L}{\partial w}= w^T(\Sigma+ \Sigma^T) +\lambda 1^T$
<br>
$\Longrightarrow \frac{\partial L}{\partial \lambda}=w^T1−1$
<br><br>
$\frac{\partial L}{\partial w}=0 \Longrightarrow w^T(\Sigma+ \Sigma^T) +\lambda 1^T=0$ <br>
$\Longrightarrow w^T =-\frac12\lambda 1^T \Sigma^{-1}\longrightarrow w =-\frac12\lambda 1\Sigma^{-1}$
<br>
$w^T1=1 \longrightarrow (-\frac12\lambda \Sigma^{-1} 1^T)1=1$ <br>
$\lambda=\frac{-2}{1^T\Sigma^{-1}1}$<br><br>

$w=\frac{-1}{2}\frac{-2}{1^T\Sigma^{-1}1}\Sigma^{-1}=\frac{\Sigma^{-1}}{1^T\Sigma^{-1}1}$






## Chebyshev's Inequality
$Pr(|X-\mu|\ge k\sigma)\le\frac1{k^2}$<br>
$Pr(|X-\mu|\ge a)\le\frac{\sigma^2}{k^2{a^2}}$<br>
if k=$\frac\mu\sigma$ then, $Pr(|X-\mu|\ge\mu)\le\frac{\sigma^2}{\mu^2}$<br>
$$
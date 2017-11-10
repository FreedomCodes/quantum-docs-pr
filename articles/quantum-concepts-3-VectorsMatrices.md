---
# Mandatory fields. See more on aka.ms/skyeye/meta.
title: Intent and product brand in a unique string of 43-59 chars including spaces | Microsoft Docs 
description: 115-145 characters including spaces. Edit the intro para describing article intent to fit here. This abstract displays in the search result.
services: service-name-with-dashes-AZURE-ONLY 
keywords: Don’t add or edit keywords without consulting your SEO champ.
author: QuantumWriter
ms.author: MSFT-alias-person-or-DL
ms.date: 10/09/2017
ms.topic: article-type-from-white-list
# Use only one of the following. Use ms.service for services, ms.prod for on-prem. Remove the # before the relevant field.
# ms.service: service-name-from-white-list
# product-name-from-white-list

# Optional fields. Don't forget to remove # if you need a field.
# ms.custom: can-be-multiple-comma-separated
# ms.devlang:devlang-from-white-list
# ms.suite: 
# ms.tgt_pltfrm:
# ms.reviewer:
# manager: MSFT-alias-manager-or-PM-counterpart
---

# Vectors and Matrices

Some familiarity with vectors and matrices is essential to understand quantum computing. We provide a brief introduction below and interested readers are recommended to read a standard reference on linear algebra such as [Strang, G. (1993). Introduction to linear algebra (Vol. 3). Wellesley, MA: Wellesley-Cambridge Press] or an online reference such as http://joshua.smcvt.edu/linearalgebra/.

A column vector (or simply vector) $v$ of dimension (or size) $n$ is a collection of $n$ complex numbers $(v_1, v_2, \ldots, v_n)$ arranged as a column:
\begin{equation}
	v =\begin{bmatrix}
	v_1\\
	v_2\\
	\vdots\\
	v_n
	\end{bmatrix}.
\end{equation}
The norm of a vector $v$ is defined as $\sqrt{\sum_i |v_i|^2}$. A vector is said to be of unit norm (or alternatively it is called a unit vector) if its norm is $1$. The adjoint of a vector $v$ is denoted $v^\dagger$ and is defined to be the following row vector
\\(
	\begin{bmatrix}x_1 \\ \vdots \\ x_n \end{bmatrix}^\dagger = \begin{bmatrix}x_1^* & \cdots & x_n^* \end{bmatrix}.
\\)

The most common way to multiply two vectors together is through the inner product, otherwise known as a dot product.  The inner product gives the projection of one vector onto another and is invaluable in describing how to express one vector as a sum of other simpler vectors.  The inner product between $\phi$ and $\psi$, denoted $\left\langle \phi, \psi\right\rangle$ is defined as
$$
\left\langle \begin{bmatrix}\phi_1 \\\vdots\\ \phi_{n} \end{bmatrix},\begin{bmatrix}\psi_1 \\\vdots\\ \psi_{n} \end{bmatrix} \right\rangle = \phi^\dagger \psi=\phi_1^*\psi_1 + \cdots + \phi_n^* \psi_n.
$$
This notation also allows the norm of a vector $v$ to be written as $\sqrt{\langle v, v\rangle}$.

We can multiply a vector with a number $c$ to form a new vector whose entries are multiplied by $c$. We can also add two vectors $u$ and $v$ to form a new vector whose entries are the sum of the entries of $u$ and $v$. These operations are depicted below:
$$\mathrm{If}~u =\begin{bmatrix}
u_1\\
u_2\\
\vdots\\
u_n
\end{bmatrix}~\mathrm{and}~
v =\begin{bmatrix}
	v_1\\
	v_2\\
	\vdots\\
	v_n
\end{bmatrix},~\mathrm{then}~
au+bv =\begin{bmatrix}
au_1+bv_1\\
au_2+bv_2\\
\vdots\\
au_n+bv_n
\end{bmatrix}.
$$

A matrix of size $m \times n$ is a collection of $mn$ complex numbers arranged in $m$ rows and $n$ columns as shown below:
$$M = 
\begin{bmatrix}
M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\
M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\
\ddots\\
M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\
\end{bmatrix}$$

Note that a vector of dimension $n$ is simply a matrix of size $n \times 1$. Just like with vectors, we can multiply a matrix with a number $c$ to obtain a new matrix where every entry is multiplied with $c$, and we can add two matrices of the same size to produce a new matrix whose entries are the sum of the respective entries of the two matrices. 

We can also multiply two matrices $M$ of dimension $m\times n$ and $N$ of dimension $n \times p$ to get a new matrix $P$ of dimension $m \times p$ as follows:
$$
\begin{bmatrix}
	M_{11} ~~ M_{12} ~~ \cdots ~~ M_{1n}\\
	M_{21} ~~ M_{22} ~~ \cdots ~~ M_{2n}\\
	\ddots\\
	M_{m1} ~~ M_{m2} ~~ \cdots ~~ M_{mn}\\
\end{bmatrix}\times
\begin{bmatrix}
N_{11} ~~ N_{12} ~~ \cdots ~~ N_{1p}\\
N_{21} ~~ N_{22} ~~ \cdots ~~ N_{2p}\\
\ddots\\
N_{n1} ~~ N_{n2} ~~ \cdots ~~ N_{np}\\
\end{bmatrix} =
\begin{bmatrix}
P_{11} ~~ P_{12} ~~ \cdots ~~ P_{1p}\\
P_{21} ~~ P_{22} ~~ \cdots ~~ P_{2p}\\
\ddots\\
P_{m1} ~~ P_{m2} ~~ \cdots ~~ P_{mp}\\
\end{bmatrix},
$$
where the entry $P_{ik} = \sum_j M_{ij}N_{jk}$. For example, the entry $P_{11}$ is the inner product of the first row of $M$ with the first column of $N$. Note that since a vector is simply a special case of a matrix, this definition extends to matrix--vector multiplication. 

All the matrices we consider will either be square matrices, where the number of rows and columns are equal, or vectors, which corresponds to only $1$ column. One special square matrix is the identity matrix, denoted $\boldone$, which has all its diagonal elements equal to $1$ and the remaining elements equal to $0$:
$$\boldone=\begin{bmatrix}
1 ~~ 0 ~~ \cdots ~~ 0\\
0 ~~ 1 ~~ \cdots ~~ 0\\
~~ \ddots\\
0 ~~ 0 ~~ \cdots ~~ 1\\
\end{bmatrix}.$$
For a square matrix $A$, we say a matrix $B$ is its inverse if $AB = \boldone$. The inverse of a matrix need not exist, but when it exists it is unique and we denote it $A^{-1}$. For any matrix $M$, the adjoint or conjugate transpose of $M$, is a matrix $N$ such that $N_{ij} = M^*_{ji}$. The adjoint of $M$ is usually denoted $M^\dagger$. We say a matrix $U$ is unitary if $UU^\dagger = \boldone$ or equivalently, $U^{-1} = U^\dagger$.  Perhaps the most important property of unitary matrices is that they preserve the norm of a vector.  This happens because $\langle v,v \rangle=v^\dagger v = v^\dagger U^{-1} U v = \langle U v, U v\rangle$.  



Finally, the tensor product (or Kronecker product) of two matrices $M$ of size $m\times n$ and $N$ of size $p \times q$ is a larger matrix $P=M\otimes N$ of size $mp \times nq$, and is obtained from $M$ and $N$ as follows:
$$
M \otimes N = 
\begin{bmatrix}
M_{11} ~~ \cdots ~~ M_{1n}\\
\ddots\\
M_{m1}  ~~ \cdots ~~ M_{mn}\\
\end{bmatrix}\times
\begin{bmatrix}
N_{11}  ~~ \cdots ~~ N_{1q}\\
\ddots\\
N_{p1} ~~ \cdots ~~ N_{pq}\\
\end{bmatrix}
=
\begin{bmatrix}
M_{11} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\ \ddots\\ N_{p1} ~~ \cdots ~~ N_{pq}\\ \end{bmatrix}~~ \cdots ~~ 
M_{1n} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\ \ddots\\ N_{p1} ~~ \cdots ~~ N_{pq}\\ \end{bmatrix}\\
\ddots\\
M_{m1} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\ \ddots\\ N_{p1} ~~ \cdots ~~ N_{pq}\\ \end{bmatrix}~~ \cdots ~~ 
M_{mn} \begin{bmatrix} N_{11}  ~~ \cdots ~~ N_{1q}\\ \ddots\\ N_{p1} ~~ \cdots ~~ N_{pq}\\ \end{bmatrix}\\
\end{bmatrix}.
$$
This is better demonstrated using some examples:
$$
\begin{bmatrix} a \\ b  \end{bmatrix} \otimes \begin{bmatrix} c \\ d \\ e\end{bmatrix} 
=\begin{bmatrix} a \begin{bmatrix} c \\ d \\ e\end{bmatrix}  \\[1.5em] b \begin{bmatrix} c \\ d \\ e\end{bmatrix}  \end{bmatrix}
= \begin{bmatrix} a c \\ a d \\a e \\ b c \\ b d \\ be\end{bmatrix}, \mathrm{~~and} \quad 
\begin{bmatrix}
a\ b\\c\ d
\end{bmatrix}
\otimes 
\begin{bmatrix}
e\ f\\g\ h
\end{bmatrix}
=
\begin{bmatrix}
a\begin{bmatrix}
e\ f\\g\ h
\end{bmatrix}
b\begin{bmatrix}
e\ f\\g\ h
\end{bmatrix}
\\[1em]
c\begin{bmatrix}
e\ f\\g\ h
\end{bmatrix}
d\begin{bmatrix}
e\ f\\g\ h
\end{bmatrix}
\end{bmatrix}
=
\begin{bmatrix}
ae\ af\ be\ bf\\
ag\ ah\ bg\ bh\\
ce\ cf\ de\ df\\
cg\ ch\ dg\ dh
\end{bmatrix}.
$$

A final notation surrounding tensor products that is useful is that, for any vector $v$ or matrix $M$, $v^{\otimes n}$ or $M^{\otimes n}$ is short hand for an $n$--fold repeated tensor product.  For example
$$
\begin{bmatrix} 1 \\ 0 \end{bmatrix}^{\otimes 1} = \begin{bmatrix} 1 \\ 0 \end{bmatrix}\qquad \begin{bmatrix} 1 \\ 0 \end{bmatrix}^{\otimes 2} = \begin{bmatrix} 1 \\ 0\\0\\0 \end{bmatrix}\qquad X^{\otimes 2}= \begin{bmatrix} 0 &0&0&1 \\ 0 &0&1&0 \\0 &1&0&0\\1 &0&0&0\end{bmatrix}.
$$
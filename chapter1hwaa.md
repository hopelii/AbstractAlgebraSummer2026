# Exercise 1.3: Binary Operations {#exercise-1.3-binary-operations .unnumbered}

A binary operation on a set $S$ is a function $$*:S\times S\to S.$$

Therefore, for every $a,b\in S$, the expression $a*b$ must:

1.  be defined, and

2.  belong to $S$.

In other words, the operation must be **closed** on $S$.

## (a) {#a .unnumbered}

Let $$S=\mathbb{Z},
\qquad
a*b=a+b^2.$$

If $a,b\in\mathbb{Z}$, then $$b^2\in\mathbb{Z}.$$

Since integers are closed under addition, $$a+b^2\in\mathbb{Z}.$$

Therefore, $*$ is a binary operation on $\mathbb{Z}$.

$$\boxed{\text{Yes}}$$

## (b) {#b .unnumbered}

Let $$S=\mathbb{Z},
\qquad
a*b=a^2b^3.$$

If $a,b\in\mathbb{Z}$, then $$a^2\in\mathbb{Z}
\qquad\text{and}\qquad
b^3\in\mathbb{Z}.$$

Since integers are closed under multiplication, $$a^2b^3\in\mathbb{Z}.$$

Therefore, $*$ is a binary operation on $\mathbb{Z}$.

$$\boxed{\text{Yes}}$$

## (c) {#c .unnumbered}

Let $$S=\mathbb{R},
\qquad
a*b=\frac{a}{a^2+b^2}.$$

Consider $$a=0,
\qquad
b=0.$$

Then $$0*0
=
\frac{0}{0^2+0^2}
=
\frac{0}{0},$$ which is undefined.

Since the operation is not defined for every pair in
$$\mathbb{R}\times\mathbb{R},$$ it is not a binary operation on
$\mathbb{R}$.

$$\boxed{\text{No}}$$

## (d) {#d .unnumbered}

Let $$S=\mathbb{Z},
\qquad
a*b=\frac{a^2+2ab+b^2}{a+b}.$$

Factor the numerator: $$a^2+2ab+b^2=(a+b)^2.$$

Thus, when $a+b\neq 0$, $$a*b
=
\frac{(a+b)^2}{a+b}
=
a+b.$$

However, if $$a=1
\qquad\text{and}\qquad
b=-1,$$ then $$a+b=0.$$

Therefore, $$1*(-1)
=
\frac{1^2+2(1)(-1)+(-1)^2}{1+(-1)}
=
\frac{0}{0},$$ which is undefined.

Hence, $*$ is not a binary operation on $\mathbb{Z}$.

$$\boxed{\text{No}}$$

## (e) {#e .unnumbered}

Let $$S=\mathbb{Z},
\qquad
a*b=a+b-ab.$$

If $a,b\in\mathbb{Z}$, then $$a+b-ab\in\mathbb{Z},$$ because integers
are closed under addition, subtraction, and multiplication.

Therefore, $*$ is a binary operation on $\mathbb{Z}$.

$$\boxed{\text{Yes}}$$

## (f) {#f .unnumbered}

Let $$S=\mathbb{R},
\qquad
a*b=b.$$

If $a,b\in\mathbb{R}$, then $$a*b=b\in\mathbb{R}.$$

The fact that the operation does not use $a$ does not matter.

Therefore, $*$ is a binary operation on $\mathbb{R}$.

$$\boxed{\text{Yes}}$$

## (g) {#g .unnumbered}

Let $$S=\{1,-2,3,2,-4\},
\qquad
a*b=|b|.$$

Choose $$b=-4.$$

Then $$a*(-4)=|-4|=4.$$

However, $$4\notin S.$$

Therefore, the operation is not closed on $S$, so it is not a binary
operation.

$$\boxed{\text{No}}$$

## (h) {#h .unnumbered}

Let $$S=\{1,6,3,2,18\},
\qquad
a*b=ab.$$

Choose $$a=6,
\qquad
b=6.$$

Then $$6*6=36.$$

However, $$36\notin S.$$

Therefore, $S$ is not closed under the operation, so $*$ is not a binary
operation on $S$.

$$\boxed{\text{No}}$$

## (i) {#i .unnumbered}

Let $S$ be the set of all $2\times 2$ matrices with real entries.

Suppose $$a=
\begin{pmatrix}
r_1&r_2\\
r_3&r_4
\end{pmatrix}
\qquad\text{and}\qquad
b=
\begin{pmatrix}
r_5&r_6\\
r_7&r_8
\end{pmatrix}.$$

The operation is defined by $$a*b
=
\begin{pmatrix}
r_1+r_5&r_2+r_6\\
r_3+r_7&r_4+r_8
\end{pmatrix}.$$

Since each entry is the sum of two real numbers, every entry is real.

Therefore, $$a*b$$ is again a $2\times 2$ matrix with real entries.

Hence, $*$ is a binary operation on $S$.

$$\boxed{\text{Yes}}$$

## (j) {#j .unnumbered}

Let $S$ be the set of all subsets of a set $X$, and define
$$A*B=(A\triangle B)\triangle B.$$

Using associativity of symmetric difference, $$(A\triangle B)\triangle B
=
A\triangle(B\triangle B).$$

Since $$B\triangle B=\varnothing,$$ we obtain $$A*B
=
A\triangle\varnothing
=
A.$$

Since $A\subseteq X$, the result is again a subset of $X$.

Therefore, $*$ is a binary operation on $S$.

$$\boxed{\text{Yes}}$$

# Final Answers {#final-answers .unnumbered}

$$\begin{array}{c|c}
\text{Part} & \text{Binary operation on }S?\\
\hline
(a) & \text{Yes}\\
(b) & \text{Yes}\\
(c) & \text{No}\\
(d) & \text{No}\\
(e) & \text{Yes}\\
(f) & \text{Yes}\\
(g) & \text{No}\\
(h) & \text{No}\\
(i) & \text{Yes}\\
(j) & \text{Yes}
\end{array}$$

# Main Idea to Remember {#main-idea-to-remember .unnumbered}

$$\boxed{
\text{A binary operation on }S\text{ must produce a defined result in }S
\text{ for every pair }a,b\in S.
}$$

Equivalently, $$\boxed{
a,b\in S
\implies
a*b\in S
}$$ and the expression $a*b$ must be defined for every pair $a,b\in S$.

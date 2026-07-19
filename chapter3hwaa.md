# Abstract Algebra Homework -- Section 3 {#abstract-algebra-homework-section-3 .unnumbered}

## Exercise 3.3 {#exercise-3.3 .unnumbered}

Find elements $A,B,C\in GL(2,\mathbb{R})$ such that $$AB=BC$$ but
$$A\neq C.$$

Recall that $$GL(2,\mathbb{R})$$ is the set of all invertible $2\times2$
matrices with real entries.

Choose $$A=
\begin{pmatrix}
2&0\\
0&1
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix},
\qquad
C=
\begin{pmatrix}
1&0\\
0&2
\end{pmatrix}.$$

All three matrices are invertible because $$\det(A)=2,
\qquad
\det(B)=-1,
\qquad
\det(C)=2.$$

Thus, $$A,B,C\in GL(2,\mathbb{R}).$$

Now compute $$\begin{aligned}
AB
&=
\begin{pmatrix}
2&0\\
0&1
\end{pmatrix}
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}\\
&=
\begin{pmatrix}
2(0)+0(1)&2(1)+0(0)\\
0(0)+1(1)&0(1)+1(0)
\end{pmatrix}\\
&=
\begin{pmatrix}
0&2\\
1&0
\end{pmatrix}.
\end{aligned}$$

Also, $$\begin{aligned}
BC
&=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix}
\begin{pmatrix}
1&0\\
0&2
\end{pmatrix}\\
&=
\begin{pmatrix}
0(1)+1(0)&0(0)+1(2)\\
1(1)+0(0)&1(0)+0(2)
\end{pmatrix}\\
&=
\begin{pmatrix}
0&2\\
1&0
\end{pmatrix}.
\end{aligned}$$

Therefore, $$AB=BC.$$

However, $$A=
\begin{pmatrix}
2&0\\
0&1
\end{pmatrix}
\neq
\begin{pmatrix}
1&0\\
0&2
\end{pmatrix}
=C.$$

Hence, $$\boxed{
A=
\begin{pmatrix}
2&0\\
0&1
\end{pmatrix},
\quad
B=
\begin{pmatrix}
0&1\\
1&0
\end{pmatrix},
\quad
C=
\begin{pmatrix}
1&0\\
0&2
\end{pmatrix}
}$$ is one valid answer.

Note that $B$ cannot be canceled from $$AB=BC$$ because $B$ appears on
the right side of $A$ in $AB$, but on the left side of $C$ in $BC$.

## Exercise 3.4 {#exercise-3.4 .unnumbered}

Let $g$ be an element of a group $(G,*)$ such that, for some $x\in G$,
$$x*g=x.$$

Show that $$g=e.$$

Since $G$ is a group, $x$ has an inverse $x^{-1}$.

Multiply both sides of $$x*g=x$$ on the left by $x^{-1}$:
$$x^{-1}*(x*g)=x^{-1}*x.$$

Using associativity, $$(x^{-1}*x)*g=x^{-1}*x.$$

Since $$x^{-1}*x=e,$$ we obtain $$e*g=e.$$

Because $e$ is the identity, $$e*g=g.$$

Therefore, $$\boxed{g=e.}$$

Equivalently, rewrite $$x*g=x$$ as $$x*g=x*e.$$

By left cancellation, $$\boxed{g=e.}$$

## Exercise 3.9 {#exercise-3.9 .unnumbered}

Let $(G,*)$ be a group. Show that $(G,*)$ is abelian if and only if
$$(x*y)^{-1}=x^{-1}*y^{-1}$$ for all $x,y\in G$.

We prove both directions.

### Forward Direction {#forward-direction .unnumbered}

Assume that $(G,*)$ is abelian.

In every group, $$(x*y)^{-1}=y^{-1}*x^{-1}.$$

Since $G$ is abelian, $$y^{-1}*x^{-1}=x^{-1}*y^{-1}.$$

Therefore, $$\boxed{
(x*y)^{-1}=x^{-1}*y^{-1}.
}$$

### Reverse Direction {#reverse-direction .unnumbered}

Now assume that $$(x*y)^{-1}=x^{-1}*y^{-1}$$ for all $x,y\in G$.

But in every group, $$(x*y)^{-1}=y^{-1}*x^{-1}.$$

Therefore, $$x^{-1}*y^{-1}=y^{-1}*x^{-1}.$$

Take inverses of both sides: $$\left(x^{-1}*y^{-1}\right)^{-1}
=
\left(y^{-1}*x^{-1}\right)^{-1}.$$

Using $$(a*b)^{-1}=b^{-1}*a^{-1},$$ the left side becomes
$$\left(x^{-1}*y^{-1}\right)^{-1}
=
\left(y^{-1}\right)^{-1}*
\left(x^{-1}\right)^{-1}
=
y*x.$$

Similarly, the right side becomes $$\left(y^{-1}*x^{-1}\right)^{-1}
=
\left(x^{-1}\right)^{-1}*
\left(y^{-1}\right)^{-1}
=
x*y.$$

Thus, $$y*x=x*y.$$

Therefore, $$x*y=y*x$$ for all $x,y\in G$.

Hence, $$\boxed{(G,*)\text{ is abelian}.}$$

Therefore, $$\boxed{
(G,*)\text{ is abelian}
\iff
(x*y)^{-1}=x^{-1}*y^{-1}
\text{ for all }x,y\in G.
}$$

## Exercise 3.11 {#exercise-3.11 .unnumbered}

Let $(G,*)$ be a group such that $$x^2=e$$ for every $x\in G$.

Here, $$x^2=x*x.$$

Show that $(G,*)$ is abelian.

Since $$x*x=e,$$ the element $x$ is its own inverse. Therefore,
$$\boxed{x^{-1}=x}$$ for every $x\in G$.

Now let $x,y\in G$.

Since $x*y\in G$, the assumption also applies to $x*y$. Thus,
$$(x*y)^2=e.$$

Therefore, $$x*y$$ is its own inverse: $$(x*y)^{-1}=x*y.$$

However, in every group, $$(x*y)^{-1}=y^{-1}*x^{-1}.$$

Since $$x^{-1}=x
\qquad\text{and}\qquad
y^{-1}=y,$$ we have $$(x*y)^{-1}=y*x.$$

Thus, $$x*y=(x*y)^{-1}=y*x.$$

Therefore, $$x*y=y*x$$ for all $x,y\in G$.

Hence, $$\boxed{(G,*)\text{ is abelian}.}$$

## Exercise 3.12 {#exercise-3.12 .unnumbered}

Let $(G,*)$ be a group. Show that $(G,*)$ is abelian if and only if
$$(x*y)^2=x^2*y^2$$ for all $x,y\in G$.

Recall that $$(x*y)^2=(x*y)*(x*y).$$

We prove both directions.

### Forward Direction {#forward-direction-1 .unnumbered}

Assume that $(G,*)$ is abelian.

Then $$x*y=y*x$$ for all $x,y\in G$.

Now, $$\begin{aligned}
(x*y)^2
&=(x*y)*(x*y)\\
&=x*y*x*y.
\end{aligned}$$

Since the group is abelian, we may switch the middle $y$ and $x$:
$$x*y*x*y=x*x*y*y.$$

Therefore, $$(x*y)^2=x^2*y^2.$$

Hence, $$\boxed{
(G,*)\text{ abelian}
\implies
(x*y)^2=x^2*y^2.
}$$

### Reverse Direction {#reverse-direction-1 .unnumbered}

Now assume that $$(x*y)^2=x^2*y^2$$ for all $x,y\in G$.

Expanding both sides gives $$x*y*x*y=x*x*y*y.$$

Multiply both sides on the left by $x^{-1}$: $$x^{-1}*(x*y*x*y)
=
x^{-1}*(x*x*y*y).$$

Using associativity, $$(x^{-1}*x)*y*x*y
=
(x^{-1}*x)*x*y*y.$$

Since $$x^{-1}*x=e,$$ we get $$y*x*y=x*y*y.$$

Now multiply both sides on the right by $y^{-1}$: $$(y*x*y)*y^{-1}
=
(x*y*y)*y^{-1}.$$

Using associativity, $$y*x*(y*y^{-1})
=
x*y*(y*y^{-1}).$$

Since $$y*y^{-1}=e,$$ we obtain $$y*x=x*y.$$

Therefore, $$x*y=y*x$$ for all $x,y\in G$.

Hence, $$\boxed{(G,*)\text{ is abelian}.}$$

Therefore, $$\boxed{
(G,*)\text{ is abelian}
\iff
(x*y)^2=x^2*y^2
\text{ for all }x,y\in G.
}$$

# Main Ideas to Remember {#main-ideas-to-remember .unnumbered}

$$\boxed{
AB=AC\implies B=C
}$$ and $$\boxed{
BA=CA\implies B=C.
}$$

Cancellation only works when the common element appears on the same
side.

$$\boxed{
x*g=x\implies g=e.
}$$

$$\boxed{
(x*y)^{-1}=y^{-1}*x^{-1}
}$$ in every group.

$$\boxed{
(G,*)\text{ is abelian}
\iff
(x*y)^{-1}=x^{-1}*y^{-1}.
}$$

$$\boxed{
x^2=e\text{ for every }x\in G
\implies
x^{-1}=x.
}$$

$$\boxed{
x^2=e\text{ for every }x\in G
\implies
(G,*)\text{ is abelian}.
}$$

$$\boxed{
(G,*)\text{ is abelian}
\iff
(x*y)^2=x^2*y^2.
}$$

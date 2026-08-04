::: center
**Abstract Algebra Final Review**\
**Equivalence Relations, Lagrange's Theorem, Conjugacy, Normal
Subgroups, and Quotient Groups**
:::

# Equivalence Relations

## Problem 9.12 {#problem-9.12 .unnumbered}

Let $G$ be a group, and for $a,b\in G$, define $$aRb$$ to mean that
there exists an element $x\in G$ such that $$a=xbx^{-1}.$$ Show that $R$
is an equivalence relation on $G$.

### Reflexive {#reflexive .unnumbered}

Let $a\in G$. Choose $x=e$. Then $$eae^{-1}=a.$$ Therefore, $$aRa.$$

### Symmetric {#symmetric .unnumbered}

Suppose $$aRb.$$ Then there exists $x\in G$ such that $$a=xbx^{-1}.$$

Multiplying on the left by $x^{-1}$ and on the right by $x$ gives
$$x^{-1}ax=b.$$

Therefore, $$b=x^{-1}a(x^{-1})^{-1}.$$

Since $x^{-1}\in G$, we have $$bRa.$$

### Transitive {#transitive .unnumbered}

Suppose $$aRb
\qquad\text{and}\qquad
bRc.$$

Then there exist $x,y\in G$ such that $$a=xbx^{-1}$$ and $$b=ycy^{-1}.$$

Substituting the expression for $b$ into the first equation gives
$$a=x(ycy^{-1})x^{-1}.$$

By associativity, $$a=(xy)c(y^{-1}x^{-1}).$$

Since $$(xy)^{-1}=y^{-1}x^{-1},$$ we obtain $$a=(xy)c(xy)^{-1}.$$

Therefore, $$aRc.$$

Hence, $$\boxed{R\text{ is an equivalence relation on }G.}$$

## Problem 9.14 {#problem-9.14 .unnumbered}

Let $G$ be a group, and for $a,b\in G$, define $$aRb$$ to mean that
$$ab=ba.$$

Determine when $R$ is an equivalence relation.

### Reflexive {#reflexive-1 .unnumbered}

For every $a\in G$, $$aa=aa.$$ Therefore, $$aRa.$$

### Symmetric {#symmetric-1 .unnumbered}

Suppose $$aRb.$$ Then $$ab=ba.$$ The same equality also gives $$ba=ab.$$
Therefore, $$bRa.$$

### Transitive {#transitive-1 .unnumbered}

In general, commuting is not transitive.

Suppose that $R$ is transitive. The identity element commutes with every
element of $G$. Thus, for arbitrary $a,b\in G$, $$aRe
\qquad\text{and}\qquad
eRb.$$

By transitivity, $$aRb.$$

Therefore, $$ab=ba$$ for every $a,b\in G$, so $G$ is abelian.

Conversely, if $G$ is abelian, then every pair of elements commutes.
Hence, $R$ is reflexive, symmetric, and transitive.

Therefore, $$\boxed{
R\text{ is an equivalence relation on }G
\iff
G\text{ is abelian}.
}$$

## Problem 9.16 {#problem-9.16 .unnumbered}

Let $H$ be a subgroup of $G$. Define a relation $\equiv_H$ on $G$ by
$$x\equiv_H y
\quad\Longleftrightarrow\quad
x^{-1}y\in H.$$

Show that $\equiv_H$ is an equivalence relation.

### Reflexive {#reflexive-2 .unnumbered}

For every $x\in G$, $$x^{-1}x=e.$$

Since $H$ is a subgroup, $$e\in H.$$

Therefore, $$x^{-1}x\in H,$$ so $$x\equiv_H x.$$

### Symmetric {#symmetric-2 .unnumbered}

Suppose $$x\equiv_H y.$$

Then $$x^{-1}y\in H.$$

Since $H$ is closed under inverses, $$(x^{-1}y)^{-1}\in H.$$

But $$(x^{-1}y)^{-1}=y^{-1}x.$$

Therefore, $$y^{-1}x\in H,$$ so $$y\equiv_H x.$$

### Transitive {#transitive-2 .unnumbered}

Suppose $$x\equiv_H y
\qquad\text{and}\qquad
y\equiv_H z.$$

Then $$x^{-1}y\in H
\qquad\text{and}\qquad
y^{-1}z\in H.$$

Since $H$ is closed under products, $$(x^{-1}y)(y^{-1}z)\in H.$$

Now, $$(x^{-1}y)(y^{-1}z)
=
x^{-1}(yy^{-1})z
=
x^{-1}z.$$

Therefore, $$x^{-1}z\in H,$$ so $$x\equiv_H z.$$

Hence, $$\boxed{\equiv_H\text{ is an equivalence relation on }G.}$$

# Index and Lagrange's Theorem

## Problem 10.2(a) {#problem-10.2a .unnumbered}

In $$G=(\mathbb{Z}_{48},\oplus),$$ find $[G:H]$ for
$$H=\langle 32\rangle.$$

The order of $32$ in $\mathbb{Z}_{48}$ is
$$o(32)=\frac{48}{\gcd(48,32)}.$$

Since $$\gcd(48,32)=16,$$ we obtain $$o(32)=\frac{48}{16}=3.$$

Thus, $$|H|=3.$$

In fact, $$H=\langle 32\rangle=\{0,32,16\}.$$

Therefore, $$[G:H]=\frac{|G|}{|H|}
=\frac{48}{3}
=16.$$

Hence, $$\boxed{[G:H]=16.}$$

## Problem 10.2(b) {#problem-10.2b .unnumbered}

In $$G=(\mathbb{Z}_{54},\oplus),$$ find $[G:H]$ for
$$H=\langle24\rangle.$$

The order of $24$ is $$o(24)=\frac{54}{\gcd(54,24)}.$$

Since $$\gcd(54,24)=6,$$ we obtain $$o(24)=\frac{54}{6}=9.$$

Thus, $$|H|=9.$$

Therefore, $$[G:H]
=
\frac{54}{9}
=
6.$$

Hence, $$\boxed{[G:H]=6.}$$

## Problem 10.2(c) {#problem-10.2c .unnumbered}

In $$G=(\mathbb{Z}_{112},\oplus),$$ find $[G:H]$ for
$$H=\langle100\rangle.$$

The order of $100$ is $$o(100)=\frac{112}{\gcd(112,100)}.$$

Since $$\gcd(112,100)=4,$$ we obtain $$o(100)=\frac{112}{4}=28.$$

Thus, $$|H|=28.$$

Therefore, $$[G:H]
=
\frac{112}{28}
=
4.$$

Hence, $$\boxed{[G:H]=4.}$$

## Problem 10.5 {#problem-10.5 .unnumbered}

Let $G$ be a group of order $8$ that is not cyclic. Show that $$a^4=e$$
for every $a\in G$.

By Lagrange's Theorem, the order of $a$ must divide $8$. Therefore,
$$o(a)\in\{1,2,4,8\}.$$

Since $G$ is not cyclic, no element can have order $8$. Otherwise, an
element of order $8$ would generate all of $G$.

Thus, $$o(a)\in\{1,2,4\}.$$

If $o(a)=1$, then $a=e$, so $$a^4=e.$$

If $o(a)=2$, then $$a^2=e,$$ so $$a^4=(a^2)^2=e.$$

If $o(a)=4$, then directly $$a^4=e.$$

Therefore, $$\boxed{a^4=e\text{ for every }a\in G.}$$

## Problem 10.6 {#problem-10.6 .unnumbered}

Let $H$ and $K$ be subgroups of a group $G$ such that $$|H|=12
\qquad\text{and}\qquad
|K|=5.$$

Prove that $$H\cap K=\{e\}.$$

The intersection $H\cap K$ is a subgroup of both $H$ and $K$.

By Lagrange's Theorem, $$|H\cap K|\mid |H|$$ and $$|H\cap K|\mid |K|.$$

Therefore, $$|H\cap K|\mid12$$ and $$|H\cap K|\mid5.$$

The only positive integer dividing both $12$ and $5$ is $1$. Hence,
$$|H\cap K|=1.$$

Every subgroup contains the identity. Therefore, the only subgroup of
order $1$ is $$\{e\}.$$

Thus, $$\boxed{H\cap K=\{e\}.}$$

## Problem 10.8 {#problem-10.8 .unnumbered}

Let $G$ be a group of order $$p^2,$$ where $p$ is prime. Show that $G$
has a subgroup of order $p$.

Choose any nonidentity element $$a\in G.$$

By Lagrange's Theorem, $$o(a)\mid p^2.$$

Since $a\neq e$, its order is not $1$. Thus, $$o(a)=p
\qquad\text{or}\qquad
o(a)=p^2.$$

If $$o(a)=p,$$ then $$\langle a\rangle$$ is a subgroup of order $p$.

If $$o(a)=p^2,$$ then consider $a^p$. Its order is $$o(a^p)
=
\frac{o(a)}{\gcd(o(a),p)}
=
\frac{p^2}{p}
=
p.$$

Therefore, $$\langle a^p\rangle$$ is a subgroup of order $p$.

Hence, $$\boxed{G\text{ contains a subgroup of order }p.}$$

## Problem 10.15 {#problem-10.15 .unnumbered}

Let $G$ be a finite group, let $H\leq G$, and let $K\leq H$. Prove that
$$[G:K]=[G:H][H:K].$$

By Lagrange's Theorem, $$[G:H]=\frac{|G|}{|H|}$$ and
$$[H:K]=\frac{|H|}{|K|}.$$

Therefore, $$[G:H][H:K]
=
\frac{|G|}{|H|}
\cdot
\frac{|H|}{|K|}.$$

Cancelling $|H|$ gives $$[G:H][H:K]
=
\frac{|G|}{|K|}
=
[G:K].$$

Hence, $$\boxed{[G:K]=[G:H][H:K].}$$

## Problem 10.21 {#problem-10.21 .unnumbered}

Prove that every group of order $77$ has an element of order $7$ and an
element of order $11$.

We have $$|G|=77=7\cdot11.$$

Since $7$ is a prime divisor of $|G|$, Cauchy's Theorem guarantees that
$G$ contains an element of order $7$.

Since $11$ is also a prime divisor of $|G|$, Cauchy's Theorem guarantees
that $G$ contains an element of order $11$.

Therefore, $$\boxed{
G\text{ has an element of order }7
\text{ and an element of order }11.
}$$

# Conjugacy Classes

## Problem 10.26 {#problem-10.26 .unnumbered}

Find the conjugacy classes of $D_4$ and write the class equation.

The elements of $D_4$ are $$D_4=\{e,f,f^2,f^3,g,fg,f^2g,f^3g\}.$$

The conjugacy class of an element $a$ is $$[a]
=
\{xax^{-1}:x\in D_4\}.$$

The center of $D_4$ is $$Z(D_4)=\{e,f^2\}.$$

Elements in the center form singleton conjugacy classes. Thus,
$$[e]=\{e\}$$ and $$[f^2]=\{f^2\}.$$

For $f$, $$gfg^{-1}=f^{-1}=f^3.$$

Therefore, $$[f]=\{f,f^3\}.$$

For $g$, $$fgf^{-1}=f^2g.$$

Therefore, $$[g]=\{g,f^2g\}.$$

For $fg$, $$f(fg)f^{-1}=f^3g.$$

Therefore, $$[fg]=\{fg,f^3g\}.$$

Hence, the distinct conjugacy classes are $$\boxed{
\{e\},\quad
\{f^2\},\quad
\{f,f^3\},\quad
\{g,f^2g\},\quad
\{fg,f^3g\}.
}$$

Their sizes are $$1,\quad1,\quad2,\quad2,\quad2.$$

Thus, the class equation is $$\boxed{8=1+1+2+2+2.}$$

### How to use the multiplication chart {#how-to-use-the-multiplication-chart .unnumbered}

To find the conjugacy class of $a$, calculate $$xax^{-1}$$ for each
$x\in D_4$.

Collect all distinct answers. Once an element has already appeared in a
conjugacy class, it does not need to be checked again as a new
representative.

# Normal Subgroups

## Problem 11.4 {#problem-11.4 .unnumbered}

Let $$H\trianglelefteq G
\qquad\text{and}\qquad
K\trianglelefteq G.$$

Show that $$H\cap K\trianglelefteq G.$$

The intersection of two subgroups is a subgroup, so $$H\cap K\leq G.$$

Let $a\in G$ and $x\in H\cap K$. Then $$x\in H
\qquad\text{and}\qquad
x\in K.$$

Since $H\trianglelefteq G$, $$axa^{-1}\in H.$$

Since $K\trianglelefteq G$, $$axa^{-1}\in K.$$

Therefore, $$axa^{-1}\in H\cap K.$$

Thus, $$a(H\cap K)a^{-1}\subseteq H\cap K.$$

Applying the same argument with $a^{-1}$ in place of $a$ gives
$$a^{-1}(H\cap K)a\subseteq H\cap K.$$

Conjugating by $a$ gives $$H\cap K\subseteq a(H\cap K)a^{-1}.$$

Therefore, $$a(H\cap K)a^{-1}=H\cap K.$$

Hence, $$\boxed{H\cap K\trianglelefteq G.}$$

## Problem 11.5 {#problem-11.5 .unnumbered}

Let $G$ be a group, let $$H\leq G,$$ and let $$K\trianglelefteq G.$$

Show that $$H\cap K\trianglelefteq H.$$

The intersection of two subgroups is a subgroup, so $$H\cap K\leq H.$$

Let $$h\in H
\qquad\text{and}\qquad
x\in H\cap K.$$

Since $x,h\in H$ and $H$ is a subgroup, $$hxh^{-1}\in H.$$

Also, $x\in K$ and $K\trianglelefteq G$. Since $h\in H\subseteq G$,
$$hxh^{-1}\in K.$$

Therefore, $$hxh^{-1}\in H\cap K.$$

Hence, $$\boxed{H\cap K\trianglelefteq H.}$$

## Problem 11.7 {#problem-11.7 .unnumbered}

Let $$H\trianglelefteq G,
\qquad
K\trianglelefteq G,
\qquad
H\cap K=\{e\}.$$

Show that if $$x\in H
\qquad\text{and}\qquad
y\in K,$$ then $$xy=yx.$$

Consider $$c=xyx^{-1}y^{-1}.$$

Since $H\trianglelefteq G$ and $x^{-1}\in H$, $$yx^{-1}y^{-1}\in H.$$

Since $x\in H$, $$x(yx^{-1}y^{-1})\in H.$$

Thus, $$c\in H.$$

Since $K\trianglelefteq G$ and $y\in K$, $$xyx^{-1}\in K.$$

Since $y^{-1}\in K$, $$(xyx^{-1})y^{-1}\in K.$$

Thus, $$c\in K.$$

Therefore, $$c\in H\cap K.$$

But $$H\cap K=\{e\},$$ so $$xyx^{-1}y^{-1}=e.$$

Multiplying on the right by $y$ and then by $x$ gives $$xy=yx.$$

Hence, $$\boxed{xy=yx.}$$

## Problem 11.8 {#problem-11.8 .unnumbered}

Let $N$ be a normal subgroup of $G$, and let $H$ be any subgroup of $G$.
Define $$NH=\{nh:n\in N,\ h\in H\}.$$

Show that $$NH\leq G.$$

Let $$n_1h_1,\ n_2h_2\in NH,$$ where $$n_1,n_2\in N
\qquad\text{and}\qquad
h_1,h_2\in H.$$

Then $$(n_1h_1)(n_2h_2)
=
n_1h_1n_2h_2.$$

Insert $$h_1^{-1}h_1=e:$$ $$n_1h_1n_2h_2
=
n_1h_1n_2(h_1^{-1}h_1)h_2.$$

Regroup: $$n_1h_1n_2h_2
=
n_1(h_1n_2h_1^{-1})(h_1h_2).$$

Since $N\trianglelefteq G$, $$h_1n_2h_1^{-1}\in N.$$

Since $N$ is closed under products, $$n_1(h_1n_2h_1^{-1})\in N.$$

Since $H$ is closed under products, $$h_1h_2\in H.$$

Therefore, $$(n_1h_1)(n_2h_2)$$ is an element of $N$ multiplied by an
element of $H$. Hence, $$(n_1h_1)(n_2h_2)\in NH.$$

Thus, $NH$ is closed under products, and therefore $$\boxed{NH\leq G.}$$

# Quotient Groups

## Problem 11.17 {#problem-11.17 .unnumbered}

Let $G$ be abelian, and let $H\leq G$. Show that $$G/H$$ is abelian.

Since $G$ is abelian, every subgroup of $G$ is normal. Therefore,
$$H\trianglelefteq G,$$ so $G/H$ is a quotient group.

Let $$aH,bH\in G/H.$$

Then $$(aH)(bH)=abH.$$

Since $G$ is abelian, $$ab=ba.$$

Therefore, $$abH=baH.$$

But $$baH=(bH)(aH).$$

Thus, $$(aH)(bH)=(bH)(aH).$$

Hence, $$\boxed{G/H\text{ is abelian}.}$$

## Problem 11.23 {#problem-11.23 .unnumbered}

Let $G$ be a group and let $H$ be a subgroup of index $2$. Show that for
every $a\in G$, $$a^2\in H.$$

Let $a\in G$.

### Case 1: $a\in H$ {#case-1-ain-h .unnumbered}

Since $H$ is closed under products, $$a^2\in H.$$

### Case 2: $a\notin H$ {#case-2-anotin-h .unnumbered}

Since $$[G:H]=2,$$ there are exactly two left cosets of $H$ in $G$: $$H
\qquad\text{and}\qquad
aH.$$

Thus, $$G=H\cup aH.$$

Suppose, for contradiction, that $$a^2\notin H.$$

Then $$a^2\in aH.$$

Therefore, there exists some $h\in H$ such that $$a^2=ah.$$

Cancelling $a$ on the left gives $$a=h.$$

Thus, $$a\in H,$$ which contradicts the assumption that $a\notin H$.

Therefore, $$a^2\in H.$$

Hence, $$\boxed{a^2\in H\text{ for every }a\in G.}$$

## Problem 11.29 {#problem-11.29 .unnumbered}

Show that if $$G/Z(G)$$ is cyclic, then $G$ is abelian.

Assume $$G/Z(G)$$ is cyclic. Then there exists some $a\in G$ such that
$$G/Z(G)=\langle aZ(G)\rangle.$$

Let $x,y\in G$. Since every coset is a power of $aZ(G)$, there exist
integers $m,n$ such that $$xZ(G)=a^mZ(G)$$ and $$yZ(G)=a^nZ(G).$$

Thus, there exist $$z_1,z_2\in Z(G)$$ such that $$x=a^mz_1$$ and
$$y=a^nz_2.$$

Now, $$xy=(a^mz_1)(a^nz_2).$$

Since $z_1,z_2\in Z(G)$, they commute with every element of $G$.
Therefore, $$xy=a^{m+n}z_1z_2.$$

Similarly, $$yx=(a^nz_2)(a^mz_1)
=a^{n+m}z_2z_1.$$

Since $$m+n=n+m$$ and $$z_1z_2=z_2z_1,$$ we obtain $$xy=yx.$$

Since $x$ and $y$ were arbitrary, $$\boxed{G\text{ is abelian}.}$$

# True and False Review

## 1. Right and left cosets {#right-and-left-cosets .unnumbered}

Let $H\leq G$ and $a\in G$.

A right coset is $$\boxed{Ha=\{ha:h\in H\}.}$$

The representative $a$ appears on the right.

A left coset is $$\boxed{aH=\{ah:h\in H\}.}$$

The representative $a$ appears on the left.

## 2. $G=\mathbb{Z}_{12}$ and $H=\langle4\rangle$ {#gmathbbz_12-and-hlangle4rangle .unnumbered}

In the additive group $\mathbb{Z}_{12}$,
$$H=\langle4\rangle=\{0,4,8\}.$$

Thus, $$|H|=3.$$

However, $$[G:H]=\frac{|G|}{|H|}
=
\frac{12}{3}
=
4.$$

Therefore, $$\boxed{|H|=3,\qquad [G:H]=4.}$$

## 3. The number of cosets is the index {#the-number-of-cosets-is-the-index .unnumbered}

Statement: The number of distinct left or right cosets of $H$ in $G$ is
$$[G:H].$$

$$\boxed{\text{True}.}$$

The index $[G:H]$ is defined to be the number of distinct cosets of $H$
in $G$.

## 4. $\mathbb{Z}_8$ has an element of order $5$ {#mathbbz_8-has-an-element-of-order-5 .unnumbered}

$$\boxed{\text{False}.}$$

By Lagrange's Theorem, the order of an element must divide the order of
the group.

Since $$|G|=8,$$ the only possible element orders are divisors of $8$:
$$1,2,4,8.$$

Since $$5\nmid8,$$ there is no element of order $5$.

## 5. All right cosets have the same size {#all-right-cosets-have-the-same-size .unnumbered}

Statement: All right cosets of a subgroup $H$ of $G$ have the same size.

$$\boxed{\text{True}.}$$

For each $a\in G$, the function $$H\longrightarrow Ha,
\qquad
h\longmapsto ha$$ is a bijection.

Therefore, $$|Ha|=|H|.$$

## 6. Converse of Lagrange's Theorem {#converse-of-lagranges-theorem .unnumbered}

Statement: If $$k\mid |G|,$$ then $G$ must have a subgroup of order $k$.

$$\boxed{\text{False}.}$$

Lagrange's Theorem says $$H\leq G
\quad\Longrightarrow\quad
|H|\mid |G|.$$

It does not say that every divisor of $|G|$ must occur as the order of a
subgroup.

## 7. The center is always strictly smaller than the group {#the-center-is-always-strictly-smaller-than-the-group .unnumbered}

$$\boxed{\text{False}.}$$

The center is $$Z(G)=\{z\in G:zg=gz\text{ for every }g\in G\}.$$

If $G$ is abelian, then every element commutes with every other element.
Therefore, $$Z(G)=G.$$

Thus, the center is not always strictly smaller than the group.

## 8. If $G$ is abelian, then $G/Z(G)$ is cyclic {#if-g-is-abelian-then-gzg-is-cyclic .unnumbered}

$$\boxed{\text{True}.}$$

If $G$ is abelian, then $$Z(G)=G.$$

Therefore, $$G/Z(G)=G/G.$$

This quotient contains only one coset, so it is the trivial group. The
trivial group is cyclic.

## 9. The center is normal {#the-center-is-normal .unnumbered}

Statement: If $G$ is a group, then $$Z(G)\trianglelefteq G.$$

$$\boxed{\text{True}.}$$

Let $z\in Z(G)$ and $a\in G$. Since $z$ commutes with $a$, $$az=za.$$

Therefore, $$aza^{-1}
=
zaa^{-1}
=
z.$$

Thus, conjugation preserves $Z(G)$, so $$Z(G)\trianglelefteq G.$$

## 10. Size of the quotient group {#size-of-the-quotient-group .unnumbered}

Statement: $$|G/H|=[G:H].$$

$$\boxed{\text{True}.}$$

The set $G/H$ consists of the distinct cosets of $H$ in $G$. Therefore,
its number of elements is exactly the index: $$|G/H|=[G:H].$$

For $G/H$ to be a quotient *group*, we require $$H\trianglelefteq G.$$

# True and False Answer Key

$$\begin{array}{c|c}
\textbf{Question} & \textbf{Answer}\\
\hline
1 & Ha\text{ is right; }aH\text{ is left}\\
2 & |H|=3,\quad [G:H]=4\\
3 & \text{True}\\
4 & \text{False}\\
5 & \text{True}\\
6 & \text{False}\\
7 & \text{False}\\
8 & \text{True}\\
9 & \text{True}\\
10 & \text{True}
\end{array}$$

# Main Formulas and Facts to Memorize

$$\boxed{
Ha=\{ha:h\in H\}
\quad\text{and}\quad
aH=\{ah:h\in H\}
}$$

$$\boxed{
[G:H]=\frac{|G|}{|H|}
}$$

$$\boxed{
|G|=|H|[G:H]
}$$

$$\boxed{
o(a)\mid |G|
}$$

For $a\in\mathbb{Z}_n$, $$\boxed{
o(a)=\frac{n}{\gcd(n,a)}
}$$

$$\boxed{
[G:K]=[G:H][H:K]
\quad\text{when }K\leq H\leq G
}$$

$$\boxed{
|\operatorname{Cl}(a)|=[G:Z(a)]
}$$

$$\boxed{
N\trianglelefteq G
\iff
aNa^{-1}=N
\text{ for every }a\in G
}$$

$$\boxed{
H\trianglelefteq G,\ K\trianglelefteq G
\Longrightarrow
H\cap K\trianglelefteq G
}$$

$$\boxed{
K\trianglelefteq G,\ H\leq G
\Longrightarrow
H\cap K\trianglelefteq H
}$$

$$\boxed{
N\trianglelefteq G,\ H\leq G
\Longrightarrow
NH\leq G
}$$

$$\boxed{
G\text{ abelian}
\Longrightarrow
G/H\text{ abelian}
}$$

$$\boxed{
[G:H]=2
\Longrightarrow
a^2\in H
\text{ for every }a\in G
}$$

$$\boxed{
G/Z(G)\text{ cyclic}
\Longrightarrow
G\text{ abelian}
}$$

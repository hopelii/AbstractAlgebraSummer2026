# Abstract Algebra -- Lecture 5 {#abstract-algebra-lecture-5 .unnumbered}

# Powers of an Element {#powers-of-an-element .unnumbered}

Let $G$ be a group and let $a\in G$.

For a positive integer $n$, define

$$a^n
=
\underbrace{a\cdot a\cdot a\cdots a}_{n\text{ times}}.$$

Also,

$$a^0=e,$$

where $e$ is the identity element of $G$.

For $n>0$,

$$a^{-n}
=
(a^{-1})^n
=
\underbrace{a^{-1}\cdot a^{-1}\cdots a^{-1}}_{n\text{{ times}}.$$

## Laws of Exponents {#laws-of-exponents .unnumbered}

Let $m,n\in\mathbb{Z}$. Then

$$\boxed{a^ma^n=a^{m+n}}$$

$$\boxed{(a^m)^n=a^{mn}}$$

and

$$\boxed{(a^n)^{-1}=a^{-n}}.$$

In particular,

$$\boxed{(a^{-1})^{-1}=a}.$$

These rules hold because the group operation is associative.

# Additive Notation {#additive-notation .unnumbered}

When the group operation is addition, the identity is denoted by

$$0$$

instead of $e$, and the inverse of $a$ is denoted by

$$-a$$

instead of $a^{-1}$.

The additive analogue of $a^n$ is

$$na
=
\underbrace{a+a+\cdots+a}_{n\text{ times}}.$$

For negative $n$,

$$(-n)a=-(na).$$

The exponent laws become

$$ma+na=(m+n)a,$$

and

$$n(ma)=(nm)a.$$

# Order of an Element {#order-of-an-element .unnumbered}

Let $a\in G$.

The element $a$ has **finite order** if there exists a positive integer
$k$ such that

$$a^k=e.$$

The smallest positive integer $k$ satisfying this equation is called the
**order of $a$**.

The order is denoted by

$$o(a)=k$$

or

$$\operatorname{ord}(a)=k.$$

Thus,

$$\boxed{
o(a)=k
\iff
a^k=e
\text{ and }k\text{ is the smallest positive integer with this property}.
}$$

If no positive integer $k$ satisfies

$$a^k=e,$$

then $a$ has **infinite order**, written

$$o(a)=\infty.$$

## Examples {#examples .unnumbered}

In the multiplicative group

$$(\mathbb{R}-\{0\},\cdot),$$

the element $2$ has infinite order because

$$2^k\neq1$$

for every positive integer $k$.

In the additive group

$$(\mathbb{Z},+),$$

the element $1$ has infinite order because

$$n\cdot1=n\neq0$$

for every positive integer $n$.

Consider

$$G=\{1,-1,i,-i\}$$

under multiplication of complex numbers.

Then

$$i^1=i,
\qquad
i^2=-1,
\qquad
i^3=-i,
\qquad
i^4=1.$$

Since $4$ is the smallest positive power that gives the identity,

$$\boxed{o(i)=4}.$$

In the additive group $\mathbb{Z}_{12}$,

$$[8]\oplus[8]=[16]=[4],$$

and

$$[8]\oplus[8]\oplus[8]
=
[24]
=
[0].$$

Therefore,

$$\boxed{o([8])=3}.$$

# Important Theorems About Order {#important-theorems-about-order .unnumbered}

Let $G$ be a group and let $a\in G$.

## Order of an Inverse {#order-of-an-inverse .unnumbered}

$$\boxed{o(a)=o(a^{-1})}.$$

If $a$ has finite order $n$, then

$$a^n=e.$$

Taking inverses,

$$(a^{-1})^n=e.$$

Thus, $a^{-1}$ has the same order as $a$.

If $a$ has infinite order, then $a^{-1}$ must also have infinite order.

## Powers Equal to the Identity {#powers-equal-to-the-identity .unnumbered}

If

$$o(a)=n$$

and

$$a^m=e,$$

then

$$\boxed{n\mid m}.$$

### Proof {#proof .unnumbered}

By the division algorithm, write

$$m=nq+r,
\qquad
0\leq r<n.$$

Then

$$\begin{aligned}
a^m
&=a^{nq+r}\\
&=(a^n)^qa^r\\
&=e^qa^r\\
&=a^r.
\end{aligned}$$

Since $a^m=e$,

$$a^r=e.$$

But $n$ is the smallest positive integer for which $a^n=e$, and

$$0\leq r<n.$$

Therefore,

$$r=0.$$

Hence,

$$m=nq,$$

so

$$\boxed{n\mid m}.$$

## Order of a Power {#order-of-a-power .unnumbered}

Suppose

$$o(a)=n$$

and let

$$d=\gcd(m,n).$$

Then

$$\boxed{
o(a^m)=\frac{n}{d}
=
\frac{n}{\gcd(m,n)}.
}$$

This is one of the most useful formulas for computing the order of a
power.

### Example {#example .unnumbered}

If

$$o(a)=18,$$

then

$$o(a^{12})
=
\frac{18}{\gcd(18,12)}
=
\frac{18}{6}
=
3.$$

# Cyclic Groups {#cyclic-groups .unnumbered}

A group $G$ is called **cyclic** if there exists an element $a\in G$
such that every element of $G$ is a power of $a$.

Thus,

$$G=\{a^n\mid n\in\mathbb{Z}\}.$$

The element $a$ is called a **generator** of $G$.

The notation is

$$\boxed{
\langle a\rangle
=
\{a^n\mid n\in\mathbb{Z}\}.
}$$

Therefore,

$$\boxed{
G\text{ is cyclic with generator }a
\iff
G=\langle a\rangle.
}$$

In additive notation,

$$\langle a\rangle
=
\{na\mid n\in\mathbb{Z}\}.$$

# Examples of Cyclic Groups {#examples-of-cyclic-groups .unnumbered}

## The Integers {#the-integers .unnumbered}

The additive group

$$(\mathbb{Z},+)$$

is cyclic because

$$\mathbb{Z}=\langle1\rangle.$$

Every integer can be written as

$$n\cdot1$$

for some $n\in\mathbb{Z}$.

Also,

$$\mathbb{Z}=\langle-1\rangle.$$

Thus, the generators of $(\mathbb{Z},+)$ are

$$\boxed{1\text{ and }-1}.$$

## The Group $\mathbb{Z}_n$ {#the-group-mathbbz_n .unnumbered}

The additive group

$$(\mathbb{Z}_n,\oplus)$$

is cyclic because

$$\mathbb{Z}_n=\langle[1]\rangle.$$

Indeed,

$$[0],[1],[2],\ldots,[n-1]$$

are obtained by repeatedly adding $[1]$.

## The Rational Numbers {#the-rational-numbers .unnumbered}

The additive group

$$(\mathbb{Q},+)$$

is not cyclic.

Suppose some nonzero $q\in\mathbb{Q}$ generated $\mathbb{Q}$. Then

$$\langle q\rangle
=
\{nq\mid n\in\mathbb{Z}\}.$$

However,

$$\frac{q}{2}\in\mathbb{Q},$$

but there is no integer $n$ such that

$$nq=\frac q2.$$

Therefore,

$$\boxed{(\mathbb{Q},+)\text{ is not cyclic}.}$$

# Distinct Powers in a Cyclic Group {#distinct-powers-in-a-cyclic-group .unnumbered}

Let

$$G=\langle a\rangle.$$

If

$$o(a)=\infty,$$

then

$$a^j\neq a^k$$

whenever

$$j\neq k.$$

Thus, all integer powers of $a$ are distinct, and $G$ is infinite.

If

$$o(a)=n,$$

then

$$\boxed{
a^j=a^k
\iff
j\equiv k\pmod n.
}$$

Therefore, the distinct elements of $G$ are

$$\boxed{
e,a,a^2,\ldots,a^{n-1}.
}$$

# Order of a Group {#order-of-a-group .unnumbered}

The order of a group $G$, denoted by

$$|G|,$$

is the number of elements in $G$.

Be careful:

$$|G|$$

is the order of the group, while

$$o(a)$$

is the order of an individual element $a$.

In general,

$$|G|\neq o(a).$$

However, if

$$G=\langle a\rangle,$$

then

$$\boxed{|G|=o(a)}.$$

Thus, for a cyclic group,

$$|G|=\infty
\iff
o(a)=\infty.$$

# Every Cyclic Group Is Abelian {#every-cyclic-group-is-abelian .unnumbered}

::: theorem
Every cyclic group is abelian.
:::

## Proof {#proof-1 .unnumbered}

Suppose

$$G=\langle a\rangle.$$

Let

$$x,y\in G.$$

Since $G$ is generated by $a$, there exist integers $m,n$ such that

$$x=a^m
\qquad\text{and}\qquad
y=a^n.$$

Then

$$\begin{aligned}
xy
&=a^ma^n\\
&=a^{m+n}\\
&=a^{n+m}\\
&=a^na^m\\
&=yx.
\end{aligned}$$

Therefore,

$$\boxed{xy=yx}$$

for every $x,y\in G$. Hence,

$$\boxed{G\text{ is abelian}.}$$

The converse is not necessarily true:

$$\boxed{
\text{cyclic}\implies\text{abelian},
}$$

but

$$\boxed{
\text{abelian}\centernot\implies\text{cyclic}.
}$$

# Exercise 4.21: Why $o(xy)=o(yx)$ {#exercise-4.21-why-oxyoyx .unnumbered}

Let $x,y\in G$. We want to prove

$$o(xy)=o(yx).$$

Suppose

$$o(xy)=n.$$

Then

$$(xy)^n=e.$$

The key observation is

$$yx=y(xy)y^{-1}.$$

Indeed,

$$\begin{aligned}
y(xy)y^{-1}
&=yx(yy^{-1})\\
&=yxe\\
&=yx.
\end{aligned}$$

Therefore, $yx$ is a conjugate of $xy$.

Now,

$$\begin{aligned}
(yx)^n
&=\left(y(xy)y^{-1}\right)^n\\
&=y(xy)^ny^{-1}.
\end{aligned}$$

The middle terms cancel because

$$y^{-1}y=e.$$

For example,

$$\begin{aligned}
\left(y(xy)y^{-1}\right)^2
&=y(xy)y^{-1}y(xy)y^{-1}\\
&=y(xy)e(xy)y^{-1}\\
&=y(xy)^2y^{-1}.
\end{aligned}$$

Since

$$(xy)^n=e,$$

we get

$$\begin{aligned}
(yx)^n
&=yey^{-1}\\
&=yy^{-1}\\
&=e.
\end{aligned}$$

Therefore,

$$o(yx)\mid n.$$

Since $n=o(xy)$,

$$o(yx)\mid o(xy).$$

Now reverse the roles of $xy$ and $yx$. We can also write

$$xy=x(yx)x^{-1}.$$

The same argument gives

$$o(xy)\mid o(yx).$$

Thus,

$$o(yx)\mid o(xy)$$

and

$$o(xy)\mid o(yx).$$

Two positive integers that divide each other must be equal. Therefore,

$$\boxed{o(xy)=o(yx)}.$$

# Main Ideas to Remember {#main-ideas-to-remember .unnumbered}

$$\boxed{a^ma^n=a^{m+n}}$$

$$\boxed{(a^m)^n=a^{mn}}$$

$$\boxed{(a^n)^{-1}=a^{-n}}$$

$$\boxed{
o(a)=\text{smallest positive }n\text{ such that }a^n=e
}$$

$$\boxed{o(a)=o(a^{-1})}$$

$$\boxed{
o(a)=n\text{ and }a^m=e
\implies
n\mid m
}$$

$$\boxed{
o(a^m)
=
\frac{o(a)}{\gcd(o(a),m)}
}$$

$$\boxed{
G=\langle a\rangle
=
\{a^n\mid n\in\mathbb{Z}\}
}$$

$$\boxed{
o(a)=n
\implies
a^j=a^k
\iff
j\equiv k\pmod n
}$$

$$\boxed{
G=\langle a\rangle
\implies
|G|=o(a)
}$$

$$\boxed{
\text{Every cyclic group is abelian}
}$$

$$\boxed{
\text{Cyclic}\implies\text{abelian},
\qquad
\text{but abelian does not necessarily imply cyclic}.
}$$

$$\boxed{
o(xy)=o(yx)
}$$

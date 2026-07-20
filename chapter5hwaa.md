# Abstract Algebra Homework -- Section 4 {#abstract-algebra-homework-section-4 .unnumbered}

## Exercise 4.4 {#exercise-4.4 .unnumbered}

In $(\mathbb{Z}_{30},\oplus)$, find the orders of the elements
$$[3],\ [4],\ [6],\ [7],\ [18].$$

For an element $[a]\in\mathbb{Z}_n$, its order under addition modulo $n$
is

$$\boxed{
\operatorname{ord}([a])
=
\frac{n}{\gcd(n,a)}
}.$$

Therefore,

$$\operatorname{ord}([3])
=
\frac{30}{\gcd(30,3)}
=
\frac{30}{3}
=
10.$$

$$\operatorname{ord}([4])
=
\frac{30}{\gcd(30,4)}
=
\frac{30}{2}
=
15.$$

$$\operatorname{ord}([6])
=
\frac{30}{\gcd(30,6)}
=
\frac{30}{6}
=
5.$$

$$\operatorname{ord}([7])
=
\frac{30}{\gcd(30,7)}
=
\frac{30}{1}
=
30.$$

$$\operatorname{ord}([18])
=
\frac{30}{\gcd(30,18)}
=
\frac{30}{6}
=
5.$$

Thus,

$$\boxed{
\begin{aligned}
\operatorname{ord}([3])&=10,\\
\operatorname{ord}([4])&=15,\\
\operatorname{ord}([6])&=5,\\
\operatorname{ord}([7])&=30,\\
\operatorname{ord}([18])&=5.
\end{aligned}
}$$

## Exercise 4.5 {#exercise-4.5 .unnumbered}

Let $G$ be a group and let $x\in G$ be an element of order $18$. Find
the orders of

$$x^2,\qquad x^3,\qquad x^4,\qquad x^5,\qquad x^{12}.$$

For an element $x$ of finite order $n$,

$$\boxed{
\operatorname{ord}(x^k)
=
\frac{n}{\gcd(n,k)}
}.$$

Since

$$\operatorname{ord}(x)=18,$$

we have

$$\operatorname{ord}(x^2)
=
\frac{18}{\gcd(18,2)}
=
\frac{18}{2}
=
9.$$

$$\operatorname{ord}(x^3)
=
\frac{18}{\gcd(18,3)}
=
\frac{18}{3}
=
6.$$

$$\operatorname{ord}(x^4)
=
\frac{18}{\gcd(18,4)}
=
\frac{18}{2}
=
9.$$

$$\operatorname{ord}(x^5)
=
\frac{18}{\gcd(18,5)}
=
\frac{18}{1}
=
18.$$

$$\operatorname{ord}(x^{12})
=
\frac{18}{\gcd(18,12)}
=
\frac{18}{6}
=
3.$$

Therefore,

$$\boxed{
\begin{aligned}
\operatorname{ord}(x^2)&=9,\\
\operatorname{ord}(x^3)&=6,\\
\operatorname{ord}(x^4)&=9,\\
\operatorname{ord}(x^5)&=18,\\
\operatorname{ord}(x^{12})&=3.
\end{aligned}
}$$

## Exercise 4.7 {#exercise-4.7 .unnumbered}

Let

$$G=\langle x\rangle$$

be a cyclic group of order $24$. List all elements of $G$ that have
order $4$.

Every element of $G$ has the form

$$x^k.$$

Since $\operatorname{ord}(x)=24$,

$$\operatorname{ord}(x^k)
=
\frac{24}{\gcd(24,k)}.$$

We want

$$\frac{24}{\gcd(24,k)}=4.$$

Therefore,

$$\gcd(24,k)=6.$$

For $0\leq k\leq23$, the values satisfying this condition are

$$k=6
\qquad\text{and}\qquad
k=18.$$

Therefore, the elements of order $4$ are

$$\boxed{x^6\text{ and }x^{18}}.$$

Thus,

$$\boxed{
\{x^6,x^{18}\}
}$$

is the set of all elements of order $4$ in $G$.

## Exercise 4.8 {#exercise-4.8 .unnumbered}

The set of even integers is

$$2\mathbb{Z}
=
\{\ldots,-4,-2,0,2,4,\ldots\}.$$

Determine whether this group is cyclic under addition.

Every even integer can be written as

$$2k$$

for some $k\in\mathbb{Z}$. Therefore,

$$2\mathbb{Z}
=
\langle 2\rangle.$$

Also,

$$2\mathbb{Z}
=
\langle -2\rangle.$$

Hence,

$$\boxed{
(2\mathbb{Z},+)\text{ is cyclic}.
}$$

Its generators are

$$\boxed{2\text{ and }-2}.$$

## Exercise 4.12 {#exercise-4.12 .unnumbered}

Consider the group $(\mathbb{Z},*)$, where

$$a*b=a+b-1.$$

Determine whether this group is cyclic.

First, the identity is $1$, because

$$a*1=a+1-1=a$$

and

$$1*a=1+a-1=a.$$

Consider the element $2$.

Its positive powers under the operation $*$ are

$$2^{*1}=2,$$

$$2^{*2}=2*2=2+2-1=3,$$

$$2^{*3}=(2*2)*2=3*2=3+2-1=4.$$

In general,

$$2^{*n}=n+1$$

for every positive integer $n$.

The inverse of $2$ is $0$, since

$$2*0=2+0-1=1.$$

Therefore,

$$2^{*-1}=0,$$

$$2^{*-2}=0*0=-1,$$

and continuing gives all negative integers.

Thus,

$$\langle 2\rangle
=
\mathbb{Z}.$$

Therefore,

$$\boxed{
(\mathbb{Z},*)\text{ is cyclic}.
}$$

One generator is

$$\boxed{2}.$$

Similarly, $0$ is also a generator.

## Exercise 4.13 {#exercise-4.13 .unnumbered}

Show that if $G$ is a finite group, then every element of $G$ has finite
order.

Let

$$x\in G.$$

Consider the sequence

$$e,x,x^2,x^3,\ldots.$$

Since $G$ is finite, this infinite sequence cannot consist entirely of
distinct elements. Therefore, there exist integers $m<n$ such that

$$x^m=x^n.$$

Multiply both sides on the left by $x^{-m}$:

$$x^{-m}x^m=x^{-m}x^n.$$

Thus,

$$e=x^{n-m}.$$

Since

$$n-m>0,$$

there exists a positive integer $k=n-m$ such that

$$x^k=e.$$

Therefore, $x$ has finite order.

Since $x\in G$ was arbitrary,

$$\boxed{
\text{Every element of a finite group has finite order}.
}$$

## Exercise 4.16 {#exercise-4.16 .unnumbered}

Prove that if

$$G=\langle x\rangle,$$

then

$$G=\langle x^{-1}\rangle.$$

Since

$$G=\langle x\rangle,$$

every element of $G$ has the form

$$x^n$$

for some $n\in\mathbb{Z}$.

Now,

$$(x^{-1})^n=x^{-n}.$$

Therefore,

$$\begin{aligned}
\langle x^{-1}\rangle
&=
\{(x^{-1})^n\mid n\in\mathbb{Z}\}\\
&=
\{x^{-n}\mid n\in\mathbb{Z}\}.
\end{aligned}$$

As $n$ runs through all integers, $-n$ also runs through all integers.
Thus,

$$\{x^{-n}\mid n\in\mathbb{Z}\}
=
\{x^m\mid m\in\mathbb{Z}\}.$$

Hence,

$$\langle x^{-1}\rangle
=
\langle x\rangle
=
G.$$

Therefore,

$$\boxed{
G=\langle x^{-1}\rangle.
}$$

## Exercise 4.17 {#exercise-4.17 .unnumbered}

Suppose

$$G=\langle x\rangle$$

and $G$ is infinite. Prove that $x$ and $x^{-1}$ are the only generators
of $G$.

By Exercise 4.16,

$$\langle x^{-1}\rangle=G.$$

Thus, both $x$ and $x^{-1}$ generate $G$.

Now suppose that $x^k$ is also a generator of $G$. Then

$$\langle x^k\rangle=G.$$

Since $x\in G$, there exists some $m\in\mathbb{Z}$ such that

$$(x^k)^m=x.$$

Therefore,

$$x^{km}=x.$$

Multiplying by $x^{-1}$, we obtain

$$x^{km-1}=e.$$

Since $G$ is infinite cyclic, $x$ has infinite order. Therefore,

$$x^r=e$$

can occur only when

$$r=0.$$

Hence,

$$km-1=0,$$

so

$$km=1.$$

Since $k,m\in\mathbb{Z}$, the only possibilities are

$$k=1,\qquad m=1,$$

or

$$k=-1,\qquad m=-1.$$

Thus,

$$x^k=x$$

or

$$x^k=x^{-1}.$$

Therefore, the only generators of $G$ are

$$\boxed{x\text{ and }x^{-1}}.$$

## Exercise 4.21 {#exercise-4.21 .unnumbered}

Show that for any two elements $x,y$ of a group $G$,

$$o(xy)=o(yx).$$

Observe that

$$yx=y(xy)y^{-1}.$$

Indeed,

$$y(xy)y^{-1}
=
yx(yy^{-1})
=
yx.$$

Thus, $yx$ is conjugate to $xy$.

Suppose first that

$$o(xy)=n.$$

Then

$$(xy)^n=e.$$

Now,

$$\begin{aligned}
(yx)^n
&=
\left(y(xy)y^{-1}\right)^n\\
&=
y(xy)^ny^{-1}\\
&=
yey^{-1}\\
&=
e.
\end{aligned}$$

Therefore,

$$o(yx)\mid n.$$

Since

$$xy=x(yx)x^{-1},$$

the same argument with $xy$ and $yx$ reversed gives

$$o(xy)\mid o(yx).$$

Thus, each order divides the other. Therefore,

$$\boxed{
o(xy)=o(yx).
}$$

# Main Ideas to Remember {#main-ideas-to-remember .unnumbered}

For $[a]\in\mathbb{Z}_n$,

$$\boxed{
\operatorname{ord}([a])
=
\frac{n}{\gcd(n,a)}
}.$$

If $\operatorname{ord}(x)=n$, then

$$\boxed{
\operatorname{ord}(x^k)
=
\frac{n}{\gcd(n,k)}
}.$$

In a cyclic group $G=\langle x\rangle$,

$$\boxed{
G=\langle x^{-1}\rangle.
}$$

If $G=\langle x\rangle$ is infinite, then

$$\boxed{
x\text{ and }x^{-1}\text{ are the only generators of }G.
}$$

Every element of a finite group has finite order:

$$\boxed{
G\text{ finite}
\implies
o(x)<\infty
\text{ for every }x\in G.
}$$

Conjugate elements have the same order:

$$\boxed{
b=aga^{-1}
\implies
o(b)=o(g).
}$$

Since $xy$ and $yx$ are conjugate,

$$\boxed{
o(xy)=o(yx).
}$$

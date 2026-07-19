# Abstract Algebra -- Lecture 4 {#abstract-algebra-lecture-4 .unnumbered}

# Divisibility and Prime Numbers {#divisibility-and-prime-numbers .unnumbered}

## Prime Numbers {#prime-numbers .unnumbered}

A **prime number** is an integer $p\geq 2$ whose only positive divisors
are $1$ and $p$.

Examples of prime numbers include
$$2,3,5,7,11,13,17,19,23,29,31,37,41,43,\ldots$$

A **composite number** is an integer $n\geq 2$ that is not prime.

Examples include $$4,6,8,9,10,12,14,\ldots$$

## Euclid's Theorem {#euclids-theorem .unnumbered}

::: theorem
There are infinitely many prime numbers.
:::

## Fundamental Theorem of Arithmetic {#fundamental-theorem-of-arithmetic .unnumbered}

::: theorem
Every integer $n>1$ is either prime or can be written uniquely, up to
the order of the factors, as a product of prime numbers.
:::

For example, $$12=2^2\cdot 3.$$

Although $12$ can also be written as $$12=1\cdot12,
\qquad
12=2\cdot6,
\qquad
12=3\cdot4,$$ its prime factorization is uniquely
$$\boxed{12=2^2\cdot3}.$$

The uniqueness means that there are no primes other than $2$ and $3$
whose product, with appropriate multiplicities, equals $12$.

# Divisibility {#divisibility .unnumbered}

Let $d,n\in\mathbb{Z}$.

We say that $d$ **divides** $n$ if there exists $q\in\mathbb{Z}$ such
that $$n=dq.$$

The notation is $$d\mid n.$$

If $d\mid n$, then:

- $n$ is a multiple of $d$;

- $d$ is a divisor or factor of $n$.

For example, $$3\mid 9$$ because $$9=3\cdot3.$$

A divisor $d$ of $n$ is called a **proper divisor** if $$d\neq n.$$

For example, $$3\mid 9$$ and $3$ is a proper divisor of $9$, while
$$9\mid 9$$ but $9$ is not a proper divisor of itself.

# The Division Algorithm {#the-division-algorithm .unnumbered}

::: theorem
Let $n\in\mathbb{Z}$ and let $d\in\mathbb{Z}$ with $d>0$. Then there
exist unique integers $q,r\in\mathbb{Z}$ such that $$n=dq+r,$$ where
$$0\leq r<d.$$
:::

Here:

- $q$ is the quotient;

- $r$ is the remainder.

Examples: $$18=5\cdot3+3,$$ so when $18$ is divided by $5$, the
remainder is $3$.

Also, $$25=5\cdot5+0,$$ so $5\mid25$.

Finally, $$17=6\cdot2+5.$$

# Greatest Common Divisor {#greatest-common-divisor .unnumbered}

Let $m,n\in\mathbb{Z}$, not both zero.

The **greatest common divisor** of $m$ and $n$, denoted $$\gcd(m,n),$$
is the largest positive integer that divides both $m$ and $n$.

For example, $$\gcd(2,3)=1$$ and $$\gcd(12,18)=6.$$

The value $$\gcd(0,0)$$ is undefined because every integer divides $0$,
so there is no largest positive common divisor.

Also, $$\gcd(m,n)=\gcd(|m|,|n|).$$

Therefore, when computing greatest common divisors, we may assume that
$m$ and $n$ are nonnegative.

# The Euclidean Algorithm {#the-euclidean-algorithm .unnumbered}

The Euclidean algorithm is used to compute $$\gcd(m,n).$$

Assume $$m\geq n>0.$$

Apply the division algorithm repeatedly:

$$m=q_1n+r_1,
\qquad
0\leq r_1<n,$$

$$n=q_2r_1+r_2,
\qquad
0\leq r_2<r_1,$$

$$r_1=q_3r_2+r_3,
\qquad
0\leq r_3<r_2,$$

and continue:

$$r_{k-2}=q_kr_{k-1}+r_k,
\qquad
0\leq r_k<r_{k-1}.$$

Eventually, one of the remainders is $0$. The last nonzero remainder is
the greatest common divisor:

$$\boxed{\gcd(m,n)=\text{last nonzero remainder}.}$$

## Example {#example .unnumbered}

Find $$\gcd(3084,1424).$$

Using the Euclidean algorithm, $$3084=2(1424)+236,$$

$$1424=6(236)+8,$$

$$236=29(8)+4,$$

$$8=2(4)+0.$$

The last nonzero remainder is $4$. Therefore,
$$\boxed{\gcd(3084,1424)=4}.$$

# Bézout's Identity {#bézouts-identity .unnumbered}

::: theorem
Let $m,n\in\mathbb{Z}$, not both zero, and let $$d=\gcd(m,n).$$

Then there exist integers $x,y\in\mathbb{Z}$ such that $$mx+ny=d.$$
:::

The integers $x$ and $y$ can be found using the **Extended Euclidean
Algorithm**.

# The Extended Euclidean Algorithm {#the-extended-euclidean-algorithm .unnumbered}

The Extended Euclidean Algorithm reverses the steps of the Euclidean
algorithm in order to write the greatest common divisor as an integer
linear combination of the original numbers.

## Example {#example-1 .unnumbered}

Find integers $x$ and $y$ such that $$3084x+1424y=4.$$

From the Euclidean algorithm, $$3084=2(1424)+236,$$ so
$$236=3084-2(1424).$$

Also, $$1424=6(236)+8,$$ so $$8=1424-6(236).$$

Finally, $$236=29(8)+4,$$ so $$4=236-29(8).$$

Substitute the expression for $8$: $$\begin{aligned}
4
&=236-29\bigl(1424-6(236)\bigr)\\
&=236-29(1424)+174(236)\\
&=175(236)-29(1424).
\end{aligned}$$

Now substitute $$236=3084-2(1424):$$

$$\begin{aligned}
4
&=175\bigl(3084-2(1424)\bigr)-29(1424)\\
&=175(3084)-350(1424)-29(1424)\\
&=175(3084)-379(1424).
\end{aligned}$$

Therefore, one solution is $$\boxed{x=175,\qquad y=-379}.$$

Indeed, $$3084(175)+1424(-379)=4.$$

# Relatively Prime Integers {#relatively-prime-integers .unnumbered}

If $$\gcd(m,n)=1,$$ then $m$ and $n$ are called **relatively prime** or
**coprime**.

Examples include $$\gcd(11,29)=1$$ and $$\gcd(3,8)=1.$$

By Bézout's identity, $$\gcd(m,n)=1$$ if and only if there exist
integers $x,y$ such that $$mx+ny=1.$$

# Euclid's Lemma {#euclids-lemma .unnumbered}

::: theorem
Let $a,b,c\in\mathbb{Z}$. If $$a\mid bc$$ and $$\gcd(a,b)=1,$$ then
$$a\mid c.$$
:::

## Proof {#proof .unnumbered}

Since $$\gcd(a,b)=1,$$ Bézout's identity gives integers
$x,y\in\mathbb{Z}$ such that $$ax+by=1.$$

Since $$a\mid bc,$$ there exists $k\in\mathbb{Z}$ such that $$bc=ak.$$

Multiply $$ax+by=1$$ by $c$: $$acx+bcy=c.$$

Since $$bc=ak,$$ we obtain $$acx+aky=c.$$

Factor out $a$: $$a(cx+ky)=c.$$

Because $$cx+ky\in\mathbb{Z},$$ it follows that $$\boxed{a\mid c}.$$

# Products of Coprime Integers {#products-of-coprime-integers .unnumbered}

::: theorem
Let $m,n,d\in\mathbb{Z}$ be nonzero integers. If $$\gcd(m,d)=1$$ and
$$\gcd(n,d)=1,$$ then $$\gcd(mn,d)=1.$$
:::

## Proof {#proof-1 .unnumbered}

Since $$\gcd(m,d)=1,$$ Bézout's identity gives integers
$s,t\in\mathbb{Z}$ such that $$ms+dt=1.$$

Since $$\gcd(n,d)=1,$$ there exist integers $k,r\in\mathbb{Z}$ such that
$$nk+dr=1.$$

Substitute $$ms+dt=1$$ into the second equation: $$nk+d r=1.$$

Multiplying the first Bézout identity by $nk$, we have $$nk(ms+dt)=nk.$$

Thus, $$mn(sk)+d(tnk)=nk.$$

Now substitute this into $$nk+dr=1:$$

$$mn(sk)+d(tnk)+dr=1.$$

Factor $d$: $$mn(sk)+d(tnk+r)=1.$$

Since $$sk\in\mathbb{Z}
\qquad\text{and}\qquad
tnk+r\in\mathbb{Z},$$ Bézout's identity implies
$$\boxed{\gcd(mn,d)=1}.$$

# Main Ideas to Remember {#main-ideas-to-remember .unnumbered}

$$\boxed{
p\text{ is prime if its only positive divisors are }1\text{ and }p.
}$$

$$\boxed{
d\mid n
\iff
n=dq\text{ for some }q\in\mathbb{Z}.
}$$

$$\boxed{
n=dq+r,
\qquad
0\leq r<d.
}$$

$$\boxed{
\gcd(m,n)=\text{the last nonzero remainder in the Euclidean algorithm}.
}$$

$$\boxed{
\gcd(m,n)=d
\implies
mx+ny=d
\text{ for some }x,y\in\mathbb{Z}.
}$$

$$\boxed{
\gcd(m,n)=1
\iff
mx+ny=1
\text{ for some }x,y\in\mathbb{Z}.
}$$

$$\boxed{
a\mid bc
\text{ and }
\gcd(a,b)=1
\implies
a\mid c.
}$$

$$\boxed{
\gcd(m,d)=\gcd(n,d)=1
\implies
\gcd(mn,d)=1.
}$$

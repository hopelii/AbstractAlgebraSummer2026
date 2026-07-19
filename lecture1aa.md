# Abstract Algebra -- Lecture 1 Summary {#abstract-algebra-lecture-1-summary .unnumbered}

This lecture introduces the basic language used in abstract algebra:
$$\text{sets, functions, binary operations, the well-ordering principle, and mathematical induction.}$$

## 1. Sets {#sets .unnumbered}

A **set** is a collection of objects called **elements**.

Sets can be written using **roster notation**, where all elements are
listed: $$A=\{1,3,5,-13,\pi\}.$$

They can also be written using **set-builder notation**, where the
elements are described by a condition:
$$\{x\in\mathbb{R}\mid x\geq 10\}.$$

The order in which elements are listed does not matter. For example,
$$\{1,3,5\}=\{5,1,3\}.$$

Repeated elements are only counted once.

Important number sets include: $$\mathbb{N}=\{1,2,3,\ldots\},$$ the set
of natural or counting numbers;

$$\mathbb{Z}=\{\ldots,-2,-1,0,1,2,\ldots\},$$ the set of integers;

$$\mathbb{Q}
=
\left\{
\frac{a}{b}
\;\middle|\;
a,b\in\mathbb{Z},\ b\neq 0
\right\},$$ the set of rational numbers;

and $$\mathbb{I}
=
\left\{
x\in\mathbb{R}
\;\middle|\;
x \text{ cannot be written as } \frac{a}{b},
\ a,b\in\mathbb{Z},\ b\neq 0
\right\},$$ the set of irrational numbers.

An interval such as $$(3,11)$$ represents all real numbers strictly
between $3$ and $11$.

It is not the same as $$\{3,11\},$$ which is a set containing only the
two elements $3$ and $11$.

## 2. Empty Sets and Subsets {#empty-sets-and-subsets .unnumbered}

The **empty set** is denoted by $$\varnothing.$$

It contains no elements.

Be careful: $$\{\varnothing\}\neq\varnothing.$$

The set $\{\varnothing\}$ contains one element, namely the empty set,
while $\varnothing$ contains no elements.

We write $$B\subseteq A$$ when every element of $B$ is also an element
of $A$.

Important facts include: $$A\subseteq A$$ for every set $A$, and
$$\varnothing\subseteq A$$ for every set $A$.

Two sets are equal exactly when each is a subset of the other: $$A=B
\iff
A\subseteq B
\text{ and }
B\subseteq A.$$

The **difference** of two sets is $$A-B
=
\{x\mid x\in A \text{ and } x\notin B\}.$$

For example, if $E$ is the set of even integers, then $$\mathbb{Z}-E
=
\{x\in\mathbb{Z}\mid x \text{ is odd}\}.$$

## 3. Union and Intersection {#union-and-intersection .unnumbered}

The **intersection** of two sets contains the elements that belong to
both sets: $$A\cap B
=
\{x\mid x\in A \text{ and } x\in B\}.$$

The **union** of two sets contains the elements that belong to at least
one of the sets: $$A\cup B
=
\{x\mid x\in A \text{ or } x\in B\}.$$

The word "or" is inclusive, so an element may belong to both $A$ and
$B$.

Some important identities are: $$A\cup A=A,
\qquad
A\cap A=A,$$ $$A\cup\varnothing=A,
\qquad
A\cap\varnothing=\varnothing,$$ $$A\cup B=B\cup A,
\qquad
A\cap B=B\cap A.$$

Union and intersection are associative:
$$A\cup(B\cup C)=(A\cup B)\cup C,$$ $$A\cap(B\cap C)=(A\cap B)\cap C.$$

They are also distributive: $$A\cap(B\cup C)
=
(A\cap B)\cup(A\cap C),$$ $$A\cup(B\cap C)
=
(A\cup B)\cap(A\cup C).$$

The following subset relationships are useful: $$A\subseteq B
\iff
A\cup B=B,$$ and $$A\subseteq B
\iff
A\cap B=A.$$

## 4. Cartesian Products {#cartesian-products .unnumbered}

The **Cartesian product** of two sets $A$ and $B$ is $$A\times B
=
\{(x,y)\mid x\in A,\ y\in B\}.$$

The elements of $A\times B$ are ordered pairs, so order matters:
$$(x,y)\neq(y,x)$$ in general.

For example, if $$A=\{a,b,c\}
\qquad\text{and}\qquad
B=\{3,4\},$$ then $$A\times B
=
\{(a,3),(a,4),(b,3),(b,4),(c,3),(c,4)\}.$$

## 5. Functions {#functions .unnumbered}

A **function** $$f:A\to B$$ is a rule that assigns exactly one element
of $B$ to each element of $A$.

The set $A$ is called the **domain**.

The set $B$ is called the **codomain**.

The **range** is the set of values in the codomain that the function
actually reaches.

A relation is not a function if one input is assigned to more than one
output.

### Injective Functions {#injective-functions .unnumbered}

A function is **injective**, or one-to-one, if different inputs produce
different outputs: $$a\neq b
\implies
f(a)\neq f(b).$$

An equivalent statement, which is often easier to prove, is $$f(a)=f(b)
\implies
a=b.$$

For example, let $$f:\mathbb{R}\to\mathbb{R}$$ be defined by
$$f(x)=2x+3.$$

To show that $f$ is injective, assume $$f(a)=f(b).$$

Then $$2a+3=2b+3.$$

Subtracting $3$ from both sides gives $$2a=2b,$$ so $$a=b.$$

Therefore, $f$ is injective.

### Surjective Functions {#surjective-functions .unnumbered}

A function is **surjective**, or onto, if every element of the codomain
is reached.

Formally, $$\forall b\in B,\ \exists a\in A
\text{ such that }
f(a)=b.$$

For example, let $$f:\mathbb{R}\to\mathbb{R}$$ be defined by
$$f(x)=2x+5.$$

Take an arbitrary $$b\in\mathbb{R}.$$

We want to find $a\in\mathbb{R}$ such that $$f(a)=b.$$

Solving $$2a+5=b$$ for $a$, we get $$a=\frac{b-5}{2}.$$

Since $$\frac{b-5}{2}\in\mathbb{R},$$ we have
$$f\left(\frac{b-5}{2}\right)
=
2\left(\frac{b-5}{2}\right)+5
=
b.$$

Therefore, $f$ is surjective.

### Bijective Functions {#bijective-functions .unnumbered}

A function is **bijective** if it is both injective and surjective:
$$f \text{ is bijective}
\iff
f \text{ is injective and surjective}.$$

For finite sets $A$ and $B$, a bijection exists exactly when
$$|A|=|B|.$$

A function is bijective if and only if it has an inverse:
$$f \text{ is bijective}
\iff
f^{-1} \text{ exists}.$$

## 6. Binary Operations {#binary-operations .unnumbered}

A **binary operation** on a set $S$ is a function $$*:S\times S\to S.$$

It takes each ordered pair $$(a,b)\in S\times S$$ and assigns another
element of $S$, denoted by $$a*b.$$

For an operation to be binary on $S$, it must satisfy two conditions:

1.  The operation must be defined for every pair $a,b\in S$.

2.  The output $a*b$ must also belong to $S$.

The second requirement is called **closure**.

For example, define $$a*b=a+b^2$$ on $\mathbb{Z}$.

Since $a\in\mathbb{Z}$ and $b^2\in\mathbb{Z}$, we have
$$a+b^2\in\mathbb{Z}.$$

Therefore, this is a binary operation on $\mathbb{Z}$.

Now consider $$a*b=\frac{1}{a^2+b^2}$$ on $\mathbb{R}$.

For $a=b=0$, $$0*0
=
\frac{1}{0^2+0^2}
=
\frac{1}{0},$$ which is undefined.

Therefore, this is not a binary operation on $\mathbb{R}$.

As another example, let $$S=\{1,-2,3,2,-4\}$$ and define $$a*b=|b|.$$

Then $$1*(-4)=|-4|=4.$$

However, $$4\notin S.$$

Therefore, the operation is not closed on $S$, so it is not a binary
operation on $S$.

## 7. Well-Ordering Principle {#well-ordering-principle .unnumbered}

The **well-ordering principle** states:

> Every nonempty subset of $\mathbb{N}$ contains a smallest element.

For example, the set $$\{5,8,12,20,\ldots\}$$ is a nonempty subset of
$\mathbb{N}$, and its smallest element is $5$.

## 8. Mathematical Induction {#mathematical-induction .unnumbered}

Mathematical induction is used to prove that a statement $P(n)$ is true
for every natural number $n$.

The proof has three main parts.

### Step 1: Base Case {#step-1-base-case .unnumbered}

Prove that the statement is true for the first value, usually $n=1$:
$$P(1) \text{ is true}.$$

### Step 2: Inductive Hypothesis {#step-2-inductive-hypothesis .unnumbered}

Assume that the statement is true for some natural number $k$:
$$P(k) \text{ is true}.$$

### Step 3: Inductive Step {#step-3-inductive-step .unnumbered}

Use the assumption that $P(k)$ is true to prove that $$P(k+1)$$ is also
true.

Once these steps are completed, we conclude that $$P(n)$$ is true for
every relevant $n\in\mathbb{N}$.

### Example 1: Sum of Squares {#example-1-sum-of-squares .unnumbered}

Prove that $$1^2+2^2+\cdots+n^2
=
\frac{n(n+1)(2n+1)}{6}$$ for every $n\in\mathbb{N}$.

#### Base Case

For $n=1$, $$1^2
=
\frac{1(1+1)(2\cdot1+1)}{6}
=
\frac{1\cdot2\cdot3}{6}
=
1.$$

Therefore, the formula is true for $n=1$.

#### Inductive Hypothesis

Assume that the formula is true for some $k\in\mathbb{N}$:
$$1^2+2^2+\cdots+k^2
=
\frac{k(k+1)(2k+1)}{6}.$$

#### Inductive Step

We want to prove that $$1^2+2^2+\cdots+k^2+(k+1)^2
=
\frac{(k+1)(k+2)(2k+3)}{6}.$$

Using the inductive hypothesis, $$1^2+2^2+\cdots+k^2+(k+1)^2
=
\frac{k(k+1)(2k+1)}{6}
+
(k+1)^2.$$

Factor out $k+1$: $$=
(k+1)
\left[
\frac{k(2k+1)}{6}
+
(k+1)
\right].$$

Combine the terms: $$=
(k+1)
\left[
\frac{2k^2+k+6k+6}{6}
\right].$$

Factor the numerator: $$2k^2+7k+6
=
(2k+3)(k+2).$$

Therefore, $$1^2+2^2+\cdots+k^2+(k+1)^2
=
\frac{(k+1)(k+2)(2k+3)}{6}.$$

Thus, the formula is true for $k+1$, so by mathematical induction,
$$1^2+2^2+\cdots+n^2
=
\frac{n(n+1)(2n+1)}{6}$$ for all $n\in\mathbb{N}$.

### Example 2: Divisibility {#example-2-divisibility .unnumbered}

Prove that $$3\mid n^3-n$$ for every $n\geq 1$.

The notation $$3\mid n^3-n$$ means that $3$ divides $n^3-n$.

#### Base Case

For $n=1$, $$1^3-1=0.$$

Since $$0=3\cdot0,$$ we have $$3\mid 1^3-1.$$

#### Inductive Hypothesis

Assume that $$3\mid k^3-k.$$

This means that there exists some integer $a$ such that $$k^3-k=3a.$$

#### Inductive Step

Consider $$(k+1)^3-(k+1).$$

Expanding gives $$(k+1)^3-(k+1)
=
k^3+3k^2+3k+1-k-1.$$

Therefore, $$(k+1)^3-(k+1)
=
k^3-k+3k^2+3k.$$

Factor: $$=
(k^3-k)+3(k^2+k).$$

Using the inductive hypothesis, $$k^3-k=3a.$$

Thus, $$(k+1)^3-(k+1)
=
3a+3(k^2+k).$$

Factor out $3$: $$=
3(a+k^2+k).$$

Therefore, $$3\mid (k+1)^3-(k+1).$$

Hence, by mathematical induction, $$3\mid n^3-n$$ for every $n\geq 1$.

# Main Ideas to Remember {#main-ideas-to-remember .unnumbered}

$$\boxed{
\text{A set is an unordered collection of distinct elements.}
}$$

$$\boxed{
A=B
\iff
A\subseteq B
\text{ and }
B\subseteq A
}$$

$$\boxed{
A\cap B
=
\text{elements in both }A\text{ and }B
}$$

$$\boxed{
A\cup B
=
\text{elements in }A\text{ or }B
}$$

$$\boxed{
A\times B
=
\{(a,b)\mid a\in A,\ b\in B\}
}$$

$$\boxed{
\text{A function assigns exactly one output to each input.}
}$$

$$\boxed{
f \text{ is injective}
\iff
f(a)=f(b)\implies a=b
}$$

$$\boxed{
f \text{ is surjective}
\iff
\forall b\in B,\ \exists a\in A
\text{ such that }f(a)=b
}$$

$$\boxed{
f \text{ is bijective}
\iff
f \text{ is injective and surjective}
}$$

$$\boxed{
f \text{ is bijective}
\iff
f^{-1} \text{ exists}
}$$

$$\boxed{
\text{A binary operation on }S\text{ must be defined for every pair in }S
\text{ and must produce an output in }S.
}$$

$$\boxed{
\text{Closure means that if }a,b\in S,\text{ then }a*b\in S.
}$$

$$\boxed{
\text{Every nonempty subset of }\mathbb{N}\text{ has a smallest element.}
}$$

$$\boxed{
\text{Induction consists of a base case, an inductive hypothesis, and an inductive step.}
}$$

$$\boxed{
P(1)\text{ true}
\quad\text{and}\quad
P(k)\implies P(k+1)
\quad\Longrightarrow\quad
P(n)\text{ true for all }n\in\mathbb{N}.
}$$

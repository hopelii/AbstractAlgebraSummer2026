# Abstract Algebra Homework: Groups {#abstract-algebra-homework-groups .unnumbered}

## Exercise 2.1 {#exercise-2.1 .unnumbered}

Determine which of the following are groups under the given operations.

A set $G$ with a binary operation $*$ is a group if it satisfies:

1.  **Closure:** $$x,y\in G \implies x*y\in G.$$

2.  **Associativity:** $$(x*y)*z=x*(y*z)$$ for all $x,y,z\in G$.

3.  **Identity:** There exists $e\in G$ such that $$x*e=e*x=x$$ for
    every $x\in G$.

4.  **Inverses:** For every $x\in G$, there exists $x^{-1}\in G$ such
    that $$x*x^{-1}=x^{-1}*x=e.$$

A group is called **abelian** if $$x*y=y*x$$ for every $x,y\in G$.

### (a) $\mathbb{R}^{+}$ under addition {#a-mathbbr-under-addition .unnumbered}

Assume $$\mathbb{R}^{+}=\{x\in\mathbb{R}\mid x>0\}.$$

The operation is closed because the sum of two positive real numbers is
positive. Addition is also associative.

However, the additive identity is $$0,$$ and $$0\notin\mathbb{R}^{+}.$$

Therefore, the set does not contain an identity element.

$$\boxed{(\mathbb{R}^{+},+)\text{ is not a group}.}$$

### (b) $3\mathbb{Z}$ under addition {#b-3mathbbz-under-addition .unnumbered}

The set of multiples of $3$ is
$$3\mathbb{Z}=\{3k\mid k\in\mathbb{Z}\}.$$

Let $$3m,3n\in3\mathbb{Z}.$$

For closure, $$3m+3n=3(m+n).$$

Since $m+n\in\mathbb{Z}$, $$3(m+n)\in3\mathbb{Z}.$$

Addition is associative because ordinary integer addition is
associative.

The identity is $$0=3(0)\in3\mathbb{Z}.$$

The inverse of $3m$ is $$-3m=3(-m)\in3\mathbb{Z}.$$

Therefore, $$\boxed{(3\mathbb{Z},+)\text{ is a group}.}$$

Since addition is commutative, $$3m+3n=3n+3m,$$ the group is abelian.

$$\boxed{(3\mathbb{Z},+)\text{ is an abelian group}.}$$

### (c) $\mathbb{R}-\{0\}$ under $a*b=|ab|$ {#c-mathbbr-0-under-abab .unnumbered}

Let $$G=\mathbb{R}-\{0\}$$ and define $$a*b=|ab|.$$

If $a,b\neq0$, then $$|ab|>0,$$ so $$|ab|\in G.$$

Thus, the operation is closed.

Also, $$(a*b)*c
=
\bigl||ab|c\bigr|
=
|abc|,$$ while $$a*(b*c)
=
\bigl|a|bc|\bigr|
=
|abc|.$$

Therefore, the operation is associative.

However, there is no identity element. If $e$ were an identity, then
$$a*e=|ae|=a$$ would have to hold for every nonzero real number $a$.

Choose $$a=-1.$$

Then we would need $$|-e|=-1,$$ which is impossible because an absolute
value cannot be negative.

Therefore, $$\boxed{(\mathbb{R}-\{0\},*)\text{ is not a group}.}$$

### (d) $\{1,-1\}$ under multiplication {#d-1-1-under-multiplication .unnumbered}

Let $$G=\{1,-1\}.$$

The multiplication table is $$\begin{array}{c|cc}
\cdot & 1 & -1\\
\hline
1 & 1 & -1\\
-1 & -1 & 1
\end{array}.$$

Every product belongs to $G$, so the operation is closed.

Ordinary multiplication is associative.

The identity is $$e=1.$$

Each element is its own inverse: $$1^{-1}=1$$ and $$(-1)^{-1}=-1.$$

Therefore, $$\boxed{(\{1,-1\},\cdot)\text{ is a group}.}$$

Since multiplication is commutative,
$$\boxed{(\{1,-1\},\cdot)\text{ is an abelian group}.}$$

### (f) $\mathbb{R}^{2}$ under $(x,y)*(z,w)=(x+z,y-w)$ {#f-mathbbr2-under-xyzwxzy-w .unnumbered}

Let $$(x,y),(z,w),(u,v)\in\mathbb{R}^{2}.$$

First, $$\begin{aligned}
\bigl((x,y)*(z,w)\bigr)*(u,v)
&=(x+z,y-w)*(u,v)\\
&=(x+z+u,y-w-v).
\end{aligned}$$

On the other hand, $$\begin{aligned}
(x,y)*\bigl((z,w)*(u,v)\bigr)
&=(x,y)*(z+u,w-v)\\
&=(x+z+u,y-(w-v))\\
&=(x+z+u,y-w+v).
\end{aligned}$$

In general, $$y-w-v\neq y-w+v.$$

Therefore, $$\bigl((x,y)*(z,w)\bigr)*(u,v)
\neq
(x,y)*\bigl((z,w)*(u,v)\bigr).$$

The operation is not associative, so
$$\boxed{\mathbb{R}^{2}\text{ under this operation is not a group}.}$$

### (g) Pairs $(x,y)$ with $y\neq0$ {#g-pairs-xy-with-yneq0 .unnumbered}

Let $$G=\{(x,y)\in\mathbb{R}^{2}\mid y\neq0\}$$ with operation
$$(x,y)*(z,w)=(x+z,yw).$$

For closure, if $y\neq0$ and $w\neq0$, then $$yw\neq0.$$

Therefore, $$(x+z,yw)\in G.$$

For associativity, $$\begin{aligned}
\bigl((x,y)*(z,w)\bigr)*(u,v)
&=(x+z,yw)*(u,v)\\
&=(x+z+u,ywv),
\end{aligned}$$ and $$\begin{aligned}
(x,y)*\bigl((z,w)*(u,v)\bigr)
&=(x,y)*(z+u,wv)\\
&=(x+z+u,ywv).
\end{aligned}$$

Thus, the operation is associative.

To find the identity, let $$e=(e_1,e_2).$$

We require $$(x,y)*(e_1,e_2)=(x,y).$$

Thus, $$(x+e_1,ye_2)=(x,y),$$ so $$e_1=0
\qquad\text{and}\qquad
e_2=1.$$

Therefore, the identity is $$\boxed{e=(0,1)}.$$

To find the inverse of $(x,y)$, solve $$(x,y)*(z,w)=(0,1).$$

This gives $$x+z=0
\qquad\text{and}\qquad
yw=1.$$

Therefore, $$z=-x
\qquad\text{and}\qquad
w=\frac{1}{y}.$$

Hence, $$\boxed{
(x,y)^{-1}
=
\left(-x,\frac{1}{y}\right)
}.$$

Therefore, $$\boxed{(G,*)\text{ is a group}.}$$

Furthermore, $$(x,y)*(z,w)=(x+z,yw)$$ and $$(z,w)*(x,y)=(z+x,wy).$$

Since real addition and multiplication are commutative, $$x+z=z+x
\qquad\text{and}\qquad
yw=wy.$$

Therefore, $$\boxed{(G,*)\text{ is an abelian group}.}$$

### (h) $\mathbb{R}-\{1\}$ under $a*b=a+b-ab$ {#h-mathbbr-1-under-abab-ab .unnumbered}

Let $$G=\mathbb{R}-\{1\}$$ and define $$a*b=a+b-ab.$$

For closure, observe that $$1-(a*b)
=
1-a-b+ab
=
(1-a)(1-b).$$

Since $a\neq1$ and $b\neq1$, $$1-a\neq0
\qquad\text{and}\qquad
1-b\neq0.$$

Thus, $$(1-a)(1-b)\neq0.$$

Therefore, $$1-(a*b)\neq0,$$ which means $$a*b\neq1.$$

Hence, $$a*b\in G.$$

For associativity, $$\begin{aligned}
(a*b)*c
&=(a+b-ab)+c-(a+b-ab)c\\
&=a+b+c-ab-ac-bc+abc.
\end{aligned}$$

Also, $$\begin{aligned}
a*(b*c)
&=a+(b+c-bc)-a(b+c-bc)\\
&=a+b+c-ab-ac-bc+abc.
\end{aligned}$$

Therefore, $$(a*b)*c=a*(b*c).$$

To find the identity, solve $$a*e=a.$$

Then $$a+e-ae=a,$$ so $$e-ae=0.$$

Factoring, $$e(1-a)=0.$$

Since $a\neq1$, $$e=0.$$

Therefore, the identity is $$\boxed{e=0}.$$

To find the inverse of $a$, solve $$a*b=0.$$

Thus, $$a+b-ab=0.$$

Rearranging, $$b-ab=-a,$$ so $$b(1-a)=-a.$$

Therefore, $$b=\frac{-a}{1-a}
=
\frac{a}{a-1}.$$

Hence, $$\boxed{
a^{-1}=\frac{a}{a-1}
}.$$

This inverse is not equal to $1$, because $$\frac{a}{a-1}=1$$ would
imply $$a=a-1,$$ which is impossible.

Therefore, the inverse belongs to $G$.

Hence, $$\boxed{(\mathbb{R}-\{1\},*)\text{ is a group}.}$$

Since $$a+b-ab=b+a-ba,$$ the operation is commutative.

Thus, $$\boxed{(\mathbb{R}-\{1\},*)\text{ is an abelian group}.}$$

### (i) $\mathbb{Z}$ under $a*b=a+b-1$ {#i-mathbbz-under-abab-1 .unnumbered}

Let $$a*b=a+b-1.$$

For closure, if $a,b\in\mathbb{Z}$, then $$a+b-1\in\mathbb{Z}.$$

For associativity, $$\begin{aligned}
(a*b)*c
&=(a+b-1)+c-1\\
&=a+b+c-2.
\end{aligned}$$

Also, $$\begin{aligned}
a*(b*c)
&=a+(b+c-1)-1\\
&=a+b+c-2.
\end{aligned}$$

Therefore, $$(a*b)*c=a*(b*c).$$

To find the identity, solve $$a*e=a.$$

Then $$a+e-1=a,$$ so $$e=1.$$

Thus, $$\boxed{e=1}.$$

To find the inverse of $a$, solve $$a*b=e=1.$$

Then $$a+b-1=1,$$ so $$b=2-a.$$

Thus, $$\boxed{a^{-1}=2-a}.$$

Since $2-a\in\mathbb{Z}$, every element has an inverse in the set.

Therefore, $$\boxed{(\mathbb{Z},*)\text{ is a group}.}$$

Since $$a+b-1=b+a-1,$$ the group is abelian.

$$\boxed{(\mathbb{Z},*)\text{ is an abelian group}.}$$

## Final Answers for Exercise 2.1 {#final-answers-for-exercise-2.1 .unnumbered}

$$\begin{array}{c|c|c}
\text{Part} & \text{Group?} & \text{Abelian?}\\
\hline
(a) & \text{No} & \text{N/A}\\
(b) & \text{Yes} & \text{Yes}\\
(c) & \text{No} & \text{N/A}\\
(d) & \text{Yes} & \text{Yes}\\
(f) & \text{No} & \text{N/A}\\
(g) & \text{Yes} & \text{Yes}\\
(h) & \text{Yes} & \text{Yes}\\
(i) & \text{Yes} & \text{Yes}
\end{array}$$

## Exercise 2.2(a) {#exercise-2.2a .unnumbered}

Of the examples from Exercise 2.1 that are groups, determine which are
abelian.

The groups from the selected parts of Exercise 2.1 are
$$(b),\qquad(d),\qquad(g),\qquad(h),\qquad(i).$$

Each of these operations is commutative. Therefore, $$\boxed{
(b),\ (d),\ (g),\ (h),\text{ and }(i)
\text{ are all abelian groups}.
}$$

## Exercise 2.4 {#exercise-2.4 .unnumbered}

Write down the operation tables for the following finite groups.

The operation $\oplus$ represents addition modulo $n$:
$$[a]\oplus[b]=[a+b].$$

### (a) $(\mathbb{Z}_4,\oplus)$ {#a-mathbbz_4oplus .unnumbered}

$$\mathbb{Z}_4=\{[0],[1],[2],[3]\}.$$

The operation table is $$\begin{array}{c|cccc}
\oplus &[0]&[1]&[2]&[3]\\
\hline
[0]&[0]&[1]&[2]&[3]\\
[1]&[1]&[2]&[3]&[0]\\
[2]&[2]&[3]&[0]&[1]\\
[3]&[3]&[0]&[1]&[2]
\end{array}$$

For example, $$[2]\oplus[3]=[5]=[1],$$ because $$5\equiv1\pmod4.$$

### (b) $(\mathbb{Z}_5,\oplus)$ {#b-mathbbz_5oplus .unnumbered}

$$\mathbb{Z}_5=\{[0],[1],[2],[3],[4]\}.$$

The operation table is $$\begin{array}{c|ccccc}
\oplus &[0]&[1]&[2]&[3]&[4]\\
\hline
[0]&[0]&[1]&[2]&[3]&[4]\\
[1]&[1]&[2]&[3]&[4]&[0]\\
[2]&[2]&[3]&[4]&[0]&[1]\\
[3]&[3]&[4]&[0]&[1]&[2]\\
[4]&[4]&[0]&[1]&[2]&[3]
\end{array}$$

For example, $$[3]\oplus[4]=[7]=[2],$$ because $$7\equiv2\pmod5.$$

### (c) $(\mathbb{Z}_6,\oplus)$ {#c-mathbbz_6oplus .unnumbered}

$$\mathbb{Z}_6=\{[0],[1],[2],[3],[4],[5]\}.$$

The operation table is $$\begin{array}{c|cccccc}
\oplus &[0]&[1]&[2]&[3]&[4]&[5]\\
\hline
[0]&[0]&[1]&[2]&[3]&[4]&[5]\\
[1]&[1]&[2]&[3]&[4]&[5]&[0]\\
[2]&[2]&[3]&[4]&[5]&[0]&[1]\\
[3]&[3]&[4]&[5]&[0]&[1]&[2]\\
[4]&[4]&[5]&[0]&[1]&[2]&[3]\\
[5]&[5]&[0]&[1]&[2]&[3]&[4]
\end{array}$$

For example, $$[4]\oplus[5]=[9]=[3],$$ because $$9\equiv3\pmod6.$$

The identity in each group is $$[0].$$

In $\mathbb{Z}_6$, the inverse pairs are $$[0]^{-1}=[0],
\qquad
[1]^{-1}=[5],$$ $$[2]^{-1}=[4],
\qquad
[3]^{-1}=[3].$$

## Exercise 2.5 {#exercise-2.5 .unnumbered}

Let $$S=\{a,b,c\}$$ with the binary operation defined by the table
$$\begin{array}{c|ccc}
* & a & b & c\\
\hline
a & a & b & c\\
b & b & b & c\\
c & c & c & c
\end{array}.$$

Determine whether $(S,*)$ is a group.

The element $a$ is the identity because $$a*x=x*a=x$$ for every
$x\in S$.

Indeed, $$a*a=a,\qquad a*b=b,\qquad a*c=c,$$ and
$$a*a=a,\qquad b*a=b,\qquad c*a=c.$$

However, $b$ does not have an inverse. To have an inverse, there would
need to be some $x\in S$ such that $$b*x=a.$$

But the $b$-row gives $$b*a=b,\qquad b*b=b,\qquad b*c=c.$$

None of these products equals $a$.

Likewise, $c$ has no inverse because
$$c*a=c,\qquad c*b=c,\qquad c*c=c.$$

Therefore, $$\boxed{
(S,*)\text{ is not a group because }b\text{ and }c
\text{ do not have inverses}.
}$$

## Exercise 2.7 {#exercise-2.7 .unnumbered}

Let $$S=\{a,b\}.$$

Define a binary operation $*$ on $S$ by the table $$\begin{array}{c|cc}
* & a & b\\
\hline
a & a & b\\
b & b & a
\end{array}.$$

We verify that this table defines a group.

Every output is either $a$ or $b$, so the operation is closed on $S$.

The element $a$ is the identity because $$a*a=a,\qquad a*b=b,$$ and
$$a*a=a,\qquad b*a=b.$$

Thus, $$a*x=x*a=x$$ for every $x\in S$.

Each element has an inverse: $$a*a=a,$$ so $$a^{-1}=a.$$

Also, $$b*b=a,$$ so $$b^{-1}=b.$$

This operation has the same structure as addition modulo $2$, under the
correspondence $$a\longleftrightarrow[0],
\qquad
b\longleftrightarrow[1].$$

Since addition modulo $2$ is associative, this operation is associative.

Therefore, $$\boxed{(S,*)\text{ is a group}.}$$

The table is symmetric across its main diagonal, so the operation is
commutative. Hence, $$\boxed{(S,*)\text{ is an abelian group}.}$$

## Exercise 2.10 {#exercise-2.10 .unnumbered}

Let $$G=
\left\{
\begin{pmatrix}
a&b\\
-b&a
\end{pmatrix}
\;\middle|\;
a,b\in\mathbb{R},\ a^2+b^2\neq0
\right\}.$$

Show that $G$ is a group under matrix multiplication.

### Closure {#closure .unnumbered}

Let $$A=
\begin{pmatrix}
a&b\\
-b&a
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
c&d\\
-d&c
\end{pmatrix}
\in G.$$

Then $$\begin{aligned}
AB
&=
\begin{pmatrix}
a&b\\
-b&a
\end{pmatrix}
\begin{pmatrix}
c&d\\
-d&c
\end{pmatrix}\\
&=
\begin{pmatrix}
ac-bd&ad+bc\\
-(ad+bc)&ac-bd
\end{pmatrix}.
\end{aligned}$$

This has the required form $$\begin{pmatrix}
x&y\\
-y&x
\end{pmatrix},$$ where $$x=ac-bd
\qquad\text{and}\qquad
y=ad+bc.$$

We must also verify that $x$ and $y$ are not both zero.

Observe that $$\begin{aligned}
x^2+y^2
&=(ac-bd)^2+(ad+bc)^2\\
&=a^2c^2-2abcd+b^2d^2
+a^2d^2+2abcd+b^2c^2\\
&=a^2(c^2+d^2)+b^2(c^2+d^2)\\
&=(a^2+b^2)(c^2+d^2).
\end{aligned}$$

Since $$a^2+b^2\neq0
\qquad\text{and}\qquad
c^2+d^2\neq0,$$ we have $$x^2+y^2\neq0.$$

Therefore, $$AB\in G.$$

### Associativity {#associativity .unnumbered}

Matrix multiplication is associative. Therefore, $$A(BC)=(AB)C$$ for
every $A,B,C\in G$.

### Identity {#identity .unnumbered}

The identity matrix is $$I=
\begin{pmatrix}
1&0\\
0&1
\end{pmatrix}.$$

This belongs to $G$ because it has the required form with
$$a=1,\qquad b=0,$$ and $$1^2+0^2=1\neq0.$$

Also, $$AI=IA=A$$ for every $A\in G$.

### Inverses {#inverses .unnumbered}

Let $$A=
\begin{pmatrix}
a&b\\
-b&a
\end{pmatrix}\in G.$$

Its determinant is $$\det(A)
=
a(a)-b(-b)
=
a^2+b^2.$$

Since $$a^2+b^2\neq0,$$ the inverse exists.

Using the $2\times2$ matrix inverse formula, $$A^{-1}
=
\frac{1}{a^2+b^2}
\begin{pmatrix}
a&-b\\
b&a
\end{pmatrix}.$$

Thus, $$A^{-1}
=
\begin{pmatrix}
\dfrac{a}{a^2+b^2}
&
\dfrac{-b}{a^2+b^2}\\[6pt]
\dfrac{b}{a^2+b^2}
&
\dfrac{a}{a^2+b^2}
\end{pmatrix}.$$

This has the required form $$\begin{pmatrix}
x&y\\
-y&x
\end{pmatrix},$$ where $$x=\frac{a}{a^2+b^2},
\qquad
y=\frac{-b}{a^2+b^2}.$$

Furthermore, $$\begin{aligned}
x^2+y^2
&=
\frac{a^2}{(a^2+b^2)^2}
+
\frac{b^2}{(a^2+b^2)^2}\\
&=
\frac{a^2+b^2}{(a^2+b^2)^2}\\
&=
\frac{1}{a^2+b^2}\neq0.
\end{aligned}$$

Therefore, $$A^{-1}\in G.$$

Hence, $$\boxed{G\text{ is a group under matrix multiplication}.}$$

These matrices also commute. Indeed, $$AB=
\begin{pmatrix}
ac-bd&ad+bc\\
-(ad+bc)&ac-bd
\end{pmatrix}
=
BA.$$

Therefore, $$\boxed{G\text{ is an abelian group}.}$$

## Exercise 2.11 {#exercise-2.11 .unnumbered}

Let $$G=
\left\{
\begin{pmatrix}
a&0\\
0&b
\end{pmatrix}
\;\middle|\;
a,b\in\mathbb{R},\ a\neq0,\ b\neq0
\right\}.$$

Show that $G$ is a group under matrix multiplication.

### Closure {#closure-1 .unnumbered}

Let $$A=
\begin{pmatrix}
a&0\\
0&b
\end{pmatrix},
\qquad
B=
\begin{pmatrix}
c&0\\
0&d
\end{pmatrix}
\in G.$$

Then $$AB
=
\begin{pmatrix}
a&0\\
0&b
\end{pmatrix}
\begin{pmatrix}
c&0\\
0&d
\end{pmatrix}
=
\begin{pmatrix}
ac&0\\
0&bd
\end{pmatrix}.$$

Since $$a,b,c,d\neq0,$$ we have $$ac\neq0
\qquad\text{and}\qquad
bd\neq0.$$

Therefore, $$AB\in G.$$

### Associativity {#associativity-1 .unnumbered}

Matrix multiplication is associative. Thus, $$A(BC)=(AB)C$$ for all
$A,B,C\in G$.

### Identity {#identity-1 .unnumbered}

The identity matrix is $$I=
\begin{pmatrix}
1&0\\
0&1
\end{pmatrix}.$$

Since its diagonal entries are nonzero, $$I\in G.$$

Furthermore, $$AI=IA=A$$ for every $A\in G$.

### Inverses {#inverses-1 .unnumbered}

Let $$A=
\begin{pmatrix}
a&0\\
0&b
\end{pmatrix}\in G.$$

Since $a\neq0$ and $b\neq0$, define $$A^{-1}
=
\begin{pmatrix}
\dfrac{1}{a}&0\\[4pt]
0&\dfrac{1}{b}
\end{pmatrix}.$$

This matrix belongs to $G$, and $$\begin{aligned}
AA^{-1}
&=
\begin{pmatrix}
a&0\\
0&b
\end{pmatrix}
\begin{pmatrix}
\dfrac{1}{a}&0\\[4pt]
0&\dfrac{1}{b}
\end{pmatrix}\\
&=
\begin{pmatrix}
1&0\\
0&1
\end{pmatrix}.
\end{aligned}$$

Similarly, $$A^{-1}A=I.$$

Therefore, $$\boxed{G\text{ is a group under matrix multiplication}.}$$

Since diagonal matrices of this form commute, $$AB
=
\begin{pmatrix}
ac&0\\
0&bd
\end{pmatrix}
=
\begin{pmatrix}
ca&0\\
0&db
\end{pmatrix}
=
BA.$$

Thus, $$\boxed{G\text{ is an abelian group}.}$$

# Main Ideas to Remember {#main-ideas-to-remember .unnumbered}

To prove that $(G,*)$ is a group, check $$\boxed{
\text{closure, associativity, identity, and inverses}.
}$$

To show that something is not a group, it is enough to find one group
property that fails.

$$\boxed{
\text{Once one group property fails, the structure is not a group}.
}$$

The identity depends on the operation. It is not always $0$ or $1$.

For example, under $$a*b=a+b-1,$$ the identity is $$e=1.$$

Under $$a*b=a+b-ab,$$ the identity is $$e=0.$$

To find an inverse, solve $$a*b=e$$ for the second element.

For a $2\times2$ matrix $$A=
\begin{pmatrix}
a&b\\
c&d
\end{pmatrix},$$ the inverse formula is $$\boxed{
A^{-1}
=
\frac{1}{ad-bc}
\begin{pmatrix}
d&-b\\
-c&a
\end{pmatrix}
}$$ provided that $$ad-bc\neq0.$$

For a diagonal matrix, $$A=
\begin{pmatrix}
a&0\\
0&b
\end{pmatrix},$$ the inverse is $$\boxed{
A^{-1}
=
\begin{pmatrix}
\dfrac{1}{a}&0\\[4pt]
0&\dfrac{1}{b}
\end{pmatrix}
}$$ provided that $$a\neq0
\qquad\text{and}\qquad
b\neq0.$$

# Further Background

### Relations and functions

A binary relation $R$ is a relation between two elements $x$ and $y$ such as "$x$ loves $y$" or $y = x^2$ or $x = y + 1$.

The relation $R$ determines a unique set of ordered pairs $(x, y)$ such that $x$ stands in relation $R$ to $y$.

This is written $R(x, y)$, or sometimes $x R y$, as in $x < y$ or $x = y$ (the identity relation) rather than $= (x, y)$.

One can define the binary relation $R$ as the set of all ordered pairs $(x, y)$ that stand in relation $R$.

Similar remarks apply to $n$-ary relations and $n$-tuples (p. 37).

A function $f$ of one argument is a relation such that for each $x$ there is one and only one $y$ such that $(x, y)$ stands in the relation, and this $y$ is denoted $f(x)$.

This is also obviously generalizable to $n$-ary functions and $n$-tuples.

### Mathematical Induction

(1) An inhabitant says, "This is not the first time I have said what I am now saying." Is he a knight or a knave?

A: Assuming he is a knight, he must have spoken the sentence some time in the past, and some time before that, ad infinitum, so unless he has lived for an infinitely long period of time, he would have uttered the sentence for the first time at some point, and that would have been a lie, so he must be a knave.

The *principle of mathematical induction* is that if a property $P$ holds for $0$ and if it never holds for any number $n$ without also holding for $n + 1$, then it holds for all natural numbers (p. 39).

### Complete Induction

Suppose a property $P$ is such that if $P$ holds for all natural numbers less than $n$, then $P$ also holds for $n$.

Conclusion: $P$ holds for all natural numbers.

(2) (a) Prove the principle of complete mathematical induction using the principle of mathematical induction. (b) Show that the principle of mathematical induction logically follows from the principle of complete mathematical induction.

(a) We start with the assumption that $P$ is such that if $P(n)$ for all $m < n$, then $P(n)$, and we show that $P(0)$ and also that $P(n) \implies P(n + 1)$.

There are no natural numbers less than $0$, so $P$ must hold for all natural numbers less than 0.

By the induction premise then, $P$ also holds for $0$ (written $P(0)$).

Now we consider a property $Q$ that is stronger than $P$. Symbolically, $\forall n \in \mathbb{N}, Q(n) \implies P(n)$.

Define $Q(n)$ to mean that $P$ holds for $n$ and all numbers less than $n$.

We use mathmatical induction on $Q$ (we show that $Q(0)$ and that $Q(n) \implies Q(n + 1)$).

$Q$ vacuously holds for all natural numbers less than $0$, and $P(0) \implies Q(0)$ (thus the base case holds).

Now given a number $n$ such that $Q(n)$, $P$ also holds for $n$ and all numbers less than $n$, by the definition of $Q$.

Thus, by our starting assumption about $P$, $P$ also holds for $n + 1$.

This proves $Q(0)$ and $Q(n) \implies Q(n + 1)$, and therefore by mathematical induction $Q$ holds for all natural numbers, and this fact also implies that $P$ holds for all natural numbers.

(b) We start with the assumption that $P$ is a property such that (1) $P(0)$ and (2) $\forall n, P(n) \implies P(n + 1)$, and we show that if $P$ holds for all numbers less than $n$ then it also holds for $n$.

So let us assume that $P$ holds for all numbers less than $n$.

For $n = 0$, we are already given that $P(0)$.

For $n \neq 0$, $n = m + 1$ for the number $m = n - 1$.

Since $m < n$, we know that $P$ holds for $m$, and we are given that $P(m) \implies P(m + 1)$, therefore $P$ also holds for $n$.

So if $P$ holds for all numbers less than $n$, $P$ also holds for $n$.

Thus, mathematical induction follows from complete mathematical induction, and vice versa, and the two are therefore equivalent.


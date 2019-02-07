# Beginning Propositional Logic

Propositions can be linked together to form more complex propositions by *logical connectives*.

The principle logical connectives are:

1. $\neg$ (Smullyan uses ~) - negation, not
2. $\and$ - conjunction, and
3. $\or$ - disjunction, or
4. $\to$ (Smullyan uses $\supset$) - implication, if-then
5. $\equiv$ (sometimes written $\leftrightarrow$) - equivalence, if and only if, iff

### Negation

For any proposition $p$, $\neg p$ means that $p$ is not true.

The proposition $\neg p$ is true iff $p$ is false, and is false iff $p$ is true.

| $p$  | $\neg p$ |
| ---- | -------- |
| T    | F        |
| F    | T        |

### Conjunction

For any two propositions $p$ and $q$, the proposition that $p$ and $q$ are both true is written $p \and q$.

| $p$  | $q$  | $p \and q$ |
| ---- | ---- | ---------- |
| T    | T    | T          |
| T    | F    | F          |
| F    | T    | F          |
| F    | F    | F          |

### Disjunction

For any two propositions $p$ and $q$, the proposition that at least one of $p, q$ is true is written $p \or q$.

Note that this is "or" in the inclusive sense.

| $p$  | $q$  | $p \or q$ |
| ---- | ---- | --------- |
| T    | T    | T         |
| T    | F    | T         |
| F    | T    | T         |
| F    | F    | F         |

### Implication (or Conditional)

In the statement "if $p$ then $q$" (symbolically $p \to q$), $p$ is called the *antecedent* and $q$ the *consequent*.

Such a proposition is to be regarded as false iff the antecedent is true and the consequent is false (cf. chapter 1 notes).

Symbolically, $p \to q \equiv p \and \neg q$.

| $p$  | $q$  | $p \to q$ |
| ---- | ---- | --------- |
| T    | T    | T         |
| T    | F    | F         |
| F    | T    | T         |
| F    | F    | T         |

### Equivalence (or Biconditional)

We write $p \equiv q$ to mean that either both $p$ and $q$ are true, or both are false, or in other words, each implies the other.

This is read "$p$ if and only if $q$" or "$p$ and $q$ are equivalent" (in terms of truth or falsity).

| $p$  | $q$  | $p \equiv q$ |
| ---- | ---- | ------------ |
| T    | T    | T            |
| T    | F    | F            |
| F    | T    | F            |
| F    | F    | T            |

### Exercise

Show that the set of all formulas of propositional logic is a denumerable set.

If we consider the five connectives shown above, we see that one is unary and four are binary.

Given a single proposition $p$, there are only two possible formulas, namely $p$ and $\neg p$.

With two propositions $p, q$, we can make the following formulas:

$p \and q$, $\neg p \and q$, $p \and \neg q$, $\neg p \and \neg q$

And so forth for the other three binary connectives ($4 \times 4 = 16$).

With three propositions $p, q, r$ there are now $2^3 = 8$ unary formulas, giving $4 \times 8 = 32$ binary formulas.

In order to calculate the number of ternary formulas, we must take the number of binary formulas and multiply it by the number of unary formulas (4), binary connectives (4), and possible precedences (2), so $32 \times 4 \times 4 \times 2 = 1024$.

In any case, we can see that for any finite number $n$ of propositions, there is a finite number of possible formulas.

So to enumerate the set of formulas we simply enumerate all possible formulas for $1,2,...,n$ propositions.


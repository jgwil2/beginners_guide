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

$p$, $\neg p$, $q$, $\neg q$

$p \and q$, $\neg p \and q$, $p \and \neg q$, $\neg p \and \neg q$

And so forth for the other three binary connectives ($4 + 4 \times 4 = 20$).

With three propositions $p, q, r$ there are now $2^3 = 8$ unary formulas, giving $4 \times 8 = 32$ binary formulas.

In order to calculate the number of ternary formulas, we must take the number of binary formulas and multiply it by the number of unary formulas (8), binary connectives (4), and possible precedences (2), so $32 \times 8 \times 4 \times 2 = 2048$.

So the total number of formulas for three propositions is $8 + 32 + 2048 = 2088$.

In any case, we can see that for any finite number $n$ of propositions, there is a finite number of possible formulas.

So to enumerate the set of formulas we simply enumerate all possible formulas for $1,2,...,n$ propositions.

### Compound Truth Tables

In addition to the simple truth tables given above, we can determine the truth value for any complex formula of two propositions $p$ and $q$.

For example, suppose $X$ to be the formula $p \equiv (q \or \neg (p \and q))$.

Given the truth values of $p$ and $q$, we can determine the truth values of $p \and q$, $\neg (p \and q)$, $q \or \neg (p \and q)$, and finally $p \equiv (q \or \neg (p \and q))$.

| $p$  | $q$  | $p \and q$ | $\neg (p \and q)$ | $q \or \neg (p \and q)$ | $p \equiv (q \or \neg (p \and q))$ |
| ---- | ---- | ---------- | ----------------- | ----------------------- | ---------------------------------- |
| T    | T    | T          | F                 | T                       | T                                  |
| T    | F    | F          | T                 | T                       | T                                  |
| F    | T    | F          | T                 | T                       | F                                  |
| F    | F    | F          | T                 | T                       | F                                  |

Obviously, we can construct a truth table for a formula with three propositions $p,q,r$, and then there would be eight rows ($2^3 = 8$).

In general, given $n$ propositions, there are $2^n$ cases (or *interpretations*) to consider.

### Tautologies

Consider the formula $q \or \neg (p \and q)$ in the fourth column of the table above.

We see that its value is true in all four cases; that is to say, it is true under all interpretations.

A formula is a tautology if it is true under all interpretations; it is *contradictory* if false under all interpretations.

A formula that is true under some interpretations and false under others is *contingent*, that is to say, neither a contradiction nor a tautology.

1. Which of the following are tautologies, contradictions, and contingent?

   a. $(p \to q) \to (q \to p)$

   | $p$  | $q$  | $p \to q$ | $q \to p$ | $(p \to q) \to (q \to p)$ |
   | ---- | ---- | --------- | --------- | ------------------------- |
   | T    | T    | T         | T         | T                         |
   | T    | F    | F         | T         | T                         |
   | F    | T    | T         | F         | F                         |
   | F    | F    | T         | T         | T                         |

   Contingent.

   b. $(p \to q) \to (\neg p \to \neg q)$

   | $p$  | $q$  | $p \to q$ | $\neg p \to \neg q$ | $(p \to q) \to (\neg p \to \neg q)$ |
   | ---- | ---- | --------- | ------------------- | ----------------------------------- |
   | T    | T    | T         | T                   | T                                   |
   | T    | F    | F         | T                   | T                                   |
   | F    | T    | T         | F                   | F                                   |
   | F    | F    | T         | T                   | T                                   |

   Contingent, equivalent to (a).

   c. $(p \to q) \to (\neg q \to \neg p)$

   | $p$  | $q$  | $p \to q$ | $\neg q \to \neg p$ | $(p \to q) \to (\neg q \to \neg p)$ |
   | ---- | ---- | --------- | ------------------- | ----------------------------------- |
   | T    | T    | T         | T                   | T                                   |
   | T    | F    | F         | F                   | T                                   |
   | F    | T    | T         | T                   | T                                   |
   | F    | F    | T         | T                   | T                                   |

   Tautology.

   d. $p \to \neg p$

   | $p$  | $\neg p$ | $p \to \neg p$ |
   | ---- | -------- | -------------- |
   | T    | F        | F              |
   | F    | T        | T              |

   Contingent, equivalent to $\neg p$.

   e. $p \equiv \neg p$

   | $p$  | $\neg p$ | $p \equiv \neg p$ |
   | ---- | -------- | ----------------- |
   | T    | F        | F                 |
   | F    | T        | F                 |

   Contradiction.

   f. $(p \equiv q) \equiv (\neg p \equiv \neg q)$

   | $p$  | $q$  | $p \equiv q$ | $\neg p \equiv \neg q$ | $(p \equiv q) \equiv (\neg p \equiv \neg q)$ |
   | ---- | ---- | ------------ | ---------------------- | -------------------------------------------- |
   | T    | T    | T            | T                      | T                                            |
   | T    | F    | F            | F                      | T                                            |
   | F    | T    | F            | F                      | T                                            |
   | F    | F    | T            | T                      | T                                            |

   Tautology.

   g. $\neg (p \and q) \equiv (\neg p \and \neg q)$

   | $p$  | $q$  | $\neg(p \and q)$ | $\neg p \and \neg q$ | $\neg (p \and q) \equiv (\neg p \and \neg q)$ |
   | ---- | ---- | ---------------- | -------------------- | --------------------------------------------- |
   | T    | T    | F                | F                    | T                                             |
   | T    | F    | T                | F                    | F                                             |
   | F    | T    | T                | F                    | F                                             |
   | F    | F    | T                | T                    | T                                             |

   Contingent, equivalent to $\equiv$.

   h. $\neg (p \and q) \equiv (\neg p \or \neg q)$

   | $p$  | $q$  | $\neg (p \and q)$ | $\neg p \or \neg q$ | $\neg (p \and q) \equiv (\neg p \or \neg q)$ |
   | ---- | ---- | ----------------- | ------------------- | -------------------------------------------- |
   | T    | T    | F                 | F                   | T                                            |
   | T    | F    | T                 | T                   | T                                            |
   | F    | T    | T                 | T                   | T                                            |
   | F    | F    | T                 | T                   | T                                            |

   Tautology (cf. De Morgan's laws).

   i. $(\neg p \or \neg q) \equiv \neg (p \or q)$

   | $p$  | $q$  | $\neg p \or \neg q$ | $\neg (p \or q)$ | $(\neg p \or \neg q) \equiv \neg (p \or q)$ |
   | ---- | ---- | ------------------- | ---------------- | ------------------------------------------- |
   | T    | T    | F                   | F                | T                                           |
   | T    | F    | T                   | F                | F                                           |
   | F    | T    | T                   | F                | F                                           |
   | F    | F    | T                   | T                | T                                           |

   Contingent, equivalent to $\equiv$ and (g).

   j. $(\neg p \or \neg q) \equiv \neg (p \and q)$

   | $p$  | $q$  | $\neg p \or \neg q$ | $\neg (p \and q)$ | $(\neg p \or \neg q) \equiv \neg (p \or q)$ |
   | ---- | ---- | ------------------- | ----------------- | ------------------------------------------- |
   | T    | T    | F                   | F                 | T                                           |
   | T    | F    | T                   | T                 | T                                           |
   | F    | T    | T                   | T                 | T                                           |
   | F    | F    | T                   | T                 | T                                           |

   Tautology (cf. De Morgan's laws).

   k. $(p \equiv (p \and q)) \equiv (q \equiv (p \or q))$

   | $p \and q$ | $p \or q$ | $p \equiv p \and q$ | $q \equiv p \or q$ | $(p \equiv (p \and q)) \equiv (q \equiv (p \or q))$ |
   | ---------- | --------- | ------------------- | ------------------ | --------------------------------------------------- |
   | T          | T         | T                   | T                  | T                                                   |
   | F          | T         | F                   | F                  | T                                                   |
   | F          | T         | T                   | T                  | T                                                   |
   | F          | F         | F                   | F                  | T                                                   |

   Tautology.

2. What method can be used to find a formula to match an arbitrary truth table?

   | $p$  | $q$  | $r$  | $X$  |
   | ---- | ---- | ---- | ---- |
   | T    | T    | T    | T    |
   | T    | T    | F    | F    |
   | T    | F    | T    | T    |
   | F    | T    | T    | F    |
   | T    | F    | F    | T    |
   | F    | T    | F    | F    |
   | F    | F    | T    | F    |
   | F    | F    | F    | F    |

   Every row of the table has a value of either true or false; let's consider only those whose value is true.

   For each such row, write each proposition (or its negation) and connect them with $\and$, creating a formula whose truth value will match that of the table for that row.

   For the above table we get the following formulas, $p \and q \and r$, $p \and q \and \neg r$, $p \and \neg q \and \neg r$.

   Then, since we want a formula that is true iff one of the resulting formulas are true, we simply combine them with $\or$.

   For this table, that gives us $(p \and q \and r) \or (p \and q \and \neg r) \or (p \and \neg q \and \neg r)$.

   ### Propositional Constants

   Formulas may include the symbols $t$ and $f$, whose values are always true and false respectively.

   Any formula involving $t$ or $f$ is equivalent to a formula involving no constants, or $t$ alone, or $f$ alone.

3. Reduce the following formulas either to a formula with no constants, or $t$, or $f$.

   a. $((t \to p) \and (q \or f)) \to ((q \to f) \or (r \and t))$

   $(p \and q) \to (\neg q \or r)$

   b. $(p \or t) \to q$

   $t \to q$

   $q$

   c. $\neg (p \or t) \equiv (f \to q)$

   $\neg t \equiv t$

   $f \equiv t$

   $f$

4. Knights and Knaves

   a. If A says, "Both of us are knaves," then he is saying that he is a liar, which is a contradiction.

   But his statement is still false if B is a knight, since only one of the two conditions need be false in order for the statement to be false.

   Therefore, A is a knave and B is a knight

   b. If A says, "At least one of us is a knave," then A must be a knight and B a knave.

   If A is a knave, then he would have made a true statement, which is a contradiction.

   So A must be a knight, and since his statement is true, B must be a knave.

   c. A says, "B and I are of the same type, either both knights or both knaves."

   If A is a knight, then B also has to be a knight, since A's statement is true.

   If A is a knave, then they cannot both be of the same type, so B must be a knight.

   Hence, B must be a knight, but we cannot determine A's type.

5. $p \or q \iff \neg (\neg p \and \neg q)$

6. $p \and q \iff \neg (\neg p \or \neg q)$

7. $p \to q \iff \neg(p \and \neg q)$

8. $p \to q \iff \neg p \or q$

9. $p \and q \iff \neg (p \to \neg q)$

10. $p \or q \iff \neg p \to q$

11. $p \or q \iff (p \to q) \to q$

12. $p \equiv q \iff (p \to q) \and (q \to p)$

13. $p \equiv q \iff (p \and q) \or \neg (p \or q)$

14. $\neg p \iff p \to f$

    # Joint Denial

    We show above that all five logical connectives can be defined in terms of $\neg,\and$, or $\neg,\or$, or $\neg,\to$, or $\to,f$.

    There is a single connective, *joint denial*, that can define all other connectives.

    Joint denial means, "Both $p$ and $q$ are false," or symbolically, $p \downarrow q$ (cf. NOR).

    | $p$  | $q$  | $p \downarrow q$ |
    | ---- | ---- | ---------------- |
    | T    | T    | F                |
    | T    | F    | F                |
    | F    | T    | F                |
    | F    | F    | T                |

15. $\neg p \iff p \downarrow p$

    $\neg (p \downarrow q) \iff p \or q$

    By problem 6, $\and$ can be derived from $\or$ and $\neg$, and by problem 2 any truth table can be derived from $\and, \or, \neg$.

    ### Alternative Denial

    There is another single connective from which all others can be derived.

    Alternative denial means, "At least one of $p,q$ is false," and is written $p \mid q$ or $p \uparrow q$.

    Also called Sheffer stroke (cf. NAND).

    | $p$  | $q$  | $p \uparrow q$ |
    | ---- | ---- | -------------- |
    | T    | T    | F              |
    | T    | F    | T              |
    | F    | T    | T              |
    | F    | F    | T              |

16. $\neg p \iff p \uparrow p$

    (Incidentally, $p \uparrow p \iff p \downarrow p \iff \neg p$)

    $\neg (p \uparrow q) \iff p \and q$

    By problem 5, $\or$ can be derived from $\neg$ and $\and$, and by problem 2 any truth table can be derived from $\and, \or, \neg$.

17. "If I am a knight, then there is gold here."

    The only way for a statement of implication to fail to be true is if the antecedent is true and the consequent is false.

    In this case, then, the statement, "I am a knight" would have to be true.

    But this would be a contradiction, since a knight cannot make a false statement.

    Therefore, the implication must be true, and since it is true, the antecedent (that the speaker is a knight) also must be true (since only a knight makes true statements), and therefore the consequent, that there must be gold here, also follows.

18. $p \and q \iff (p \to q) \equiv p$

    This relates to 19 because in 19, we take the proposition $p \to q$ (if I am a knight, there is gold), and make it's truth value equivalent to that of $p$ (since only knights can make true statements).

    As we saw above, the statement was true, and its being true implied that both the antecedent and the precedent were true.

    If either the antecedent, the precedent, or both had been false, the entire equivalence would have been false.

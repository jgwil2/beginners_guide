# Some Problems Arise

### Russell Paradox

Call a set *ordinary* if it does not contain itself, and extraordinary if it does contain itself.

Whether or not extraordinary sets exist, ordinary sets certainly do.

Consider the set $M$ of all ordinary sets; is $M$ ordinary or not?

If $M$ is ordinary, then it does not contain itself, but then it is not the set of all ordinary sets, so it cannot be ordinary.

On the other hand, if $M$ is extraordinary, then it does contain itself, and thus is not the set of all ordinary sets.

This is illustrated by the barber paradox: a barber shaves all men in town who do not shave themselves; does he shave himself?

(p. 29)

1. The barber does not exist.

2. Berry Paradox: "The smallest number not describable in less than eleven words."

   Solution: the word "describable" is not well-defined.

   ### Well-defined

   In mathematics, an expression is called *well-defined* or *unambiguous* if its definition assigns it a unique interpretation (cf. [Wikipedia](https://en.wikipedia.org/wiki/Well-defined)).

3. Because the description gives contradictory information, it cannot be considered well-defined. Since it is not genuine, it is considered a *pseudo-description*.

   ### Hypergame

   Call a game *normal* if it must terminate in some finite number $n$ moves, such as tic-tac-toe or chess under tournament rules.

   Hypergame is a game in which the player makes the first move by choosing any normal game to be played, and then that game continues on normally.

   Now the paradox is: is hypergame normal?

   It must be normal, because a normal game terminates after $n$ moves, so hypergame must terminate after $n + 1$ moves.

   But if it is normal, then each player can continue choosing it, resulting in a game that never ends.

4. Given the contradiction, hypergame must not be well-defined.

   Hypergame can be well-defined for a set of normal games, but not if that set contains hypergame.

   ### Proof of Cantor's Theorem via Hypergame

   Cantor's Theorem recap: for any set $A$, the power set $\mathcal{P}(A)$ is numerically greater than $A$.

   Proof: for all members $x \in A$, there exists a function $f$ such that $f(x) = y \in \mathcal{P}(A)$.

   But there is at least one set, the set $B = \{x \in A | x \notin f(x)\}$, for which there can be no $x$ such that $f(x) = x$.

   Zwicker shows the existence of an entirely different set for which there can be no $x$ such that $f(x) = x$.

   By a path we mean any finite or infinite sequence constructed as follows: for any element $x \in A$ we go to $S_x$.

   If $S_x$ is empty, the path ends; otherwise, we choose some element $y \in S_x$ and go to $S_y$.

   Every path must either hit the empty set and terminate or be infinite.

   An element $x$ is called *normal* if all paths starting at $x$ are finite.

   Zwicker proved that the set $M$ of all *normal* elements of $A$ cannot be $S_x$ for any $x$.

   (pp. 30-31)

5. Q: Prove this.

   A: Suppose that $S_x = M$.

   Then every element in $S_x$ must terminate; additionally, no elements outside of $S_x$ may terminate.

   But is $x$ then a member of $S_x$?

   If it isn't, then there is at least one element $x \notin M$ that terminates, which is a contradiction.

   If $x \in S_x$, then we can create an infinite path from $x$ to $S_x$, then choosing $x$ again which again leads to $S_x$ (as in the hypergame paradox), so there is an infinite path in $M$, which is also a contradiction.

   Therefore there can be no $x$ such that $S_x = M$.

   Note: why can $M$ not be empty and why does this matter?

6. The notion of a genuine description is not well-defined.

   ### Zermelo set theory

   Frege's work in set theory included an axiom called the *abstraction principle*, which states that given any property, there exists the set of all things having that property (p. 33).

   But this axiom leads to Russell's paradox, so it needs some modification.

   Zermelo replaced this axiom with the *limited abstraction principle*:

   $Z_0$: [*limited abstraction principle*] For any property $P$ and any set $S$, there exists the the set of all elements of $S$ having property $P$.

   $Z_1$: [*existence of empty set*] There exists a set containing no elements at all.

7. Q: If Zermelo had taken as an axiom, "There exists a set," instead of $Z_1$, the existence of the empty set would still follow. Why?

   A: If there exists a set $S$, then by $Z_0$ there exists the set of all elements of $S$ having property $P$.

   Now take $P$ to be a property that no element can have, like $x \neq x$.

   There must exist the set of all elements of $S$ having property $P$ and that is the empty set.

   $Z_2$: [*pairing principle*] For any pair of sets $x$ and $y$, there is a set that contains both $x$ and $y$.

8. Q: Prove that for any sets $x$ and $y$ there is a set whose elements are just $x$ and $y$.

   A: By $Z_2$ there exists a set containing both $x$ and $y$.

   Call $S$ the set containing $x$ and $y$; call $P$ the property of being equal to $x$ or equal to $y$.

   By $Z_0$ there must be a set containing all the sets of $S$ having property $P$; that set is $\{x, y\}$.

9. Q: Prove that for any set $x$ there is a set $\{x\}$ containing only $x$ [such a set is called a *singleton*].

   A: By $Z_2$ there exists a set $S$ containing $x$ and the empty set, denoted $S = \{\{\}, x\}$.

   Let $P$ be the property of having members (being non-empty).

   By $Z_0$ there must be a set $S_0$ for $P$ and $S$, and that set is $\{x\}$.
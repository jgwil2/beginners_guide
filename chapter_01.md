# Genesis

## Problems

1. Q: Is there a difference between the statements "Cheap food isn't good. Good food isn't cheap?"

    A: Both statements say the same thing, namely, that there is no food that is both cheap and good.

    Statements of the form "if *p*, then *q*" or "*p* implies *q*" (symbolically written *p* ⊃ *q* or *p* ⟶ *q*) are to be regarded as false only if *p* is true and *q* is false.
    This is called *material implication* and has the curious property that a false proposition implies any proposition (p. 9).

    Truth table for material implication:
    | *p* | *q* | *p* ⊃ *q* |
    |-----|-----|-----------|
    |  T  |  T  |     T     |
    |  T  |  F  |     F     |
    |  F  |  T  |     T     |
    |  F  |  F  |     T     |

    (p. 63)

2. Q: Is the empty set a subset of every set?

    A: Yes, the empty set is a subset of every set.
    "The only way that set A can fail to be a subset of set B is when A contains at least one element that is not in B." (p. 8)
    Since the empty set contains no elements, it cannot possibly contain an element that is not in any other set.

3. Q: Which, if any, of the following statements is true:
    1. If $A \cup B = B$, then $B \subseteq A$.

    2. If $A \cup B = B$, then $A \subseteq B$.

        If $A \cup B = B$, then A does not contain any elements that are not in B.

        Therefore A is a subset of B.

        But the reverse is not necessarily the case, because if B contained an element $x \notin A$, then the proposition $A \cup B = B$  would still hold.

        Therefore statement 1 is false and statement 2 is true.

    3. If $A \subseteq B$, then $A \cup B = B$.

    4. If $A \subseteq B$, then $A \cup B = A$.

        If $A \subseteq B$, then B contains all elements that are members of A.
        Therefore $A \cup B = B$ holds.
        However, $A \cup B = A$ does not necessarily hold, because B may contain some element $x \notin A$.
        Therefore, statement 3 is true and statement 4 is false.

    A: Statements 2 and 3 are true.

4. Q: Which of the following statements are true:
    1. If $A \cap B = B$, then $B \subseteq A$.

    2. If $A \cap B = B$, then $A \subseteq B$.

      If $A \cap B = B$, then A must contain all elements in B.
      Therefore B must be a subset of A.
      But A may contain elements not in B, which would be excluded from the intersection.
      Therefore A ⊆ B does not necessarily hold.
      So statement 1 is true and statement 2 is false.

    3. If $A \subseteq B$, then $A \cap B = B$.

    4. If $A \subseteq B$, then $A \cap B = A$.

      If $A \subseteq B$, then $A \cap B$ would remove all elements $x \in B, x \notin A$, and contain all members of A, so $A \cap B = A$ would hold.
      But if $A \subseteq B$, then B may contain elements not in A, and these elements would not exist in $A \cap B$, so $A \cap B = B$ would not necessarily hold.
      Therefore statement 3 is false and statement 4 is true.

    A: Statements 1 and 4 are true.

5. Q: If $A \cap B = A \cup B$, does it follow that $A = B$?

    Assume that $A \neq B$.
    Then there is at least one element $x \in A, x \notin B$ or one element $x \in B, x \notin A$.
    Let us take the first example $x \in A, x \notin B$.
    Since $x \in A$, it is also the case that $x \in A \cup B$ but since $x \notin B$, it is also the case that $x \notin A \cap B$.
    Therefore, $A \cap B \neq A \cup B$.

    So if $A \cap B = A \cup B$, then it must be the case that $A = B$.

6. Q: Which, if either, of the following statements is true:

    1. If $A \subseteq B$ then $A' \subseteq B'$.
    2. If $A \subseteq B$ then $B' \subseteq A'$.

    If $A \subseteq B$ then $\forall x \in A, x \in B$.

    Also, $\forall x \notin A, x \notin B$ and, $\forall x \notin A, x \in A'$.

    In order for statement 1 to be true, it must be the case that there is no element $x \in A', x \notin B'$.

    But there can be such an element, because $A \subseteq B$, so there can be an element $x \notin A, x \in B$.

    If $x \notin A$ then by definition $x \in A'$, and if $x \in B$ then by definition $x \notin B'$.

    Therefore statement 1 is false.

    In order for statement 2 to be true, it must be the case that there is no element $x \in B', x \notin A'$.

    If there is such an element, then also $x \notin B, x \in A$.

    But we are given that $A \subseteq B$, so such an element cannot exist.

    Therefore statement 2 is true.

### Exercises


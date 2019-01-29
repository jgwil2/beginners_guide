Consier a book with denumerably many pages (i.e the pages can be numbered $1, 2, ..., n$).

Each page contains a (possibly infinite) a subset of positive integers (list of numbers $1, 2, ..., n$).

Call a number $x$ selfish if page $x$ contains the number $x$ in its list.

Call a number $x$ unselfish if page $x$ does not contain the number $x$ in its list.

Call the set of all unselfish numbers $U$.

We will show that there cannot be a number $x$ such that page $x$ contains the set $U$.

Therefore the set of natural numbers is numerically smaller (has a lower cardinality) than its power set (the set of all possible subsets of natural numbers).

Consider a page $x$ such that the list of numbers on page $x$ ($p(x)$) is equal to $U$ (the set of all unselfish numbers).

Either $x \in U$ or $x \notin U$.

If $x \in U$, then $x$ is selfish, by the definition of selfish numbers, in which case $U$ would not be the set of all unselfish numbers.

Therefore it cannot possibly be the case that $x \in U$.

On the other hand, if $x \notin U$, then $x$ is an unselfish number, by the definition of unselfish numbers, and so $U$ is also not the set of all unselfish numbers.

Therefore it cannot possibly be the case that $x \notin U$.

Since both possibilities (either $x \in U$ or $x \notin U$) lead to contradictions, the only possible conclusion is that there is no page $x$ on which set $U$ can be listed (there is no $x$ such that $p(x) = U$).
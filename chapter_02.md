# Infinite Sets

## Problems

1. A set containing three elements $S = \{1, 2, 3\}$ has $8 = 2^3$ subsets: $\{\}, \{1\}, \{2\}, \{3\}, \{1, 2\}, \{1, 3\}, \{2, 3\}, \{1, 2, 3\}$.

  Observe that adjoining one element $S \cup \{x\}$ will double the number of subsets, because we can make a new subset by adjoining $x$ to each of the previously existing subsets.

  Therefore, in general, a set of $n$ elements has $2^n$ subsets.

  Note that the empty set has only one subset, itself ($2^0 = 1$).

  ### Denumerable Sets

  A set is called *denumerable* or *denumerably infinite* if it can be put into a 1-1 correspondence with the set of positive integers, or the set of natural numbers (which are the same thing because they can be put into a 1-1 correspondence with one another).

  A 1-1 correspondance between a set A and the set of positive integers is called an *enumeration* of A.

  Cantor's question was whether every infinite set is also denumerable, or if there are different sizes of infinite sets.

  (N.B. There is a sense in which the set of natural numbers is greater than the set of positive integers, and that is because the positive integers form a *proper subset* of the natural numbers, but numerically, they are the same size).

  (p. 19)

2. You can alternate between guessing positive and negative numbers ($1, -1, 2, -2,..., n, -n$).

3. You should guess 1, 1, then 2, 1, then 1, 2, then 2, 2, then 3, 1; 1, 3; 3, 2; 2, 3; 3, 3.

  So for a number *n* you can guess all of the possible pairs of elements of the set $\{0,1,...,n\}$.

4. Similar to above, a fraction can be considered an ordered pair.

  So for any positive integer $n$ we would guess the sequence $\frac{n}{1},\frac{n}{2},...,\frac{n}{n},\frac{n - 1}{n},...,\frac{2}{n},\frac{1}{n}$.

5. We have seen that any finite set of $n$ integers has a finite number, $2^n$, of subsets (problem 1).

  So we simply go through the positive integers and list all subsets whose highest number is 1, then 2, etc.

  ### Cantor's Discovery

  The above solution shows that the set of all finite sets of integers is denumerable.

  But what about the set of *all* sets of integers, finite or infinite?

  Imagine a book with denumerably many pages, each of which contains a description of a set of natural numbers.

  (p. 21)

6. A number $n$ is *extraordinary* if the set described on page $n$ contains $n$.

  It is *ordinary* if the set described on page $n$ does not contain $n$.

  Can the set of all ordinary numbers be described in the book? Of extraordinary numbers?

  Let us assume that page $n$ contains a description of the set of all ordinary numbers.

  Because this is the set of ordinary numbers, $n$ cannot be described in the set.

  But if $n$ is not described on page $n$, it must not be a member of the set of ordinary numbers, and so must be extraordinary.

  But in order for $n$ to be extraordinary, then it would have to be described on page $n$, which cannot be because page $n$ describes the set of ordinary numbers.

  This contradiction shows that it is not possible for the set of all ordinary numbers to be described in the book.

  Therefore there is at least one set that cannot be placed into a 1-1 correspondence with the natural numbers, so the set of all sets of integers is not denumerable.

  ### Power Set

  For any set $A$, the set of all subsets of $A$ is called the *power set*, written $\mathcal{P}(A)$. The above result shows that $\mathbb{N}$ cannot be put into a 1-1 correspondence with $\mathcal{P}(\mathbb{N})$.

7. Why is it true that $\mathbb{N}$ can be put into a 1-1 correspondence with $\mathcal{P}(\mathbb{N})$?

  We have already shown that set $\mathcal{F}$, the set of all finite sets of $\mathbb{N}$ is denumerable (problem 5) and that is obviously a subset of the power set, which is the set of all sets both finite and infinite.

  ### Cantor's Theorem

  For any set $A$, the power set $\mathcal{P}(A)$ is numerically larger than $A$.

8. Prove Cantor's Theorem:

  In plain English, replace the notion of pages with a generalized mapping from some member of $A$ to some set $S$ which is a member $\mathcal{P}(A)$, or in other words to some subset of $A$, since $\mathcal{P}(A)$ is the set of all subsets of $A$.

  Call element $a$ extraordinary if $S$ contains $a$ and call $a$ ordinary if it does not.

  Let us consider the set $O$ of all ordinary elements.

  If $o$ maps to $O$, then $o$ cannot be a member of $O$, because if it were, then it would be extraordinary, and we are given that $O$ contains only ordinary elements.

  But then $O$ would not be the set of all ordinary elements, because it would have not have included $o$, which is by definition ordinary, since it maps to $O$ and is not a member of $O$.

  Therefore, there is at least one set, $O$, that cannot be mapped from $A$ to $\mathcal{P}(A)​$.

  In mathematical terms, assume every member of $A$ can be mapped to some set $S \in \mathcal{P}(A)$.

  We call this mapping $f$, so that $\forall x \in A, f(x) = S_x \in \mathcal{P}(A)$.

  Cantor's theorem holds that the function $f : A \to \mathcal{P}(A)$ is not *surjective*.

  Surjective means that, given a mapping from $X$ to $Y$, for every $y \in Y$ there is an $x \in X$ such that $f(x) = y$.

  Symbolically, if $f : X \to Y$, then $f$ is said to be surjective if $\forall y \in Y, \exist x \in X, f(x) = y$. ([Wikipedia](https://en.wikipedia.org/wiki/Surjective_function#Definition))

  In order for $f : X \to Y$ to fail to be surjective, there must be at least one value $y \in Y$ for which there is no $x \in X$ such that $f(x) = y$.

  Let $f$ be a map from $A$ to $\mathcal{P}({A})$.

  Let us define $B = \{x \in A | x \notin f(x)\}$.

  This can be read as, "For all $x$ in $A$, $x \in B$ if and only if $x \notin f(x)$."

  This is a formal definition of our set of "ordinary" elements above; $x$ is a member of $B$ iff it is not a member of the set it maps to, i.e. $f(x)$.

  Therefore, $\forall x, f(x) \neq B$, because $B$ excludes any $x \in f(x)$, and since $B \in \mathcal{P}(A)$ (by virtue of being constructed from elements of $A$, this shows that $f : A \to B$ is not surjective.

  > More specifically, consider any $x \in A$, then either $x \in f(x)$ or $x \notin f(x)$. In the former case, $f(x)$ cannot equal $B$ because $x \in f(x)$ by assumption, and $x \notin B$ by the construction of $B$. In the latter case, $f(x)$ cannot equal $B$ because $x \notin f(x)$ by assumption, and $x \in B$ by the construction of $B$.
  >
  > ...More formally, we just proved that the existence of $\xi \in A$ such that $f(\xi) = B$ implies the following contradiction:
  >$$
\begin{align*}
\xi \in f(\xi) \iff \xi \in B \quad\quad& \text{(by assumption that } f(\xi) = B \text{);}\\
\xi \in B \iff \xi \notin f(\xi) \quad\quad& \text{(by definition of } B \text{).}
\end{align*}
$$
  >
  > Therefore, by reductio ad absurdum, the assumption must be false

  ([Wikipedia](https://en.wikipedia.org/wiki/Cantor%27s_theorem#Proof))

  Note: the above represents the bulk of the proof, but omits the definition of cardinality:

  "By definition of cardinality, we have card(*X*) < card(*Y*) for any two sets *X* and *Y* if and only if there is an [injective function](https://en.wikipedia.org/wiki/Injective_function) but no [bijective function](https://en.wikipedia.org/wiki/Bijective_Function) from *X* to *Y*. It suffices to show that there is no surjection from *X* to *Y*." (idem)

  Smullyan does not cover this aspect of the proof in detail.

9. The union of two denumerable sets is necessarily denumerable, because we could simply alternate between the enumerations of each set in order to put the union into a 1-1 correspondence with the positive integers.

10. The set of all infinite sets of natural numbers cannot be denumerable.

  We know from problem 5 that the set of all finite sets of natural numbers is denumerable, and from problem 9 that the union of two denumerable sets is also denumerable.

  Now, in problem 6 we showed that the set of all finite and infinite sets of natural numbers is not denumerable.

  But if the set of all infinite sets of natural numbers were denumerable, the union of it and the set of all finite sets of natural numbers (the power set) would have to also be denumerable, which has been shown not to be the case.

  Therefore, the set of all infinite sets of natural numbers is not denumerable.

11. Q: Consider a denumerable sequence $D_1,D_2,..,D_n$, of denumerable sets and let $S$ be their union; that is the set of all elements $x$ which belong to at least one of $D_1,D_2,..,D_n$. Is $S$ denumerable?

   A: Yes, because the union of any two denumerable sets is denumerable.

12. Q: Given a denumerable set $D$, is the set of all *finite sequences* of elements of $D$ a denumerable set?

   A: How could we put all finite sequences of elements of $D$ into a 1-1 correspondence with $\mathcal{P}(\mathbb{N})$?

   Conversely, how could we enumerate the set of all finite sequences of elements of $D$?

   Given a finite subset $S$ of $D$, it seems that there are infinite possible finite sequences of elements of $S$, so it would seem we cannot enumerate.

   On the other hand, it seems impossible to create a unique, finite sequence of elements of $D$ to correspond to an infinite subset of $\mathbb{N}$.

   From Smullyan: Let $k$ be the length of a sequence and $n$ be the number of elements in that sequence.

   Let $D_k$ be the set of all sequences of length $k$.

   Let $(D_k)_n$ be the set of sequences of length $k$, drawing from the subset of $D$ composed of the first $n$ elements in an enumeration of $D$: $\{D_1,...,D_n\}$.

   Now, $(D_k)_1$ is finite, since there can only be one sequence which only $D_1$, namely, the sequence $(D_1)$.

   $(D_k)_2$ is also finite; if the length of sequences is 1, then $(D_1)_2 = \{(D_1),(D_2)\}$; for a length of 2, then $(D_2)_2 = \{(D_1, D_1) (D_1, D_2),(D_2, D_1), (D_2, D_2)\}$; in general, the size of the set $(D_k)_n$ equals $n^k$.

   We have now shown that we can enumerate $D_k$ for any value of $k$ by first enumerating $(D_k)_1$, then $(D_k)_2$, etc.

   Since each of the sets $D_1,...,D_k$ is denumerable, their union is also denumerable (problem 9).

13. Q: Consider the set of all *infinite sequences* of 1's and 0's. Prove that it is the same size as $\mathcal{P}(\mathbb{N})$.

   A: It has already been shown that the set of all infinite sets of $\mathbb{N}$ is not denumerable (problem 10).

   Take any infinite subset of $\mathbb{N}$; we can create a corresponding infinite sequence of 0's and 1's by concatenating the binary representation of the elements of the subset (e.g. $S = \{1,2,3,...\}$ could be represented as $11011...$).

   Edit: Obviously, there is a problem with this method of deriving unique sequences from sets, since $11011...$ could also represent the set $S = \{27,...\}$. Uniqueness is crucial the proof, as it shows that the correspondence is 1-1. But as Smullyan shows, there is at least one method of deriving unique sequences from sets, so the proof holds (p. 27).

   So the subsets of $\mathbb{N}$ can be put into a 1-1 correspondence with sequences of 0's and 1's.

   Therefore, the set of all infinite sequences of 1's and 0's is the same size as the set of all subsets of $\mathbb{N}$, i.e. $\mathcal{P}(\mathbb{N})$.

14. Q: Prove that every infinite set must have a denumerable subset.

    A: We can remove an element $x$ from an infinite set $S$, and $S - \{x\}$ will obviously still be infinite.

    So if we remove $x_1$ from $S$, we can then remove $x_2$, and so forth, generating a denumerable sequence $x_1,...,x_n$ of elements of $S$.

15. Q: Prove that every infinite set, even a non-denumerable one, can be put into a 1-1 correspondence with a proper subset of itself.

    A: We can put $S$ into a 1-1 correspondence with its infinite (problem 15) subset $S - \{x\}$ by pairing $x_1$ with $x_2$, $x_2$ with $x_3$, and so forth.

    [This needs further elaboration]

16. We can marry every unloved man to his lover, and every unloved woman to her lover.

    Therefore every unloved man and every unloved woman is now married.

    All other members are therefore loved, so we can simply marry them to their lovers.

    [Why is this insufficient?]

    ###Bernstein-Schroeder Theorem

    For any pair of infinite sets $A$ and $B$, if $A$ can be put into a 1-1 correspondence with a subset of $B$, and $B$ can be put into a 1-1 correspondence with a subset of $A$, then the whole of $A$ can be put into a 1-1 correspondence with the whole of $B$ (p. 24).

17. Q: Suppose $A$ is an infinite set of the same size as a subset of $B$, where $B$ is a subset of $A$. Are $A$ and $B$ necessarily of the same size?

    A: We are given that $C \subseteq B \subseteq A$ and $card(A) = card(C)$.

    Thus, $A$ can be put into a 1-1 correspondence with a subset of $B$ (namely $C$)

    Also, we know that $B$ can be put into a 1-1 correspondence with a subset of $A$ (problem 15).

    Therefore, by the Bernstein-Schroeder Theorem, $card(A) = card(B)$.

##Exercises

- Prove that if $D$ is a denumerable set, then any infinite subset of $D$ must also be a denumerable set.

  By problem 15, we know that any infinite set can be put into a 1-1 correspondence with a proper subset of itself.

  We are given that $D$ is denumerable, and therefore any set with which it can be put into a 1-1 correspondence is also denumerable.
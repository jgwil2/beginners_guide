# Beginning First-Order Logic

First-order logic deals with the connectives of propositional logic, along with the notions of *all* and *some*. Here *some* has the plain English meaning of "at least one."

1. Q: Each person on the island of knights and knaves says, "Every one of us here is of the same type."

   A: Since each individual said the same thing, they must be of the same type. Suppose they are all knaves. Then they would be telling the truth, which would be a contradiction, so they must be all knights.

2. Q: Each person says, "Some of us are knights and some of us are knaves."

   A: Again, they are all of the same type. The statement is therefore false, so they all must be knaves.

3. Q: Each person says, "Everyone here who is a knight smokes." What can we tell about truth-telling and smoking?

   A: Assume this statement is false. That means there must be at least one knight here who does not smoke. But if the statement is false, then every inhabitant must be a knave, which contradicts the previous conclusion. Therefore, all the inhabitants are knights and they all smoke.

4. Q: Each person says, "Some of us here are knaves and smoke." What can be deduced?

   A: All inhabitants are of the same type. Assume they are all knights. Then the statement that there exist some knaves among them would be false, which is a contradiction. Therefore they are all knaves. Furthermore, none of them smoke, because if any of them did smoke, then the statement would be true, which is a contradiction.

5. Q: All inhabitants are of the same type, and each says, "If I smoke, then everyone here smokes."

   A: In order for this statement to be false, the speaker must smoke, and there must be at least one person who does not smoke. But it cannot be true that each inhabitant smokes *and also* at least one does not smoke. Therefore the statement must be true, and all inhabitants of the island are knights who either smoke or do not smoke.

6. Q: Again, all inhabitants are of the same type. Each says, "If any one of us here smokes, then I smoke."

   A: In order for the statement to be false, then at least one person must smoke, and the speaker must not smoke. But again, it is not possible that each speaker not smoke, but at least one of them smoke. So the statement is true and either they all smoke or none do.

7. Q: All inhabitants are of the same type, and say, "Some of us smoke, but I don't."

   A: If the statement is true, then at least one person must smoke and be lying about it. But we are given that all inhabitants are of the same type, so if one is lying, then they all must be, so the statement would be false, which is a contradiction. Therefore, the statement must be false, and either none smoke or all do.

8. Q: Suppose instead that each inhabitant made two statements: "(1) Some of us smoke. (2) I don't smoke."

   A: It is not possible for knights or knaves to make both of those statements, even on an island of mixed inhabitants. Assume both statements are true. Then every knight must not smoke, by (2), and at least one knave must smoke, by (1). But suppose a knave also made those statements: (2) would be false, but (1) would be true, which is impossible since knaves don't tell the truth.

   ## The Universal and Existential Quantifiers

   We use the letters $x, y, z$ to stand for arbitrary objects of some domain under consideration (p. 134).

   Given a property $P$ and an object $x$, the proposition that $x$ has property $P$ is written $P x$.

   The proposition that all objects $x$ have property $P$ is written $\forall x P x$ (universal quantifier).

   The proposition that some (at least one) $x$ has property $P$ is written $\exists x P x$ (existential quantifier).

   These quantifiers are used along with the logical connectives from propositional logic to form propositions in first-order logic.

   For example, let $G$ be the property of being good. $\forall x G x$ means all people are good. $\exists x G x$ means at least one person is good.

   How do we say no one is good? $\neg \exists x G x$, or $\forall x (\neg G x)$.

   Let $g$ stand for God and $xHy$ mean "x helps y." How can we say "God helps those who help themselves?"

   The English-language statement is ambiguous; it could mean (a) God helps all those who help themselves (and maybe others), (b) God only helps those who help themselves (and perhaps not all of them), or (c) God helps all those who help themselves, and no one else.

   (a) $\forall x (x H x \to g H x)$

   (b) $\forall x (g H x \to x H x)$

   (c) $\forall x (x H x \equiv g H x)$

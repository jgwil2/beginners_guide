# Axiomatic Propositional Logic

An axiom system works from a set of formulas, called the *axioms* of the system, and a set of relations called *inference rules*, being of the form, "From the formulas $X_1,…,X_n$, we can infer formula $X$."

Diagramatically:
$$
\frac{X_1,…,X_n}{X}
$$
A *proof* in an axiom system consists of a finite sequence of formulas, each of which is either an axiom of the system or can be inferred from an earlier formula by the inference rules of the system.

*Modus Ponens* (abbreviated MP):
$$
\frac{X, X \to Y}{Y}
$$
Read as, "From the formulas $X$ and $X \to Y$, the formula $Y$ can be inferred."

The axiom system we will work in is a modification of $System \space \mathcal{K}$, described by Stephen Kleene [1952].

Our system shall be called $System \space \mathcal{S_0}$; it takes as primitive connectives $\neg, \and, \or, \to$, and has the following nine axiom schemes:
$$
\begin{align*}
&S_1: \space (X \and Y) \to Y\\
&S_2: \space (X \and Y) \to X\\
&S_3: \space [(X \and Y) \to Z] \to [X \to (Y \to Z)]\\
&S_4: \space [(X \to Y) \and (X \to (Y \to Z))] \to (X \to Z)\\
&S_5: \space X \to (X \or Y)\\
&S_6: \space Y \to (X \or Y)\\
&S_7: \space [(X \to Z) \and (Y \to Z)] \to ((X \or Y) \to Z)\\
&S_8: \space [(X \to Y) \and (X \to \neg Y)] \to \neg X\\
&S_9: \space \neg \neg X \to X\\
\end{align*}
$$
(0) Prove the following preliminary facts (in $System \space \mathcal{S_0}$):

$F_1$. If $\vdash X \to Y$, then $X \vdash Y$.
$$
\begin{align*}
&(1)\space \vdash X \to Y \quad\quad& \text{(Hypothesis)}\\
&(2)\space \vdash X \quad\quad& \text{(Hypothesis)}\\
&(3)\space \vdash Y \quad\quad& \text{(By 1, 2, MP)}
\end{align*}
$$
$F_2$. If $\vdash X \to (Y \to Z)$, then $X, Y \vdash Z$.
$$
\begin{align*}
&(1)\space \vdash X \to (Y \to Z) \quad\quad& \text{(Hypothesis)}\\
&(2)\space \vdash X \quad\quad& \text{(Hypothesis)}\\
&(3)\space \vdash Y \quad\quad& \text{(Hypothesis)}\\
&(4)\space \vdash Y \to Z \quad\quad& \text{(By 1, 2, MP)}\\
&(5)\space \vdash Z \quad\quad& \text{(By 3, 4, MP)}
\end{align*}
$$

$F_3$. $(X \and Y) \to Z \vdash X \to (Y \to Z)$ (exportation, abbreviated "Exp.")
$$
\begin{align*}
&(1)\space \vdash (X \and Y) \to Z \quad\quad& \text{(Hypothesis)}\\
&(2)\space \vdash [X \to (Y \to Z)] \to [X \to (Y \to Z)] \quad\quad& \text{($S_3$)}\\
&(3)\space \vdash X \to (Y \to Z) \quad\quad& \text{(By 1, 2, MP)}
\end{align*}
$$

$F_4$. If $\vdash (X \and Y) \to Z$, then $X,Y \vdash Z$.
$$
\begin{align*}
&(1)\space \vdash (X \and Y) \to Z \quad\quad& \text{(Hypothesis)}\\
&(2)\space \vdash X \to (Y \to Z) \quad\quad& \text{(By 1, $F_3$)}\\
&(3)\space X, Y \vdash Z \quad\quad& \text{(By 2, $F_2$)}\\
\end{align*}
$$

(1) Prove the following with axiom schemes $S_1, S_2, S_3, S_4$.

$T_1$. $\vdash X \to (Y \to Y)$
$$
\begin{align*}
&(1) \space (X \and Y) \to Y \vdash X \to (Y \to Y) \quad\quad& \text{($F_3$)}\\
&(2) \space \vdash (X \and Y) \to Y \quad\quad& \text{($S_1$)}\\
&(3) \space \vdash X \to (Y \to Y) \quad\quad& \text{(By 2, 1, MP)}
\end{align*}
$$
$T_2$. $\vdash Y \to Y$
$$
\begin{align*}
&(1) \space \vdash X \to (Y \to Y) \quad\quad& \text{($T_1$)}\\
&(2) \space \vdash [(X \and Y) \to Y] \to (Y \to Y) \quad\quad& \text{(sub $S_1$ or any provable formula for X)}\\
&(3) \space \vdash Y \to Y \quad\quad& \text{(By MP)}
\end{align*}
$$

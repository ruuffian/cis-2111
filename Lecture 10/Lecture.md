February 13th, 2023

$L(M_1) = A$ and $L(M_2) = B$, both of which are *regular* languages ($M_1$ and $M_2$ are DFAs). 

We know that the unions and complements of two regular languages is in fact regular. Is the same true for intersections?

$\overline{A} \cup \overline{B}$ is regular.

Then, $\overline{\overline{A} \cup \overline{B}} = \overline{\overline{A}} \cap \overline{\overline{B}} = A \cap B$, thus $A \cap B$ is regular.

$M_1 = \left\{ Q = \{q_1 \dots q_i\} ,\sum, \delta_1, q_1, F_1 \right\}$
$M_2 = \left \{ Q = \{r_1\dots r_j\}, \sum, \delta_2., r_1, F_2 \right \}$

So, if we want some $M \ni L(M) = A \cup B$, we get this:
$\delta^*(q_1, r_1, w) = \left( d_1^*(q_1, w), d_2^*(r_1, w) \right)$
 So, clearly, we accept a string $w$ if we end up in $F_1 \cup F_2$.
 Similarly for intersection, we end up in $F_1 \cap F_2$.

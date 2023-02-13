February 13th, 2023

$L(M_1) = A$ and $L(M_2) = B$, both of which are *regular* languages ($M_1$ and $M_2$ are DFAs). 

We know that the unions and complements of two regular languages is in fact regular. Is the same true for intersections?

$\overline{A} \cup \overline{B}$ is regular.

Then, $\overline{\overline{A} \cup \overline{B}} = \overline{\overline{A}} \cap \overline{\overline{B}} = A \cap B$, thus $A \cap B$ is regular.


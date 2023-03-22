March 22nd, 2023

FINALLY having TMQ 3 today, on NFA to DFA. Maybe this one will be easier. Here is the process:

Suppose $Q$ is the set of states in the NFA $M_1$. Then, we take $\mathcal{P}(Q)$, and compute $E(x), \thinspace \forall x \in \mathcal{P}(Q)$. Then, we create a new set $Q' = \{ x \in \mathcal{P}(Q) \thinspace | \thinspace E(x) = x \}$. Finally, we compute $\delta_1$, using the states in $Q'$ as our new DFA. IMPORTANT: $\epsilon$ moves are transitive- keep this in mind when computing $E(x)$. 
Reminder: $E(x) =\{ y \in Q \thinspace | \thinspace \text{y is reachable from x by an epsilon move}\}$  
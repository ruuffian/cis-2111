January 20th, 2023

Say we have two languages $\sum$ and $\sum'$.
$$
\sum = \{0,1\}
\sum' = \{0,1,2,ww\}
$$
We want to combine two automota, $M$ and $M'$. To do so, we need to extend the languages of our two automotan to accept each other.

![Extended Automota](images/extended.png)

 This is an example of an automotan that has been combined with the automotan from [last class](obsidian://open?vault=CIS%202111&file=Lecture%201%2FLecture).

Now we define a two-state finite automotan $M_2$.

![Finite Automotan M_2](images/m2.png)

We know a few things about this automotan from this image:

$M_2 = (\{q_1, q_2\}, \{0,1\}, \delta, q_1, \{q_2\})$

where $\delta$ is the transition function - 
![transition function](images/delta.png)

 Let's check some codes to see if they belong in the language of $M_2$:
1101 - $q_0 \rightarrow q_1 \rightarrow q_1 \rightarrow q_0 \rightarrow q_1 \therefore$ $q_1$ is a terminal/accepting state, so 1101 is accepted.
110 - $q_0 \rightarrow q_1 \rightarrow q_1 \rightarrow q_0 \therefore$ $q_2$ is not a terminal state, so 110 is NOT accepted.

The language of $M_2$: $\{0, 1\}^*1$

This can be verified with [JFLAP](obsidian://open?vault=CIS%202111&file=Lecture%202%2Fm2.jff). So, we can say $L(M_2) = \{w | w \text{ ends with a 1}\}$

Lets define $M_3$:
![Finite Automotan M3](images/m3.png)

$M_3 = (\{q_0, q_1\}, \{0,1\}, \delta, q_0, \{q_0\})$ with the transition function $\delta$ defined below-
![delta 2](images/delta2.png)

The language of $M_3$ can be described as follows:

$M_3 = \{ w | w \text{ is } \epsilon \text{ or ends with } 0\}$

Next week we will look at a more complicated automotan.

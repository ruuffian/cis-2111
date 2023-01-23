January 23rd, 2023

It is important that every state in an automotan has a transition associated with every member of said automotan's alphabet- this is to ensure that every string within the alphabet can at least be read. Note it is not necessary to <i>accept</i> every string, simply that it is able to <i>read</i> each string.

Quick review:

![Automotan M_2](images/m2.png)

We already know the language of this automotan- $L(M_2) = \{ w | w \text{ ends in a 1} \}$

Let's make a small alteration, call it $M_3$:

![Automotan M_3](images/m3.png)

The only change here is the terminal state moving from $q_1$ to $q_0$.

What is the language for $M_3$?

- Start in $q_0$
- any number of 0's will be accepted
- after 1, can have any number of 1's
- 0 has to follow 1

Using these vague descriptions we can say $0^* \cup \{0, 1\}^* \ 1 \ 0^+$
Basically, any number of 0s is valid -> if we input a 1, we absolutely need to terminate with a 0.

$L(M_3) = \epsilon \cup \{0, 1\}^* \ 1 \ 0^+$


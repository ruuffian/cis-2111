February 22nd, 2023

### Minimal DFA

A *Minimal DFA* is the "simplest" version of a DFA. As we know, there are infinitely many DFA's that correspond to the same lanugage. A minimal DFA is unique up to labeling, meaning the shape (not the labels/language) are identical.

![[Pasted image 20230222141556.png]]

Here is an $O(n^2)$ Alogorithm for reducing a DFA to its minimal form:

First, partition your states:
	Non-Final States => $A = \{0, 5, 6\}$
	Final States => $F = \{1,2,3,4\}$
Now take a pair of indistinguishible states: For example $(0, 5)$
$\delta((0,5), 0) = (1, 6)$ and $\delta((0,5), 1) = (2, 5)$. $(1,6)$ and $(0,5)$ are distinguishible, so these states cannot be combined.
$\delta((2,4),0) = (4,4)$, 4=4 so we cannot combine these.

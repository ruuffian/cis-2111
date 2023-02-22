February 22nd, 2023

### Minimal DFA

A *Minimal DFA* is the "simplest" version of a DFA. As we know, there are infinitely many DFA's that correspond to the same lanugage. A minimal DFA is unique up to labeling, meaning the shape (not the labels/language) are identical.

![[Pasted image 20230222141556.png]]

Here is an $O(n^2)$ Alogorithm for reducing a DFA to its minimal form:

First, partition your states:
	Non-Final States => $A = \{0, 5, 6\}$
	Final States => $F = \{1,2,3,4\}$

February 10th, 2023

### Context-Free Languages

A grammar consists of a colelction of substitution rules, also called productions. Each rule appears as a line in the grammar, comprising a symbol and a string separated by an arrow. The symobl is called a *variable* and the string is a collection of *terminals*. 
Here is an example of a grammer:

![Grammar](grammar.png)

##### Formal Definition of a Grammar

![grammar def](def.png)

$G_2 = (V, T, S, P)$
$V = \{A, B\}$ and $T = \{a, b\}$
with $P = \{$
	$S \rightarrow AB$
	$A \rightarrow aaA\thinspace|\thinspace\epsilon$
	$B \rightarrow Bb\thinspace|\thinspace\epsilon$
$\}$

Let's use this grammar now.
$S \rightarrow AB \rightarrow aaAB \rightarrow aaA\epsilon \rightarrow aaaaA \rightarrow aaaa\epsilon \rightarrow aaaa$
$S \overset{*}\rightarrow aaaa$
$\overset *\rightarrow$ means derivation, as in $aaaa$ is derived from $S$.

Grammars can be ambiguous, meaning a string may have multiple different derivations. 

##### Derivation Trees

We can use ordered trees to show the derivation of a string in a grammar.
![derivation tree](tree1.png)

If we wanted to get the steps of the derivation, we can number each node with parent > child like so:
![numbered tree](numbered_tree.png)

$S \overset 1 \rightarrow AB \overset 2 \rightarrow ABb \overset 3 \rightarrow aaABb \overset 4 \rightarrow aaAb \overset 5 \rightarrow aaB \overset 6 \rightarrow aab$

In ambiguous (bad) grammars, we can have multiple derivations, thus multiple derivation trees. THere is an example in the notes.

Leftmost derivation can be visualized as a preorder tree traversal, and a rightmost derivation corresponds to a postorder traversal.

A context-free grammar is in *Chomsky-normal form* if every rule is of the form:
$A \rightarrow BC$
$A \rightarrow a$

Where $a$ is any terminal, and $A, B, C$ are any variables, except that $B$ and $C$ may not be the start variable. Additionally, we permit the rule $S \rightarrow \epsilon$.

This is an important result, but we will not use it.

### Pushdown Automota (PDA)

A *pushdown automota* is similar to a NFA, but it include an extra piece- namely, a stack. A PDA can read and write symbols from a stack. Reading is destructive (popping) and writing is constructive (pushing). This extra piece of memory allows PDA to recognize some non-regular languages. Now, we consider a semi-infinite input tape to read symbols from- see below.
![PDA](pda_schematic.png)

A PDA can recognize the non-regular lanugauage $\{0^n1^n\}$. Here is the procedure
```
Read symbols from input tape
If a 0 is read, push a 0 onto the stack
If a 1 is read, pop a 1 off the stack
If the stack is empty at the end, accept the input
If the stack is non-empty OR you attempt to pop an empty stack, reject the input
```

DPDA and NPDA do not equate, unlike DFA and NFA.


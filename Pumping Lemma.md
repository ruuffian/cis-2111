If A is a regualr language, then there is a number $p$ (the pumping length) where if $s$ is any string in $A$ of length at least $p$, then $s$ may be composed into three pieces, $s = xyz$, with the following conditions:

$$
\begin{enumerate}
	\item{\text{For each i \geq 0, xy^iz \in A}}
	\item{y > 0}
	\item{|xy| < p}
\end{enumerate}
$$
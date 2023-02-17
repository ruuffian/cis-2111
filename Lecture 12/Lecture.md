Febrauary 17th, 2023

### Mealy Machine

A *Mealy Machine* is a 6-tuple $M = \left ( Q, q_0, \sum, \Gamma, \delta, \lambda \right)$. $\Gamma$ is the output alphabet, and $\lambda$ is called the output function. The important thing about Mealy Machines is that each transition outputs a value. $\frac{a}{b}$ represents the transition and output, with $a$ being the transition and $b$ being the output value.

![example](images/mealy.png)

### Moore Machine

Related to *Mealy Machines* are *Moore Machines*. These are defined identically to *Mealy Machines*, except the output values are associated with states rather than transitions.
![example](images/moore.png)

Importantly, all *Mealy Machines* can be converted to *Moore Machines*.


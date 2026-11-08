![[Pasted image 20261108173143.png]]

- $\underline{A}$ & $\underline{B}$ together is the key
- *Nonprimes* are the one that are not underlined --> $C,D,E,F$
	- These nonprimes are fully depending on the key
- $FD_{1}$ is a *full dependency* --> Satisfies 2nd Normal Form
	- **Full Dependency:** Keys --> Nonprimes
	- **Partial Dependency:** One Single Key --> Nonprimes
		- ![[Pasted image 20261108180915.png]]
		- $FD_{1}$ is a full dependency
		- $FD_{2}$ & $FD_{3}$ are partial dependencies
		- ![[Pasted image 20261108181956.png]]
- $R\ (ABCDEF)$ where $AB\to\{ABCDEF\}$, if $B\to \{D\}$ ---> $R'(ABCEF)$ where $AB\to\{CEF\}$ & $R_{1}(BD)$ where $B\to\{D\}$
	- Here, $B$ is a copy from the original relation
	- But $D$ is removed from original relation `hi`
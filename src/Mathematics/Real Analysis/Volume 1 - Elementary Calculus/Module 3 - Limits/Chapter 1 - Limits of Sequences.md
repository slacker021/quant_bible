---
dg-publish:
---
Measuring real physical quantities is an imperfect process that raises three important questions: 
1. What relation does the sequence of approximations so obtained have to the quantity being measured? In mathematics, this can be translated to getting an exact expression of of the sequence of multiple values which describes the value of the quantity being measured. Is the description unambiguous, or can the same sequence correspond to the same different values of the measured quantity?
2. How're the operations on the approximate values connected with the same operations on the exact values, and how can the operations that can legitimately be carried out by replacing exact values with approximate ones be characterized?
3. Can the sequence of numbers be determined to be a sequence of arbitrarily precise approximations of the values of some quantity, or does the sequence not approach some value at all?
These questions are answered by the concept of a *limit*, which plays a fundamental role in calculus. Both sequences and functions utilize this concept. In fact, it can be argued that real analysis fundamentally relies on the rigorous concepts of limits. 

---
# Limit of a Sequence
$$
\begin{gather}
\textbf{Definition: Sequence } \\[5mm]
\text{A function } f:\mathbb{N} \rightarrow X \text{ whose domain of definition is the } \\
\text{set of natural numbers is a sequence. }
\end{gather}
$$
The values $f(n)$ is the function $f$ are the *terms* of the sequence. An alternative way to denote a sequence is by assigning it a symbol for an element of the set into which the mapping goes. Thus, $x_{n} : = f(n)$, with the sequence itself being denoted as $\{x_{n}\} = x_{1},x_{2},\dots,x_{n}$. This is called the *sequence in* $X$ or a sequence of elements in * $X$,  where $x_{n}$ is the $n$th term of the sequence. 


>[!Info]+ Remark: Most Common Type of Sequence
>The most common type of sequence is $f:\mathbb{N} \rightarrow \mathbb{R}$. In other words, most sequences map the natural numbers to the real numbers, providing an infinite ordered list of values whose *asymptotic* behavior is the fundamental object of focus in the analysis of the limit of sequences. 

With the concept of a sequence having been defined, the asymptotic behavior can now be analyzed. The asymptotic behavior of a sequence can be described as how the terms of a sequence change as the index $n$ grows very large, or as $n \rightarrow \infty$:
$$\begin{gather}  \textbf{Definition: Limit of a Sequence} \\[5mm] \text{A real number } A \text{ is the limit of a sequence } \{x_n\} \text{ if for every } \varepsilon > 0, \\ \text{there exists a natural number } N \text{ such that for all } n > N, \\ \text{the inequality } \vert{}x_n - A\vert{} < \varepsilon \text{ holds.} \\ \text{If such a limit exists, the sequence is said to converge to } A, \text{ denoted as } \lim_{n \to \infty} x_n = A. \end{gather}$$

>[!danger]+ Intuition: Error Tolerance
>In the context of the rigorous definition of a limit, the value $\varepsilon$ can be thought of as some sort of "error tolerance". No matter what level of precision $\varepsilon > 0$ is prescribed, there is an index $N$ such that the absolute error in approximating the number $A$ by terms of the sequence $\{ x_{n} \}$ is less than $\varepsilon$ as soon as $n > N$. 

There're two types of sequence limits that're said to emerge when testing for their asymptotic behavior:
$$
\begin{gather}
\textbf{Definition: Sequence Convergence} \\[5mm]
\text{If } \lim_{ n \to \infty } x_{n} = A, \text{ then the sequence } \{ x_{n} \} \text{ converges or tends to } A, \text{ which can be represented as } x_{n} \rightarrow A  \\
\text{as } n \rightarrow \infty. \text{ This sequence is convergent. } \\[2.5mm]
\text{If a sequence doesn't have a limit, then it's divergent. }
\end{gather}
$$

>[!info]+ Remark: What the Definition of a Sequence Limit Actually Does
>The definition of the limit of a sequence doesn't actually provide the value of the limit itself. Instead, it's there to help prove that the limit for the sequence indeed exists (or doesn't exists). Should one claim to have found the limit of a sequence—whether by hypothesis, brute force through expanding the sequence, or some other method—the definition can be used to prove that the claim is true. 
>
>Furthermore, the value of $\varepsilon$ is entirely arbitrary. It can be chosen to be as small as desired as long as it's greater than zero. 

>[!example]+ Some Examples of Limits
>1. $\lim_{ n \to \infty } \frac{1}{n} = 0$
>Proof:
>Let $f: \mathbb{N} \rightarrow \mathbb{R}$, where $f(n) = \frac{1}{x_{n}} = \left\{  \frac{1}{1}, \frac{1}{2}, \frac{1}{3} \dots \frac{1}{n}  \right\}$.  Since $|\frac{1}{n} - 0| < \varepsilon = \frac{1}{n} < \varepsilon$ when $n > N = [\frac{1}{\varepsilon}]$. As an example, if the value of $n = 100$ and $\varepsilon = 0.000001$, then it would be shown that
>$$x_{100} = \frac{1}{100} \implies |x_{n} - 0| < \frac{1}{100} \text{ when } n > 100 \tag{1}$$
>2. $\lim_{ n \to \infty } \frac{n + 1}{n} = 1$ 
>Proof:
>Let $f:\mathbb{N} \rightarrow \mathbb{R}$, where $f(n) = \frac{n + 1}{n} = \left\{2, \frac{3}{2}, \frac{4}{3}\dots \frac{n+1}{n}\right\}$. The aforementioned expression can be rewritten as
>$$
>\frac{n+1}{n} = 1 + \frac{1}{n} \tag{2}
>$$
>Which would imply 
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

>[!example]+ Example: Some Examples of Limits
>1. $\lim_{ n \to \infty } \frac{1}{n} = 0$
>Proof:
>Let $f: \mathbb{N} \rightarrow \mathbb{R}$, where $f(n) = \frac{1}{n} = \left\{  \frac{1}{1}, \frac{1}{2}, \frac{1}{3} \dots \frac{1}{n}  \right\}$.  Suppose that the candidate limit value of the sequence is $A = 0$. It follows that
>$$
>|f(n) - A| < \varepsilon \implies \left|\frac{1}{n} - 0\right| < \varepsilon \tag{1}
>$$
>Since $n$ is a natural number, $\frac{1}{n}$ must be positive. This makes the absolute value signs redundant, resulting in $\frac{1}{n} < \varepsilon$. The goal is now to isolate $n$, which involves multiplying both sides by $n$ and dividing by $\varepsilon$:
>$$
\frac{1}{n} < \varepsilon \implies 1 < n\varepsilon \implies \frac{1}{\varepsilon} < n \tag{2}
>$$
>This inequality shows that for the distance between $x_{n}$ and $0$ to be less than $\varepsilon$, the index $n$ must be greater than $\frac{1}{\varepsilon}$. Now, since $n$ must be a natural number, a number $N$ must be chosen such that any natural number larger than it satisfies the condition. This is to be denoted as
>$$
>N = \left\lceil \frac{1}{\varepsilon} \right\rceil \tag{4}
>$$
>Now, assume that for any given $\varepsilon > 0$, a specific $N$ must be chosen. It must be checked if this choice of $N$ guarantees the inequality for all $n > N$. If $n > N$, and since $N \ge \frac{1}{\varepsilon}$, it follows that 
>$$
>n > \frac{1}{\varepsilon} \implies n\varepsilon > 1 \implies \varepsilon > \frac{1}{n} \implies \left| \frac{1}{n} - 0 \right| < \varepsilon \tag{5}
>$$
>Since a number $N$ for an arbitrarily given $\varepsilon > 0$ was found, the limit condition is met. 
>2. $\lim_{ n \to \infty } \frac{n+1}{n} = 1$
>   Proof:
>   Let $f: \mathbb{N} \rightarrow \mathbb{R}$, where $f(n) = \frac{n+1}{n} = \left\{ 2, \frac{3}{2}, \frac{4}{3}\dots \frac{n+1}{n}\right\}$. Suppose that the candidate value for the limit is $1$. By definition of the sequence limit, 
>$$
> | f(n) - A | < \varepsilon \implies \left| \frac{n+1}{n} - 1 \right| < \varepsilon \tag{6}   
>$$
>Since $n$ is a natural number, it's a positive integer. Additionally, the value of $n$ must now be isolated:
>$$
>\left|\frac{n+1}{n} - 1 \right| < \varepsilon \implies \frac{n+1}{n} - 1 < \varepsilon \implies \frac{n}{n} + \frac{1}{n} - 1 < \varepsilon \implies 1 + \frac{1}{n} - 1 < \varepsilon \tag{7}
>$$
>The expression can then be simplified into 
>$$
\frac{1}{n} < \varepsilon \implies 1 < n\varepsilon \implies \frac{1}{\varepsilon} < n \tag{8}
>$$ 
>Since $n$ is a natural number, there must a number $N$ that is chosen such that any $n > N$ satisfies the condition of $N = l\left\lceil  \frac{1}{\varepsilon}  \right\rceil$. It would then follow that 
>$$
\frac{1}{\varepsilon} < n \implies 1 < n\varepsilon \implies \frac{1}{n} < \varepsilon \implies \left| \frac{1}{n} + 1 \right| < \varepsilon + 1 \tag{9}
>$$
>Since a number $N$ for an arbitrarily given $\varepsilon > 0$ was found, the limit condition is met. 
>3. $\lim_{ n \to \infty } \left[1 + \frac{(-1)^{n}}{n} \right] = 1$. 
> Proof:
> Let $f: \mathbb{N} \rightarrow \mathbb{R}$, where $f(n) = \left[1 + \frac{(-1)^{n}}{n} \right]$. Suppose that the candidate limit value is $1$. By definition, 
> $$
> \left| \left[1 + \frac{(-1)^{n}}{n} \right] - 1 \right| < \varepsilon \tag{10}
> $$
> The number $n$ must be isolated:
> $$
> \left[ \frac{(-1)^{n}}{n} \right]  < \varepsilon \tag{11}
> $$













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
>The definition of the limit of a sequence doesn't actually provide the value of the limit itself. Instead, it's there to help prove that the limit for the sequence indeed exists (or doesn't exists). Should one claim to have found the limit of a sequence—whether by hypothesis, brute force through expanding the sequence, or some other method—the definition can be used to prove that the claim is true. Otherwise, one must try to find the value of the limit first before proving that it exists. 
>
>Furthermore, the value of $\varepsilon$ is entirely arbitrary. It can be chosen to be as small as desired as long as it's greater than zero. 

>[!example]- Example: Some Examples of Limits
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


### Unique Sequence Types
Broadly speaking, there're two type of sequences: 
$$
\begin{gather}
\textbf{Definition: Constant Sequences } \\[5mm]
\text{If there's a number } A \text{ and an index } N \text{ such that } x_{n} = A \text{ for all } n > N,  \\
\text{the sequence } \{x_{n}  \} \text{ is ultimately constant. } \\[5mm]
\textbf{Definition: Bounded Sequence } \\[5mm]
\text{A sequence } \{ x_{n} \} \text{ is bounded if there's a } M \text{ such that } |x_{n}| < M \text{ for all } n \in \mathbb{N}. 
\end{gather}
$$

### Basic Properties of Limits
With these definitions provided, basic properties of limits can be deduced:
$$
\begin{gather}
\textbf{Theorem: Basic Properties of Limits} \\[5mm]
\text{1. An ultimately constant sequence converges. } \\
\text{2. Any neighborhood of the limit of a sequence contains all but a finite number } \\
\text{of terms of the sequence. } \\
\text{3. A sequence can't have multiple distinct limit values. In other words, a convergent } \\
\text{has a unique limit. } \\
\text{4. A convergent sequence is bounded. }
\end{gather}
$$

(see [[Proof of the Basic Properties of Limits|proof]])

##### Arithmetic Operations Involving Limits
Given that existent limits are real numbers, it's only natural that the standard arithmetic operations defined as axioms of addition and multiplication apply to limits: 
$$
\begin{gather}
\textbf{Theorem: Arithmetic Properties of Limits} \\[5mm]
\text{If } \lim_{ n \to \infty } x_{n} = A \text{ and } \lim_{ n \to \infty } y_{n} = B, \text{ then } \\[2.5mm]
\text{1. } \lim_{ n \to \infty }(x_{n} + y_{n}) = A + B \\
\text{2. } \lim_{ n \to \infty }(x_{n} \cdot y_{n}) A \cdot B \\
\text{3. } \lim_{ n \to \infty } \frac{A}{B} \text{ if } B \neq 0 \text{ and } y_{n} \neq 0 \text{ for all } n. 
\end{gather}
$$
(see [[Proof of Arithmetic Operations Involving Limits|proof]])
These operations allow for the decomposition and analysis of complex sequences constructed from simpler components. 

>[!danger]+ Intuition: Convergence vs. Boundedness 
>It is crucial to note that while convergence strictly implies boundedness, the converse is decisively false. A sequence can oscillate within strict bounds (like $x_n = (-1)^n$) without ever settling toward a single point. To guarantee convergence in a bounded sequence, an additional structural condition must be introduced, such as *monotonicity*.

##### Inequalities Involving Limits of Sequences
Another consequence of the limits of sequences being real numbers is that the axioms of ordering apply to them:
$$
\begin{gather}
\textbf{Theorem: Inequalities Involving Limits} \\[5mm]
\text{1. If } \{x_{n}  \} \text{ and } \{y_{n}  \} \text{ are two convergence sequences with } \lim_{ n \to \infty } x_{n} = A \text{ and } \lim_{ n \to \infty } y_{n} = B,  \\
\text{ where } A < B, \text{ then there's an index } N \in \mathbb{N} \text{ such that } x_{n} < y_{n} \text{ for all } n > N.  \\[2.5mm]
\text{2. Suppose the sequences } \{x_{n}  \}, y_{n}, \text{ and } z_{n} \text{ are such that } x_{n} \le y_{n} \le z_{n} \text{ for all } n > N \in \mathbb{N}. \text{If } \\
\text{the sequences } \{x_{n}  \} \text{ and } \{z_{n} \} \text{ converge to the same limit, then the sequence } \\
\{ y_{n} \} \text{ also converges to that limit. } 
\end{gather}
$$
(see [[Proof of Inequalities Involving Limits|proof]])

It then easily follows that
$$
\begin{gather}
\textbf{Corollary: } \\[5mm]
\text{Suppose } \lim_{ n \to \infty } x_{n} = A \text{ and } \lim_{ n \to \infty } y_{n} = B. \text{ If there's a } N \text{ such that for all } n > N, \text{ then } \\[2.5mm]
\text{1. } x_{n} \ge y_{n} \implies A \ge B \\
\text{2. } x_{n} \ge y_{n} \implies A \ge B \\
\text{3. } x_{n} > B \implies A \ge B \\
\text{4. } x_{n} \ge B \implies A \ge B
\end{gather}
$$
(see [[Proof of the Corollary for Limit Inequalities|proof]])

>[!info]+ Remark: 
>It's worth noting that strict inequality may become equality in the limit. As an example, $\frac{1}{n} > 0$ for all $n \in \mathbb{N}$ yet $\lim_{ n \to \infty } \frac{1}{n} = 0$.
>

### Questions Involving the Existence of Sequence Limits

Relying on an external candidate $A$ to verify convergence is frequently impractical. A purely internal criterion for convergence is necessary, one that examines how elements of the sequence behave relative to one another rather than comparing them to a predefined limit:
$$
\begin{gather}
\textbf{Definition: Cauchy Sequence } \\[5mm]
\text{A sequence } \{x_{n}\} \text{ is a fundamental or Cauchy sequence if for any } \varepsilon > 0, \text{ there's an index } N \in \mathbb{N}  \\
\text{such that } |x_{m} - x_{n}| < \varepsilon \text{ whenever } n > N \text{ and } m > N. 
\end{gather}
$$

The definition above is useful because it can be used to demonstrate whether or not a sequence is convergence. The completeness of the real numbers ensures that this internal stabilization perfectly aligns with standard convergence: 
$$\begin{gather} \textbf{Theorem: Cauchy Criterion for Convergence} \\[5mm] \text{A sequence of real numbers converges if and only if it is a Cauchy sequence.} \end{gather}$$
(see [[Proof of the Cauchy Criterion for Sequences|proof]])


### A Criterion for the Existence of the Limit of a Monotonic Sequence
A unique type of sequence can be constructed depending on the size of the terms increasing or decreasing as the sequence goes on:
$$
\begin{gather}
\textbf{Definition: Monotonic Sequences} \\[5mm]
\text{1. A sequence } \{x_{n}  \} \text{ is increasing if } x_{n} < x_{n+1} \text{ for all } n \in \mathbb{N}.  \\
\text{2. A sequence }  \{x_{n}\} \text{ is nondecreasing if } x_{n} \ge x_{n+1} \text{ for all } n \in \mathbb{N}. \\
\text{3. A sequence is descreasing if } x_{n} > x_{n+1} \text{ for all } n \in \mathbb{N}.  \\[5mm]
\textbf{Definition: Sequence Bounded Above} \\[5mm]
\text{A sequence } \{ x_{n} \} \text{ is bounded above if there is a number } M \text{ such that } x_{n} < M  \\
\text{for all } n \in \mathbb{N}. 
\end{gather}
$$

With these two definitions being used to deduce and construct an important fact:
$$
\begin{gather}
\textbf{Theorem: Weierstrass} \\[5mm]
\text{For a nondescreasing sequence to have a limit, it's necessary and sufficient that it be bounded above. }
\end{gather}
$$
(see [[Proof of Weierstrass Theorem|proof]])

Which can then be used to demonstrate that 
$$
\begin{gather}
\textbf{Corollary: } \\[5mm]
\text{1. } \lim_{ n \to \infty } \sqrt[n]{n} = 1 \\
\text{2. } \lim_{ n \to \infty } \sqrt[n]{a} = 1 \text{ for any } a > 0
\end{gather}
$$

### Euler's Constant
A unique type of number can be discovered using the limits of sequences. Unlike other numbers, which have their origins from geometry, this number has its origin from calculus: 
$$
\begin{gather}
\textbf{Theorem: Euler's Number} \\[5mm]
\text{The number } \lim_{ n \to \infty } \left(1 + \frac{1}{n} \right)^n \text{ exists and is denoted as } e.  \\
\end{gather}
$$
(see [[Derivation of Euler's Constant|derivation]])

>[!question]+ Application: Euler's Number and Interest Rates
>Euler's Number is frequently used to calculate the decay or growth of a particular factor overtime. A good example of this is in compound interest:
>$$
>\begin{align}
>V_{F} = V_{P}e^{rt}, \text{ where } & V_{F} \text{ is the future value. } \\
>& V_{P} \text{ is the present value.} \\
>& r \text{ is the interest rate being compounded.} \\
>& t \text{ is the time in years.} 
>\end{align}
>$$



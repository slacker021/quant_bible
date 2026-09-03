---
dg-publish:
---
# The Most Important Classes of Real Numbers and Computational Aspects of Operations with Real Numbers
Having established the axiomatic foundation of the real numbers, it's time to turn to identifying several fundamental subsets within $\mathbb{R}$. While there's many real numbers that one could think of, these subsets form the most critical classes of real numbers that formulate the theoretical and fundamental foundations of computation-based mathematics. Furthermore, these subsets provide useful tools that enable the discovery of interesting properties that can be used to prove important statements. 

---
# The Natural Numbers and the Principle of Induction
The concept of an *inductive set* has several meanings in set theory. In the case of these notes, an inductive set is a *nonempty partially ordered* set where every element has a successor:
$$\begin{gather} \textbf{Definition: Inductive Set} \\ \text{A set } X \subset \mathbb{R} \text{ is inductive if for each number } x \in X, \text{ it also contains } x + 1. \end{gather}$$

>[!example]+ Example: The Set of Real Numbers being Inductive
>The set of real numbers $\mathbb{R}$ is an inductive set. Additionally, the set of positive numbers is also inductive. The intersection $X = \bigcap_{a \in A} X_{\mathcal{a}}$, if not empty, is an inductive set. More formally, 
>$$
>\begin{gather} \\
> \left( x \in X = \bigcap X_{\mathcal{a}} \right) \implies (\forall \mathcal{a} \in A (x \in X_{\mathcal{a}})) \implies  \\
> (\forall \mathcal{a} \in A ((x + 1)) \in X_{\mathcal{a}}) \implies \left((x + 1) \in \bigcap_{\mathcal{a} \in A} X_{\mathcal{a \in A}} X_{\mathcal{a}} = X \right) \tag{1}
\end{gather}
>$$

The example above provides the general idea and notation used to describe an inductive set. 

The most basic and intuitive subset of real numbers which can be described as inductive are the *natural numbers*:
$$\begin{gather} \textbf{Definition: The Set of Natural Numbers} \\ \text{The set of natural numbers, denoted } \mathbb{N}, \text{ is the smallest inductive set containing 1.} \\ \text{It is the intersection of all inductive sets that contain 1.} \end{gather}$$

>[!info]+ Remark: To or Not to Include $0$ as Part of the Natural Numbers?
>From a set-theoretic perspective, it might be more rational to begin the natural numbers with $0$. This would alter the definition of the set of natural numbers such that it's the smallest inductive set containing $0$. However, these notes will stick to the provided definition above. 
>
>Instead, the set of natural numbers with zero will be defined as the *whole numbers*. 

The definition of the natural numbers, where the set's smallest element begins at $1$, yields a direct corollary that serves as a vital proof technique:
$$\begin{gather} \textbf{Theorem: The Principle of Induction} \\ \text{If a subset } E \subset \mathbb{N} \text{ satisfies } 1 \in E \text{ and } (x \in E \implies (x + 1) \in E), \text{ then } E = \mathbb{N}. \end{gather}$$
(see [[Proof that Induction Works|proof]])

This principle can be illustrated in action by having it prove several useful properties of the natural numbers that'll see constant use from now on:
$$\begin{gather} \textbf{Proposition: Properties of Natural Numbers} \\ \text{1. The sum and product of natural numbers are natural numbers.} \\ \text{2. } (n \in \mathbb{N}) \wedge (n \ne 1) \implies ((n - 1) \in \mathbb{N}). \\ \text{3. For any } n \in \mathbb{N}, \text{ the set } \{x \in \mathbb{N} \mid n < x\} \text{ contains a minimal element, namely, } \\ \min\{x \in \mathbb{N} \mid n < x\} = n + 1. \\ \text{4. } (m, n \in \mathbb{N}) \wedge (n < m) \implies (n + 1 \le m). \\ \text{5. } n + 1 \text{ is the immediate successor of } n \text{ in } \mathbb{N} \text{ (no natural numbers lie between them).} \\ \text{6. If } n \ne 1, n - 1 \text{ is the immediate predecessor of } n \text{ in } \mathbb{N}. \\ \text{7. Any nonempty subset of } \mathbb{N} \text{ contains a minimal element.} \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

---
# Rational and Irrational Numbers

$$\begin{gather} \textbf{Definition 3: The Integers} \\ \text{The set of integers, denoted } \mathbb{Z}, \text{ is the union of the set of natural numbers,} \\ \text{the set of their negatives, and zero.} \end{gather}$$

Addition and multiplication of integers yield integers. Thus, $\mathbb{Z}$ is an additive Abelian group, but it is not a multiplicative group because reciprocals of integers (other than $1$ and $-1$) do not belong to $\mathbb{Z}$.

> [!info]+ Remark: Divisibility 
> If $m, n \in \mathbb{Z}$ and $k = m \cdot n^{-1} \in \mathbb{Z}$, we say $m$ is a multiple of $n$, or $n$ divides $m$.

$$\begin{gather} \textbf{Theorem 2: Fundamental Theorem of Arithmetic} \\ \text{Each natural number admits a representation as a product } n = p_1 \cdots p_k, \\ \text{where } p_i \text{ are prime numbers. This representation is unique except for the order of factors.} \end{gather}$$$$\begin{gather} \textbf{Definition 4: The Rational Numbers} \\ \text{Numbers of the form } m \cdot n^{-1} \text{ (or } m/n \text{), where } m, n \in \mathbb{Z} \text{ and } n \ne 0, \\ \text{are called rational. The set of rational numbers is denoted } \mathbb{Q}. \end{gather}$$

Any rational number can be represented by proportional pairs $(m_1, n_1)$ and $(m_2, n_2)$ where $m_1n_2 = m_2n_1$.

$$\begin{gather} \textbf{Definition 5: The Irrational Numbers} \\ \text{Real numbers that are not rational are called irrational.} \end{gather}$$$$\begin{gather} \textbf{Proposition 2: Existence of Irrational Numbers} \\ \text{There exists a real number } s > 0 \text{ such that } s^2 = 2, \text{ and } s \notin \mathbb{Q} \text{ (denoted } \sqrt{2} \text{).} \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

> [!info]+ Remark: Algebraic vs. Transcendental 
> Real numbers are _algebraic_ if they are roots of polynomial equations with rational coefficients. Otherwise, they are _transcendental_ (e.g., $\pi$).

## The Principle of Archimedes

The Principle of Archimedes links order and completeness. We first note properties of sets bounded above/below in $\mathbb{N}$ and $\mathbb{Z}$.

$$\begin{gather} \textbf{Proposition 3: Bounds in } \mathbb{N} \text{ and } \mathbb{Z} \\ \text{1. Any nonempty subset of } \mathbb{N} \text{ bounded above contains a maximal element.} \\ \text{2. The set } \mathbb{N} \text{ is not bounded above.} \\ \text{3. Any nonempty subset of } \mathbb{Z} \text{ bounded above contains a maximal element.} \\ \text{4. Any nonempty subset of } \mathbb{Z} \text{ bounded below contains a minimal element.} \\ \text{5. The set } \mathbb{Z} \text{ is unbounded above and below.} \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

$$\begin{gather} \textbf{Theorem 3: The Principle of Archimedes} \\ \text{For any fixed positive number } h \text{ and any real number } x, \\ \text{there exists a unique integer } k \text{ such that } (k - 1)h \le x < kh. \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

$$\begin{gather} \textbf{Proposition 4: Corollaries to Archimedes' Principle} \\ \text{1. For any } \epsilon > 0, \text{ there exists } n \in \mathbb{N} \text{ such that } 0 < 1/n < \epsilon. \\ \text{2. If } x \ge 0 \text{ and } x < 1/n \text{ for all } n \in \mathbb{N}, \text{ then } x = 0. \\ \text{3. Between any real numbers } a < b, \text{ there is a rational } r \in \mathbb{Q} \text{ such that } a < r < b. \\ \text{4. For any } x \in \mathbb{R}, \text{ there exists a unique } k \in \mathbb{Z} \text{ such that } k \le x < k + 1. \\ \text{This } k \text{ is the integer part } [x], \text{ and } \{x\} := x - [x] \text{ is the fractional part.} \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

## Geometric Interpretation and Computations

The set $\mathbb{R}$ can be modeled geometrically as a continuous line where each point corresponds to a coordinate.

$$\begin{gather} \textbf{Definition 6: Intervals} \\ \text{Open: } ]a, b[ := \{x \in \mathbb{R} \mid a < x < b\} \\ \text{Closed: } [a, b] := \{x \in \mathbb{R} \mid a \le x \le b\} \\ \text{Half-open: } ]a, b] := \{x \in \mathbb{R} \mid a < x \le b\}, \ [a, b[ := \{x \in \mathbb{R} \mid a \le x < b\} \\ \text{The length of interval } I \text{ with endpoints } a, b \text{ is } \vert{}I\vert{} = b - a. \end{gather}$$$$\begin{gather} \textbf{Definition 7: Neighborhood} \\ \text{An open interval containing a point } x \in \mathbb{R} \text{ is a neighborhood of } x. \\ \text{A } \delta\text{-neighborhood of } x \text{ is } ]x - \delta, x + \delta[ \text{ (where } \delta > 0\text{).} \end{gather}$$$$\begin{gather} \textbf{Definition 8: Distance and Absolute Value} \\ \text{The absolute value } \vert{}x\vert{} \text{ is } x \text{ if } x \ge 0, \text{ and } -x \text{ if } x < 0. \\ \text{The distance between } x, y \in \mathbb{R} \text{ is } \vert{}x - y\vert{}. \end{gather}$$$$\begin{gather} \textbf{Proposition 5: The Triangle Inequality} \\ \vert{}x + y\vert{} \le \vert{}x\vert{} + \vert{}y\vert{} \\ \text{Equality holds if and only if } x \text{ and } y \text{ are both nonnegative or both nonpositive.} \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

### Errors in Computations

$$\begin{gather} \textbf{Definition 9: Errors} \\ \text{If } x \text{ is exact and } \tilde{x} \text{ is an approximation:} \\ \text{Absolute error: } \Delta(\tilde{x}) := \vert{}x - \tilde{x}\vert{} \\ \text{Relative error: } \delta(\tilde{x}) := \Delta(\tilde{x}) / \vert{}\tilde{x}\vert{} \text{ (for } \tilde{x} \ne 0\text{)} \end{gather}$$$$\begin{gather} \textbf{Proposition 6: Propagation of Errors} \\ \Delta(\tilde{x} + \tilde{y}) \le \Delta(\tilde{x}) + \Delta(\tilde{y}) \\ \Delta(\tilde{x} \cdot \tilde{y}) \le \vert{}\tilde{x}\vert{}\Delta(\tilde{y}) + \vert{}\tilde{y}\vert{}\Delta(\tilde{x}) + \Delta(\tilde{x})\Delta(\tilde{y}) \\ \Delta\left(\frac{\tilde{x}}{\tilde{y}}\right) \le \frac{\vert{}\tilde{x}\vert{}\Delta(\tilde{y}) + \vert{}\tilde{y}\vert{}\Delta(\tilde{x})}{\tilde{y}^2 (1 - \delta(\tilde{y}))} \text{ (provided } \delta(\tilde{y}) < 1\text{)} \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

### Positional Computation System

$$\begin{gather} \textbf{Lemma 3: Base representation} \\ \text{For a fixed base } q > 1 \text{ and any } x > 0, \text{ there exists a unique integer } k \text{ such that } q^{k-1} \le x < q^k. \end{gather}$$

(see [proof](Proof%20of%20the%20Properties%20of%20Natural%20Numbers.md "null"))

This allows the construction of the positional $q$-ary system, where a positive number $x$ corresponds to a unique sequence of digits $a_p \dots a_{p-n} \dots$ representing rational approximations $r_n = \sum_{k=0}^n a_{p-k}q^{p-k}$ converging to $x$.
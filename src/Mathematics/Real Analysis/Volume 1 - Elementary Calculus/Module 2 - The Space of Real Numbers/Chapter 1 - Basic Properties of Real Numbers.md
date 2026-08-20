# The Axiom System and Some General Properties of the Set of Real Numbers

Mathematical theories find application because they allow the transformation of one set of numbers—the initial data or collection of inputs—into another set, representing the intermediate or final objective of computations—which are usually seen as outputs. Thus, numerical-valued functions hold a distinguished position in mathematics and its applications. These functions, specifically differentiable ones, form the core subject of classical real analysis. However, a complete description of these functions' properties necessitates a precise definition of the set of real numbers on which they operate.

The concept of numbers is fundamental, yet achieving a rigorous understanding requires abstraction. This chapter aims to construct the universe of real numbers that are utilized in basic algebra and arithmetic, but in a more non-ambiguous fashion.  Given that real numbers are one of the most basic abstractions in mathematics, a dedicated course could even be provided for this topic. However, this module seeks only to unify and explain what the reader already knows from highschool and their everyday experience with counting. 

---
# Definition of the Set of Real Numbers

$$\begin{gather} \textbf{Definition 1: The Set of Real Numbers} \\[5mm] \text{A set } \mathbb{R} \text{ is called the set of real numbers, and its elements are real numbers,} \\ \text{if it satisfies the axioms of addition and multiplication.} \end{gather}$$


### Axioms of Addition
$$
\begin{gather}
\textbf{Axiom: Rules of Addition} \\[5mm]
\text{An operation } \\[2.5mm] +:\mathbb{R} \times \mathbb{R}, \\[2.5mm] \text{ which is the operation of addition, is defined, according to each} \\
\text{ordered pair } (x,y) \text{ of elements } x,y \in \mathbb{R} \text{, which is the sum of  } x \text{ and } y\text{.} \\
\text{This operation satsfies the following conditions: } \\
\end{gather}
$$
$$
\begin{align}
& \text{1. There's a neutral element or identity element } 0 \text{, which is zero, such that } \\[2.5mm]
 & \mathmakebox[4][c]{x + 0 = 0 + x = x} \\[2.5mm]
& \text{2. For every element } x \in \mathbb{R}\text{, there's an element } -x \text{ such that } \\[2.5mm]
& \mathmakebox[3][c]{x + (-x) = (-x) + x = 0} \\[2.5mm] 
& \text{3. The operation } + \text{ is associative, that is, the relation } \\[2.5mm]
& \mathmakebox[3][c]{x + (y + z) = (x + y) + z} \\[2.5mm] 
& \text{4. The operation } + \text{ is commutative, that is, } \\[2.5mm]
& \mathmakebox[5.5][c]{x + y = y + x} \\[2.5mm]
\end{align}
$$

>[!info]+ Remark: Additive and Abelian Group 
> If an operation is defined on a set $G$ satisfying axioms 1-3, this is described as a *group structure* that's defined on $G$ or that $G$ is a group. If the operation is called addition, the group is an *additive group*. If it's also known that the operation is commutative, that is, condition 4 holds, the group is *commutative* or *Abelian.* Therefore, the four basic rules of addition assert that $\mathbb{R}$ is an additive abelian group. 

### (II) Axioms for Multiplication

An operation of multiplication is defined, $\cdot: \mathbb{R} \times \mathbb{R} \rightarrow \mathbb{R}$, assigning to each ordered pair $(x, y)$ a product $x \cdot y \in \mathbb{R}$. This operation satisfies:

1. **Existence of One:** There exists a neutral element $1 \in \mathbb{R} \setminus \{0\}$ such that $x \cdot 1 = 1 \cdot x = x$ for all $x \in \mathbb{R}$.
    
2. **Existence of an Inverse:** For every $x \in \mathbb{R} \setminus \{0\}$, there exists an element $x^{-1} \in \mathbb{R}$ such that $x \cdot x^{-1} = x^{-1} \cdot x = 1$.
    
3. **Associativity:** $x \cdot (y \cdot z) = (x \cdot y) \cdot z$ for all $x, y, z \in \mathbb{R}$.
    
4. **Commutativity:** $x \cdot y = y \cdot x$ for all $x, y \in \mathbb{R}$.
    

> [!info]- Remark: Multiplicative Group The set $\mathbb{R} \setminus \{0\}$ forms a multiplicative group. The combination of operations satisfying Axioms I and II defines a structure known as a field.

### (I, II) The Connection Between Addition and Multiplication

Multiplication is distributive with respect to addition:

$$(x + y)z = xz + yz$$

for all $x, y, z \in \mathbb{R}$. Due to commutativity, this also holds if the order of factors is reversed.

### (III) Order Axioms

There is a relation $\le$ between elements of $\mathbb{R}$, allowing comparison:

1. **Reflexivity:** $\forall x \in \mathbb{R} \ (x \le x)$.
    
2. **Antisymmetry:** $(x \le y) \wedge (y \le x) \implies (x = y)$.
    
3. **Transitivity:** $(x \le y) \wedge (y \le z) \implies (x \le z)$.
    
4. **Comparability (Linear Ordering):** $\forall x \in \mathbb{R} \ \forall y \in \mathbb{R} \ (x \le y) \lor (y \le x)$.
    

> [!info]- Remark: Ordering A set satisfying the first three conditions is partially ordered. The addition of the fourth condition makes $\mathbb{R}$ a linearly ordered set.

### Connection Axioms

- **(I, III) Connection Between Addition and Order:** If $x, y, z \in \mathbb{R}$, then $(x \le y) \implies (x + z \le y + z)$.
    
- **(II, III) Connection Between Multiplication and Order:** If $x, y \in \mathbb{R}$, then $(0 \le x) \wedge (0 \le y) \implies (0 \le x \cdot y)$.
    

### (IV) The Axiom of Completeness (Continuity)

If $X$ and $Y$ are nonempty subsets of $\mathbb{R}$ such that $x \le y$ for every $x \in X$ and every $y \in Y$, then there exists $c \in \mathbb{R}$ such that $x \le c \le y$ for all $x \in X$ and $y \in Y$.

> [!info]- Remark: Consistency and Categoricity This axiomatic system is consistent (a model can be constructed using set theory) and categorical (any two models satisfying these axioms are isomorphic, meaning there exists a bijective correspondence preserving arithmetic operations and order).

## General Algebraic Properties of Real Numbers

From these axioms, the familiar properties of numbers can be rigorously deduced.

$$\begin{gather} \textbf{Proposition 1: Consequences of the Addition Axioms} \\ \text{1. There is only one zero in the set of real numbers.} \\ \text{2. Each element of the set of real numbers has a unique negative.} \\ \text{3. In the set } \mathbb{R}, \text{ the equation } a + x = b \text{ has the unique solution } x = b + (-a) =: b - a. \end{gather}$$

(see [proof](placeholder_link "null"))

$$\begin{gather} \textbf{Proposition 2: Consequences of the Multiplication Axioms} \\ \text{1. There is only one multiplicative unit (one) in the real numbers.} \\ \text{2. For each } x \ne 0, \text{ there is only one reciprocal } x^{-1}. \\ \text{3. For } a \in \mathbb{R} \setminus \{0\}, \text{ the equation } a \cdot x = b \text{ has the unique solution } x = b \cdot a^{-1}. \end{gather}$$

(see [proof](placeholder_link "null"))

$$\begin{gather} \textbf{Proposition 3: Consequences of the Connection Axiom} \\ \text{For any } x, y \in \mathbb{R}: \\ \text{1. } x \cdot 0 = 0 \cdot x = 0. \\ \text{2. } (x \cdot y = 0) \implies (x = 0) \lor (y = 0). \\ \text{3. } -x = (-1) \cdot x. \\ \text{4. } (-1)(-x) = x. \\ \text{5. } (-x) \cdot (-x) = x \cdot x. \end{gather}$$

(see [proof](placeholder_link "null"))

$$\begin{gather} \textbf{Proposition 4: Consequences of the Order Axioms} \\ \text{Strict inequality } x < y \text{ denotes } x \le y \text{ and } x \ne y. \\ \text{1. For any } x, y \in \mathbb{R}, \text{ precisely one holds: } x < y, x = y, x > y. \\ \text{2. For any } x, y, z \in \mathbb{R}: \\ (x < y) \wedge (y \le z) \implies (x < z) \\ (x \le y) \wedge (y < z) \implies (x < z) \end{gather}$$

(see [proof](placeholder_link "null"))

$$\begin{gather} \textbf{Proposition 5: Consequences of Order with Addition and Multiplication} \\ \text{For any } x, y, z, w \in \mathbb{R}: \\ \text{1. } (x < y) \implies (x + z) < (y + z) \\ \text{2. } (0 < x) \implies (-x < 0) \\ \text{3. } (x \le y) \wedge (z \le w) \implies (x + z) \le (y + w) \\ \text{4. } (x \le y) \wedge (z < w) \implies (x + z < y + w) \\ \text{5. } (0 < x) \wedge (0 < y) \implies (0 < xy) \\ \text{6. } (x < 0) \wedge (y < 0) \implies (0 < xy) \\ \text{7. } (x < 0) \wedge (0 < y) \implies (xy < 0) \\ \text{8. } (x < y) \wedge (0 < z) \implies (xz < yz) \\ \text{9. } (x < y) \wedge (z < 0) \implies (yz < xz) \\ \text{10. } 0 < 1 \\ \text{11. } (0 < x) \implies (0 < x^{-1}) \\ \text{12. } (0 < x) \wedge (x < y) \implies (0 < y^{-1}) \wedge (y^{-1} < x^{-1}) \end{gather}$$

(see [proof](placeholder_link "null"))

## The Completeness Axiom and Bounds

$$\begin{gather} \textbf{Definition 2: Bounded Sets} \\ \text{A set } X \subset \mathbb{R} \text{ is bounded above (respectively, bounded below) if there} \\ \text{exists a number } c \in \mathbb{R} \text{ such that } x \le c \text{ (respectively, } c \le x \text{) for all } x \in X. \\ \text{The number } c \text{ is called an upper bound (majorant) or lower bound (minorant).} \\ \text{A set bounded both above and below is called bounded.} \end{gather}$$$$\begin{gather} \textbf{Definition 3: Maximal and Minimal Elements} \\ \text{An element } a \in X \text{ is the largest or maximal element (} \max X \text{) if } x \le a \text{ for all } x \in X: \\ (a = \max X) := (a \in X) \wedge \forall x \in X (x \le a). \\ \text{Similarly, for the minimal element (} \min X \text{):} \\ (a = \min X) := (a \in X) \wedge \forall x \in X (a \le x). \end{gather}$$

Not every bounded set has a maximal or minimal element (e.g., $X = \{x \in \mathbb{R} \mid 0 \le x < 1\}$ has no maximum).

$$\begin{gather} \textbf{Definition 4: Least Upper Bound and Greatest Lower Bound} \\ \text{The least upper bound (supremum) of a set } X \text{ bounded above is denoted } \sup X: \\ (s = \sup X) := \forall x \in X (x \le s) \wedge \forall s' < s \ \exists x' \in X (s' < x'). \\ \text{The greatest lower bound (infimum) of a set } X \text{ bounded below is denoted } \inf X: \\ (i = \inf X) := \forall x \in X (i \le x) \wedge \forall i' > i \ \exists x' \in X (x' < i'). \end{gather}$$$$\begin{gather} \textbf{Lemma 1: The Least Upper Bound Principle} \\ \text{Every nonempty set of real numbers that is bounded from above has a} \\ \text{unique least upper bound.} \end{gather}$$

(see [proof](placeholder_link "null"))

$$\begin{gather} \textbf{Lemma 2: The Greatest Lower Bound Principle} \\ \text{Every nonempty set of real numbers that is bounded from below has a} \\ \text{unique greatest lower bound.} \end{gather}$$

(see [proof](placeholder_link "null"))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            
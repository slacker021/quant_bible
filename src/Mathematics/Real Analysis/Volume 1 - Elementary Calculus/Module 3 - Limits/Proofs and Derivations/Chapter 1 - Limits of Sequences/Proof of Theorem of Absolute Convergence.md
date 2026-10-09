---
dg-publish: true
---
By definition, the series $\sum_{n=1}^{\infty} x_n$ is absolutely convergent if the series of absolute values, $\sum_{n=1}^{\infty} |x_n|$, converges to some finite limit $S$.

The [[Proof of the Cauchy Criterion for Sequences|Cauchy Criterion]] states that a series $\sum_{n=1}^{\infty} x_n$ converges if and only if for every $\varepsilon > 0$, there exists an integer $N$ such that for all $m > n > N$, the partial sum of the remaining terms satisfies
$$
\left| \sum_{k=n+1}^{m} x_k \right| < \varepsilon \tag{1}
$$
Consider the series $\sum_{n=1}^{\infty} |a_n|$. Since this series is given as absolutely convergent, it must satisfy the Cauchy Criterion. Therefore, for any $\varepsilon > 0$, there exists a positive integer $N$ such that for all $m > n > N$, 
$$
\sum_{k=n+1}^{m} |x_k| < \varepsilon
$$
Now, consider the original series $\sum_{n=1}^{\infty} a_n$. Examining the partial sums for $m > n > N$ shows that
$$
\left| \sum_{k=n+1}^{m} x_k \right| \tag{2}
$$
By applying the [[Proof of the Triangle Inequality|Triangle Inequality]]:
$$
\left| \sum_{k=n+1}^{m} x_k \right| \le \sum_{k=n+1}^{m} |x_k| \tag{3}
$$
Substituting the result from the Cauchy Criterion for the series of absolute values, it follows that:
$$
\left| \sum_{k=n+1}^{m} x_k \right| < \varepsilon \tag{4}
$$
Since the series $\sum_{n=1}^{\infty} x_n$ satisfies the Cauchy Criterion, it is concluded that the series is convergent.
$$
\textbf{Q.E.D.}
$$

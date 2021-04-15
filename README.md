# data-structer

given a multiplicative function $f(n)$, where $f(p^c)$ is a polynomial of $p$.
Find the value of $F(n) = \sum\limits_{1 \le x \le n} f(x)$
$F(n) = \sum\limits_{\substack{1 \le x \le n \\ \not \exists p > \sqrt{n}, p \mid x}} f(x) (1 + \sum\limits_{\sqrt{n} < p \le \lfloor \frac{n}{x} \rfloor}f(p))$
$F(n)=f(1, n)+\sum\limits_{1 \le x \le \sqrt{n}}f(x)(g(\lfloor \frac{n}{x} \rfloor)-g(\sqrt{n}))$, where $g(n)=\sum\limits_{1 \le p \le n}f(p)$, $f(1,n)=\sum\limits_{\substack{1 \le x \le n \\ \not \exists p > p_m, p \mid x}} f(x)$ and $p_m$ is the largest prime less than or equal to $\sqrt{n}$.
$f(i,n)=\sum\limits_{\substack{1 \le x \le n \\ \not \exists p > p_m \text{or } p < p_{i}, p \mid x}} f(x)$, $f(i,n)=f(i+1,n)+\sum\limits_{c \ge 1}f(i+1, \lfloor \frac{n}{p_i^c}\rfloor)$.
the following program is an example of \sum_{i=1}^{n} \sigma_0(i^m)

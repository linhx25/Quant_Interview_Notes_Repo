# Math, Calculus and Differential Equation

## 1. What's the value of $i^i$, where $i=\sqrt{-1}$ ?
By Euler's formula, we have $e^{i\theta} = cos\theta + isin\theta$;
Therefore, $e^{i\frac{\pi}{2}} = cos\frac\pi2 + isin\frac \pi 2 = i$, $i^i = (e^{i\frac \pi 2})^i = e^{-\frac \pi 2}$.

## 2. Which is larger: $\pi^e$ or $e^\pi$
We could solve this by comparing $\pi$ and $e\ln\pi$.
Let $f(x):=x-e\ln x$, we have $f'(x) =1-\frac e x$, $f''(x) = \frac e {x^2} \geq 0$;
Therefore, $f(e)=0$ is the minimum, $f(\pi)>f(e)=0 \iff \pi > e\ln \pi \iff e^\pi > \pi ^e$.

## 3. Show that $\frac {e^x+e^y} 2 \geq e^{\frac {x+y} 2}$
This is a special case of Jensen's Equation. However, we can solve it by another way:
Squaring both sides, we derive $\frac 1 4 (e^{2x}+e^{2y}+2e^{x+y}) - e^{x+y} = \frac 1 4 (e^{2x}+e^{2y}-2e^{x+y})=(\frac {e^x-e^y} 2)^2 \geq 0$.

## 4. Solve $x^6=64$
Recall the solution of n-th unit root: $z^n = 1$, it has n roots: $\omega_0,...,\omega_n$, where $\sum\omega_i = 0, \omega_i = e^{i\frac {2k\pi} n}$.
Hence, we have 6 unit roots $\omega_i = e^{i\frac {k\pi} 3}, k=0,1,2,3,4,5$. Knowing that $\sqrt[6]{64} = 2$, so the solution should be $2e^{i\frac {k\pi} 3},k=0:5$.

## 5. Derivative of $x^x$
$(x^x)' = (e^{x\ln x})' = e^{x\ln x}(1+\ln x)$

## 6. Calculate $\sqrt{2+\sqrt{2+\sqrt{2+...}}}$
Given its existence, we could denote $x:=\sqrt{2+\sqrt{2+\sqrt{2+...}}}$, then $x^2 = 2+x \Rightarrow (x+1)(x-2)=0 \Rightarrow x=-1 \,or\,2$, since $x\gt 0$, then 2 is the answer. 

How to ensure its existence? By monotone bounded convergence theorem, we should prove:
(1) the series is bounded by upper limit 2.
(2) the series is montone increasing.
For (1), it is easy to proove by induction.
For (2), for case k, $x_k > x_{k-1} \iff x_k > \sqrt{x_k^2 -2}$,
for case k+1, $x_{k+1} = \sqrt{2+x_k} > \sqrt{x_k^2} =x_k$.
Hence we proove the convergence.

## 7. Find x such that $x^{x^{x^{.^.}}}=2$
Given its existence, we have $x^2 = 2 \Rightarrow x = \sqrt 2$ is a solution.
To show its existence, we applied monotone bounded convergence theorem.
(1)The series is bounded by upper limit 2; (induction)
(2)The series is montone increasing; (induction)
With the convergence prooved, we can calculate the limit of $x_n = \sqrt 2^{x_{n-1}}$, let the limit denoted by $x$, then $\ln x = x\ln \sqrt2$, we have a solution $x=2$. To prove its uniqueness, let $f(x) = \frac {\ln x} x$, $f'(x) = \frac 1 {x^2}(1-\ln x)$, with $x=e$ is the global maximum. Here we have the solution of $f(x)=\ln {\sqrt2}$ in $(0,e)$ should be unique.

## 8.Convergence: $\sum_{k=1}^{\infty}\frac 1 {k^2}$,$\sum_{k=1}^{\infty}\frac 1 {k}$,$\sum_{k=1}^{\infty}\frac 1 {k\ln k}$
(1)$\sum_{k=1}^{\infty}\frac 1 {k^2}=1+\sum_{k=2}(\frac 1 {k-1}-\frac 1 k)<2$: Convergent.
(2)$\sum_{k=1}^{\infty}\frac 1 k$, first proove $\int_1^n\frac 1 x dx<-\frac 1 n + \sum_{k=1}^n\frac 1 k$, then we have $\sum_{k=1}^n\frac 1 k >\ln n\, ,\forall n$, then we show the divergence.
(3)$\sum_{k=1}^{\infty}\frac 1 {k\ln k}$ should be divergent using similar proof as (2).

## 9. Compute $\int \frac 1 {1+x^2}dx$
$arctan x+C$, remember that $tan'x=sec^2x,\quad1+tan^2x=sec^2x$

## 10. Compute $\int x \ln x dx$ and $\int x e^x dx$
$\frac 1 2 x^2\ln x-\frac 1 4 x^2+C$; $e^x(x-1)+C$

## 11. Compute $\int x^n \ln xdx$
$\frac 1 {n+1}x^{n+1}(\ln x - \frac 1 {n+1})+C,\, n\neq-1$
$\frac 1 2 (\ln x)^2+C,\, n=-1$ 

## 12. Compute $\int \ln^n xdx$
let $I(n)=\int \ln^n xdx = x\ln^n x - nI(n-1)$, and $I(1) = x(\ln x -1)$, then we have $I(n) = \sum_{k=0}^n  \frac {(-1)^kn!}{(n-k)!}x\ln ^{n-k}x+C$

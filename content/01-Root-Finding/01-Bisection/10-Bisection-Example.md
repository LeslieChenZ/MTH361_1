# Bisection Method Example

> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.


## Problem
Given $f(x)=x^5-x^4+x^3+2$.

1. Prove that $f(x)$ has a root on the interval $[-1,1]$.
2. Use bisection to find an approximate solution with accuracy $10^{-3}$.
3. Estimate the number of iterations needed to achieve accuracy $10^{-3}$.
4. Find an upper bound for $|p_5-p|$.

## 1) Existence of a root on $[-1,1]$
Compute endpoint values:
- $f(-1)=(-1)^5-(-1)^4+(-1)^3+2=-1-1-1+2=-1$
- $f(1)=1-1+1+2=3$

Since $f$ is a polynomial, it is continuous on $[-1,1]$. Because $f(-1)f(1)<0$, there exists $p\in(-1,1)$ such that $f(p)=0$.

## 2) Bisection with accuracy $10^{-3}$
Run bisection on $[-1,1]$ and stop when the chosen stopping criterion indicates error at most $10^{-3}$.

## 3) Iteration count estimate for accuracy $10^{-3}$
Using the bound
$$
|p-p_n|\le \frac{b-a}{2^{n+1}},
$$
<!-- LaTeX source (fallback):
|p-p_n| <= (b-a)/2^{n+1}
-->
with $b-a=2$, it suffices to have
$$
\frac{2}{2^{n+1}}\le 10^{-3}
\quad\Longleftrightarrow\quad
2^n\ge 10^3,
$$
<!-- LaTeX source (fallback):
2/2^{n+1} <= 1e-3  <=>  2^n >= 1e3
-->
so we can take
$$
n \ge \lceil \log_2(10^3)\rceil = 10.
$$
<!-- LaTeX source (fallback):
n >= ceil(log2(1e3)) = 10
-->

## 4) Upper bound for $|p_5-p|$
After 5 iterations,
$$
|p-p_5|\le \frac{b-a}{2^{6}}=\frac{2}{64}=\frac{1}{32}\approx 3.125\times 10^{-2}.
$$
<!-- LaTeX source (fallback):
|p-p_5| <= (b-a)/2^6 = 2/64 = 1/32
-->

## MATLAB verification (short snippet)
Summary: Run the bisection solver on $f(x)=x^5-x^4+x^3+2$ on $[-1,1]$ and display iteration data.
```matlab
% Solve: f(x) = x^5 - x^4 + x^3 + 2 = 0 on [-1,1]
clear; clc; close all;
format shortE

f = @(x) x.^5 - x.^4 + x.^3 + 2;

a    = -1;
b    =  1;
tol  = 1e-3;
nmax = 1000;

[x, xdiff, fx, nit] = bisect(a,b,tol,nmax,f);

disp('-------------------------------------------')
disp('   x_k       |x_k - x_{k-1}|    f(x_k)')
disp('-------------------------------------------')
disp([x, xdiff, fx])
```

## Table: first 5 iterates
| Iteration | $x_k$ | $f(x_k)$ |
|---:|---:|---:|
| 1 | 0 | 2 |
| 2 | -0.5 | 1.7812 |
| 3 | -0.75 | 1.0244 |
| 4 | -0.875 | 0.23099 |
| 5 | -0.9375 | -0.32065 |

## Figure (export from MATLAB)
![Plot of $f(x)$ on $[-1,1]$ with a dashed line $y=0$ and red markers showing the first five bisection iterates.](../assets/rootfinding-bisection-first5-iterates.png)

*Figure: Function and first 5 bisection iterates for $f(x)=x^5-x^4+x^3+2$ on $[-1,1]$.*

# Bisection Method Example

> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.


## Problem
Given $f(x)=x^5-x^4+x^3+2$.

1. Prove that $f(x)$ has a root on the interval $[-1,1]$.
2. Use the bisection method to find an approximate solution with accuracy $10^{-3}$.
3. Estimate the number of iterations needed to find an approximate solution with accuracy $10^{-3}$.
4. Find an upper bound for $|p_5-p|$, where $p$ is the exact root and $p_5$ is the bisection approximation after 5 iterations.

## Table: first 5 iterates
| Iteration | $x_k$ | $f(x_k)$ |
|---:|---:|---:|
| 1 | 0 | 2 |
| 2 | -0.5 | 1.7812 |
| 3 | -0.75 | 1.0244 |
| 4 | -0.875 | 0.23099 |
| 5 | -0.9375 | -0.32065 |

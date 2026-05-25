# Bisection Method Stopping Criteria

> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.


## Common stopping criteria
In practice you may stop when one of the following is satisfied.

## Criterion 1 (interval-based)
Stop when the error bound from the interval is below tolerance. A common choice is:
$$
\frac{1}{2}|b_k-a_k|\le \text{tol}.
$$
<!-- LaTeX source (fallback):
(1/2)|b_k-a_k| <= tol
-->

## Criterion 2 (relative change)
Stop when a relative change measure based on successive iterates is small (choose carefully).

## Criterion 3 (function value)
Stop when $|f(p_k)|\le \text{tol}$.

<!-- LaTeX source (fallback):
|f(p_k)| <= tol
-->

## Caution
Difficulties can arise using any stopping criterion. Choose wisely.

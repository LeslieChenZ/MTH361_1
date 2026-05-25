---
cssclasses:
  - wide-page
---
# Fixed-Point Convergence Theorem

---
<!-- .slide: data-visibility="hidden" -->
> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.

---
## Theorem (fixed-point theorem)

1. Condition 1 (invariance)
$g(x)\in[a,b]$ for all $x\in[a,b]$.

<!-- LaTeX source (fallback):
g(x) in [a,b] for all x in [a,b]
-->

2. Condition 2 (contraction)
There exists a constant $k$ such that
$$
|g'(x)|\le k<1 \quad \text{for all } x\in[a,b].
$$
<!-- LaTeX source (fallback):
|g'(x)| <= k < 1 for all x in [a,b]
-->

---
Then for any initial approximation $x_0\in[a,b]$, the sequence defined by
$$
x_{n+1}=g(x_n)
$$
converges to the unique fixed point in $[a,b]$.

<!-- LaTeX source (fallback):
x_{n+1}=g(x_n)
-->
---
## Corollary (error estimate) — TODO
Extract and insert the exact corollary lines from the full HTML.


---

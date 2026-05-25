---
cssclasses:
  - wide-page
---
# Existence and Uniqueness of a Fixed Point

---
<!-- .slide: data-visibility="hidden" -->
> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.

---
## Theorem (existence and uniqueness of a fixed point)

## Existence
If $g(x)\in[a,b]$ for all $x\in[a,b]$, then $g$ has at least one fixed point in $[a,b]$.

<!-- LaTeX source (fallback):
g(x) in [a,b] for all x in [a,b]
-->

---
## Uniqueness
If, in addition, there exists a constant $k$ such that
$$
|g'(x)|\le k<1 \quad \text{for all } x\in[a,b],
$$
<!-- LaTeX source (fallback):
|g'(x)| <= k < 1 for all x in [a,b]
-->
then the fixed point in $[a,b]$ is unique.

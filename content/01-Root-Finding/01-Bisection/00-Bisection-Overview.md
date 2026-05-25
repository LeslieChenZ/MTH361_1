---
cssclasses:
  - wide-page
---
# Bisection Method

---
<!-- .slide: data-visibility="hidden" -->
> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.

---
## Goal
Approximate a root $p$ of $f(x)=0$ on an interval $[a,b]$ where the function changes sign.

---
## Assumptions
- $f$ is continuous on $[a,b]$
- $f(a)f(b)<0$

By the Intermediate Value Theorem, there exists at least one root $p\in(a,b)$.

---
## Algorithm (bisection)
Let $a_0=a$ and $b_0=b$.

For $k=0,1,2,\dots$:
1. Compute midpoint
   $$
   p_{k+1}=\frac{a_k+b_k}{2}.
   $$
   <!-- LaTeX source (fallback):
   p_{k+1} = (a_k+b_k)/2
   -->
2. Evaluate $f(p_{k+1})$.
3. Update the interval:
   - if $f(a_k)f(p_{k+1})>0$, set $a_{k+1}=p_{k+1}$ and $b_{k+1}=b_k$;
   - otherwise set $a_{k+1}=a_k$ and $b_{k+1}=p_{k+1}$.

---
## Error bound (interval-based)
After $n$ bisection steps,
- the interval length is
  $$
  b_n-a_n = \frac{b-a}{2^n},
  $$
  <!-- LaTeX source (fallback):
  b_n - a_n = (b-a)/2^n
  -->
- and the midpoint approximation $p_n$ satisfies the common bound
  $$
  |p-p_n|\le \frac{b-a}{2^{n+1}}.
  $$
  <!-- LaTeX source (fallback):
  |p-p_n| <= (b-a)/2^{n+1}
  -->

---
## Remarks
- Bisection cannot find zeros where the graph only *touches* the $x$-axis (no sign change). Example: $f(x)=x^2$.
- If there are multiple zeros in $[a,b]$, applying bisection to $[a,b]$ finds one root (depending on the sign checks). To locate others, use different intervals.

## Next
- [Stopping criteria](./02-Bisection-Stopping-Criteria.md)
- [Worked example](./10-Bisection-Example.md)

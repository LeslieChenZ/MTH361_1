---
cssclasses:
  - wide-page
---
# Fixed-Point Iterations

---
<!-- .slide: data-visibility="hidden" -->
> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.

---
## Goal
Solve a root-finding problem $f(x)=0$ by rewriting it in fixed-point form: $x=g(x)$.

---
## Iteration
Choose an initial approximation $x_0$ and define
$$
x_{n+1}=g(x_n), \quad n=0,1,2,\dots
$$
<!-- LaTeX source (fallback):
x_{n+1}=g(x_n)
-->

---
## Key question
To solve a root-finding problem $f(x)=0$, there are many ways to write it into a fixed-point form $x=g(x)$. What kind of $g$ should we choose?

---
## Contents
- [Definition of a fixed point](./01-Fixed-Point-Definition.md)
- [Existence and uniqueness of a fixed point](./02-Fixed-Point-Existence-Uniqueness.md)
- [Fixed-point convergence theorem](./03-Fixed-Point-Convergence-Theorem.md)
- [Examples](./10-Fixed-Point-Examples.md)
- [MATLAB (full code)](./90-Fixed-Point-MATLAB-Full-Code.md)

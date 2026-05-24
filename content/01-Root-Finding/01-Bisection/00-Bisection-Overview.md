# Bisection Method

> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.


## Purpose
Use a sign change on an interval to iteratively narrow down where a root $p$ of $f(x)=0$ lies.

## Key prerequisite
Continuity on $[a,b]$ plus a sign change: $f(a)f(b)<0$.

## Linked theory
- [Intermediate Value Theorem](./01-Intermediate-Value-Theorem.md)

## Algorithm (conceptual)
1. Start with an interval $[a,b]$ such that $f(a)f(b)<0$.
2. Compute the midpoint $c=\dfrac{a+b}{2}$.
3. Decide which half-interval still contains a sign change:
   - if $f(c)f(a)>0$, replace $a \leftarrow c$,
   - otherwise replace $b \leftarrow c$.
4. Repeat until a stopping criterion is met.

---
cssclasses:
  - wide-page
---
# Root Finding / Solution of Equations

> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.


## Problems
Solving nonlinear equations: find $x$ such that $f(x)=0$.

## Numerical methods for finding a root (solution) of an equation
These are iterative methods:
- Bisection method
- Fixed-point iteration method
- Newton’s method

We hope that $x_n \to p$ where $f(p)=0$.

## Remark
It may take forever to find the exact solution $p$. What we can get is an approximate solution $x_n$.

## Questions
1. How do we start the iteration (choose $x_0$ or an initial interval)?
2. Are the approximate solutions $x_n$ convergent to the exact solution $p$?
3. When should we terminate the iteration?

## Table of contents (Topic 1)
- [1.1 Bisection Method](./01-Bisection/00-Bisection-Overview.md)  
  - [Intermediate Value Theorem](./01-Bisection/01-Intermediate-Value-Theorem.md)
  - [Stopping Criteria](./01-Bisection/02-Bisection-Stopping-Criteria.md)
  - [Worked Example](./01-Bisection/10-Bisection-Example.md)
  - [MATLAB Code (Full)](./01-Bisection/90-Bisection-MATLAB-Full-Code.md)
- [1.2 Fixed-Point Iterations](./02-Fixed-Point/00-Fixed-Point-Overview.md)
- [1.3 Newton's Method](./03-Newton/00-Newton-Overview.md)
- [1.4 Alternatives to Newton's method](./04-Alternatives/00-Alternatives-Overview.md)
- [1.5 Error Analysis for Iterative Methods](./05-Error-Analysis/00-Error-Analysis-Overview.md)
- [1.6 Accelerating Convergence](./06-Accelerating-Convergence/00-Accelerating-Convergence-Overview.md)

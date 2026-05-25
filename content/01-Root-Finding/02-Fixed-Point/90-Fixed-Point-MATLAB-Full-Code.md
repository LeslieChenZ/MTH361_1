---
cssclasses:
  - wide-page
---
# MATLAB Code: Fixed-Point Iterations (Full)

---
<!-- .slide: data-visibility="hidden" -->
> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.

---
## Example: contraction test for $g(x)=x^2$
Summary: Plot $g(x)=x^2$ and test the contraction condition on $[-1/3,1/3]$ using $\max |g'(x)|$.
```matlab
clear; clc; close all;

g = @(x) x.^2;

x = linspace(-1,1,400);
figure
plot(x, g(x), 'b', 'LineWidth',2); hold on
plot(x, x, 'k--', 'LineWidth',1.5)
grid on
xlabel('x')
ylabel('y')
title('Function g(x) = x^2')
legend('g(x)=x^2','y=x','Location','northwest')
axis equal

syms x
g_sym = x^2;
dg = diff(g_sym, x);

x_small = linspace(-1/3,1/3,400);
dg_fun = matlabFunction(dg);

max_derivative = max(abs(dg_fun(x_small)));
fprintf('Maximum value of |g''(x)| on [-1/3,1/3]:\n')
fprintf('%.4f\n', max_derivative)

if max_derivative < 1
    fprintf('\ng(x) is a contraction on [-1/3,1/3].\n')
else
    fprintf('\ng(x) is NOT a contraction on [-1/3,1/3].\n')
end
```

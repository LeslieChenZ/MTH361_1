---
cssclasses:
  - wide-page
---
# MATLAB Code: Bisection Method (Full)

---
<!-- .slide: data-visibility="hidden" -->
> [!info]   Attribution
> - Created by Dr. Zheng Chen (UMass Dartmouth Math Department).
> - Date Modified: `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.DATE_MED_WITH_WEEKDAY))`, `$= dv.el('span', dv.current().file.mtime.toLocaleString(DateTime.TIME_WITH_SHORT_OFFSET))`.

---
## Function: bisect.m
Summary: Implement the bisection method to approximate a root of $f(x)=0$ on an interval $[a,b]$.
```matlab
function [xvect,xdif,fx,nit]=bisect(a,b,tol,nmax,fun)
    err=tol+1;
    nit=0;
    xvect=[]; fx=[]; xdif=[];
    while nit<nmax && err>tol
        nit=nit+1;
        c=(a+b)/2;
        x=c; fc=feval(fun,x);
        xvect=[xvect;x]; fx=[fx;fc]; x=a;
        err=0.5*abs(b-a); xdif=[xdif;err];
        if fc*feval(fun,x)>0
            a=c;
        else
            b=c;
        end
    end
    if nit == nmax
        fprintf("Stop: Bisection method does not converge after %i iterations.",nmax);
    end
return
```

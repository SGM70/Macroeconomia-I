---
jupytext:
  formats: ipynb,md:myst
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.14.1
kernelspec:
  display_name: Python 3 (ipykernel)
  language: python
  name: python3
---

El Modelo de Solow
===================

```{code-cell} ipython3
%cd /home/sam/Lab/intro
from pymacro.functions import *
from pymacro.gen import *
import enum
from collections import OrderedDict
from abc import ABC, ABCMeta, abstractmethod
from sympy import symbols, Eq, solve, diff, dsolve, Function, log
from tabulate import tabulate

from typing import List

t, alpha, s, n, g, delta =\
    symbols('t alpha s n g delta', positive=True)
k = Function('k', positive=True)(t)
a, b, x0 = symbols('a b x_0')
x = Function('x')(t)

solow = {
        'capital per units of efficiency labor': k,\
        'capital share, alpha': alpha,\
        'maginal propensity to save': s,\
        'rate of population growth' : n,\
        'rate of exogenous growth': g,\
        'rate of capital depretiation': delta,\
        'Default values': {
                            alpha: .3,
                            's': .25,
                            n: .01,
                            g: .02,
                            delta: .07
                            }
        }
default = {alpha:.3, s:0.8, n:.01, g:.04, delta:.07}

def simple_ode(a=symbols('a'),b=symbols('b'), x=Function('x')(t)):
    rhs = a*x+b
    eq = Eq(diff(x,t), rhs)
    sol = dsolve(eq,x)
    c = list(sol.free_symbols.difference({a,b,t}))[0]
    x0 = sol.subs({t:0})
    d = solve(x0,c)[0]
    return sol.subs(c,d)

@autorepr
class Solow(object): 
    model_data = Gen(solow) 
    rhs = s*k**alpha - (n+g+delta)*k
    abstract_eq = Eq(diff(k, t), rhs)
    A, B  = -(n+g+delta), s/(1-alpha)
    D = {a:A, b:B}
    abstract_sol = simple_ode().subs(D).simplify()
```

```{code-cell} ipython3
Gen(solow).info()
```

```{code-cell} ipython3
Solow().abstract_eq
```

```{code-cell} ipython3
Solow().abstract_sol
```

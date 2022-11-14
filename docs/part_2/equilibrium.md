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

Equilibrio
===========

```{code-cell} ipython3

%cd /home/sam/Lab/intro
from pymacro.diccionarios import *
from pymacro.gen import *
from sympy import Eq

islm = {**is_dict, **lm_dict}

_A, _b, _c, _pi = symbols('A b c, \pi')
_m, _h, _k = symbols('m h k')

@autorepr
class IS(object):
    data = Gen(is_dict)  
    para = list(is_dict.values())[1:]
    default = data.default[0]
    A:float = default['A']
    b:float = default['b']
    c:float = default['c']
    def rhs(A,b,c, pi):
        return A + c*Y - b*(i-pi)
    abstract = Eq(Y, rhs(_A,_b,_c, _pi))
    numerical = Eq(Y, rhs(*list(default.values()))).simplify()
    
@autorepr    
class LM(object):
    data = Gen(lm_dict)
    para = list(is_dict.values())[1:]
    default = data.default[0]
    m:float = default['m']
    h:float = default['h']
    k:float = default['k']
    def rhs(a,b):
        return a*Y - b*i
    lm_abstract = Eq(_m, rhs(_h,_k))
    lm_numerical = Eq(m, rhs(h,k))
    
@autorepr
class ISLM(IS, LM):
    model_data = Gen(islm) 
```

```{code-cell} ipython3
ISLM = ISLM()
```

```{code-cell} ipython3
ISLM
```

```{code-cell} ipython3
ISLM.data.info()
```

```{code-cell} ipython3
IS.
```

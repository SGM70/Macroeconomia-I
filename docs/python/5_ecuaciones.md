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

```{code-cell} ipython3
def find_max(nums):
    max_num = float("-inf") # smaller than all other numbers
    for num in nums:
        if num > max_num:
            return max_num
```

```{code-cell} ipython3
find_max([1,3,5,6])
```

# Ecuaciones Básicas

bla bla

```{code-cell} ipython3
from sympy import Symbol, solve
x = Symbol('x')
y = Symbol('y')
expr = x - 12
solve(expr)[0]
```

```{code-cell} ipython3
from sympy import exp, symbols
a, b, c, d = symbols('a b c d')
expr =  exp(a)-b
solve(expr,a)
```

```{code-cell} ipython3
from sympy import init_printing
init_printing(order='rev-lex')
expr = a*x**2 + b*x + c
solve(expr,x)
```

```{code-cell} ipython3
expr1 = a*x + b*y
expr2 = c*x + d*y
expr = [expr1, expr1]
solve(expr, [x,y])
```

```{code-cell} ipython3
θ1, θ2 = symbols('theta_1 theta_2')
expr1 = a*x + b*y - θ1
expr2 = c*x + d*y - θ2
expr = [expr1, expr2]
Δ = a*d - b*c
solve(expr, [x,y])
```

$$\lim_{n\to \infty}x\left(1+\frac{r}{n}\right)^{nt}$$

```{code-cell} ipython3
from sympy import symbols, Limit, S
x, r, t, n = symbols('x r t n', positive=True)
Limit(x*(1+r/n)**(n*t), n, S.Infinity).doit()
```

```{code-cell} ipython3
from sympy import Matrix, simplify, symbols, pprint
A = Matrix(2,2,symbols('a1:3(1:3)'))
b = Matrix(2,1,symbols('b1:3'))
x = simplify(A.LUsolve(b))
pprint(A)
pprint(b)
x
```

```{code-cell} ipython3
from sympy import sin, log, Derivative, Integral
```

```{code-cell} ipython3
x = symbols('x')
y = symbols('y', positive=True)
```

```{code-cell} ipython3
f = sin(x*log(y))
```

```{code-cell} ipython3
Derivative(f,x).doit()
```

```{code-cell} ipython3
Integral(f,x).doit()
```

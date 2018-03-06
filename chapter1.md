---
title: Solving Matrix Equations
description: >-
  Test


---
## The long way

```yaml
type: NormalExercise
lang: python
xp: 100
skills: 2
key: c5511f767e
```

'Solving' matrices is a basic concept in linear algebra.

Let's take a problem $\mathbf{Ax}=\mathbf{b}$.

where the variables are:

$\mathbf{A} = \left[
\begin{array}{ccc}
    2& 1 & 1\\
    1 & 3 & 0\\
    1 & 0 & 0
\end{array}
\right]$ , 
$\mathbf{x} = \left[
\begin{array}{ccc}
    a\\
    b\\
    c
\end{array}
\right]$
,
$\mathbf{b} = \left[
\begin{array}{ccc}
    4\\
    5\\
    6
\end{array}
\right]$

This is a standard matrix problem where we want to solve for $\mathbf{x}$.

The standard approach to solve this would be:

$\mathbf{A^{-1}Ax}=\mathbf{x}=\mathbf{A^{-1}b}$

So the solution for $\mathbf{x}$ can be found by taking the inverse of $\mathbf{A}$ and dotting it with $\mathbf{b}$.




`@sample_code`
```{python}
import numpy as np

# define matrix A using Numpy arrays 
A = np.array([[2, 1, 1], [1, 3, 2], [1, 0, 0]]) 

#define matrix b 
b = np.array([4, 5, 6]) 

x = np.linalg.inv(...).dot(...)

print("Solution:\n", x)
```
`@solution`
```{python}
import numpy as np

# define matrix A using Numpy arrays 
A = np.array([[2, 1, 1], [1, 3, 2], [1, 0, 0]]) 

#define matrix b 
b = np.array([4, 5, 6]) 

x = np.linalg.inv(A).dot(b)

print("Solution:\n", x)
```
`@sct`
```{python}
Ex().check_object('x').has_equal_value()
success_msg('Great job!')
```





---
## Using `linalg.solve()`

```yaml
type: NormalExercise

xp: NaN

key: 632f323c4b
```

Whilst this can be implemented simply in Python, taking the inverse of matrices is computationally expensive and may not be feasible.

A range of methods exist for solving these types of problem - the most standard approach is to use `x = np.linalg.solve(A, b)`. This is much more efficient.

`@instructions`


`@hint`


`@pre_exercise_code`
```{}
import numpy as np
```
`@sample_code`
```{}
# define matrix A using Numpy arrays 
A = np.array([[2, 1, 1], [1, 3, 2], [1, 0, 0]]) 

#define matrix b 
b = np.array([4, 5, 6]) 

x = np.linalg.solve( ___ , ___ )

# linalg.solve is the function of NumPy to solve a system of linear scalar equations 
print("Solution:\n", x )
```
`@solution`
```{}
# define matrix A using Numpy arrays 
A = np.array([[2, 1, 1], [1, 3, 2], [1, 0, 0]]) 

#define matrix b 
b = np.array([4, 5, 6]) 

# linalg.solve is the function of NumPy to solve a system of linear scalar equations 
print("Solution:\n", np.linalg.solve(A, b ) )
```
`@sct`
```{}
Ex().check_object('x').has_equal_value()
success_msg('Great job!')
```





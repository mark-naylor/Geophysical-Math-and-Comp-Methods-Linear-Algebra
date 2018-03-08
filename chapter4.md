---
title: Basic Matrix Operations
description: >-
  undefined


---
## Matrix Equality

```yaml
type: TabExercise

xp: NaN

key: 5bcf5ade9a
```

In these exercises we will explore the concept of matrix equality and how it is implemented in Python.

Two matrices are equal if all three of the following conditions are met:

-  Each matrix has the same number of rows.
-  Each matrix has the same number of columns.
-  Corresponding elements within each matrix are equal.











***



```yaml
type: NormalExercise

xp: 100

key: a50d12ec7d
```



`@instructions`
Let's start by looking at what happens if we use the equality operator ``==`` to compare two matrices.

Create two matrices...

Is this the same as the mathematical definition of matrix equality?

`@hint`



`@sample_code`
```{}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,3],[2,4]] )

print( a==b )
```
`@solution`
```{}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,3],[2,4]] )

print( a==b )
```
`@sct`
```{}
Ex().check_object('a').has_equal_value()
Ex().check_object('b').has_equal_value()
success_msg('Great job! Note that this is not the same as the mathematical definition of matrix equality. Re-read the defintion above to see why.')
```



***



```yaml
type: NormalExercise

xp: NaN

key: 1553b7299f
```



`@instructions`
This example uses the ``np.isEqual()`` method to compare two matrices.

- run the script and examine the output
- modify the array $b$ so that ``np.equal(a,b)`` is ``TRUE``

`@hint`



`@sample_code`
```{}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,3],[2,4]] )

is_Equal =  np.equal(a,b)

print( is_Equal )
```
`@solution`
```{}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,2],[3,4]] )

is_Equal =  np.equal(a,b)

print( is_Equal )
```
`@sct`
```{}
Ex().check_object('is_Equal').has_equal_value()
success_msg('Great job! This is the same as the mathematical definition matrix equality.')
```






---
## Transpose of a Matrix

```yaml
type: TabExercise
key: 256c8afbac
lang: python
xp: 100
```


`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}

```

***

### Sub Heading

```yaml
type: NormalExercise
xp: 100
key: 8fbd06e0f7
```

`@instructions`

Use the transpose method on $a$

`@sample_code`
```{}
## Load numpy on first use
import numpy as np

## Define an array A
a = np.array([[1, 2], [3, 4]])
print(a)

b = ___.___()
print(b)
```


`@solution`
```{python}
## Load numpy on first use
import numpy as np

## Define an array A
a = np.array([[1, 2], [3, 4]])
print(a)

b = a.transpose()
print(b)

```

`@hint`

`@sct`
```{python}

```

***

### Sub Heading 2

```yaml
type: NormalExercise
xp: 100
key: 9c766c9f0e
```

`@instructions`
Alternatively, you can use the 




`@sample_code`
```{}
## Load numpy on first use
import numpy as np

## Define an array A
a = np.array([[1, 2], [3, 4]])
print(a)

b = ___.___()
print(b)
```


`@solution`
```{python}
## Load numpy on first use
import numpy as np

## Define an array A
a = np.array([[1, 2], [3, 4]])
print(a)

b = a.T
print(b)
```

`@hint`

`@sct`
```{python}

```


---
## Solving Matrix Equations

```yaml
type: TabExercise
key: 25e0f1445a
lang: python
xp: 100
```


`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}

```

***
## The long way

```yaml
type: NormalExercise
lang: python
xp: 100
skills: 2
key: c5511f767e
```

Online resources:

<br>- https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/matrices-elimination/v/matrices-reduced-row-echelon-form-1
</div>


Consider a set of linear equations:

\begin{equation*}
    \begin{array}{cccccc}
    a_{11}x_1+&a_{12}x_2+&\ldots&+a_{1n}x_n&=&b_1\\
    a_{21}x_1+&a_{22}x_2+&\ldots&+a_{2n}x_n&=&b_2\\
    &\vdots&&\vdots&=&\vdots\\
    a_{n1}x_1+&a_{n2}x_2+&\ldots&+a_{nn}x_n&=&b_n
    \end{array}
  \end{equation*}

Which we can write as $\mathbf{A}\mathbf{x}=\mathbf{b}$.  Then
  $\mathbf{x}=\mathbf{A}^{-1}\mathbf{b}$.  
  
Problems of this type can be solved to find `x` using: `np.linalg.solve(A,b)`




`@instructions`
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

`@hint`



`@sample_code`
```{python}
import numpy as np

# define matrix A using Numpy arrays 
A = np.array([[2, 1, 1], [1, 3, 2], [1, 0, 0]]) 

#define matrix b 
b = np.array([4, 5, 6]) 

x = np.linalg.inv( ___ ).dot( ___ )

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





***

## Using `linalg.solve()`

```yaml
type: NormalExercise

xp: 100

key: 632f323c4b
```

Whilst this can be implemented simply in Python, taking the inverse of matrices is computationally expensive and may not be feasible.

A range of methods exist for solving these types of problem - the most standard approach is to use `x = np.linalg.solve(A, b)`. This is much more efficient.

`@instructions`
Solve the matrix equation $\mathbf{Ax}=\mathbf{b}$ for $\mathbf{x}$ using `lining.solve()`

`@hint`
You can look up the help page by typing `?np.linalg.solve()` in the iPython shell

`@pre_exercise_code`
```{undefined}
import numpy as np
```
`@sample_code`
```{undefined}
# define matrix A using Numpy arrays 
A = np.array([[2, 1, 1], [1, 3, 2], [1, 0, 0]]) 

#define matrix b 
b = np.array([4, 5, 6]) 

x = np.linalg.solve( ___ , ___ )

# linalg.solve is the function of NumPy to solve a system of linear scalar equations 
print("Solution:\n", x )
```
`@solution`
```{undefined}
# define matrix A using Numpy arrays 
A = np.array([[2, 1, 1], [1, 3, 2], [1, 0, 0]]) 

#define matrix b 
b = np.array([4, 5, 6]) 

# linalg.solve is the function of NumPy to solve a system of linear scalar equations 
print("Solution:\n", np.linalg.solve(A, b ) )
```
`@sct`
```{undefined}
Ex().check_object('x').has_equal_value()
success_msg('Great job!')
```



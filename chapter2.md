---
title: Solving Simultaneous Equation
description: >-
  In this chapter you will explore how to solve sets of simultaneous equations by solving matrices


---
## Solving two simultaneous equations

```yaml
type: TabExercise

xp: NaN

key: a32c80fcb2
```

In this exercise we will explore how to visualise and solve two simultaneous equations using numpy.

In the next section, we will go on to explore what it means for two simultaneous equations to have no solution and finally generalise this approach to more than two equations.

``numpy`` has been imported as ``np`` and ``matplotlib.pyplot`` as ``plt``



`@pre_exercise_code`
```{undefined}
import numpy as np
import matplotlib.pyplot as plt
```







***



```yaml
type: NormalExercise

xp: 100

key: a50d12ec7d
```



`@instructions`
Let's start by looking at what happens if we use the equality operator ``==`` to compare two matrices.

Create two matrices...

`@hint`



`@sample_code`
```{undefined}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,3],[2,4]] )

print( a==b )
```
`@solution`
```{undefined}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,3],[2,4]] )

print( a==b )
```
`@sct`
```{undefined}
Ex().check_object('a').has_equal_value()
Ex().check_object('b').has_equal_value()
success_msg('Great job!')
```






***



```yaml
type: NormalExercise

xp: 100

key: 0e46483072
```



`@instructions`
You should see that these two lines intersect near 0.

Now, look at this page: http://dwightreid.com/blog/2015/09/21/python-how-to-solve-simultaneous-equations/

which I found by googling "python solution to simultaneous equations".

Use this linear algebra method to solve the equations above

`@hint`



`@sample_code`
```{undefined}
A = np.array([[-5,1], [2,5]])
B = np.array([-2,1])

C = np.linalg.solve(___, ___)

print("Solution:\n",C)
```
`@solution`
```{undefined}
A = np.array([[-5,1], [2,5]])
B = np.array([-2,1])

C = np.linalg.solve(A, B)

print("Solution:\n",C)
```
`@sct`
```{undefined}
Ex().check_object('C').has_equal_value()
success_msg('Great job!')
```






***



```yaml
type: NormalExercise

xp: 100

key: ac15a94b68
```



`@instructions`
# Graphical check that you have the correct solution

Now add horizontal and vertical lines corresponding to your solution using plt.axvline() and plt.axhline().

If they intersect with where the two equations cross - you have done it right.

`@hint`



`@sample_code`
```{undefined}
A = np.array([[-5,1], [2,5]])
B = np.array([-2,1])

C = np.linalg.solve(A, B)

print("Solution:\n",C)


plt.plot(x,y1, label="y1 = 5x-2")
plt.plot(x,y2, label="y2 = 1-2x/5")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()


plt.axvline(..., ls='--', c='r')
plt.axhline(..., ls='--', c='r')

plt.show()
```
`@solution`
```{undefined}
A = np.array([[-5,1], [2,5]])
B = np.array([-2,1])

C = np.linalg.solve(A, B)

print("Solution:\n",C)

plt.plot(x,y1, label="y1 = 5x-2")
plt.plot(x,y2, label="y2 = 1-2x/5")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()


plt.axvline(C[0], ls='--', c='r')
plt.axhline(C[1], ls='--', c='r')

plt.show()
```
`@sct`
```{undefined}
Ex().check_object('C').has_equal_value()
success_msg('Great job!')
```






---
## Simultaneous equations with no solution

```yaml
type: TabExercise

xp: NaN

key: e9cb524f11
```

An important concept for understanding how to solve simultaneous equations is to be able to diagnose when and why equations do not have a solution.



`@pre_exercise_code`
```{undefined}
```







***



```yaml
type: NormalExercise

xp: NaN

key: 8d994fdb1b
```



`@instructions`
Plot the lines $x+y=1$ and  $ x+y=2$ over the range $x \in [-10,10]$ and consider why these simultaneous equations have no solution.

`@hint`



`@sample_code`
```{undefined}
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(___,___)
plt.plot( x, 1-x, 'b', x, 2-x, 'g.')

plt.show()
```
`@solution`
```{undefined}
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(-2,2)
plt.plot( x, 1-x, 'b', x, 2-x, 'g.')

plt.show()
```
`@sct`
```{undefined}
Ex().check_object('x').has_equal_value()
success_msg('Great job!')
```






***



```yaml
type: NormalExercise

xp: NaN

key: 706f2fe98c
```



`@instructions`


`@hint`



`@sample_code`
```{undefined}
A = np.array([[___,___],[___,___]]) 
b = np.array([[___],[___]])

x = np.linalg.solve(A,b)

print("Solution:\n",x )
```
`@solution`
```{undefined}
A = np.array([[1,1],[1,1]]) 
b = np.array([[1],[2]])

x = np.linalg.solve(A,b)

print("Solution:\n",x )
```
`@sct`
```{undefined}
Ex().check_object('x').has_equal_value()
success_msg('Great job!')
```




***



```yaml
type: NormalExercise

xp: NaN

key: 706f2fe98c
```



`@instructions`

We should have a way of knowing in advance that there is no solution...

- Solving a matrix is costly for large matrices
- How can we tell if a set of simultaneous equations have a solution?
- We need them to be all INDEPENDENT!!
- The tool for telling this is the Rank


### Matrix Properties: Rank

<div class="alert alert-block alert-info">
Online resource:
<br>- https://www.khanacademy.org/math/linear-algebra/vectors-and-spaces/linear-independence/v/linear-algebra-introduction-to-linear-independence
</div>

A set of vectors $\mathbf{a_j}$ is **linearly independent**  if:

$$ \sum_j  \mathbf{a_j} c_j = 0\  \mbox{   only when } c_j $$


Let's take an example where the rows are not all independent:
  \begin{eqnarray*}
    \mathbf{a_1}=&(1, 0, 1, 0)\\
    \mathbf{a_2}=&(1, 0, -1, 0)\\
    \mathbf{a_3}=&(1, 0, 0, 0)\\
    \mathbf{a_4}=&(0, 1, 0, 1)
  \end{eqnarray*}
  
  $\mathbf{a_1}+\mathbf{a_2}-2\mathbf{a_3}=\mathbf{0}$ so these vectors are
linear dependant. 

The **Rank** of a matrix is the number of linearly independent rows of a matrix, in the case above only 3 of the 4 rows are linearly independent. 

Use the numpy function `np.linalg.matrix_rank()` to compute it.

`@hint`



`@sample_code`
```{undefined}
import numpy as np
A = np.array([[1,0,1,0],[1,0,-1,0],[1,0,0,0],[0,1,0,1]])

print(A)

length_A = len(A)
rank_A = ___

print("Number of independent rows = ", rank_A)
print("Number of rows = ", length_A)

```


`@solution`
```{undefined}
import numpy as np
A = np.array([[1,0,1,0],[1,0,-1,0],[1,0,0,0],[0,1,0,1]])

print(A)

length_A = len(A)
rank_A = np.linalg.matrix_rank(A)

print("Number of independent rows = ", rank_A)
print("Number of rows = ", length_A)

```
`@sct`
```{undefined}
Ex().check_object('rank_A').has_equal_value()
success_msg('Great job!')
```





---
## Geophysical Examples

```yaml
type: TabExercise

xp: NaN

key: e9645e0fd0
```













***



```yaml
type: NormalExercise

xp: NaN

key: be19e96b1c
```



`@instructions`
In the Measurement Theory course you will have seen that one way in which acceleration (and thus gravity) can be measured is to make measurements of the time and distance of a falling mass. 
  
  The height of the mass as a function of time, initial position, initial velocity and acceleration due to gravity is given by:

  $ z(t) = z_{0} + v _{0} t + \frac{1}{2} g t^2 $
  
Let's assume that we do not know the initial height (  $ z_{0} $ ) , the initial velocity ( $ v_{0} $ ) and
the acceleration due to gravity ($g$). 
  
However, we have measurements of the position ($z(t)$) at 3 different times. 

  Time, $t$ | Position, $z(t)$
 -----|----------
  0.1 | 0.25 
  0.2 | 0.5
  0.3 | 0.85

- Insert these values into the equation above to create a set of 3 simultaneous equations.

- From these simultaneous equations, set up the matrix problem as you did in the previous section where you are solving for $ \mathbf{x} = ( z_{0}, v_{0}, g)$
  
- Now solve for $z_0$, $v_0$ and $g$ in exactly the same way you did in the previous section.

`@hint`
We have 3 equations:

$0.25=Z_o+ 0.1 V_o +\frac{1}{2} g 0.1^2$

$0.50=Z_o+ 0.2 V_o +\frac{1}{2} g 0.2^2$

$0.85=Z_o+ 0.3 V_o +\frac{1}{2} g 0.3^2$

We can write this in the form $\mathbf{Ax}=\mathbf{y}$

$\mathbf{x}=(Z_o, V_o, g)$

$\mathbf{y}=(0.25, 0.50, 0.85)$

$\mathbf{A}= \left[
\begin{array}{ccc}
    1& 0.1 & 0.005\\
    1 & 0.5 & 0.020\\
    1 & 0.3 & 0.045
\end{array}
\right]$


`@sample_code`
```{undefined}
import numpy as np

A = np.array([[1,0.1,0.005], [1,0.2,0.020], [1, 0.3, 0.045]])
y = np.array([0.25, 0.50, 0.85])
x = np.linalg.solve(A, y)

print( "Initial height = ", x[0] )
print( "Initial velocity = ", x[1] )
print( "g = ", x[2] )
```
`@solution`
```{undefined}
import numpy as np

A = np.array([[1,0.1,0.005], [1,0.2,0.020], [1, 0.3, 0.045]])
y = np.array([0.25, 0.50, 0.85])
x = np.linalg.solve(A, y)

print( "Initial height = ", x[0] )
print( "Initial velocity = ", x[1] )
print( "g = ", x[2] )
```







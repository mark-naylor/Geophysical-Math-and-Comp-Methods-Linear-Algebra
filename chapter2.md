---
title: Solving Simultaneous Equation
description: >-
  Insert the chapter description here


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

xp: NaN

key: a50d12ec7d
```



`@instructions`
Plot a graph of the two lines below including the region where they intersect.

$y = 5x-2$

$ 5y + 2x = 1$

`@hint`



`@sample_code`
```{undefined}
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(-10,10)
y1 = ...
y2 = ...

plt.plot(x,y1, label="$y_1 = 5x-2$")
plt.plot(x,y2, label="$y_2 = 1-2x/5$")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()

plt.show()
```
`@solution`
```{undefined}
import numpy as np
import matplotlib.pyplot as plt

x = np.linspace(-10,10)
y1 = 5*x-2
y2 = 1./5-2*x/5

plt.plot(x,y1, label="y1 = 5x-2")
plt.plot(x,y2, label="y2 = 1-2x/5")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()

plt.show()
```
`@sct`
```{undefined}
Ex().check_object('y1').has_equal_value()
Ex().check_object('y2').has_equal_value()
success_msg('Great job!')
```






***



```yaml
type: NormalExercise

xp: NaN

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

xp: NaN

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

key: 93cf3c5ae0
```














---
## More than two simultaneous equations

```yaml
type: TabExercise

xp: NaN

key: e71726be53
```














---
## Geophysical Examples

```yaml
type: TabExercise

xp: 

key: e9645e0fd0
```













***



```yaml
type: NormalExercise

xp: 

key: be19e96b1c
```



`@instructions`


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
```{}
import numpy as np

A = np.array([[1,0.1,0.005], [1,0.2,0.020], [1, 0.3, 0.045]])
y = np.array([0.25, 0.50, 0.85])
x = np.linalg.solve(A, y)

print( "Initial height = ", x[0] )
print( "Initial velocity = ", x[1] )
print( "g = ", x[2] )
```
`@solution`
```{}
import numpy as np

A = np.array([[1,0.1,0.005], [1,0.2,0.020], [1, 0.3, 0.045]])
y = np.array([0.25, 0.50, 0.85])
x = np.linalg.solve(A, y)

print( "Initial height = ", x[0] )
print( "Initial velocity = ", x[1] )
print( "g = ", x[2] )
```







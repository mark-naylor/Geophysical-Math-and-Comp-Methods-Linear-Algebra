---
title: Solving Simultaneous Equation
description: >-
  Insert the chapter description here


---
## Insert exercise title here

```yaml
type: NormalExercise

xp: NaN

key: 859b9ea529
```



`@instructions`
Plot a graph of the two lines below including the region where they intersect.

$y = 5x-2$

$ 5y + 2x = 1$



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





---
## Solving two simultaneous equations

```yaml
type: TabExercise

xp: NaN

key: a32c80fcb2
```

To











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
import numpy as np

A = np.array([[-5,1], [2,5]])
B = np.array([-2,1])
C = np.linalg.solve(___, ___)
print("Solution:\n",C)
```
`@solution`
```{undefined}
import numpy as np

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






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
%matplotlib inline 

x = np.linspace(-10,10)
y1 = ...
y2 = ...

plt.plot(x,y1, label="$y_1 = 5x-2$")
plt.plot(x,y2, label="$y_2 = 1-2x/5$")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
```
`@solution`
```{undefined}
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline 

x = np.linspace(-10,10)
y1 = 5*x-2
y2 = 1./5-2*x/5

plt.plot(x,y1, label="y1 = 5x-2")
plt.plot(x,y2, label="y2 = 1-2x/5")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
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

xp: 

key: a32c80fcb2
```

To 











***



```yaml
type: NormalExercise

xp: 

key: a50d12ec7d
```



`@instructions`
Plot a graph of the two lines below including the region where they intersect.

$y = 5x-2$

$ 5y + 2x = 1$

`@hint`



`@sample_code`
```{}
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline 

x = np.linspace(-10,10)
y1 = ...
y2 = ...

plt.plot(x,y1, label="$y_1 = 5x-2$")
plt.plot(x,y2, label="$y_2 = 1-2x/5$")
plt.xlabel("X")
```
`@solution`
```{}
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline 

x = np.linspace(-10,10)
y1 = 5*x-2
y2 = 1./5-2*x/5

plt.plot(x,y1, label="y1 = 5x-2")
plt.plot(x,y2, label="y2 = 1-2x/5")
plt.xlabel("X")
plt.ylabel("Y")
plt.legend()
```
`@sct`
```{}
Ex().check_object('y1').has_equal_value()
Ex().check_object('y2').has_equal_value()
success_msg('Great job!')
```






***



```yaml
type: NormalExercise

xp: 

key: 0e46483072
```



`@instructions`


`@hint`



`@sample_code`
```{}
A = np.array([[-5,1], [2,5]])
B = np.array([-2,1])
C = np.linalg.solve(___, ___)
print("Solution:\n",C)
```
`@solution`
```{}
A = np.array([[-5,1], [2,5]])
B = np.array([-2,1])
C = np.linalg.solve(A, B)
print("Solution:\n",C)
```







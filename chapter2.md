---
title: Solving Simultaneous Equation
description: >-
  Insert the chapter description here


---
## Insert exercise title here

```yaml
type: NormalExercise

xp: 

key: 859b9ea529
```



`@instructions`


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
plt.ylabel("Y")
plt.legend()
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





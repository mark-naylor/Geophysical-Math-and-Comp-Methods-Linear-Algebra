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













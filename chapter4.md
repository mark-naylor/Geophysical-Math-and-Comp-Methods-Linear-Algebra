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






---
## Is a==b the same as the mathematical definition of matrix equality?

```yaml
type: PureMultipleChoiceExercise

xp: 50
skills: 2
key: 9c7dc76122
```

Is the use of the operator ``==`` on two matrices the same as the mathematical definition of matrix equality?

`@instructions`


`@hint`






`@possible_answers`
- True

- False

`@feedbacks`
msg1 = "Incorrect"
msg2 = "Correct"

test_mc(2, [msg1, msg2])




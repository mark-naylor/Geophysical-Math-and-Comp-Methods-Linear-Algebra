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
type: PureMultipleChoiceExercise

xp: 50
skills: 2
key: 9c7dc76122
```

Is the use of the operator ``==`` on two matrices the same as the mathematical definition of matrix equality?







`@possible_answers`
- True
- [False]

`@feedbacks`
- Incorrect
- Correct




***

```yaml
type: NormalExercise

xp: 

key: 1553b7299f
```



`@instructions`

This example uses the ``np.isEqual()`` method to compare two matrices.

- run the script and examine the output
- modify the array $b$ so that ``np.equal(a,b)`` is ``TRUE``

`@hint`


`@sample_code`
```{undefined}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,3],[2,4]] )

is_Equal =  np.equal(a,b)

print( is_Equal )
```

`@solution`
```{undefined}
import numpy as np

a = np.array( [[1,2],[3,4]] )
b = np.array( [[1,2],[3,4]] )

is_Equal =  np.equal(a,b)

print( is_Equal )

```
`@sct`
```{undefined}
Ex().check_object('is_Equal').has_equal_value()
success_msg('Great job!')
```

***

```yaml
type: PureMultipleChoiceExercise
xp: 50
skills: 2
key: a73b0abbce
```

Is the use of the method ``np.equal()`` on two matrices the same as the mathematical definition of matrix equality?







`@possible_answers`
- [True]
- False

`@feedbacks`
- Incorrect
- Correct





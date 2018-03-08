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

---
title: Eigenvalue Eigenvector Problems
description: >-
  undefined


---
## What are eigenvalue eigenvectors?

```yaml
type: TabExercise

xp: 

key: edebfb1a2c
```













***



```yaml
type: NormalExercise

xp: 

key: 5cac61dd4f
```



`@instructions`
# How do we compute Eigenvectors and values 


1. The definition of an eigenvalue is $\mathbf{A}\mathbf{x} = \lambda \mathbf{x}$

2. Rearrange to give $(\mathbf{A}-\lambda\mathbf{I})\mathbf{x}=\mathbf{0}$

3. For any non-trivial solution $(\mathbf{A}-\lambda\mathbf{I})$ must be
    non-invertible (this indicates that the determinent is 0).

4. Thus, $\det{(\mathbf{A}-\lambda\mathbf{I})}=0$. The determinent generates the **Characteristic Polynomial** of the matrix.

Once you have solved this problem then you can compute the eigenvectors.
  
  As the Characteristic Polynomial is a $N$ degree polynomial it has
  $N$ roots though these roots need not be necessarily distinct. So a
  $N\times N$ matrix has $N$ (though not necessarily distinct)
  eigenvalues (or eigenvectors).

## EXAMPLE: Computing the eigenvalues of a 2x2 martix
  
  Lets find eigenvectors and eigenvalues for the matrix:

$$
\left(
  \begin{array}{cc}
    1 & 2 \\
    3 & 2
  \end{array}
\right)
$$

To find the eigenvalues we need to solve the problem:
$$
\left|
  \begin{array}{cc}
    1-\lambda & 2 \\
    3 & 2-\lambda
  \end{array}
\right|=0
$$

or $(1-\lambda)(2-\lambda)-6=0$ which after some rearrangement is
$(\lambda-4)(\lambda+1)=0$. Solutions for this are $\lambda=4
\mbox{  or } -1$.

`@hint`


`@pre_exercise_code`
```{}
import numpy as np
```
`@sample_code`
```{}
A = np.array([[1,2],[3,2]])
print( np.linalg.eigvals(A) )
```
`@solution`
```{}
A = np.array([[1,2],[3,2]])
print( np.linalg.eigvals(A) )
```
`@sct`
```{}
Ex().check_object('A').has_equal_value()
success_msg('Great job!')
```






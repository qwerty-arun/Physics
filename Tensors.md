# What are Tensors?
- Wikipedia: A tensor may be represented as a (potentially multidimensional) array. Just as a vector in an n-dimensional space is represented by a one-dimensional array with n components with respect to a given basis, any tensor with respect to a basis is represented by a multidimensional array.
- But, we haven't got an intuitive sense as to why it must be a multidimensional array.
- [YT](https://www.youtube.com/watch?v=k2FP-T6S1x0). Here is a video explaining what are tensors and its intuitive sense.
- [NASA Documentation on Tensors](https://www.grc.nasa.gov/www/k-12/Numbers/Math/documents/Tensors_TM2002211716.pdf). Official source for "Tensors" by NASA.

## Conducitivty
- We know that Current 'I' is proportional to Voltage 'V':
```math
 I \propto V 
```
- In Vector Form:
```math
\bar J \propto \bar E
```
- With proportionality constant $\sigma$, the equation becomes:
```math
\bar J  =  \sigma \bar E
```
- For anisotropic crystals, $\sigma$ is not the same in all directions.

- Now imagine a crystal(symmetrical), draw all the coordinate axes and apply a field E in a direction at an angle to X axis.
Now lets imagine conductivity happens only in X direction. Sigma x = 4 and Sigma y = 0. Split the 'E' into Ex and Ey.
Ex will be in direction of J. Actually, we just chose an easy case. Rotate the coordinate system and see.
Then you will see that Jx will depend on both Ex and Ey components.
```math
J_x = \sigma_{xx} * E_x + \sigma_{xy} * E_y
J_y = \sigma_{yx} * E_x + \sigma_{yy} * E_y
```
- We can rewrite this in the form of matrices:
```math
\begin{bmatrix}
J_x \\
J_y
\end{bmatrix}
=
\begin{bmatrix}
\sigma_{xx} & \sigma_{xy} \\
\sigma_{yx} & \sigma_{yy}
\end{bmatrix}
 *
\begin{bmatrix}
E_x \\
E_y
\end{bmatrix}
```
- We we add just one more dimension, that is 3-D, we will need 3*3 = 9 numbers to represent the conductivity.
```math
Scalars \to n^0  (Energy, Mass)
```
```math
Vectors \to n^1  (Force)
```
```math
Rank-2 \to n^2 (Conductivity)
```
- All of them are tensors, just of different ranks. Scalar is a rank 0 tensor, Vector is a rank 1 tensor
- $\bar p = m * \bar v$, since $\bar p$ and $\bar v$ are always aligned, this means mass 'm' is a scalar.
- Now look at the rotational form: $\bar L = I * \bar \omega$
- Turns out $\bar L$ and $\bar \omega$ are not aligned which means Moment of Inertia is a Rank-2 Tensor!!
- Now look at the Force equation: $\bar F = S * \bar A$. Here, stress S is a $n^2$ tensor
# Higher Ranks of Tensors
## Rank-3: Piezoelectric Effect
- Electric field is generated when a crystal is squeezed.
- $\bar E = p * \bar S$
- Since $\bar E$ is a rank-1 and $\bar S$ a rank-2 tensor, the piezoelectric constant must be a rank-3 tensor because, for every value in the $\bar S$ (there are n^2 in total), it needs to spit out 'n' vectors.
## Rank-4: Elasticity
- $Strain = e * S$
- Strain is a n^2 tensor and S is also a n^2 tensor. So, 'e' must be a rank-4 tensor because for every one of n^2 values of S, we need n^2 value of strains.
- This tensor analogy only works for linear proportionality.

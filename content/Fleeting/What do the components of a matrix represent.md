--
publish: true
--

We have a matrix:
 $$
 \begin{bmatrix}
 a & b\\
 c & d
 \end{bmatrix}
 $$
 - Here the first column represents where the $\hat i$ vector lands after transformation and the second column represents where the $\hat j$ vector lands after transformation.
 - Considering the first column, the first row in it represents the transformation of $\hat i$ along the x-direction.
 - Similarly, the second row in the second column represents the transformation of $\hat j$ along the y-direction.
 - So the right-diagonal represents scaling along the original x, y directions.
 - The second row of column 1 represents the y-coordinate of the transformed $\hat i$, so sheering along the y-axis.
 - So the cross diagonal represents sheering along the opposite axis.
 - Rotations can also be represented as a composite action of shears.

- Rotations, shears, scaling are linear tf so they won't move the origin.
- For translation, we _append_ another transformation after performing our lin tf.
$$
\begin{bmatrix}
a & b\\
c & d
\end{bmatrix}
\begin{bmatrix}
x\\
y
\end{bmatrix}
+
\begin{bmatrix}
e\\
f
\end{bmatrix}
$$
- But this is ugly [[Fleeting/Everything I learnt while building Tinyrenderer#Perspective Projection|Perspective Proj]]

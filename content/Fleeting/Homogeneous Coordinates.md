- They are an (semi) alternate coordinate system which allow us to represent points in 2D as projections of points in 3D.
- In the Euclidean world, any point in the plane can be represented only by a unique pair of coordinates.
- But since this is a projective world, many different points in 3D get projected onto the same 2D coordinate.

- Since every cartesian coordinate has an associated non-unique projective coordinate, one of the simplest projective coordinate is:
$$
(x, y) \rightarrow (x, y, 1)
$$
- So the homogenous coordinate, projected onto the plane z = 1 gives us the 2D coordinate (x, y).
- We could have chosen to project any other point as well, but that would require us to alter x and y:
$$
(x, y) \rightarrow (cx, cy, c)
$$
- In cartesian coordinates, translation and perspective projection are non-linear transformations => cannot be represented by matrices => matrices cannot be composed into a single transformation.
- Homogeneous coordinates allow us to represent translation and perspective projection in a higher dimension, where they are indeed linear, enabling us to compose 1000s of transformations into a single matrix.
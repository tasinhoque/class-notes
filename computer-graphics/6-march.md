Line representations:

- Two points
- Parametric

3D representation of a line passing through (x1, y1, z1) and (x2, y2, z2):

(x - x1) / (x1 - x2) = (y - y1) / (y1 - y2) = (z - z1) / (z1 - z2)

Parametric form of a line passing through p and having direction **v**:

p + t**v**; -inf < t < inf

When we're talking about a line, note that we're not talking about line segment. A line segment have a definite length, which a line do not.

We can generate infinite number of planes through two points.

Plane representation:

- Three points
- Parametric
- Point normal

Parametric representation:

p(s, t) = c + s**a** + t**b**

Point normal form: (c, **n**)

It's possible to interchange representations.

### Parametric to point normal

We get **n** by taking cross product of **a** and **b**.

### Point normal to parametric

We take a vector **v** passing through c and take cross product of **n** and **v**. The vector that we'll get will be perpendicular to **n**. If we take cross product of this vector and **n** after that, we'll get another vector perpendicular to both of the vectors. The latter two vectors and c represent the required plane.

### Three point

- Parametric: **a** = A - C, **b** = B - C
- Point normal:

### Point normal to three point

(c, **n**) -> (A, B, C)

Let A be a point on z axis

(A - C).**n** = 0
A.**n** = C.**n**

A = (0, 0, **n**C/_n_)
B = (0, **n**C/_n_, 0)

### Line plane intersection

Plane: ax + by + cz + d = 0
Line: p + t**v**

At intersection, t = _t_

Edge cases:

- Line parallel to the plane (e.g. -1 = 5)
- Line on the plane (e.g. -1 = -1)

### Line-line intersection

Parallel
Coincident: Parallel and have a common point
Condition: They must be contained by a plane.

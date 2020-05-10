# Metric Spaces

[Metrics Spaces](#definition) |
[Open Balls in Metric Spaces](#open-balls-in-metric-spaces) |
[Open Sets in Metric Spaces](#open-sets-in-metric-spaces)

## Definition

A **metric** on a set *X* is a function

```
d: X x X -> R
(x, y) |-> d(x, y)
```

which assigns a **distance** *d(x, y)* between each pair of points
*x, y ∈ X*, satisfying the three axioms:

**[M1]** - For all *x, y ∈ X, d(x, y) > 0* if *x =/ y* and *d(x, x) = 0*

**[M2]** - *d(x, y)* = *d(y, x)* for all *x, y ∈ X*

**[M3]** - *d(x, z) ≤ d(x, y) + d(y, z)* for all *x, y ∈ X*

the latter is called the **triangle inequality**.
- the length of any side of a triangle is less than the sum of the two other sides

--------------------

- [M1] says:
  - each point is distant 0 from itself, but distinct points are at       positive distance apart


- [M2]says:
  - distance from *x* to *y* is the same distance as the distance from *y* to *x*


- [M3] says:
    - Any journey from *x* to *z* doesn't get any shorter if you have to take a detour by *y*, but it may get longer

These axioms have been chosen so as to give metrics just enough properties to **define a topology**

## Definition 2.3

A **metric space** is a pair *(X, d)*, where *X* is a set and *d* is a metric on *X*.

In most cases M1, M2 are trivial; we only have to check M3.

## Examples

The real line *R* with the **usual metric**
```
d(x, y) = |x - y|
```

is a metric space.

Proof:

```
[M1] For all *x, y ∈ R*

d(x, y) = |x - y| > 0 if x =/ y
d(x, x) = |x - x| = 0

[M2] For all *x, y ∈ R*

d(x, y) = |x - y| = |y -x| = d(y, x)

[M3] For all *x, y ∈ R*

d(x, z) = |x - z|
        = |(x + y) - (z + y)|
        = |x - y| + |y - z|
        = d(x, y) + d(y, z)
```

The **complex plane** *C* with the usual metric

*d(z<sub>1</sub>, z<sub>2</sub>) = |z<sub>1</sub> - z<sub>2</sub>|*

is a metric space.

**Sphere metric**

```
Let *X* be the set of points on the surface of a sphere.
Let the distance between the two points be the length of the shorter of the two circle arcs joining them.

Then (X, d) is a metric space.
```

This is the metric used when measuring surfaces on the Earth's surface.

**Discrete metric**

We can define at least one metric, the **discrete metric** on any set X.

```
d(x, x) = 0 and d(x, y) = 1 if x =/y
```

That is, distinct points are distance 1 apart.

# Open Balls in Metric Spaces

## Definition 2.12

- Let *(X, d)* be a metric space
- Let *a ∈ X*
- Let *r ∈ R, r > 0*

The **open ball** with **centre** *a*, **radius** *r* is the set

```
B(a, r) = {x ∈ X: d(a, x) < r}
```
consisting of all points of X whose distance from *a* is less than *r*

## Examples

Consider the metric space *(R, d)*. An **open ball** *B(a, r)* in the real line *R*

```
B(a, r) = {x ∈ R: d(a, x) < r}
        = {x ∈ R: |x - a| < r}
```
is an open interval *(a - r, a + r)*

Consider the metric space *(C, d)*. For *a ∈ C* and r > 0, the
**open ball** *B(a, r)* in the complex plane *C*.

```
B(a, r) = {z ∈ C: d(a, z) < r}
        = {z ∈ C: |z - a| < r}
```
is the disc consisting of all points interior to the circle with centre *a* and radius *r*


Consider the metric space *(X, d)* with the **discrete metric** *d*.

For *a ∈ X* and *r > 0*, the open ball

```
B(a, r) = {z ∈ X: d(a, z) < r}

Recall that

d(x,x) = 0 and d(x, y) = 1 if x =/ y

=>

B(a, r) = { {a} if r ≤ 1
          { X if r > 1
```

-----------------------

Open balls need not be spherical!

# Open Sets in Metric Spaces

We shall now use open balls to define a topology on any metric space.

## Definition 2.20

A subset U of a metric space (X, d) is **open** if and only if for each *u ∈ U* there is a positive real number *r* such that *B(u, r) ⊆ U*

Thus **an open set in a metric space is one which contains an open ball about each of its points**.

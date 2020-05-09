# Metric Spaces

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

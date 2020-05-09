# Open Subsets of R and Continuous Functions

## Definition 1.1

A subset *U* of *R* (real numbers) is **open** if:

 around each point *p* of *U* there is an open interval *(p-h, p+h)* wholly contained in *U*.

 ```
 (p - h, p + h) ⊆ U
 ```

 You should think of an *open set* as containing none of the points at the edge of the set.

 ## Examples

 **Every open interval (a, b) is an open set in R**

 Proof:

 ```
 If p ∈ (a, b), let h be the distance from p to the nearest end point

 h = min(b - p, p - a)

 => (p - h, p + h) ⊆ (a, b)
 ```

 **R is open**

 **The empty set ∅ is vacuously open**

 A vacous truth is  conditional that is only true because the antecedent cannot be satisfied.

 **The closed interval [a, b] is not open in R**

 ```
 If you take p to be a,
 then every open interval (p - h, p + h) contains points outside of [a, b]
 ```

 **A singleton is not open in R**

 ```
 {a} = [a, a] => closed interval => not open
 ```

## Definition 1.8

Continuity:

Let *S* be an open subset of *R*.

A function `f:S -> R` is **continuous** on S <=> for each *a ∈ S* and each *ε > 0* there is a *δ > 0* such that

```
|x - a| < δ => |f(x) - f(a)| < ε
```

Speaking very loosely:

*f* is **continous** at *a* if *f(x)* is close to *f(a)* when *x* is close to *a*.

## Definition 1.10

Let `f: A -> B` be a function.

- If *T* is a **subset** of *B*
- then the **inverse image** of *T* **under** *f* is:
- the subset of *A* consisting of all the elements of *A* that *f* maps into *T*

```
a ∈ f^-1(T) <=> f(a) ∈ T
```

## Example

If `f:R -> R` is defined by `f(x) = x^2` then

```
f^-1([0,9]) = (-3, 3)

f^-1([-5, -4]) = ∅

f^-1(R) = R
```
